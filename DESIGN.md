---
name: Dai Sosa — Portfolio
description: Portfolio freelance de estrategia y creación de contenido, Buenos Aires, Argentina
colors:
  noir: "#3A1C36"
  noir-soft: "color-mix(in oklch, #3A1C36 80%, white 20%)"
  amethyst: "#9B71B2"
  amethyst-bright: "color-mix(in oklch, #9B71B2 70%, white 30%)"
  thistle: "#E3D0EA"
  olive: "#6C6D11"
  moss: "#374126"
  paper: "#F4EEF4"
  paper-dim: "#ECE0EC"
  ink: "#1E1220"
  ink-muted: "#6B5568"
  on-accent: "#1E1220"
typography:
  display:
    fontFamily: "'Bodoni Moda', 'Times New Roman', serif"
    fontSize: "clamp(2.6rem, 3rem + 4.6vw, 7.6rem)"
    fontWeight: 400
    lineHeight: 0.98
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "'Bodoni Moda', 'Times New Roman', serif"
    fontSize: "clamp(2.2rem, 4.4vw, 4.4rem)"
    fontWeight: 400
    lineHeight: 1.05
  title:
    fontFamily: "'Bodoni Moda', 'Times New Roman', serif"
    fontSize: "clamp(1.5rem, 3vw, 2.6rem)"
    fontWeight: 400
    lineHeight: 1.15
  body:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "'JetBrains Mono', 'Courier New', monospace"
    fontSize: "12px"
    fontWeight: 500
    letterSpacing: "0.06em"
rounded:
  soft: "2px"
  pill: "100px"
  circle: "50%"
spacing:
  gutter: "clamp(20px, 5vw, 64px)"
  section-y: "clamp(72px, 11vw, 168px)"
components:
  button-editorial:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    padding: "14px 2px"
  button-tactile:
    backgroundColor: "{colors.amethyst}"
    textColor: "{colors.on-accent}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "18px 32px"
  chip:
    backgroundColor: "transparent"
    textColor: "{colors.ink-muted}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "6px 12px"
---

# Design System: Dai Sosa — Portfolio

## Overview

**Creative North Star: "La Sala de Montaje"**

Una sala de edición de video al atardecer, no un portfolio de vitrina: el sitio se planta como el lugar donde el trabajo de Dai efectivamente se hace, no como una galería que muestra el resultado ya terminado. Los títulos de sección van solos, sin kicker ni numeración antepuesta — decisión explícita del usuario tras probar el sistema de timecodes ("no me gusta que cada sección comience con un encabezado con una descripción literal"). Cada transición entre secciones es un corte o una disolución de edición, y toda la superficie se ve como si pasara por una corrección de color LUT — grano fino, viñeta sutil, nunca un blanco puro ni un negro plano.

La paleta nace de una fotografía de ciruelas y hojas de vid a la luz baja del atardecer: violeta-ciruela oscuro, amatista polvorienta, cardo claro, y verdes oliva/musgo como luces de tally puntuales. Es un mundo botánico y cinematográfico a la vez — más bodega o galpón de montaje al final del día que estudio SaaS iluminado en neón. El sistema reemplaza por completo al anterior ("El Cuaderno de Estrategia", violeta eléctrico + papel crema): esto es un reemplazo de identidad visual, no una re-coloreada del sistema previo.

**Key Characteristics:**
- Serif didona de autor (Bodoni Moda) para todo titular — trae presencia de tarjeta de título de film; sans técnica (Archivo) para el cuerpo; mono (JetBrains Mono) reservado a datos tabulares y meta-info (métricas, ficha del hero).
- Amatista como único acento de color con significado; oliva y musgo aparecen solo como detalle puntual (luz de tally), nunca como superficie dominante.
- Grano + viñeta fijos en toda la página (`.grain`, `.vignette`) simulan ver el sitio a través de un LUT cinematográfico.
- Cada sección (excepto el hero) se "disuelve" hacia adentro al entrar en el viewport vía `animation-timeline: view()` — un corte de edición real, no un fade-on-scroll genérico.
- Sin diseño sonoro en esta pasada: decisión explícita del usuario, no una omisión. Documentado como fase futura.

## Colors

Paleta de dos temperaturas heredada de una escena real (ciruelas y hojas al atardecer): violeta-ciruela oscuro + amatista como acento funcional, cardo como highlight sobre oscuro, oliva/musgo como acento secundario puntual, y un papel tibio con base cardo para las secciones claras.

### Primary
- **Amethyst** (`#9B71B2`): el acento funcional — línea de progreso de scroll, botones tácticos, selección de texto, bordes en foco, dot de proceso. Sobre relleno amatista el texto es oscuro (`--on-accent`, `#1E1220`), no claro — el amatista es demasiado medio-tono para sostener texto blanco con contraste AA; el texto oscuro además da un aire de "luz de tally con número grabado", coherente con el mundo de sala de edición.
- **Amethyst Bright** (`color-mix(in oklch, #9B71B2 70%, white 30%)`): variante hover/lift del acento — CTA al pasar el mouse, cursor a medida, línea de progreso.

