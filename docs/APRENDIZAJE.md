# Cobertura, transferencia y revisión del aprendizaje

Pascal & Sara · 20 de octubre de 2026 · Revisión 2

## Qué permite afirmar esta revisión

Los juegos cubren un recorrido amplio de programación en C y de Python, análisis de datos y SQL. Completar sus misiones demuestra haber superado las comprobaciones concretas del recorrido; no demuestra por sí solo que una persona pueda resolver problemas nuevos sin ayuda, justificar decisiones o conservar lo aprendido.

La revisión se realiza sobre `juegos/gremio-byte/content/catalog.json`, `juegos/forja-infinita/content/catalog.json`, la auditoría de los originales, sus matrices de cobertura y los dos textos aportados. Es una revisión de contenido y estructura de evaluación. No es una nueva ejecución de las 403 soluciones ni una investigación con estudiantes.

El material disponible contiene referencias al campus y su índice, pero no una ficha completa vigente 2026/27 que permita certificar resultados de aprendizaje, ponderación y profundidad exigida. La guía pública FPI 2025 ya analizada en la auditoría es de otro curso y contiene inconsistencias de plantilla. Las correspondencias siguientes son con los objetivos del banco facilitado, no una certificación de equivalencia oficial.

## Inventario del catálogo en el momento de la revisión

| Evidencia | Gremio Byte | Forja Infinita |
|---|---:|---:|
| Unidades, incluida introducción | 23 | 22 |
| Misiones | 176 | 227 |
| Lecturas de ejemplo | 34 | 36 |
| Predicciones | 26 | 28 |
| Completar código | 28 | 31 |
| Modo código | 88 | 128 |
| Ordenar bloques | 0 | 4 |
| Misiones con más de un caso en `tests` | 6 | 26 |
| Código/completar cuyo `starter` coincide con `solution` | 0 | 34 |

La última fila es un problema de señalización pedagógica: un código completo puede ser un buen ejemplo experimental, pero aprobarlo sin modificar nada no acredita una implementación autónoma. Las 34 coincidencias de Forja son F10-A01–A04, F11-A01–A05, F12-A01–A05, F13-A01–A06, F14-A01–A03, F15-A01–A04, F16-A01–A04 y F17-A01–A03.

El recuento de `tests` mide baterías externas declaradas, no todos los casos ejecutados dentro de los programas: algunas soluciones incorporan varios escenarios y aserciones internas. Aun así, si se evalúa solamente la salida de un programa editable, imprimir las constantes esperadas puede eludir el objetivo. Los análisis sintácticos ayudan a una práctica guiada; no garantizan comprensión.

## Matriz de C

“Ejecución” significa compilación y contraste con la salida o el arnés declarado. “Revisión” significa evidencia que necesita explicación o inspección humana adicional.

