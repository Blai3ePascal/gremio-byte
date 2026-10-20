# Fuentes y licencias

Las [fuentes correspondientes del motor, recetas y parches de Alpine y SeaBIOS/SeaVGABIOS](https://github.com/Blai3ePascal/gremio-byte/releases/tag/v1.0.0-beta.1) acompañan a los binarios de esta versión.

Pascal & Sara

# Créditos de recursos visuales

Juegos creados por Pascal & Sara.

Los iconos proceden de [Game-icons.net](https://game-icons.net/) y se distribuyen bajo [Creative Commons Attribution 3.0 Unported (CC BY 3.0)](https://creativecommons.org/licenses/by/3.0/).

Adaptación local: retirada del fondo negro para obtener transparencia. Se conserva el dibujo original en blanco; puede colorearse mediante CSS como máscara. Los créditos de autoría de los iconos corresponden a sus artistas originales.

| Archivo | Autor | Fuente exacta |
| --- | --- | --- |
| `dwarf-face.svg` | Delapouite | [dwarf-face](https://game-icons.net/1x1/delapouite/dwarf-face.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/delapouite/dwarf-face.svg) |
| `sword.svg` | Lorc | [crossed-swords](https://game-icons.net/1x1/lorc/crossed-swords.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/crossed-swords.svg) |
| `shield.svg` | Lorc | [checked-shield](https://game-icons.net/1x1/lorc/checked-shield.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/checked-shield.svg) |
| `chest.svg` | Lorc | [locked-chest](https://game-icons.net/1x1/lorc/locked-chest.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/locked-chest.svg) |
| `cog.svg` | Lorc | [cog](https://game-icons.net/1x1/lorc/cog.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/cog.svg) |
| `crystal.svg` | Lorc | [crystal-ball](https://game-icons.net/1x1/lorc/crystal-ball.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/crystal-ball.svg) |
| `book.svg` | Delapouite | [spell-book](https://game-icons.net/1x1/delapouite/spell-book.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/delapouite/spell-book.svg) |
| `coins.svg` | Delapouite | [two-coins](https://game-icons.net/1x1/delapouite/two-coins.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/delapouite/two-coins.svg) |
| `anvil.svg` | Lorc | [anvil](https://game-icons.net/1x1/lorc/anvil.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/anvil.svg) |
| `flask.svg` | Caro Asercion | [round-potion](https://game-icons.net/1x1/caro-asercion/round-potion.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/caro-asercion/round-potion.svg) |
| `castle.svg` | Delapouite | [castle](https://game-icons.net/1x1/delapouite/castle.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/delapouite/castle.svg) |
| `dragon.svg` | Lorc | [dragon-head](https://game-icons.net/1x1/lorc/dragon-head.html) · [SVG original](https://raw.githubusercontent.com/game-icons/icons/master/lorc/dragon-head.svg) |

Icons made by Lorc, Delapouite and Caro Asercion. Available on https://game-icons.net.

El archivo `LICENSE-game-icons.txt` conserva la licencia y lista de colaboradores del repositorio original. La licencia de los iconos es independiente de la licencia del código del juego.

## Kenney Tiny Dungeon

Archivo: `tiny-dungeon.png`. Autor: Kenney. [Fuente](https://kenney.nl/assets/tiny-dungeon) · [Descarga original](https://kenney.nl/media/pages/assets/tiny-dungeon/f8422efb44-1674742415/kenney_tiny-dungeon.zip) · [Licencia CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).

Atlas original sin cambios, baldosas de 16 × 16 píxeles, sin separación. Usar `image-rendering: pixelated` al ampliarlo. Licencia original incluida en `LICENSE-kenney-tiny-dungeon.txt`.

## Kenney Tiny Town

Archivo: `tiny-town.png`. Autor: Kenney. [Fuente](https://kenney.nl/assets/tiny-town) · [Descarga original](https://kenney.nl/media/pages/assets/tiny-town/a415fbeb49-1735736916/kenney_tiny-town.zip) · [Licencia CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).

Atlas original sin cambios, baldosas de 16 × 16 píxeles, sin separación. Usar `image-rendering: pixelated` al ampliarlo. Licencia original incluida en `LICENSE-kenney-tiny-town.txt`.

## Referencias de interacción

[Cookie Clicker](https://cookieclicker.com/) y [Shakes & Fidget](https://home.sfgame.net/). La adaptación emplea nombres y recursos propios o de stock con licencia; no redistribuye gráficos de esos juegos.


## Motores y documentación primaria

- [Pyodide 0.27.7](https://pyodide.org/en/0.27.7/): CPython en WebAssembly. [Código y licencia MPL 2.0](https://github.com/pyodide/pyodide/tree/0.27.7). Las bibliotecas y CPython conservan sus licencias propias en sus distribuciones.
- [sql.js 1.13.0](https://github.com/sql-js/sql.js/tree/v1.13.0): motor SQLite real, licencia MIT para sql.js; SQLite se distribuye en dominio público.
- [Pillow](https://pillow.readthedocs.io/en/stable/handbook/tutorial.html), [AST de Python](https://docs.python.org/3/library/ast.html), [claves foráneas SQLite](https://sqlite.org/foreignkeys.html), [CMake](https://cmake.org/cmake/help/latest/guide/tutorial/index.html).
- [GCC](https://gcc.gnu.org/), [v86](https://github.com/copy/v86), [Alpine](https://alpinelinux.org/), [tree-sitter](https://tree-sitter.github.io/tree-sitter/). La distribución C incluye manifiesto con versiones, hashes, textos de licencia, fuentes originales y receta de construcción en runtime-build. No se relicencian esos componentes como código propio.
- Interfaz: marked 15.0.7 (MIT), DOMPurify 3.4.17 (Apache 2.0 o MPL 2.0); herramientas de construcción esbuild 0.25.0 y javascript-obfuscator 4.1.1 (MIT/BSD según sus avisos). Se conservan los textos de los paquetes en docs/licenses.
- [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages) sirve el sitio estático. [MDN beforeunload](https://developer.mozilla.org/en-US/docs/Web/API/Window/beforeunload_event) documenta los límites de avisar al cerrar; la copia JSON se solicita mediante una acción explícita.

Las fechas de inicio —febrero de 2026 para C y junio de 2026 para Python/SQL— corresponden al contexto declarado por la dirección del proyecto. La integración de esta beta se realiza en octubre de 2026; no se modifica la fecha de los commits para aparentar otro historial.


Pruebas de interacción del DOM: [jsdom 26.1.0](https://github.com/jsdom/jsdom/tree/26.1.0), MIT. Es una dependencia de pruebas y no se incluye en el motor de la página. El archivo insignia.png es una cuadrícula de ejercicio con valores RGB calculados por coordenadas; su esquina (0,0) sigue siendo (40,120,180).


## Colores del editor

Prism 1.30.0, licencia MIT. Copia íntegra: [Prism-MIT.txt](licenses/Prism-MIT.txt). El editor conserva un campo de texto nativo para escritura, selección y navegación por teclado.
