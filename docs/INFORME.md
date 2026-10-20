# Informe de verificación

Pascal & Sara · 20 de octubre de 2026 · Beta 1.0

## Resultado

Se ejecutaron las soluciones de las **176 misiones** en Microsoft Edge/Chromium, con **176 aprobadas y 0 fallos**, sobre trabajadores ofuscados y GCC 14.2 / Linux x86 en v86. Cada misión utiliza todos sus casos de prueba declarados; el número de misiones no equivale al número de casos ni al de ejercicios independientes de escritura.

Se realizaron dos pasadas completas del banco durante la reconstrucción. La segunda incorpora los cambios del catálogo y del empaquetado del motor. La evidencia final está en `evidence/catalog-browser-v1.json`.

## Interacción

Pruebas automatizadas de clic, pistas, propuestas explicadas, ejecución real, recompensa única, representación del resultado, inventario, exportación, importación, preferencias, búsqueda de misiones, detención y persistencia de borradores.

El alias con sintaxis HTML se presenta como texto. La importación rechaza esquemas ajenos, límites incorrectos y claves peligrosas. El código de práctica se ejecuta en trabajadores que se pueden terminar.

Escritorio: 1440 px. Móvil: 390 px. Sin desbordamiento horizontal detectado, también con el texto al 200 %. La revisión con axe-core de las pantallas iniciales no detectó infracciones de las reglas WCAG A/AA seleccionadas. Esto no sustituye una auditoría manual con lectores de pantalla ni pruebas en todos los navegadores.

Se inspeccionaron capturas reales de escritorio y móvil. El informe automatizado de uso está en `evidence/ui-browser-v1.json`.

## Material docente

46 cuadernos por bloque, en versiones de práctica y propuestas explicadas, acompañan este juego. En la entrega conjunta se validaron la estructura JSON de 90 cuadernos y la sintaxis de 446 celdas Python de soluciones. Las celdas C y SQL se apoyan en las soluciones comprobadas en los motores; no se afirma una ejecución completa de los cuadernos dentro de Colab.

Los originales se conservaron. Las diapositivas y PDF originales no se han remaquetado en esta reconstrucción.

## Límites

Es una beta comprobada, no una garantía de ausencia absoluta de errores. Muchas actividades del banco son lecturas con datos fijos. Las pruebas finitas no demuestran generalización a toda entrada, ni impiden respuestas artificiosas.

El motor C usa punteros de 32 bits; los tiempos corresponden a la emulación. El contexto del navegador y los dispositivos pueden cambiar el rendimiento. No se verificó Safari ni Firefox.

La equivalencia exacta con la guía y los criterios UAX 2026/27 queda pendiente de esa documentación vigente. E/R, interpretación de gráficos y justificaciones requieren valoración docente.