| Objetivo del banco | Bloques y misiones representativas | Evidencia actual | Lo que falta demostrar |
|---|---|---|---|
| Editar, compilar y separar fuente/ejecutable | INICIO, C01; GB-01, C01-M01 | Ejecución, lectura, completar, predicción | Reconstruir un proyecto fuera del editor y explicar un diagnóstico nuevo |
| Representación, lógica, tipos y conversión | C02–C03; C02-M01/M02, C03-M01/M02 | Operaciones y salidas concretas | Elegir tipos, justificar ancho/rango y diseñar entradas inválidas propias |
| Decisiones, repetición y terminación | C04–C05; C05-sumar-entrenamientos | Predicción, trazas y algunos casos de función | Cubrir todas las ramas; justificar terminación con datos distintos |
| Descomposición funcional y recursión | C06; C06-el-avance-de-una-jugada, C06-repeticiones-de-una-jugada | Parámetros, retornos y batería de función | Diseñar interfaces y casos base sin una firma ya facilitada |
| Arrays, matrices y cadenas | C07–C08; C07-recorrer-las-dos-bandas, C08-M01/M02 | Recorridos, comparación y longitud/capacidad | Matrices no cuadradas, límites elegidos por el estudiante y entrada larga |
| Punteros, alias y modificación del llamador | C09–C10; C09-cambiar-al-portador, C10-intercambiar-dorsales | Reglas de construcción, varios casos, llamada con NULL | Explicar vida de objetos y detectar direcciones colgantes en código nuevo |
| Struct, estados y contratos de error | C11, P01 | Copia, acceso indirecto y escenarios de estado | Documentar invariantes y propiedad cuando varios campos son punteros |
| Archivos, errores y formato persistente | C12–C13; C12-M01/M02, C13-M02 | Lectura/escritura y recuentos concretos | Fallos de apertura, truncamiento, portabilidad y recuperación robusta |
| Memoria dinámica y capacidad | C14; C14-A01–A04 | Ejemplos y crecimiento de vector | Fallo de reserva, secuencia larga, alias tras realloc y liberación completa |
| Búsqueda, ordenación y coste | C15; C15-A01–A04 | Algoritmos, contratos y trazas | Generalización, conservación de multiplicidades y comparación por tamaños |
| TAD y estructuras enlazadas | C16–C19 | Pila/cola, lista, árbol y hash con escenarios acotados | Invariantes bajo secuencias nuevas; datos degenerados; límites y propiedad |
| Integración y herramientas | C20, C-TALLER | Proyecto guiado y ejemplos con módulos | Diseño desde requisitos, depurador real, historial Git y construcción limpia |

No se sustituye C por C++: clases, excepciones y referencias de C++ no se presentan como construcciones de C. El recorrido puede enseñar alternativas en C —struct, punteros, contratos y códigos de error—; la equivalencia curricular requiere confirmación si una guía vigente siguiera exigiendo contenidos de C++.

## Matriz de Python y SQL

| Objetivo del banco | Bloques y misiones representativas | Evidencia actual | Lo que falta demostrar |
|---|---|---|---|
| Entorno, expresiones, representación y algoritmo | INICIO, F01–F03, F-MET | Ejecución, predicción, pseudocódigo y búsqueda | Planificar una solución nueva y ejecutar el cuaderno desde estado limpio |
| Control, funciones, objetos, recursión y errores | F04; F04-repartir-por-filas, F04-una-puja-v-lida | Lectura/código, estructura de bucles y excepción específica | Diseñar funciones; comprobar ramas, independencia de objetos y recuperación |
| Colecciones, alias y copias | F10; F10-la-mano-en-orden-inverso | Retorno y conservación de entrada en la misión específica | Copias anidadas, matrices distintas y elección razonada de estructura |
| Búsqueda y ordenación | F03, F11 | Trazas, cinco estrategias y conteos | Implementar sin ejemplo completo, justificar coste y conservación |
| Tablas, limpieza, estadística e informe | F05A, F06, F12, F14 | Cálculos, convenciones y lectura/escritura CSV | Justificar políticas con datos nuevos y comunicar incertidumbre y límites |
| Visualización e imágenes | F05B, F13, F-PIL | Archivos, dimensiones/modos y resultados declarados | Elegir gráfico, verificar etiquetas/escala y argumentar su interpretación |
| Modelo relacional y E/R | F07–F08; F08-DISENO-1/2 | DDL, columnas, claves y rechazo de inserciones inválidas | Elaborar modelo propio, justificar participación y representar históricos |
| Consultas y modificaciones | F09, SQL | Filtros, joins, agrupaciones, subconsultas, cambios y variantes | Traducir una pregunta nueva; manejar duplicados, NULL, empates y ausencia |
| Transacciones, esquema y persistencia | F15; F15-A01–A04 | Cierre/reapertura, rollback y cambios de esquema guiados | Fallos intermedios, preservación de relaciones y migración desde otro estado |
| Memoria, caché, instrucciones y rendimiento | F02, F16 | Modelo de caché, `dis`, mediciones | Ensamblador nativo si lo exige la guía; separar modelo y máquina real |
| Interacción y comunicación | F17 | Etiqueta y límites de formulario, entradas e informes | Prueba humana con teclado, ampliación y lectura asistida; mensajes comprensibles |

