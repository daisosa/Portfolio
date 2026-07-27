---
name: Dai Sosa — Portfolio
description: Portfolio freelance de estrategia y creación de contenido, Buenos Aires, Argentina
colors:
  cream: "#F8F0EA"
  cream-warm: "#F4E6D8"
  cream-deep: "#EDE0D0"
  ink: "#3A2A2E"
  ink-soft: "color-mix(in oklch, #3A2A2E 85%, white 15%)"
  ink-muted: "#6B5058"
  lavanda: "#D8C7E8"
  lavanda-hover: "color-mix(in oklch, #D8C7E8 78%, #6B4E6B 22%)"
  durazno: "#F0C9A0"
  terracota: "#B2703C"
typography:
  display:
    fontFamily: "Georgia, 'Times New Roman', serif"
    fontSize: "clamp(2.4rem, 2.6rem + 4vw, 6rem)"
    fontWeight: 400
    lineHeight: 1.04
    letterSpacing: "-0.005em"
  script:
    fontFamily: "'Caveat', 'Segoe Script', cursive"
    fontWeight: 700
  headline:
    fontFamily: "Georgia, 'Times New Roman', serif"
    fontSize: "clamp(2.1rem, 4.2vw, 4rem)"
    fontWeight: 400
  title:
    fontFamily: "Georgia, 'Times New Roman', serif"
    fontSize: "clamp(1.3rem, 2.6vw, 2.2rem)"
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
    letterSpacing: "0.06em"
rounded:
  card: "16px"
  pill: "100px"
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
    backgroundColor: "{colors.lavanda}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "18px 32px"
  button-tactile-hover:
    backgroundColor: "{colors.lavanda-hover}"
    textColor: "{colors.cream}"
---

# Design System: Dai Sosa — Portfolio

## Overview

**Creative North Star: "Lavanda-durazno"**

Un portfolio cálido y hecho a mano, no una vitrina corporativa fría: la calidez es la prueba de que hay una persona real detrás del contenido. Crema tibio en toda la superficie — sin una sola sección oscura, a diferencia de cada sistema anterior de este proyecto — con dos blobs pastel muy difuminados (lavanda + durazno) como firma atmosférica recurrente en el hero y en el CTA final. El mundo reemplaza por completo al anterior ("Sala de Montaje", cinematográfico, violeta-amatista, Bodoni Moda + JetBrains Mono): esto es un reemplazo de identidad visual, no una re-coloreada. Se llegó a esta dirección explorando de forma iterativa con la usuaria en artifacts publicados (seis familias de su biblioteca de curaduría personal, luego seis variaciones propias dentro de "Cálido artesanal", luego seis variantes de la referencia "Muse Studio", hasta cerrar en esta versión lisa) — no por el mecanismo de dado del propio skill.

**Key Characteristics:**
- Georgia editorial para todo titular; Caveat (script real, autohospedado) reservado exclusivamente a la palabra de énfasis del hero, la frase de énfasis del CTA final y la drop-cap de "Sobre mí" — nunca en más lugares. Archivo para cuerpo. Sin monoespaciada en ningún lugar del sistema.
- Dos blobs (`.blob-lavanda`, `.blob-durazno`, círculos `border-radius:50%` con `filter:blur`) confluyen en hero y CTA final como bookends atmosféricos; su tamaño usa `clamp()` en vw/px, nunca `vmax`/porcentaje puro, para no depender de la altura del contenido del contenedor.
- Marco "Polaroid" recurrente (mate crema, esquinas suaves, rotación alterna sutil, sombra tibia nunca gris) en las tarjetas de trabajo, testimonios y la foto de "Sobre mí" — es el vocabulario táctil que ata todo el sistema.
- Terracota es el único acento de texto con significado, y solo a tamaño grande (≥24px): titulares de énfasis, numeral destacado de stats. Nunca en texto chico — ver Named Rule de Colors.
- Fila de marcas estática y envuelta (sin auto-scroll infinito) — el detector de antipatrones marca los marquees como patrón de IA.

## Colors

Paleta de un crema tibio en tres profundidades y dos acentos pastel, más un acento de texto terracota.

### Primary
- **Lavanda** (`#D8C7E8`): blob atmosférico (hero + CTA final) y relleno del CTA principal — texto oscuro encima, ~8.6:1 medido.

