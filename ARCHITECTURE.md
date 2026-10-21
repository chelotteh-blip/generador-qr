# Generador de QR — arquitectura

## Qué hace
Es una página para docentes. Ponés un título y pegás un link, y te da un QR para mandar por WhatsApp o Gmail, imprimir o descargar. No guarda nada: el QR apunta directo al link.
Publicada en https://chelotteh-blip.github.io/generador-qr/

## Cómo está armado
- `index.html`: toda la página (HTML, CSS y JS juntos).
  - Convierte los links de Drive, Docs y Dropbox en links de vista previa.
  - Rechaza los links del Drive propio.
  - Dibuja el QR según el tema del título.
- `qrcode.js`: la librería que genera el QR.
- `qr.ico`: el ícono del acceso directo «Generador de QR» del escritorio (Edge en modo app).

## Dependencias
Ninguna más. Funciona sin servidor.

## Pruebas
Abrir `index.html` y probar un link de Drive, uno de Docs y uno común. Escanear el QR con el celular.

## No tocar
Después de cada cambio, **siempre** hacer `git push`, porque si no la página publicada no se actualiza.

## Respaldo
- GitHub `chelotteh-blip/generador-qr`, rama `main`.
- El repo es **público** porque GitHub Pages gratis lo exige. No tiene datos privados.
