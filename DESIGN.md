---
name: Dai Sosa — Portfolio
description: Portfolio freelance de estrategia y creación de contenido, Buenos Aires, Argentina
colors:
  paper: "#F6F0E6"
  surface: "#FCFAF5"
  surface-2: "#EFE7DA"
  ink: "#1C1613"
  ink-2: "#6E655C"
  accent: "#9C3B20"
  accent-deep: "#6E2814"
  dark: "#2A211A"
  danger: "#A32D1C"
  ok: "#2C6A4A"
typography:
  display:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(2.05rem, 5.4vw, 4.1rem)"
    fontWeight: 800
    lineHeight: 1.03
    letterSpacing: "-0.035em"
    textTransform: "uppercase"
  headline:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(1.65rem, 3.4vw, 2.5rem)"
    fontWeight: 700
    letterSpacing: "-0.02em"
  title:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(16px, 1.7vw, 19px)"
    fontWeight: 600
  body:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "11.5px"
    fontWeight: 700
    letterSpacing: "0.16em"
    textTransform: "uppercase"
rounded:
  card: "14px"
  card-lg: "20px"
  pill: "100px"
spacing:
  gutter: "clamp(20px, 4vw, 56px)"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.paper}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "15px 26px"
  button-primary-hover:
    backgroundColor: "{colors.accent-deep}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    border: "1px solid rgba(28,22,19,.26)"
    rounded: "{rounded.pill}"
  card:
    backgroundColor: "{colors.surface}"
    border: "1px solid rgba(28,22,19,.14)"
    rounded: "{rounded.card}"
---

# Design System: Dai Sosa — Portfolio

## Overview

**Creative North Star: "Editorial neutro" (Versión C)**

Un portfolio sobrio de tipografía grande. Papel cálido de base, tinta casi negra y **una sola
familia tipográfica** (Archivo, 100–900): la jerarquía la sostienen el contraste de escala y peso,
la grilla y el aire — no el color ni la decoración. Terracota queda reservado a lo accionable y a
lo que hay que poder encontrar de un vistazo: CTA, enlaces, anillo de foco, cifras de las métricas
y numeral del ítem de acordeón abierto.

Reemplaza por completo a "Terracota-mostaza" (Instrument Serif itálica, mostaza, franjas de cuatro
colores, tablero de corcho con chinches, rotaciones de "mano suelta", marquee de logos). Es un
reemplazo de identidad completo, no una re-coloreada, y responde a un diagnóstico concreto: los
recursos anteriores leían como decoración generada, no como decisiones. Lo que se fue y por qué:

- **Franja a rayas (`.stripe`)** — separador decorativo sin significado; ahora la transición entre
  secciones es una línea de 1px y un cambio de ritmo vertical.
- **Tablero de corcho, chinches y cintas** — skeuomorfismo que restaba profesionalismo. Los
  testimonios pasan a tarjetas con el mensaje textual y la captura real plegada como prueba.
- **Instrument Serif** — el serif itálico conviviendo con Archivo producía dos jerarquías en
  paralelo. Sistema de una sola familia.
- **Rotaciones ±1–4deg** en tarjetas, chips y numerales — ruido que hacía leer la grilla como rota.
- **Marquee de logos** — movimiento permanente que competía con el contenido; ahora es una grilla
  fija en escala de grises.
- **Mostaza y dusty** — la paleta baja a un solo acento.

**Key Characteristics:**
- Titular del hero en Archivo 800 en mayúsculas con tracking negativo (`-0.035em`): el contraste de
  escala contra un cuerpo de 16px es el motor de la jerarquía.
- Patrón único de cabecera de sección (`.sec-head`): eyebrow en mayúsculas + `h2` + lead. Las seis
  secciones lo repiten sin excepción.
- Grillas con separadores de 1px conseguidos por `gap` sobre fondo `--line` (logos, métricas,
  proceso): tabla limpia sin bordes dobles.
- Elevación suave y escasa: dos niveles de sombra, sólo en tarjetas interactivas y en el formulario.
- Acordeón con indicador explícito `+` / `−` (dos trazos; el vertical se pliega al abrir).

## Colors

Papel cálido en tres profundidades, tinta casi negra y un único acento.

### Primary
- **Accent** (`#9C3B20`): CTA principal, enlaces, anillo de foco, cifras de métricas, viñetas de
  lista, numeral del acordeón abierto, palabra de énfasis del hero. Sobre papel da ~6.4:1.
- **Accent Deep** (`#6E2814`): hover de CTA y de enlaces — nunca superficie de texto largo.