### Secondary
- **Durazno** (`#F0C9A0`): segundo blob atmosférico y dots decorativos — nunca texto, es demasiado claro para sostener contraste de lectura sobre crema.
- **Terracota** (`#B2703C`): acento de texto — palabra de énfasis del titular, numeral destacado de stats, foco de campos. ~3.5:1 sobre `--cream`: pasa AA de texto grande (≥3:1) pero no el de texto chico (4.5:1); reservado a tamaños ≥24px o a bordes/foco, nunca a caption o link de footer.

### Neutral
- **Cream** (`#F8F0EA`), **Cream Warm** (`#F4E6D8`), **Cream Deep** (`#EDE0D0`): las tres profundidades de fondo — Cream para hero/para quién es/proceso/servicios/sobre mí, Cream Warm para trabajo/testimonios, Cream Deep (la más profunda, nunca negra) para el CTA final/footer.
- **Ink** (`#3A2A2E`) e **Ink Muted** (`#6B5058`): texto principal (~12:1 sobre cream) y secundario (~6.4:1 sobre cream).

### Named Rules
**La Regla del Acento sin Texto Chico.** Terracota nunca lleva texto por debajo de ~24px (falla 4.5:1); a ese tamaño se usa ink o ink-muted. El hover del footer usa `--ink`, no terracota, por esta misma razón.
**La Regla de las Tres Profundidades.** El crema nunca se apaga a negro — la variación tonal entre secciones viene de Cream/Cream Warm/Cream Deep, nunca de una sección oscura.

## Typography

**Display/Body Font:** Georgia (con Times New Roman de respaldo) para titulares; Archivo (variable, 100–900) para cuerpo.
**Script Font:** Caveat 700 (autohospedado, `fonts/caveat-700-normal.woff2`) — real, no depende de fuentes del sistema del visitante.

**Character:** Una serif editorial de peso normal sostiene toda la jerarquía de titulares; el script solo aparece como acento puntual de "escrito a mano" en tres lugares exactos (hero, CTA final, drop-cap), nunca como cuerpo de titular completo.

### Hierarchy
- **Display** (400, `clamp(2.4rem, 2.6rem + 4vw, 6rem)`, line-height 1.04): titular del hero. La palabra de énfasis pasa a Caveat 700, color terracota, ~1.2em.
- **Headline** (400, `clamp(2.1rem, 4.2vw, 4rem)`): título de cada sección.
- **Title** (400, `clamp(1.3rem, 2.6vw, 2.2rem)` según componente): nombre de servicio, paso del proceso, nombre de proyecto.
- **Body** (400, 16px, line-height 1.5–1.7): párrafos y copy general.
- **Label** (600, 11–13px, tracking .04–.1em): "PASO 0N" del proceso, tags de servicio.

### Named Rules
**La Regla del Script Puntual.** Caveat aparece solo en tres lugares (énfasis del hero, énfasis del CTA final, drop-cap de "Sobre mí") — nunca como titular completo ni como cuerpo, y nunca fuera de esos tres puntos.
**La Regla Sin Mono.** Ningún dato (métricas, timestamps, códigos) pasa a monoespaciada — ese vocabulario pertenecía al sistema anterior y este mundo lo descarta por completo.

## Layout

Contenedor centrado `max-width: 1440px`, padding lateral fluido (`--gutter`). Ritmo vertical por `--section-y` (`clamp(72px,11vw,168px)`). Grid de proyectos `repeat(3, 1fr)` con rotación alterna ±1.1–1.3deg (efecto Polaroid disperso sobre la mesa). Responsive en tres quiebres (1180px, 860px, 600px): a 1180px la foto de "Sobre mí" pasa a flujo estático — pero mantiene `position:relative` (no `static`) para que su chip de caption siga contenida y no se desprenda del marco.

## Elevation & Depth

Sombras siempre tibias (`rgba(90,60,70,...)` o `rgba(90,60,50,...)`), nunca grises ni con tinte del acento funcional (terracota/lavanda) en el propio color de sombra — evita el patrón de "glow coloreado" que el detector de antipatrones marca como IA. Profundidad adicional viene de la rotación sutil de las tarjetas Polaroid, no de capas de sombra apiladas.

### Shadow Vocabulary
- **cta-rest** / **cta-hover**: `0 20px 40px -22px rgba(90,60,70,.35)` → `0 26px 52px -18px rgba(90,60,70,.45)`, CTA principal.
- **card-ambient** / **card-lifted**: `0 20px 40px -20px rgba(90,60,70,.24)` → `0 28px 56px -16px rgba(90,60,70,.32)`, tarjetas Polaroid (trabajo, testimonios, foto).