### Secondary
- **Olive** (`#6C6D11`) y **Moss** (`#374126`): acentos secundarios de uso puntual — dot de estadística, extremo frío del degradé atmosférico en fondos oscuros (hero-bg, marco de foto). Nunca cubren una superficie completa ni cargan texto.

### Neutral
- **Thistle** (`#E3D0EA`): highlight tipográfico sobre fondo oscuro — cursiva de énfasis en el hero, subtítulo. Puramente tipográfico, nunca en botones o controles.
- **Paper** (`#F4EEF4`) y **Paper Dim** (`#ECE0EC`): fondo de las secciones claras — un papel tibio con base cardo, no el crema amarillento del sistema anterior. Paper Dim diferencia testimonios del resto del papel.
- **Noir** (`#3A1C36`) y **Noir Soft** (`color-mix(in oklch, #3A1C36 80%, white 20%)`): fondo de las secciones oscuras (hero, trabajo, contacto) y paneles internos (marco de foto, degradé de video).
- **Ink** (`#1E1220`) y **Ink Muted** (`#6B5568`): texto sobre papel. Ink Muted verificado en ~5.9:1 sobre `--paper` (AA para texto normal).

### Named Rules
**La Regla de un Solo Acento con Significado.** El amatista es el único color funcional (botones, foco, selección); oliva y musgo son atmósfera y detalle, nunca controles.
**La Regla del Texto Oscuro sobre Amatista.** Cualquier superficie rellena de `--amethyst` lleva texto en `--on-accent` (`#1E1220`), nunca `--paper`: el amatista es demasiado medio-tono para sostener blanco en contraste AA (3.4:1 medido); el oscuro sí clara (4.6:1).

## Typography

**Display Font:** Bodoni Moda (con Times New Roman de respaldo)
**Body Font:** Archivo (con Helvetica Neue, Arial de respaldo)
**Label/Mono Font:** JetBrains Mono (con Courier New de respaldo)

**Character:** Una didona de autor con presencia de tarjeta de título de cine interrumpe una sans técnica y neutra; los datos — métricas, meta-info — pasan a un monoespaciado real, no decorativo, porque en esta sala son lecturas de máquina, no texto de marca.

### Hierarchy
- **Display** (400, `clamp(2.6rem, 3rem + 4.6vw, 7.6rem)`, line-height 0.98): titular del hero únicamente. La cursiva de énfasis usa Thistle.
- **Headline** (400, `clamp(2.2rem, 4.4vw, 4.4rem)`): título de cada sección, sin kicker ni numeración antepuesta.
- **Title** (400, `clamp(1.5rem, 3vw, 2.6rem)` a `clamp(18px, 1.6vw, 22px)` según componente): nombres de proyecto, título de servicio, paso de proceso.
- **Body** (400, 16px, line-height 1.5): párrafos y copy general.
- **Label** (500, 12px, tracking 0.06em, uppercase, mono): tags de servicio, métricas de proyecto, meta-info del hero, la etiqueta "Quién escribe esto" en Sobre mí.

### Named Rules
**La Regla del Mono para Datos.** JetBrains Mono se reserva a lecturas de datos/metadata (métricas, meta-info) — nunca a titulares ni a copy de marca.

## Layout

Contenedor centrado con `max-width: 1440px` y padding lateral fluido (`--gutter`). Ritmo vertical entre secciones controlado por un único token (`--section-y`). Grid de proyectos ahora uniforme: `repeat(3, 1fr)` sin coreografía asimétrica (antes tenía spans y márgenes escalonados por card) — decisión explícita del usuario, "más sobrio". Responsive en tres quiebres (1180px, 860px, 600px); el grid de proyectos cae a 2 columnas en 860px y a 1 en 600px.

## Elevation & Depth

Se mantiene el vocabulario de sombra tibia del sistema anterior (nunca gris neutro): sombra violeta-tinta oscura sobre papel, resplandor amatista claro sobre noir. Se suma una capa nueva, fija y global: `.grain` (ruido `feTurbulence`, opacity .07, `mix-blend-mode: overlay`) + `.vignette` (radial-gradient oscuro, `mix-blend-mode: multiply`, transparente en el 50% central). Justificación: esta textura no es decoración genérica — es el mecanismo central del brief confirmado por el usuario ("quiero que se vea a través de un LUT cinematográfico"), así que se mantiene pese a que el detector de calidad marca `feTurbulence` como antipatrón por defecto.

### Shadow Vocabulary
- **ambient-card** (`box-shadow: 0 24px 48px -24px rgba(20,10,40,.18)`): reposo, superficie clara que flota (testimonios, CTA principal).
- **lifted-card** (`box-shadow: 0 32px 60px -20px rgba(20,10,40,.24–.5)`): hover/activo de la misma superficie clara.
- **ambient-glow-dark** (`box-shadow: 0 24px 48px -16px rgba(155,113,178,.25)`): reposo, superficie oscura que flota (marcos de trabajo).
- **lifted-glow-dark** (`box-shadow: 0 28px 64px -12px rgba(155,113,178,.4)`): hover/activo de la misma superficie oscura.