Se detectó una incoherencia concreta en F16: la teoría del catálogo afirmaba ejecución x86-64 mediante GCC mientras F16-A02/A03 inspeccionan bytecode de Python con `dis`. La explicación debe corregirse en juego y cuadernos. Una práctica nativa externa debe identificarse como tal, verificarse y conservarse cuando sea necesaria; no basta con nombrarla.

## Mejora de las explicaciones

El archivo `qa/coverage-guides.json` proporciona 45 guías, una por unidad, con `idea`, `steps`, `pitfall`, `transfer` y `review`. Cada guía contiene una idea central, tres acciones, un error conceptual frecuente, una modificación nueva y dos criterios de autoevaluación. Los identificadores se comprobaron contra ambos catálogos.

Su uso recomendado es:

1. Mostrar la idea central junto al reto; mantener la explicación extensa desplegable.
2. Pedir una predicción antes de ejecutar. Comparar esperado y observado, incluyendo espacios, saltos, estado y artefactos cuando sean relevantes.
3. Nombrar cada construcción cuando aparece por primera vez: qué recibe, qué hace y qué devuelve o modifica.
4. Explicar la causa del error y la próxima acción posible, sin atribuir el fallo a la persona.
5. Tras una solución, proponer transferencia con datos distintos y pedir una justificación breve.
6. Mantener separadas tres evidencias: “he consultado”, “he superado pruebas” y “puedo explicarlo en un caso nuevo”. No convertir una casilla marcada en una calificación automática.

En los cuadernos conviene que cada actividad tenga “Objetivo”, “Antes de ejecutar”, “Tu código”, “Comprueba” y “Explica el cambio”. La solución debe seguir el mismo orden. Los dibujos deben acompañarse de una descripción textual. No se debe usar solo color, sonido o movimiento para comunicar un estado. El código en una versión de trabajo debe ofrecer un punto de intervención real, o identificarse explícitamente como experimento.

## Cuatro retos integradores de C

Estos retos son propuestas de transferencia con revisión humana, no misiones existentes ya implementadas ni baterías nuevas ejecutadas.

### C-I1. Registro de expediciones

**Integra:** C03–C08, C11–C12 y C20. Leer registros `id;nombre;puntos`, validar, consultar por identificador, calcular un resumen y guardar los datos aceptados. Separar lectura, validación y operaciones en funciones.

**Contrato:** identificador positivo y único; nombre no vacío con capacidad documentada; puntos dentro del intervalo elegido; rechazar la línea completa cuando no sea válida. Mantener el orden de los registros aceptados.

**Pruebas:** archivo vacío, línea sin salto final, campo ausente, sufijo no numérico, línea demasiado larga, identificador duplicado, límites del intervalo y fallo de apertura. Tras guardar y reabrir, comparar todos los registros.

**Entrega y explicación:** fuentes, datos de prueba y resultados; dibujar el recorrido de una línea rechazada y justificar por qué no contamina la siguiente.

### C-I2. Inventario que crece

**Integra:** C07–C11, C14, C15 y P01. Construir un vector dinámico de objetos, insertar, buscar, actualizar y eliminar sin confundir longitud y capacidad.

**Contrato:** estado válido incluso cuando una operación falla; propietario único de cada reserva; referencias temporales no usadas después de crecimiento; liberar todas las reservas al terminar.

**Pruebas:** vacío, un objeto, varios crecimientos, eliminación inicial/intermedia/final, clave ausente, duplicados y fallo de reserva provocado mediante una función de reserva sustituible en pruebas.

**Entrega y explicación:** tabla de operaciones con longitud/capacidad y diagrama de propiedad antes/después de crecer. Revisar código y, en entorno nativo compatible, usar herramientas de diagnóstico de memoria como complemento; no asumir que una salida correcta demuestra ausencia de uso inválido.