### Named Rules
**La Regla de la Sombra Tibia.** Ninguna sombra es gris neutro ni lleva el tinte exacto de lavanda/durazno/terracota — siempre `rgba(90,60,...)`, un marrón-ciruela tibio propio, distinto de los acentos funcionales.

## Shapes

Radio suave y generoso (`--radius-card`, 16px) en tarjetas y marcos — opuesto a la casi-recta del sistema anterior. Pill (100px) reservado a botones y chips. Los dos blobs atmosféricos son círculos perfectos (`border-radius:50%`) muy difuminados, nunca blobs orgánicos de bordes irregulares — esa variante ("Bloques sólidos") fue explorada y descartada por la usuaria a favor de esta.

## Components

Carácter general: **táctil y hecho a mano** — cada superficie de contenido real (foto, video) vive dentro de un marco tipo Polaroid, nunca un rectángulo plano.

### Buttons
- **Editorial (secundario):** sin relleno, regla superior e inferior de 1px en `currentColor`.
- **Táctil (CTA principal):** pill, fondo Lavanda, texto Ink. Hover pasa a Lavanda Hover (más oscuro) + texto Cream + `translateY(-3px)`. Foco visible: `outline: 2px solid var(--terracota); outline-offset: 4px`.

### Cards — Marco Polaroid (componente de sistema)
- **Trabajo (`.work-card`):** marco 9:16 mate crema con placa interna oscura (`--ink` a `--ink-soft`) para el video/placeholder; rotación alterna ±1.1–1.3deg, se endereza en hover.
- **Testimonio (`.testimonial-card`):** mismo marco Polaroid, rotación ±1.6–1.8deg.
- **Foto de "Sobre mí":** mismo marco, rotación fija 2deg, chip de caption en pill superpuesto en la esquina inferior.

### Process Timeline (`.pv-timeline`)
- Track punteado horizontal (no sólido — evoca puntada/costura), 4 pasos con tag "PASO 0N" en Archivo tracked y dot alternando lavanda-oscuro/terracota. Colapsa a 2 columnas en ≤1180px (el track se oculta) y a 1 en ≤600px.

### Services (`.service-row`)
- Fila con índice serif itálico, título serif, flecha terracota que rota 45°→90° al abrir. Foco de teclado real: `tabindex="0"`, `role="button"`, `aria-expanded`, activable con Enter/Espacio además de click — no es solo un div con onclick.

### Navigation
- Header fijo, fondo crema semitransparente + `backdrop-filter: blur`, siempre legible sobre cualquier sección (reemplaza el `mix-blend-mode: difference` del sistema anterior, que existía para funcionar sobre un hero oscuro que ya no existe). Drawer mobile a pantalla completa sobre crema.

### Atmospheric Blobs (componente de sistema, no de UI)
- `.blob-lavanda` / `.blob-durazno`: círculos con `filter:blur(56px)` y una respiración lenta (`blob-breathe`, 14s, opacity .65→ escala 1.06). Tamaño y posición en `clamp()` de vw/px — nunca `vmax` puro ni porcentaje del contenedor — para no depender de la altura de contenido variable (el CTA final crece con el formulario).

## Do's and Don'ts

### Do:
- **Do** reservar Caveat a los tres puntos de énfasis (hero, CTA final, drop-cap) — nunca como titular completo.
- **Do** mantener terracota fuera de texto menor a ~24px; usar ink/ink-muted para links, captions y hover de footer.
- **Do** dimensionar cualquier elemento atmosférico decorativo (blobs) con `clamp()` en vw/px, no en `vmax` ni porcentaje del contenedor, si ese contenedor puede crecer con contenido variable (formularios, copy largo).
- **Do** dar a cada fila interactiva no nativa (como `.service-row`) `tabindex`, `role`, `aria-*` y manejo de teclado real, no solo un listener de click.
- **Do** respetar `prefers-reduced-motion` ocultando (no solo pausando) cualquier elemento puramente decorativo y en movimiento continuo, como el cursor a medida.

### Don't:
- **Don't** introducir una sección oscura/noir — este mundo es crema de punta a punta; la variación tonal viene de las tres profundidades de crema, nunca de una superficie negra.
- **Don't** usar mono técnico (JetBrains Mono u otra) para ningún dato — quedó reemplazado por Archivo tracked.
- **Don't** volver a Bodoni Moda, Instrument Serif o Inter Tight — reemplazadas por Georgia/Archivo/Caveat en el reemplazo completo de identidad.
- **Don't** reintroducir un marquee de auto-scroll infinito para la fila de marcas.
- **Don't** poner terracota como color de relleno detrás de texto — es un acento de texto/trazo, no de superficie.
