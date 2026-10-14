# Pixel Map LED · Telesonic

Herramienta web para preparar pantallas LED: pixel maps, recorridos de datos y corriente, electrónicas NovaStar con redundancia, stock de Telesonic, plantilla de señal y ficha técnica en PDF.

Funciona en el navegador del móvil y del PC, se puede instalar como app y sigue funcionando sin conexión después de la primera visita.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La herramienta completa |
| `manifest.webmanifest` | Permite instalarla como app (icono en la pantalla de inicio) |
| `sw.js` | Guarda la herramienta para usarla sin conexión |
| `icons/` | Iconos de la app |
| `logo-telesonic.png` | Logo de Telesonic (fondo transparente) para la portada y la cabecera de las fichas PDF y Word |
| `biblioteca.json` | **Opcional, lo generas tú**: módulos y electrónicas comunes para todo el equipo |

## Publicar en GitHub Pages

1. Entra en [github.com](https://github.com) y crea un repositorio nuevo, por ejemplo `pixelmap`. Puede ser público o privado (Pages en repositorios privados requiere plan de pago).
2. En el repositorio, pulsa **Add file → Upload files** y arrastra todo el contenido de esta carpeta, incluida la carpeta `icons`.
3. Pulsa **Commit changes**.
4. Ve a **Settings → Pages**. En *Build and deployment* elige **Deploy from a branch**, rama **main** y carpeta **/(root)**. Guarda.
5. En uno o dos minutos la herramienta estará en `https://TU-USUARIO.github.io/pixelmap/`.

## Enlazarla desde Google Sites

En la página de Sites: **Insertar → Botón**, texto «Pixel Map LED» y como enlace la dirección de GitHub Pages. Así se abre a pantalla completa, con descargas y guardado funcionando.

## Instalarla en el móvil

- **Android (Chrome):** abre la dirección → menú ⋮ → **Instalar app** o **Añadir a pantalla de inicio**.
- **iPhone (Safari):** abre la dirección → botón Compartir → **Añadir a pantalla de inicio**.

## Actualizar la herramienta

Sustituye `index.html` en el repositorio por la versión nueva. Si cambias algo en `sw.js`, sube el número de `CACHE` (`pixelmap-v1` → `pixelmap-v2`) para que los móviles descarguen la versión nueva.

## Biblioteca base del equipo

1. En la herramienta, pestañas **Módulos** y **Electrónicas**: deja los equipos de Telesonic como quieras (nombres, consumos, pesos, stock y unidades).
2. Pestaña **Módulos → Exportar como biblioteca base**. Se descarga `biblioteca.json`.
3. Súbelo al repositorio (Add file → Upload files → Commit changes).

Cada vez que alguien abre la herramienta, carga ese archivo: los equipos aparecen con la etiqueta **BASE** y se actualizan solos cuando subas una versión nueva. Lo que añada cada compañero se queda solo en su dispositivo y no se pierde con las actualizaciones.

## Dónde se guardan los datos

El proyecto en curso, la biblioteca de módulos y electrónicas y el logo se guardan **en el navegador de cada dispositivo**. Para pasar un proyecto o la biblioteca a otro equipo o compañero, usa **Guardar .json** y **Abrir .json**.
