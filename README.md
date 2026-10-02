# Pista de Skate 360° · María Sol Pomphile

Presentación web con un recorrido 360° orbitable y una botonera para cambiar el color de las luces.
Sitio estático: no necesita build ni dependencias.

- Cliente: Arq. María Sol Pomphile · Women Lighting · Tel. 2234569365
- Visualización: Trama Estudio de Arquitectura · Tel. 2284371204
- Junto a: Kahl Pigueiras Arquitectura (@kparquitectura)

## Archivos

```
index.html            página completa
vercel.json           caché de las imágenes en Vercel
assets/
  panorama.jpg        render 360° (8000 × 4000) para computadoras
  panorama-4k.jpg     versión liviana (4096 × 2048) para celulares
  preview.jpg         imagen que se ve mientras carga el 360
  og.jpg              miniatura para compartir el link (WhatsApp, redes)
  luz-<color>.jpg     escenas por color (turquesa, cálido, rojo, violeta, azul), 2000 px y -1000 para celular
  logo-kp.png         logo de Kahl Pigueiras Arquitectura
  tron.jpg            imagen del referente
  trama-logo.png      logo de Trama Estudio
  pannellum.js/.css   visor 360 (Pannellum 2.5.6, licencia MIT)
```

## 1. Subir a GitHub (desde el navegador)

1. Entrá a github.com y tocá **New repository**.
2. Ponele un nombre, por ejemplo `pista-skate-360`, y elegí **Public** o **Private** (Vercel funciona con los dos).
3. Tocá **Create repository**.
4. En la página del repositorio vacío, tocá **uploading an existing file**.
5. Arrastrá **el contenido** de esta carpeta (`index.html`, `vercel.json`, `README.md` y la carpeta `assets`), no la carpeta contenedora. `index.html` tiene que quedar en la raíz del repositorio.
6. Tocá **Commit changes**.

## 2. Desplegar en Vercel

1. Entrá a vercel.com e iniciá sesión con tu cuenta de GitHub.
2. Tocá **Add New… → Project** e importá el repositorio `pista-skate-360`.
3. En la configuración:
   - **Framework Preset:** Other
   - **Build Command:** dejalo vacío
   - **Output Directory:** dejalo vacío (o `.`)
4. Tocá **Deploy**. En menos de un minuto vas a tener una URL del tipo `https://pista-skate-360.vercel.app`.

Cada vez que subas un cambio al repositorio, Vercel vuelve a publicar el sitio solo.

## 3. Miniatura al compartir el link

Cuando tengas la URL definitiva, abrí `index.html` (se puede editar desde GitHub con el lápiz) y reemplazá `TU-SITIO.vercel.app` por tu dominio en las líneas de `og:image` y `og:url`. Así WhatsApp muestra la imagen del render al mandar el link.

## Probarlo en tu computadora

El visor 360 no funciona abriendo el archivo con doble clic; necesita un servidor. Desde esta carpeta:

```
python3 -m http.server 8000
```

y abrí `http://localhost:8000`.
