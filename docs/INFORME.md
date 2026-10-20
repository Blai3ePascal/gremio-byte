# Verificación de la edición 1.1

Pascal & Sara · 20 de octubre de 2026 · 1.1.0-beta.2

## Cambios

- El emblema explica +1 moneda, su uso y su carácter opcional. Hay respuesta escrita al pulsarlo.
- Anterior y Siguiente recorren el catálogo en orden; Volver y el historial del navegador conservan destinos y borradores.
- Cada una de las 45 unidades tiene idea central, pasos, error frecuente, variante de transferencia y preguntas de revisión.
- Los 90 cuadernos incluyen portada, índice, predicción, preparación plegada, código, resultados y reflexión. SQL muestra la consulta editable en varias líneas y comprueba los casos.
- Las opciones se agrupan como Lectura, imagen y sonido: texto hasta 200 %, espaciado, controles grandes, contraste, paletas, lectura en voz alta, volumen, movimiento y mesa de estudio.
- Gremio Byte usa un paisaje de aventura con niebla y partículas; Forja Infinita, siluetas de taller y cinta de producción. El movimiento se puede desactivar y respeta la preferencia del sistema.
- Se corrigieron 34 actividades Python que incluían toda la solución como código inicial; ahora tienen una parte conceptual pendiente. Las propuestas completas siguen bajo petición.
- Se corrigió la descripción de F16: inspeccionar bytecode no equivale a ejecutar ensamblador nativo.
- El trazador Python cuenta líneas sin leer variables locales: se evita una interferencia observada en comprensiones al preparar imágenes.

## Pruebas ejecutadas

| Comprobación | Resultado |
|---|---|
| Soluciones de este juego en motores reales y distribución ofuscada | 176/176 |
| Navegación anterior, siguiente, volver, adelante y salto desde mapa | Correcta; borradores conservados |
| Preferencias, recarga, mesa de estudio y movimiento reducido | Correctas |
| Móvil, texto al 200 % y controles grandes | Sin desbordamiento horizontal detectado |
| Axe: pantalla inicial, cuaderno, opciones y contraste al 200 % | Sin infracciones detectadas de las reglas WCAG 2 A/AA y 2.1 AA seleccionadas |
| Progresión, recompensas, inventario, exportar/importar, detener ejecución | Correctos |
| Estructura de los 90 cuadernos y sintaxis de 443 celdas Python de soluciones | Correctas |

En los cuadernos de C, las 176 celdas de solución coinciden exactamente con las soluciones ejecutadas mediante GCC en el navegador. Las celdas auxiliares de compilación de Colab se verificaron estructuralmente y en sintaxis; no se ejecutó la interfaz de Colab ni un compilador Linux externo.

## Evidencias y límites

Los JSON de evidence conservan los resultados por misión y comprobación. Las inspecciones visuales incluyen escritorio, móvil, cuaderno del juego y representaciones HTML de cuatro cuadernos de trabajo.

Una herramienta automática no certifica toda la experiencia de uso. La lectura en voz alta depende del soporte y las voces del navegador; el texto permanece disponible.

Completar un catálogo no demuestra aprendizaje generalizable ni equivalencia con una guía oficial no aportada. La [matriz de cobertura y los ocho retos integradores](APRENDIZAJE.md) distinguen resultados comprobables de explicaciones que requieren revisión docente. Ensamblador nativo, justificación de modelos E/R e interpretación de gráficos necesitan las prácticas o la revisión indicadas allí.

Las diapositivas y PDF originales se conservan; esta entrega mejora los juegos y los cuadernos complementarios. El código propio de publicación está ofuscado; la copia editable se entrega separada.
