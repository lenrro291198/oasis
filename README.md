# Oasis

Aplicación gratuita y de código abierto para Windows x64. Descarga vídeo y audio
con yt-dlp y añade carátulas con MusicBrainz Picard. Interfaz en español, italiano
e inglés, con temas claro y oscuro.

## Descargar

En [Releases](https://github.com/lenrro291198/oasis/releases/latest):

- **Oasis-Setup-0.6.3-Windows-x64.exe**: instalador con asistente, carpeta elegible,
  acceso directo y desinstalador. Instala para el usuario actual.
- **Oasis-0.6.3-Windows-x64.exe**: portable; no necesita instalación.
- **Oasis-fuentes-0.6.3.zip**: proyecto completo con código, recursos, pruebas y
  licencias. Extraer antes de abrir o compilar.

La primera apertura necesita Internet: descarga Node.js, yt-dlp y FFmpeg desde
sus proveedores y verifica SHA-256. Picard está incluido con su licencia y código
fuente. Los componentes descargados se guardan en `%APPDATA%\Onda\tools\bin`.
Se mantiene el perfil Onda para conservar ajustes de versiones anteriores.
Las descargas y las consultas de carátulas requieren Internet.

Requiere Windows x64 compatible con Electron 44. No es un instalador para Linux,
macOS, Windows de 32 bits ni ARM. No se ha probado en todos los equipos.
Los ejecutables no tienen un certificado comercial de firma: Windows puede
mostrar el editor como desconocido. Comprobar SHA256SUMS.json antes de ejecutar.

## Funciones

- Vídeos, audio y playlists; selección de elementos y cola de descargas.
- MP3, MP4, MKV o mejor audio original, según lo disponible en la fuente.
- Carátulas de archivos descargados o de música local, de forma opcional.
- Reintentos, cancelación, vista previa de portada y registros técnicos.

Las fuentes pueden cambiar o restringir contenido. Oasis no evita DRM ni garantiza
que todos los sitios funcionen. Usarlo con contenido propio o cuya descarga esté
autorizada. Los resultados de identificación de carátulas pueden no coincidir con
la edición exacta de un álbum. Ver también la documentación incluida en el ZIP.

## Compilar

1. Extraer `Oasis-fuentes-0.6.3.zip` y abrir PowerShell en la carpeta del proyecto.
2. Instalar Node.js para desarrollo y ejecutar `npm ci`.
3. Ejecutar `npm test`.
4. Ejecutar `npm run dist`. El script previo obtiene Picard 3.0.2 desde su fuente
   oficial y comprueba su hash. electron-builder genera el instalador y portable
   en `dist-oasis/`. Hace falta Internet para las herramientas de compilación.

Para desarrollo: ejecutar primero
`powershell -NoProfile -File setup-tools.ps1 -Destination bin -PicardOnly` y luego
`npm start`. La primera apertura preparará los demás componentes.

Las versiones están fijadas en `package-lock.json`; no actualizar dependencias
automáticamente durante una reproducción de esta versión. El código no requiere
claves API ni credenciales. No incluye perfiles, certificados locales, archivos
personales ni los diagnósticos del equipo de desarrollo.

## Licencias y verificación

Código propio: MIT, Copyright 2026 Lenrro. Los componentes independientes tienen
sus propias licencias; leer `THIRD-PARTY-NOTICES.md` y `third-party/picard`.
Picard se ejecuta como proceso separado; no se modificó su binario.

Esta versión pasó 11 pruebas automatizadas. Se comprobó la descarga real con
hashes de los componentes y de Picard. La instalación en un PC nuevo y la
compatibilidad con todos los sitios requieren pruebas adicionales.
