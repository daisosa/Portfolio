# Portfolio — Dai Sosa

Sitio web de portfolio profesional para Daiana Sosa, freelance de estrategia y creación de contenido.

Es un sitio estático de una sola página (`index.html`), sin dependencias ni build — HTML, CSS y JavaScript vanilla, listo para publicar en GitHub Pages, Netlify, Vercel o cualquier hosting estático. Las tipografías (Archivo variable e Instrument Serif) viven como archivos `.woff2` en `fonts/`.

## Contenido del sitio

- Hero con video de portada
- Marcas y métricas
- Para quién trabajo
- Trabajo (Mis ediciones / Mis guiones)
- Servicios (acordeón)
- Proceso
- Testimonios
- Sobre mí
- Contacto y footer

## Cómo editar el contenido

- **Videos**: cada pieza de los carruseles es un `<li class="carousel-item">` con `data-id` (el ID del Short de YouTube) y `data-video` (la URL completa). El video del hero usa los mismos atributos en `[data-hero-media]`.
- **Testimonios**: la cita es la transcripción literal de la captura que está en `assets/testimonios/`. Si cambiás una, tiene que seguir coincidiendo con la imagen.
- **Redes sociales**: el bloque de Instagram y LinkedIn del footer está escrito y comentado en `index.html` — descomentalo y completá las URLs.

## Cómo verlo en local

Conviene servir la carpeta con un servidor estático en vez de abrir el archivo directamente: con `file://` el navegador bloquea la carga de la tipografía por CORS y el sitio se ve con la fuente del sistema.

```bash
python3 -m http.server 8080
```

Luego entrá a `http://localhost:8080`.

## Publicar con GitHub Pages

1. Andá a **Settings → Pages** en este repositorio.
2. En "Source" elegí la rama `main` y la carpeta `/ (root)`.
3. Guardá — GitHub va a publicar el sitio en unos minutos en la URL que te indique.