### C-I3. Gestor de tareas y búsquedas

**Integra:** C05–C07, C15–C19. Gestionar tareas pendientes en cola, historial para deshacer en pila y consulta de identificadores mediante una estructura elegida.

**Contrato:** describir LIFO/FIFO; justificar lista, árbol o hash para la consulta; mantener invariantes; definir el comportamiento ante lleno, vacío y duplicados.

**Pruebas:** operaciones intercaladas, vaciado y reutilización, claves que colisionan, inserción ordenada que degenere un árbol si se elige esa estructura, consulta ausente y secuencia larga reproducible.

**Entrega y explicación:** comparar dos tamaños contando operaciones, sin confundir el conteo con tiempo exacto. Explicar por qué se eligió cada estructura y qué se pierde con esa elección.

### C-I4. Proyecto reconstruible

**Integra:** C01, C06, C09–C13 y C-TALLER. Separar uno de los proyectos anteriores en cabeceras y módulos, construirlo desde una copia limpia y localizar un error con depurador.

**Pruebas:** compilación con advertencias, cabecera incluida dos veces, declaración incoherente, fichero ausente y prueba de regresión de la corrección.

**Entrega y explicación:** fuente, instrucciones de construcción, casos de prueba y un historial de cambios. Mostrar estado antes/después de una instrucción en el depurador. No asignar esta evidencia por haber ejecutado el programa monolítico del navegador.

## Cuatro retos integradores de Python y SQL

### F-I1. Datos, decisiones e informe

**Integra:** F01–F06, F10, F12–F14 y F17. Leer un CSV de resultados, validar, distinguir ausencia/error/duplicado, resumir por grupo y producir tabla, gráfico e informe.

**Contrato:** declarar tipos, rangos, política de duplicados, denominador de dispersión y unidades. No borrar datos silenciosamente.

**Pruebas:** conjunto vacío, grupo de un elemento, ausencias, valores extremos, duplicado idéntico, identificador en conflicto, campos entrecomillados y fechas desordenadas. Cambiar los datos después del desarrollo.

**Entrega y explicación:** ejecutar desde estado limpio, reconstruir el resumen y justificar un gráfico. Evaluar etiquetas, escala, tamaño de muestra y límites de interpretación mediante revisión, no solo existencia de PNG.

### F-I2. Biblioteca con historial

**Integra:** F07–F09, F15 y SQL. Diseñar personas, ejemplares y préstamos que conserven episodios repetidos del mismo ejemplar y persona.

**Contrato:** diagrama con participación mínima y cardinalidad máxima; claves justificadas; restricciones; consultas de personas sin préstamos, préstamos abiertos y recuentos incluyendo ceros.

**Pruebas:** persona sin relación, ejemplar nunca prestado, préstamo repetido en otra fecha, fecha ausente cuando sea admisible, empate en recuentos, referencia inexistente e intento de préstamo incompatible con las reglas elegidas.

**Entrega y explicación:** diagrama, DDL, consultas y resultados sobre dos juegos de datos. La defensa del modelo se revisa aparte del SQL; se aceptan diseños alternativos coherentes con el contrato.

### F-I3. Actualización que conserva datos

**Integra:** F04, F06, F14–F15 y SQL. Importar un lote CSV a SQLite, actualizar registros existentes y registrar los rechazos sin dejar una importación parcial.

**Contrato:** transacción; consultas parametrizadas en Python; cierre y reapertura; conservación de columnas no afectadas y de relaciones. Distinguir rechazo de un registro y fallo que obliga a revertir el lote.

**Pruebas:** fallo a mitad de lote, clave repetida, texto con comillas, cambio sin coincidencia, restricción fallida y reapertura con conexión nueva. Comparar el estado completo antes/después, no solo la columna modificada.