### Neutral
- **Paper** (`#F6F0E6`): fondo de página y de las celdas de métricas/proceso.
- **Surface** (`#FCFAF5`): tarjetas, paneles del acordeón, formulario, celdas de logos.
- **Surface-2** (`#EFE7DA`): superficies hundidas — slot de video antes de que cargue la miniatura.
- **Ink** (`#1C1613`) e **Ink-2** (`#6E655C`): texto principal y secundario.
- **Line** (`rgba(28,22,19,.14)`) y **Line-2** (`rgba(28,22,19,.26)`): bordes de tarjeta y de campo.

### Surface
- **Dark** (`#2A211A`): footer, la única banda oscura del sitio. Lleva `--on-dark` (`#F6F0E6`)
  encima (~13:1) y `--on-dark-2` para texto secundario.

### Feedback
- **Danger** (`#A32D1C`): borde y mensaje de campo inválido.
- **Ok** (`#2C6A4A`): confirmación del formulario y punto de "disponible para proyectos".

### Named Rules
**La Regla del Acento Accionable.** Terracota marca lo que se puede tocar o lo que hay que leer
primero (CTA, enlace, foco, cifra). No se usa como relleno de sección ni como color de párrafo: si
algo es terracota y no es accionable, tiene que ser un dato, no una decoración.
**La Regla de la Banda Única.** El footer es la única superficie oscura del sitio. No hay secciones
de color pleno intercaladas — el ritmo lo da el espaciado, no el cambio de fondo.

## Typography

**Única familia:** Archivo variable (100–900), servida localmente en un solo `woff2`.

**Character:** Grotesca neutra de caja alta. El carácter viene del contraste extremo de escala
(display de hasta 4.1rem contra cuerpo de 16px), del tracking negativo en los titulares y del
tracking muy abierto (`.16em`) en los eyebrows — no de un cambio de familia.

### Hierarchy
- **Display** (800, `clamp(2.05rem,5.4vw,4.1rem)`, `-0.035em`, mayúsculas): sólo el `h1` del hero.
- **Headline** (700, `clamp(1.65rem,3.4vw,2.5rem)`, `-0.02em`): `h2` de cada sección.
- **Title** (600–700, 16–19px): título de acordeón, paso de proceso, cita de testimonio.
- **Body** (400, 15–16px, line-height 1.55–1.7): párrafos.
- **Lead** (400, `clamp(15px,1.5vw,17px)`, color `--ink-2`): bajada de sección, máx. 56ch.
- **Label / eyebrow** (700, 11.5–12px, `.14–.16em`, mayúsculas): eyebrow de sección, numerales de
  proceso y audiencia, meta de testimonio.

### Named Rules
**La Regla de una Sola Familia.** Ninguna fuente adicional entra al sistema — ni serif, ni script,
ni monoespaciada. Un peso o un tamaño distinto resuelve cualquier necesidad de énfasis.
**La Regla de la Mayúscula Reservada.** Las mayúsculas son sólo para el `h1` y para labels de
11–12px. Un `h2` en mayúsculas competiría con el hero.

## Layout

Contenedor centrado `max-width: 1240px` con padding lateral fluido (`--gutter`). Todas las
secciones comparten `padding: clamp(56px,7.5vw,104px) 0` y se separan con `border-top: 1px solid
var(--line)` mediante `.section + .section`.

Bandas a dos columnas donde la relación entre las dos mitades es real: hero (video | copy,
`minmax(0,320px) minmax(0,1fr)`), trabajo (ediciones | guiones, `minmax(0,1fr)` × 2), servicios
(cabecera | acordeón) y contacto (cabecera y vías directas | formulario). El resto es ancho
completo.

**Todas las columnas de grid usan `minmax(0,1fr)`, nunca `1fr`**: el carril del carrusel es más
ancho que su columna y con el mínimo automático de grid estiraría la página entera.

Quiebres: 1100px (logos a 5 columnas, servicios y contacto a una), 1000px (los dos carruseles se
apilan), 900px (hero y sobre-mí a una columna), 860px (menú en cajón), 760px (todo a una columna).

## Elevation & Depth

Dos niveles y nada más:
- `--shadow` (`0 1px 2px` + `0 8px 22px`): tarjetas de audiencia y testimonio en hover, ítem de
  acordeón abierto, formulario, foto de "Sobre mí", captura de prueba.
- `--shadow-lg`: sólo el video del hero.

El resto de la separación entre planos la da el borde de 1px y el cambio de `--paper` a `--surface`.

## Shapes

