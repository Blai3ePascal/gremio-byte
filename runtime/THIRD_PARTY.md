# Runtime de GCC local

La capa del juego y el adaptador de ejecución son de Pascal & Sara El compilador, el sistema operativo, el emulador y el analizador sintáctico son proyectos independientes de terceros, conservan sus autores y licencias, y no deben presentarse como obra original del juego.

| Componente | Versión usada | Proyecto y código fuente | Licencia |
|---|---|---|---|
| v86 | assets producción copy.sh obtenidos 2026-10-19, SHA256 fijados | https://github.com/copy/v86 ; https://copy.sh/v86/ | BSD-2-Clause, `LICENSE-v86.txt` |
| GCC | Alpine 14.2.0-r4 | https://gcc.gnu.org/releases.html ; https://ftp.gnu.org/gnu/gcc/gcc-14.2.0/ ; https://gitlab.alpinelinux.org/alpine/aports/-/tree/1a03a2a9c9e77f1a07d48b6f6805e72c8c63c03f/main/gcc | GPL con excepciones de biblioteca; textos GPL3 y excepción incluidos |
| Linux | Alpine 6.12.113-0-virt | https://www.kernel.org/ ; https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.12.113.tar.xz ; https://gitlab.alpinelinux.org/alpine/aports/-/tree/ea7e6a3e151fb325350c1802a4c212c34744778f/main/linux-lts | GPL-2.0-only, `COPYING-Linux.txt` remite al texto oficial |
| Alpine x86 y paquetes | Versiones exactas en `runtime-manifest.json` | https://alpinelinux.org/ ; https://dl-cdn.alpinelinux.org/alpine/v3.21/main/x86/ ; repositorio aports y commit de cada paquete en manifest | Licencia individual de cada paquete (`L` del manifest) |
| SeaBIOS | imagen BIOS servida por v86, SHA256 fijado | https://github.com/coreboot/seabios ; https://seabios.org/ | LGPLv3 y subcomponentes; conservar avisos fuente |
| SeaVGABIOS | SeaBIOS 1.16.2, hash exacto verificado | https://github.com/coreboot/seabios ; commit ea1b7a0733906b8425d948ae94fba63c32b1d425 | LGPL; conservar avisos fuente |
| web-tree-sitter | 0.20.8 | https://github.com/tree-sitter/tree-sitter/tree/v0.20.8 ; https://www.npmjs.com/package/web-tree-sitter/v/0.20.8 | MIT, `LICENSE-tree-sitter.txt` |
| gramática C WASM | distribución tree-sitter-wasms 0.1.12 | https://github.com/tree-sitter/tree-sitter-c ; https://www.npmjs.com/package/tree-sitter-wasms/v/0.1.12 | MIT, `LICENSE-tree-sitter-c.txt` |

Los paquetes APK se descargaron de Alpine y se extrajeron sin ejecutar sus scripts de instalación. La imagen añade un `/init` mínimo, un usuario sin privilegios y el montaje 9p de intercambio; elimina `lto1`, `lto-dump` y módulos de kernel no utilizados. No se recompiló ni alteró GCC. El compilador genera ejecutables Linux x86 de 32 bits y los ejecuta el mismo sistema invitado. `sizeof(void*)` es 4 en este entorno.

El manifiesto conserva versiones, licencias, URL de upstream, commit de aports y hashes de los APK para reconstruir o auditar. Antes de redistribuir binarios GPL/LGPL se deben conservar estas licencias y proporcionar acceso al código fuente correspondiente y a los cambios/scripts de construcción. Los enlaces anteriores identifican las fuentes; una compilación de distribución debe conservar también las fuentes y parches de aports usados y publicarlos junto a los binarios (por ejemplo, en los assets Source del mismo GitHub Release). No eliminar los avisos originales.

Se incluyen también los textos GPLv2, LGPLv3, LGPLv2.1, Apache-2.0, MPL-2.0, BSD, MIT, X11, Zlib y 0BSD, además del aviso de copyright de musl. Las expresiones de licencia de cada paquete se conservan en el manifiesto.

## Fuentes de esta distribución

[Descargar fuentes correspondientes, recetas y parches](https://github.com/Blai3ePascal/gremio-byte/releases/download/v1.0.0-beta.1/gremio-byte-runtime-corresponding-sources-2026-10-20.zip). El archivo reúne los 28 orígenes Alpine de los 39 paquetes del manifiesto y las fuentes de SeaBIOS/SeaVGABIOS. Se verificaron 286 archivos; no se afirma una reconstrucción binaria idéntica.