### Named Rules
**La Regla de la Sombra Tibia.** Ninguna sombra es gris neutro: violeta-tinta oscura sobre papel, resplandor amatista claro sobre noir.
**La Regla del Grano Permanente.** El grano LUT nunca se apaga del todo, ni siquiera sobre video real cargado (`.work-frame.is-loaded::before{ opacity:.22 }`) — la gradación es una propiedad del sitio, no un placeholder que desaparece con contenido real.

## Shapes

Sin cambios respecto al sistema anterior: radios casi rectos (`--radius-soft` 2px en marcos de imagen/video), círculo completo (dots, cursor, ícono de play) o pill (100px, botón táctil, chips). Ningún radio intermedio tipo "8px card".

## Components

Carácter general: **cinematográfico y táctil** — controles con relieve y una sensación de "consola de edición" (luces de tally, marcos con esquinas de encuadre, botón con cue de play), sin perder la tipografía como protagonista.

### Buttons
- **Editorial (secundario):** sin relleno, regla superior e inferior de 1px en `currentColor` (`.btn-editorial`).
- **Táctil (CTA principal):** `.hero-cta` / `.finale-submit` — pill, fondo Amethyst, texto `--on-accent` (oscuro), ícono de play (`#i-play`) en vez de flecha — el CTA se plantea como un cue de "play/record", coherente con la Sala de Montaje. Hover pasa a Amethyst Bright + `translateY(-3px)` + sombra `lifted-card`.

### Cards
- **Trabajo (`.work-card`):** grid uniforme de 3 columnas (antes asimétrico). Marco 9:16 con `<video>` real opcional (`data-src`): autoplay muted al entrar en viewport/hover estilo Reels, una sola card activa a la vez (tap en el ícono de play sube el volumen y pausa las demás), grano se atenúa pero no desaparece sobre footage real. Sin `data-src`, la card se queda en el placeholder visual (ícono + label en mono) sin intentar reproducir nada.
- **Testimonio (`.testimonial-card`):** sin cambios de comportamiento respecto al sistema anterior — sombra `ambient-card`/`lifted-card` + rotación tipo Polaroid.

### Process Timeline (`.pv-timeline`)
- Reemplaza la grilla asimétrica original de "Cómo trabajo" (elegida vía live-mode). Fila única de 4 pasos sobre un track horizontal (`.pv-track`, hairline en `--line-on-light`), cada paso con un tag de timecode local en mono (`00:00:0N:00`, no confundir con el kicker de sección — es un detalle interno del componente, no un encabezado) y un dot amatista marcando su posición en el track. Colapsa a 2 columnas en ≤1180px (el track se oculta, ya no conecta visualmente al envolver) y a 1 columna en ≤600px.

### Navigation
- Sin cambios de comportamiento; header con `mix-blend-mode: difference` sobre fondo transparente, drawer mobile a pantalla completa sobre Noir.

### Section Transitions (componente de sistema, no de UI)
- Cada `<section>` de primer nivel (salvo el hero) lleva `.cut-section`: `animation-timeline: view()` anima opacity + `scale(.985→1)` mientras la sección entra al viewport (`animation-range: entry 0% cover 30%`) — lee como una disolución de corte de edición al hacer scroll. Sin `filter` animado (se probó y generaba jank real en scroll); solo opacity/transform, baratos para el compositor. Bajo `prefers-reduced-motion`, la regla global existente (`animation-duration: .001ms !important`) la neutraliza — cae a corte seco sin animación, tal como pide el brief.

## Do's and Don'ts

### Do:
- **Do** usar Amethyst como único acento funcional con significado; Olive/Moss quedan para detalle puntual, nunca superficie dominante.
- **Do** poner texto `--on-accent` (oscuro) sobre cualquier relleno Amethyst — nunca `--paper` (falla contraste AA, medido 3.4:1).
- **Do** dejar el título (h2) de cada sección solo, sin kicker ni numeración antepuesta — decisión explícita del usuario.
- **Do** mantener el grano/viñeta activos incluso sobre contenido real (video cargado) — es identidad, no relleno de placeholder.
- **Do** animar transiciones de sección solo con opacity/transform (nunca `filter`) para que `animation-timeline: view()` no cause jank de scroll.

### Don't:
- **Don't** introducir un segundo color de acento funcional — el sistema es mono-acento (Amethyst), con Olive/Moss como atmósfera.
- **Don't** usar Inter Tight, Instrument Serif o Inter — quedaron reemplazadas por Archivo/Bodoni Moda/JetBrains Mono en el reemplazo completo de identidad.
- **Don't** volver al grid asimétrico de proyectos (spans + márgenes escalonados) — el usuario pidió explícitamente algo más sobrio y uniforme.
- **Don't** autoplay con sonido sin gesto del usuario — los videos de proyecto arrancan siempre muted; el tap explícito en el ícono de play es lo único que sube volumen.
- **Don't** agregar diseño sonoro sin pedirlo de nuevo — quedó fuera de alcance por decisión explícita del usuario en esta pasada.
- **Don't** reintroducir un kicker con timecode o numeración antepuesta a los títulos de sección — probado y rechazado explícitamente por el usuario ("no me gusta que cada sección comience con un encabezado con una descripción literal").
