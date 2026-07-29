---
name: Dai Sosa — Portfolio
description: Portfolio freelance de estrategia y creación de contenido, Buenos Aires, Argentina
colors:
  cream: "#F4ECE0"
  cream-card: "#EFE1C9"
  ink: "#2B1B12"
  ink-muted: "#6B5140"
  cream-onterracota: "#EFD9C4"
  terracota: "#9C3B20"
  terracota-deep: "#6E2814"
  mustard: "#E8B33D"
  dusty: "#AFCBDD"
typography:
  display:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontSize: "clamp(2.4rem, 6vw, 5.2rem)"
    fontWeight: 400
    lineHeight: 1.06
  headline:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontSize: "clamp(2rem, 4vw, 3.4rem)"
    fontWeight: 400
  title:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontSize: "clamp(1.4rem, 2.6vw, 2rem)"
    fontWeight: 400
  body:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "12px"
    fontWeight: 600
rounded:
  card: "18px"
  pill: "100px"
spacing:
  gutter: "clamp(20px, 4vw, 56px)"
components:
  button-tactile:
    backgroundColor: "{colors.terracota}"
    textColor: "{colors.cream}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "18px 32px"
  button-tactile-hover:
    backgroundColor: "{colors.terracota-deep}"
  chip:
    backgroundColor: "{colors.mustard}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
---

# Design System: Dai Sosa — Portfolio

## Overview

**Creative North Star: "Terracota-mostaza" (Versión B)**

Un portfolio artesanal con acento de especias — crema tibio de base, terracota como color de marca (CTA, marcos oscuros, títulos de énfasis) y mostaza como acento secundario (chips, numerales, highlight de titular). Una franja decorativa a rayas de cuatro colores (`.stripe`) funciona como firma recurrente entre secciones, en vez de los blobs difuminados del sistema anterior. Reemplaza por completo a "Lavanda-durazno" (pastel, Georgia/Caveat, blobs atmosféricos): esto es un reemplazo de identidad visual completo, no una re-coloreada. Se implementó a partir de un archivo de diseño (`Dai Sosa - Versión B.dc.html`) explorado previamente por la usuaria en Claude Design.

**Key Characteristics:**
- Instrument Serif itálica para titulares y énfasis; Archivo para cuerpo y navegación. Sin script cursiva ni monoespaciada en ningún lugar del sistema.
- Franja decorativa a rayas (`.stripe`, `repeating-linear-gradient` de 4 bandas de 24px) marca las transiciones entre secciones — dos variantes de orden de color (`--a`, `--b`) para no repetir siempre el mismo patrón.
- Tarjetas cálidas sin marco Polaroid: fondo `--cream-card` sólido, esquinas redondeadas (18px), rotación alterna sutil (±1deg) — más plano y gráfico que el sistema Polaroid anterior.
- Terracota funciona como color de **superficie** además de acento de texto (fondo de "Para quién es" y "Sobre mí"), no solo como trazo — a diferencia del sistema anterior donde terracota nunca era relleno.
- Fila de marcas con auto-scroll infinito (`marqueeScroll`), pausada bajo `prefers-reduced-motion` vía el reset global de animaciones — decisión explícita de esta versión, revirtiendo la regla "sin marquee" del sistema anterior.

## Colors

Base crema en dos profundidades, terracota como color de marca (texto y superficie) y mostaza como acento secundario.

### Primary
- **Terracota** (`#9C3B20`): CTA principal, marcos oscuros de placeholder, énfasis de titular, fondo de "Para quién es" y "Sobre mí" — con texto crema encima (~9:1).
- **Terracota Deep** (`#6E2814`): hover de CTA/botones y una de las bandas de la franja decorativa — nunca superficie de texto.

### Secondary
- **Mustard** (`#E8B33D`): highlight de palabra en el titular del hero, numerales sobre terracota, chips de tags de servicios — siempre con texto `--ink` encima, nunca `--cream` (mostaza es demasiado clara para sostener contraste con crema).
- **Dusty** (`#AFCBDD`): banda de la franja decorativa únicamente — no aparece en ningún otro componente.

### Neutral
- **Cream** (`#F4ECE0`): base — hero, para quién es, proceso, servicios, contacto.
- **Cream Card** (`#EFE1C9`): tarjetas — stats, casos de estudio, testimonios (sección completa).
- **Ink** (`#2B1B12`) e **Ink Muted** (`#6B5140`): texto principal y secundario sobre crema.
- **Cream on Terracota** (`#EFD9C4`): cuerpo de texto secundario sobre fondo terracota (más cálido que `--cream` puro, evita el blanco frío sobre un fondo saturado).

### Named Rules
**La Regla de la Superficie Terracota.** A diferencia del sistema "Lavanda-durazno" (terracota solo como trazo/texto), acá terracota sí es color de fondo de sección completa (Para quién es, Sobre mí) — siempre con texto crema/mostaza encima, nunca terracota-sobre-terracota.
**La Regla del Mustard sin Texto Claro.** Mostaza solo lleva texto `--ink` (oscuro) encima — nunca `--cream`, por contraste insuficiente.

## Typography

**Display/Body Font:** Instrument Serif (itálica y normal) para titulares; Archivo (variable, 400–800) para cuerpo, nav y labels.

**Character:** Itálica editorial con trazo fino sostiene el peso visual de los titulares — más ligera y manuscrita que la Georgia del sistema anterior. El highlight `<mark>` mostaza en el hero reemplaza al acento de color plano; no hay fuente script dedicada en este sistema.