Radio de 14px en tarjetas, paneles y campos; 20px en los dos bloques de medios grandes (video del
hero, foto de retrato); 10px en elementos chicos (celdas, capturas, ítems de nav mobile); pill
(100px) reservada a botones y al enlace "Volver arriba". Sin formas irregulares ni rotaciones.

## Components

### Buttons
- **Primary:** pill terracota, texto papel. Hover: `accent-deep` + `translateY(-2px)` + sombra.
- **Ghost:** transparente con borde `--line-2`; hover oscurece el borde y agrega un velo del 4%.
- **Dark:** tinta plena, ancho completo — submit del formulario; hover pasa a `accent-deep`.

### Section header (`.sec-head`)
Eyebrow (label en mayúsculas) + `h2` + lead opcional, máximo 62ch. Es el único patrón de entrada
de sección; ninguna sección abre de otra manera.

### Accordion (`.acc`)
Cuatro ítems del mismo peso tipográfico y el mismo espaciado, cada uno una tarjeta con borde. La
cabecera es un `<button>` real dentro de un `<h3>` — foco, Enter y Espacio los da el navegador — con
`aria-expanded` y `aria-controls` apuntando al panel (`role="region"` + `aria-labelledby`). El panel
anima con `grid-template-rows: 0fr → 1fr`. El indicador `+` / `−` es obligatorio y va a la derecha:
sin él, una fila cerrada no se lee como interactiva. Sólo un ítem abierto por vez; el primero abre
por defecto.

### Work carousel (`.carousel`)
Carril con scroll-snap y clones antes/después para loop infinito. La pieza centrada va a escala 1 y
opacidad 1; las laterales a `.88` y `.42` (sin `blur`: animar un filtro obliga a rasterizar de nuevo
un subárbol que tiene un video adentro). Un solo iframe de YouTube por carrusel, montado recién
cuando el desplazamiento se detiene y sólo mientras el carrusel está a la vista. Autoplay silenciado
con badge de sonido; el clic en la pieza centrada alterna el audio, y fuera del centro la centra.
Flechas debajo del carril, no encima de la pieza.

### Testimonial card
Mensaje **textual** del cliente como cita, meta ("Cliente · WhatsApp") y la captura real dentro de
un `<details>` plegado ("Ver captura"). La captura es la prueba, no el elemento principal: nunca va
suelta, rotada ni con chinches simuladas.

### Form
Campos con caja (borde 1px, radio 10px) sobre `--paper`. Cuatro estados explícitos: hover (borde
`--ink-2`), foco (borde acento + anillo de 3px), inválido (`aria-invalid="true"` → borde danger +
fondo teñido al 4% + mensaje bajo el campo) y confirmación (`.form-status.is-ok`). El error aparece
al salir del campo y se limpia mientras se corrige, nunca mientras se tipea por primera vez.

### Navigation
Header sticky con desenfoque **en un pseudo-elemento, no en el header**: un `backdrop-filter`
convierte a su elemento en bloque contenedor de todo descendiente `position:fixed`, y eso encierra
al cajón del menú mobile dentro de la barra. Ítems con ícono arriba y label debajo; por debajo de
860px pasan a cajón a pantalla completa con ícono a la izquierda. `section[id]` lleva
`scroll-margin-top: 96px` para que el header sticky no tape el título al llegar por un enlace.

### Logo wall
Grilla de 7 columnas con separadores de 1px. Todos los logos van en escala de grises al 50% de
opacidad y suben a 85% en hover — **nunca a color**: normalizarlos es lo que evita que catorce
identidades ajenas compitan entre sí y con el contenido.

## Do's and Don'ts

### Do:
- **Do** usar `minmax(0,1fr)` en toda columna de grid que pueda contener un carril con scroll.
- **Do** dar a cada fila desplegable un indicador explícito de estado (`+` / `−`) además del cambio
  de color.
- **Do** mantener los logos de clientes monocromáticos y a opacidad pareja.
- **Do** citar a los clientes de forma textual y dejar la captura original disponible como prueba.
- **Do** apoyar la jerarquía en escala, peso y espaciado antes que en color.

### Don't:
- **Don't** reintroducir una segunda familia tipográfica para "dar carácter".
- **Don't** usar terracota como fondo de sección ni como color de párrafo — es el color de lo
  accionable y de los datos.
- **Don't** volver a chinches, cintas, corcho, rotaciones sueltas, franjas de colores ni marquee.
- **Don't** poner `backdrop-filter` sobre un ancestro de un elemento `position:fixed`.
- **Don't** apilar sombras: si algo necesita destacarse más, subile el contraste del borde o el aire
  alrededor.
