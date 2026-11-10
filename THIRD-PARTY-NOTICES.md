# Componentes de terceros

La licencia MIT se aplica al código propio de Oasis. No sustituye las licencias
de componentes independientes:

- Electron y Chromium: avisos incluidos por Electron en la aplicación empaquetada.
- MusicBrainz Picard 3.0.2: GPL-2.0-or-later. Binario oficial sin modificar,
  ejecutado como proceso separado. Licencia y código fuente correspondiente
  incluidos en `third-party/picard` dentro de la aplicación y del proyecto.
- FFmpeg: descargado directamente por el usuario desde gyan.dev en la primera
  preparación, con SHA-256 verificado; no se redistribuye su binario en el
  instalador público. Su distribución conserva sus licencias GPL y avisos.
- yt-dlp 2026.08.19: descargado desde su release oficial con SHA-256 verificado;
  no se redistribuye su binario en el instalador público.
- Node.js 24.15.0: descargado desde nodejs.org con SHA-256 verificado; no se
  redistribuye su binario en el instalador público.

Proveedores y código fuente:
https://github.com/electron/electron
https://github.com/metabrainz/picard
https://www.gyan.dev/ffmpeg/builds/
https://ffmpeg.org
https://github.com/yt-dlp/yt-dlp
https://nodejs.org

Oasis no está afiliado a esos proyectos ni a MusicBrainz/MetaBrainz.
Usar únicamente contenido propio o cuya descarga esté autorizada.