**Entrega y explicación:** código, datos y pruebas; describir el estado tras rollback y explicar por qué concatenar entrada en una consulta no sustituye parámetros.

### F-I4. Algoritmo y experiencia comprobables

**Integra:** F03–F04, F10–F11, F16–F17. Implementar una búsqueda u ordenación elegida, instrumentar su trabajo y presentar un resultado con entradas validadas.

**Contrato:** conservar datos cuando se solicite; documentar caso base/precondiciones; proporcionar mensajes textuales y controles que funcionen con teclado y ampliación. Las señales sonoras son complementarias.

**Pruebas:** vacío, un valor, repetidos, orden inverso y datos nuevos; registrar comparaciones o visitas en varios tamaños. Separar esas cuentas de las mediciones de tiempo repetidas.

**Entrega y explicación:** predicción, traza, código y comentario de resultados. Explicar qué enseña `dis` y qué no enseña sobre instrucciones de CPU; evaluar por separado una práctica de ensamblador nativo si la guía vigente la requiere.

## Rúbrica común de transferencia

Aplicar a un problema nuevo, con datos cambiados respecto de los ejemplos y con acceso a documentación. La rúbrica orienta la revisión; no establece ponderaciones oficiales.

| Dimensión | Evidencia suficiente | Evidencia parcial | Pendiente |
|---|---|---|---|
| Comprensión del contrato | Declara entradas, salidas, restricciones e invariantes | Reconoce el resultado pero omite condiciones | Reproduce una salida sin explicar qué se pide |
| Diseño | Descompone y justifica estructuras y operaciones | Solución coherente con decisiones poco justificadas | Depende de copiar un caso sin adaptarlo |
| Corrección | Supera casos normales, fronteras y errores; conserva lo exigido | Resuelve nominales y algunos límites | Falla en casos esenciales o pierde datos |
| Explicación | Traza cambios y explica por qué funciona y termina | Describe instrucciones sin conectar todo el razonamiento | No puede anticipar un cambio pequeño |
| Transferencia | Adapta la solución a nuevos datos o requisito | Adapta con ayuda concreta | No puede modificarla manteniendo el contrato |
| Comunicación y reproducibilidad | Ejecución limpia, resultados legibles y límites explícitos | Resultado utilizable con pasos no documentados | No puede reproducirse o se presenta una conclusión injustificada |

Solicitar una segunda variante tras un intervalo de estudio permite observar retención. Las ayudas consultadas no deben castigarse: conviene distinguir resolución acompañada de resolución transferida y usar la evidencia para decidir qué practicar después.

## Prioridades para esta iteración

1. Hacer explícita la función opcional del emblema/cristal y separar sus recursos de la evidencia de aprendizaje.
2. Incorporar las 45 guías y una revisión por unidad que pida explicación y transferencia.
3. Corregir F16 y la señalización de ejercicios con código completo; no premiar su mera ejecución como implementación independiente.
4. Incorporar los retos integradores como práctica final con rúbrica y revisión.
5. En una iteración posterior, reforzar los validadores de implementación con entradas variables y pruebas que discriminen errores del objetivo, priorizando memoria, estructuras, gráficos y transformaciones de datos.
6. Contrastar la guía oficial vigente cuando se disponga de ella y ajustar profundidad/calendario. No concluir “se aprende toda la asignatura” solo por cobertura de títulos o porcentaje de misiones.


## Cambios aplicados en la edición 1.1

Las 34 coincidencias detectadas se han convertido en ejercicios de completar: el editor conserva datos y pruebas, pero requiere escribir el paso conceptual. Las soluciones siguen disponibles bajo petición. Las 45 unidades incorporan una idea central, pasos, error frecuente, variante de transferencia y preguntas de revisión. F16 distingue bytecode de ensamblador nativo.

Estos cambios mejoran las oportunidades de práctica, no prueban por sí mismos el aprendizaje de cada estudiante. Los retos integradores y su rúbrica requieren revisión docente.