### Hierarchy
- **Display** (400, `clamp(2.4rem, 6vw, 5.2rem)`, line-height 1.06): titular del hero, con la palabra de énfasis en `<mark>` mostaza y el cierre en itálica terracota subrayada.
- **Headline** (400, `clamp(2rem, 4vw, 3.4rem)`): título de cada sección (casos de estudio, proceso, servicios).
- **Title** (400, `clamp(1.4rem, 2.6vw, 2rem)`): título de servicio.
- **Body** (400, 16px, line-height 1.5–1.7): párrafos y copy general.
- **Label** (600, 11–13px): índices de servicio, "Vistas —" / "Interacción —" de casos de estudio.

### Named Rules
**La Regla Sin Script.** Este sistema no usa ninguna fuente cursiva-manuscrita dedicada (a diferencia de Caveat en el sistema anterior); el acento de énfasis viene del color (`<mark>` mostaza, itálica terracota), no de un cambio de familia tipográfica.

## Layout

Contenedor centrado `max-width: 1240px`, padding lateral fluido (`--gutter`, `clamp(20px,4vw,56px)`). Grid de proyectos `repeat(auto-fit, minmax(260px,1fr))` con rotación alterna ±1deg. Header en flujo normal (no fijo/sticky) — decisión explícita de esta versión, a diferencia del header fijo con blur del sistema anterior. Responsive en dos quiebres principales (860px para el menú mobile, 1000px para el grid de "Para quién es", 600px para stats/grillas de una columna).

## Elevation & Depth

Sin sombras — este sistema es plano y gráfico, la profundidad viene de la rotación sutil de las tarjetas y del contraste de color entre secciones (crema / cream-card / terracota), no de capas de sombra. Diferencia clave frente al sistema Polaroid anterior, que dependía de sombras tibias apiladas.

## Shapes

Radio suave (`--radius-card`, 18px) en tarjetas y placeholders; radio menor (10–12px) en los slots internos de imagen/video. Pill (100px) reservado a botones, chip de nav "Contacto" y tags de servicio. La franja decorativa (`.stripe`) es el único elemento geométrico "duro" del sistema — bandas rectas sin blur, contraste con el resto de superficies suaves.

## Components

Carácter general: **gráfico y de especias** — color sólido y plano en vez de textura fotográfica o marco Polaroid.

### Buttons
- **Táctil (CTA principal / submit):** pill, fondo terracota, texto crema. Hover pasa a terracota-deep + `translateY(-3px)` (solo en el CTA del hero).
- **Nav CTA:** mismo tratamiento de color en tamaño reducido (`padding:10px 20px`), sin translateY.

### Cards
- **Trabajo (`.work-card`):** fondo `--cream-card`, radio 18px, slot interno 9:16 oscuro (gradiente `--ink`) con ícono de play — rotación alterna ±1deg, se endereza en hover.
- **Testimonio (`.testimonial-card`):** fondo `--cream` (sobre sección `--cream-card`), mismo slot interno con ícono de comilla — rotación alterna ±1.4/1.6deg.
- **Stat / Audience:** fondo `--cream-card` o `--terracota` según sección, rotación fija por posición (no alterna dinámica).

### Stripe decorativo (componente de sistema, no de UI)
- `.stripe`: barra de 18px de alto, `repeating-linear-gradient` de 4 bandas de 24px. Dos variantes de orden de color (`--a` para hero/para-quién, `--b` para casos de estudio) — marca cada transición mayor de sección.

### Services (`.service-row`)
- Fila con índice serif itálico, título serif, flecha (↓) que rota 180° al abrir. Foco de teclado real: `tabindex="0"`, `role="button"`, `aria-expanded`, activable con Enter/Espacio además de click.

### Navigation
- Header en flujo normal (no fijo), fondo crema, borde inferior sutil. Drawer mobile a pantalla completa sobre crema por debajo de 860px.

### Marquee de marcas
- Auto-scroll infinito (`marqueeScroll`, 30s linear) con máscara de fade en los bordes; lista duplicada para loop continuo. Pausado/neutralizado bajo `prefers-reduced-motion` por el reset global de animaciones.

## Do's and Don'ts

### Do:
- **Do** usar terracota como fondo de sección completa cuando el texto encima es crema o mostaza — nunca terracota sobre terracota.
- **Do** mantener mostaza solo con texto `--ink` (oscuro) encima — nunca con texto crema.
- **Do** dar a cada fila interactiva no nativa (`.service-row`) `tabindex`, `role`, `aria-*` y manejo de teclado real, no solo un listener de click.
- **Do** respetar `prefers-reduced-motion` neutralizando todas las animaciones (marquee incluido) vía el reset global — no dejarlo corriendo bajo esa preferencia aunque sea una firma visual del sistema.

### Don't:
- **Don't** introducir sombras apiladas o marcos tipo Polaroid — este sistema es plano; la profundidad viene de color y rotación, no de elevación.
- **Don't** usar una fuente script/cursiva dedicada — el énfasis tipográfico viene de `<mark>` e itálica, no de un cambio de familia.
- **Don't** volver a Georgia, Caveat o los blobs difuminados — reemplazados por Instrument Serif/Archivo y la franja decorativa en el reemplazo completo de identidad.
- **Don't** poner texto crema sobre fondo mostaza, ni texto mostaza sobre fondo crema en tamaños chicos — ambos fallan contraste AA.
