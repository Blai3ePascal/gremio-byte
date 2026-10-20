# API GCC local · beta

Motor auténtico: v86 emula x86; Linux ejecuta GCC 14.2.0 y el binario resultante. Todo ocurre en el dispositivo. No hay tarjeta de red virtual ni relay. No se sustituye GCC por una emulación de `printf`, un intérprete de C ni un servicio remoto.

Carga desde un **Worker clásico**:

```js
importScripts('./runtime/v86.js', './runtime/gcc-vm.js');
const gcc = new GccVM({baseURL: new URL('./runtime/', self.location.href).href});
await gcc.init(mensaje => postMessage({type:'status', mensaje}));
const resultado = await gcc.run({source, stdin, flags: ['-std=c99'], files: {'datos.h': 'int f(int);'}});
// {stdout, stderr, exitCode, compileExitCode, compileMs, runMs}
```

Sirve el directorio con HTTP(S). GitHub Pages funciona como alojamiento estático de estos assets. La imagen de arranque se recompone en memoria a partir de archivos menores de 25 MiB. El Worker debe recibir una URL absoluta al directorio `runtime/`; las rutas relativas al Worker pueden cambiar cuando el despliegue usa un subdirectorio de repositorio.

La primera inicialización arranca Linux (unos 12–20 s en el entorno de pruebas). Los intentos siguientes reutilizan la VM; la compilación de programas pequeños suele tardar 1–3 s en el entorno de pruebas. Los tiempos mostrados son tiempo de pared en ese equipo, no una medición científica de complejidad algorítmica. No se necesita SharedArrayBuffer ni cabeceras de aislamiento cruzado.

Límites: 100 KiB por programa/entrada/archivo, 16 archivos adicionales, opciones de compilación permitidas explícitamente, 20 segundos de compilación en el invitado, 3 segundos de ejecución en el invitado, 128 KiB de salida por archivo, 128 MiB de memoria del programa, 16 procesos. El invitado usa `nobody` para ejecutar. Tras cada programa se detienen y terminan los procesos de ese usuario (STOP y KILL) antes de leer resultados, lo que impide que un hijo ordinario deje escrituras tardías en el siguiente intento. Hay watchdog de pared; al saltar se detiene la VM. El frontend debe poder **terminar y recrear el Worker** para liberar totalmente su memoria o recuperar una VM dañada. Mantener un watchdog adicional del Worker en el hilo principal, por ejemplo 100 s para arranque y 50 s por solicitud. No ejecutar este módulo en el hilo de interfaz.

La VM no tiene acceso al disco real del usuario. Los archivos que crea el programa viven en la VM. El juego solo comparte código y entrada; las salidas se tratan como texto, nunca HTML. Un programa puede dañar su propia VM o provocar errores por comportamiento indefinido; en ese caso se reinicia el motor. El aislamiento y los límites reducen alcance; no constituyen prueba formal de ausencia de vulnerabilidades del navegador/emulador.

Los controles de método (punteros, funciones, bucles anidados) se hacen sobre el árbol sintáctico, no buscando cadenas. Las pruebas de comportamiento usan varias entradas y cambios de estado. Esto admite soluciones alternativas válidas. Un análisis sintáctico no demuestra por sí solo que la técnica sea relevante o que un estudiante no haya insertado código muerto: se debe combinar con pruebas y pistas. No usar esta corrección local como sistema de examen seguro; el navegador y su progreso se pueden modificar.

El frontend debe mostrar por separado compilación fallida, salida diferente y técnica pendiente. Una solución que imprime el resultado correcto pero incumple la técnica pedida debe decirlo de forma explícita y respetuosa.

`run()` incluye también `artifacts` y `artifactsSkipped`. Cada artefacto es `{name,byteLength,base64,mime}`: archivos de datos regulares `.txt`, `.csv`, `.bin` o `.json` del directorio de trabajo, hasta 16 archivos, 128 KiB por archivo y 256 KiB total. Se rechazan enlaces simbólicos, directorios y nombres con caracteres ajenos a letras, números, `_`, `-`, `.`. Los archivos existen en la VM solo hasta el siguiente intento; descargar estos bytes conserva su contenido. La entrada `input.txt` se excluye. La interfaz puede mostrar un enlace de descarga por archivo, siempre usando el nombre como texto y nunca interpretando su contenido como HTML. Los archivos omitidos por límites se listan en `artifactsSkipped`. El hilo de interfaz debe validar nuevamente los límites de tamaño al importar partidas.
