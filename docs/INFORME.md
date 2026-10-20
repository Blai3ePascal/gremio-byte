# Verificación de la edición 1.3.0-beta.4

Pascal & Sara · 20 de octubre de 2026

## Resultados de esta edición

- **136/136 soluciones** ejecutadas con todos los casos del catálogo en los motores del navegador.
- **84/84 plantillas incompletas o reparables** rechazadas en al menos un caso antes de corregirlas.
- **136/136 recorridos de ejercicio** comprobados en la interfaz: 1910 grupos de aserciones.
- **13/13 regresiones** de requisitos y alternativas de solución: se contrastan programas incorrectos y formas válidas diferentes.
- **26 cuadernos**, con 272 celdas de trabajo y solución cotejadas con el catálogo.
- Nueve vistas por juego analizadas con axe: sin incidencias detectadas por esta herramienta. Revisión visual de escritorio, móvil, cuaderno, tutorial y ampliación al 200 %.
- Economía comprobada con pruebas de precios, producción, recompensas únicas, límites de acumulación y migración de guardados.

Las soluciones C de los cuadernos coinciden con las ejecutadas mediante GCC C99 en el navegador. Las funciones se prueban con un programa de llamada y distintas entradas.

## Recorridos y estados comprobados

En cada ejercicio: selección desde el mapa, archivo y lenguaje, ejecución vacía sin intento ni premio, restauración, recuperación del borrador tras experimentar, enunciado, pestañas del cuaderno, pista y solución formateada, anterior/siguiente, historial atrás/adelante, resaltado, solución ejecutada desde la interfaz, salida plegable y descarga. Las actividades de bloques añaden comprobación de orden y foco; las entradas fijas se identifican y protegen.

En cada motor (C, Python y SQL): detener una ejecución sin premio, error de sintaxis y recuperación, impedir modificaciones y navegación ordinaria mientras se ejecuta, cancelación al usar el historial, repetición sin duplicar recompensas y salida del editor con Shift+Tab.

También: tutorial de tres pasos con teclado y persistencia, monedas al pulsar, compra y producción de hechizos, límite y desactivación de números flotantes, mapa numerado en ambos sentidos, ayudas modales, opciones persistentes, movimiento reducido y controles en móvil.

## Cambios docentes

El banco mantiene los identificadores de las actividades existentes. Alterna lectura, predicción, reparación, completar, ordenación y resolución abierta. Las prácticas abiertas arrancan con comentarios y las interfaces necesarias, mientras los ejemplos conservan código completo para observarlo. Los enunciados especifican datos, resultados y técnicas obligatorias.

El corrector admite procedimientos alternativos dentro del contrato de cada actividad. Combina casos de ejecución, comprobaciones de estructura y, cuando corresponde, contenido de archivos, filas y restricciones de tablas o elementos de gráficos. Se rechazaron mutaciones que imprimían lo esperado sin realizar el trabajo solicitado; se aceptaron alternativas válidas seleccionadas.

Durante esta revisión se corrigieron restricciones que rechazaban soluciones correctas: recorridos sin acceso a matrices, reconocimiento de `size_t`, variantes de cadenas y tipos de datos de Python. También se reforzaron las verificaciones de archivos incluso ante `exit(0)`, bases de datos cerradas explícitamente y gráficos sin barras.

## Revisión por pares

La revisión documental contrasta el catálogo con nuestros paquetes originales y el alcance elegido. Todos los identificadores publicados son trazables a ese banco: 136 actividades de C y 207 de Python/SQL. No se incorporan nuevas unidades oficiales por inferencia.

La revisión separada de manejadores de interacción terminó con **34/34 comprobaciones aisladas correctas** para ambos juegos. Se cerraron seis defectos: borrador del experimento, sincronización de bloques, predicción mutable, foco al ordenar, entrada de referencia y Tab durante ejecución. Estas pruebas aisladas no se presentan como pruebas de navegador.

## Alcance y límites

Las pruebas usan Microsoft Edge/Chromium en Windows y la distribución ofuscada. Cubren todas las actividades del catálogo con una matriz finita de acciones; no todos los órdenes posibles de pulsaciones ni todas las entradas posibles. Los informes anteriores permanecen como historial.

La interfaz de Colab no se ejecutó directamente. Los cuadernos de trabajo contienen huecos o errores deliberados. Las comprobaciones de código, gráficos y datos no garantizan que todo intento de simular una solución sea detectable ni califican la explicación o interpretación del estudiante.

El alcance se basa en nuestros materiales. No están disponibles los PDF primarios del campus para certificar equivalencia exacta con la guía vigente. Completar el juego no demuestra por sí solo el dominio de toda la asignatura; las explicaciones y la transferencia a otros problemas requieren revisión docente.

La publicación contiene el código propio ofuscado y licencias de terceros; la copia editable de mantenimiento se entrega aparte. Los manifiestos SHA-256 permiten cotejar los archivos publicados.
