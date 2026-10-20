# Despliegue y mantenimiento

Pascal & Sara · Gremio Byte

## Distribución pública

El repositorio `Blai3ePascal/gremio-byte` contiene la distribución de publicación. GitHub Pages sirve archivos estáticos por HTTPS. El JavaScript propio, el catálogo integrado y el adaptador del motor se publican ofuscados; las bibliotecas de terceros conservan sus licencias. Los ejercicios descargables permanecen legibles.

## Edición privada

La entrega `CODIGO-EDITABLE` contiene `src/`, `content/`, `public/`, `public-assets/`, `scripts/`, `package.json` y `package-lock.json`. Conserva esta copia para mantenimiento. No edites manualmente `app.js`.

Con Node.js 22:

```text
npm ci --ignore-scripts
npm run build
npm run check
npm test
```

La salida está en `dist/`. Sirve esa carpeta por HTTP para probarla; abrir index.html con file:// no permite cargar correctamente los motores. `python -m http.server 8000 --directory dist` sirve una vista local.

Los archivos del motor son entradas versionadas, no se descargan de CDN durante el juego. Las rutas relativas permiten publicar bajo `/gremio-byte/`.

## Publicar una actualización

Construye y verifica localmente. Copia el contenido de `dist/` al repositorio de distribución, conserva `.github/workflows/pages.yml`, revisa los cambios y publícalos en `main`. El flujo de Pages publica el contenido del repositorio.

El código editable no se incorpora al repositorio público. No publiques node_modules, mapas de fuentes, partidas personales ni materiales privados del campus.

## Recuperar una versión

Conserva el ZIP de distribución y su SHA-256. Para revertir, restaura la versión anterior en un commit nuevo y deja que Pages la publique. Las partidas usan un esquema versionado; una migración futura debe validarlas antes de cambiarlo.
