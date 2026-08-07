---
name: Dai Sosa — Portfolio
description: Portfolio freelance de estrategia y creación de contenido, Buenos Aires, Argentina
colors:
  cream: "#F4ECE0"
  cream-card: "#EFE1C9"
  surface: "#FBF6EE"
  ink: "#241A13"
  ink-2: "#6B5140"
  terracota: "#9C3B20"
  terracota-deep: "#6E2814"
  mustard: "#E8B33D"
  dusty: "#AFCBDD"
  on-terracota: "#EFD9C4"
  danger: "#C2452C"
  ok: "#3E8A63"
typography:
  display:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(2.05rem, 5.4vw, 4.1rem)"
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.035em"
    textTransform: "uppercase"
  display-accent:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontStyle: "italic"
    fontWeight: 400
    textTransform: "none"
  headline:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(1.7rem, 3.6vw, 2.7rem)"
    fontWeight: 700
    letterSpacing: "-0.025em"
  title:
    fontFamily: "'Archivo', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(16px, 1.7vw, 19.5px)"
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
    letterSpacing: "0.18em"
    textTransform: "uppercase"
rounded:
  card: "16px"
  card-lg: "22px"
  pill: "100px"
spacing:
  gutter: "clamp(20px, 4vw, 56px)"
components:
  button-primary:
    backgroundColor: "{colors.terracota}"
    textColor: "{colors.cream}"
    rounded: "{rounded.pill}"
    padding: "16px 28px"
  button-primary-hover:
    backgroundColor: "{colors.terracota-deep}"
  chip:
    backgroundColor: "{colors.mustard}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
  card:
    backgroundColor: "{colors.surface}"
    border: "1px solid rgba(36,26,19,.14)"
    rounded: "{rounded.card}"
---

# Design System: Dai Sosa — Portfolio

## Overview

**Creative North Star: "Terracota editorial" (Versión D)**

Un portfolio cálido y cinematográfico donde **el scroll está coreografiado**. Recupera la paleta
completa del sistema original — crema, terracota, mostaza — y sus recursos gráficos de firma
(franja a rayas, marquee de marcas, serif itálico de énfasis, numerales fantasma), pero montados
sobre la estructura sobria y la jerarquía disciplinada de la versión neutra que la precedió.

La tesis del sistema: **la riqueza visual viene del ritmo de superficies y del movimiento ligado al
scroll, no de la decoración aplicada a los elementos**. Cada sección cambia de fondo, los titulares
se revelan por máscara, los medios llevan parallax y una barra de progreso acompaña la lectura.

**Lo que se recuperó del sistema original** (y por qué funciona acá): franja a rayas de cuatro
colores entre secciones mayores, marquee infinito de logos, Instrument Serif itálica como acento,
mostaza como acento secundario, terracota como superficie de sección completa, botones magnéticos.

**Lo que no vuelve, por diagnóstico explícito:** tablero de corcho con chinches y cintas
(skeuomorfismo que restaba profesionalismo), símbolos flotantes (`✦ ✦ ✦`, `++`, flechas
convergentes), rotaciones al azar de tarjetas y chips, y el efecto de tipeado en el proceso. Los
testimonios siguen siendo cita textual con la captura plegada como prueba, y el acordeón sigue
unificado con indicador `+` / `−`.

**Key Characteristics:**
- **Ritmo de superficies:** crema → terracota → tinta → crema → crema-card → crema → terracota →
  tinta. Ninguna sección contigua repite fondo; el cambio de superficie es la puntuación del sitio.
- **La sección de trabajo es oscura ("sala de cine"):** los Shorts verticales sobre `--ink` con
  sombra profunda. Es la única forma de que un video vertical se lea como pieza y no como recuadro.
- **Serif de énfasis:** Instrument Serif itálica aparece sólo dentro de un titular, en la frase que
  carga el significado — nunca un titular entero, nunca texto corrido.
- **Coreografía de scroll** en un único orquestador rAF: barra de progreso, parallax de medios y
  llenado de la línea de proceso salen del mismo listener.

## Colors

### Primary
- **Terracota** (`#9C3B20`): color de marca. CTA, énfasis de titular, filete del acordeón abierto,
  cifras de métricas, viñetas, y **superficie de sección completa** ("Para quién trabajo",
  "Sobre mí") con texto crema encima (5.9:1).
- **Terracota Deep** (`#6E2814`): hover de CTA y banda de la franja decorativa.

### Secondary
- **Mustard** (`#E8B33D`): acento secundario — chips de servicio, numerales de audiencia, títulos
  de carrusel sobre tinta, filete del eyebrow y encabezados del footer.
- **Dusty** (`#AFCBDD`): exclusivamente una banda de la franja decorativa.

### Neutral
- **Cream** (`#F4ECE0`): fondo de página.
- **Cream Card** (`#EFE1C9`): superficie de sección alterna (Proceso) y tarjetas de métricas.
- **Surface** (`#FBF6EE`): tarjetas elevadas sobre crema — acordeón, testimonios, formulario.
- **Ink** (`#241A13`): texto principal, superficie de "Trabajo" y del footer.
- **Ink-2** (`#6B5140`): texto secundario sobre crema.
- **On Terracota** (`#EFD9C4`): texto secundario sobre terracota (5.0:1) — más cálido que el crema
  puro, evita el blanco frío sobre un fondo saturado.

### Named Rules
**La Regla del Mustard sin Texto Claro.** Mostaza sólo lleva texto `--ink` encima, nunca crema.
**La Regla del Mustard Grande.** Mostaza sobre terracota da **3.58:1**: alcanza para texto grande
(titulares ≥24px) pero **no** para labels ni cuerpo. En la banda terracota el eyebrow va en crema y
la mostaza queda reservada a su filete decorativo. Sobre tinta, en cambio, mostaza da 8.9:1 y sí
puede llevar texto chico.
**La Regla de la Superficie Terracota.** Terracota es fondo de sección completa — siempre con texto
crema, on-terracota o mostaza-grande encima, nunca terracota sobre terracota.
**La Regla de la Alternancia.** Dos secciones contiguas nunca comparten fondo.

## Typography

**Dos familias, con roles que no se solapan:** Archivo variable (100–900) para absolutamente todo
el texto; Instrument Serif itálica sólo como acento de énfasis.

### Hierarchy
- **Display** (Archivo 800, `clamp(2.05rem,5.4vw,4.1rem)`, `-0.035em`, mayúsculas): sólo el `h1`.
- **Display accent** (Instrument Serif itálica, minúscula, 1.06em): la frase de énfasis dentro del
  `h1` — el cambio de caja y de familia es el que le da carácter al titular.
- **Headline** (Archivo 700, `clamp(1.7rem,3.6vw,2.7rem)`, `-0.025em`): `h2` de sección, con su
  `<em>` en serif itálica terracota (o mostaza sobre fondos oscuros).
- **Carousel title** (Instrument Serif itálica, `clamp(1.3rem,2.4vw,1.9rem)`, mostaza): único caso
  de titular íntegramente en serif, justificado porque es un rótulo de agrupación, no una jerarquía.
- **Title** (Archivo 600, 16–19.5px): acordeón, pasos del proceso, citas.
- **Body** (400, 15–16px, 1.55–1.7).
- **Label / eyebrow** (700, 11.5px, `.18em`, mayúsculas) con un filete de 26px a la izquierda.

### Named Rules
**La Regla del Serif Acotado.** El serif itálico aparece dentro de un titular o como rótulo de
carrusel. Nunca en párrafos, labels, botones, nav ni campos de formulario.

## Layout

Contenedor centrado `max-width: 1240px` con padding lateral fluido (`--gutter`). Secciones con
`padding: clamp(64px,8vw,120px) 0` y variante de superficie por clase (`.section--card`,
`.section--terracota`, `.section--dark`).

Bandas a dos columnas donde la relación entre mitades es real: hero (video | copy), trabajo
(ediciones | guiones), servicios (cabecera | acordeón), contacto (vías directas | formulario),
sobre mí (foto | texto).

**Todas las columnas de grid usan `minmax(0,1fr)`, nunca `1fr`**: el carril del carrusel es más
ancho que su columna y con el mínimo automático de grid estiraría la página entera.

Quiebres: 1100px (servicios/contacto a una columna, proceso a dos), 1000px (carruseles apilados),
900px (hero y sobre-mí a una), 860px (menú en cajón), 760px (todo a una).

## Motion — la coreografía de scroll

Todo lo de abajo se neutraliza bajo `prefers-reduced-motion: reduce` por el reset global.

- **Barra de progreso** (`.scroll-progress`): 3px fijos arriba, degradado terracota→mostaza,
  animada por `transform: scaleX()` — nunca por `width`, que forzaría layout en cada cuadro.
- **Revelado de titular:** la línea sube desde detrás de una máscara (`overflow:hidden` en el `h2`
  + `translateY(110%)` en un `<span>` interno). Por eso **todo `h2` lleva su texto envuelto en un
  `<span>`**: sin ese span no hay qué animar.
- **Revelado genérico** (`[data-reveal]`): sube 22px y aparece, con retardo escalonado según la
  posición del elemento dentro de su propia fila (no acumulado en toda la página).
- **Parallax** (`[data-parallax="-0.06"]`): el orquestador escribe `--py` y el CSS lo aplica como
  `translate3d`. El valor es la distancia del centro del elemento al centro de la pantalla por la
  velocidad; recorrido real de ~40px en 700px de scroll.
- **Línea del proceso:** `--fill` va de 0 a 1 según el avance de la sección por la pantalla.
- **Marquee de marcas:** animación CSS pura de 46s, en pausa al pasar el cursor.
- **Botones magnéticos** (`[data-magnetic]`): sólo con puntero fino.

**Un solo listener de scroll.** Progreso, parallax y línea de proceso se calculan juntos dentro de
un `requestAnimationFrame`. Tres listeners separados dispararían tres reflows por cuadro.

## Elevation & Depth

Dos niveles cálidos (`--shadow`, `--shadow-lg`): la sombra tiene la temperatura del papel
(`rgba(78,44,24,…)`), nunca gris neutro. Además, dos recursos de profundidad sin sombra:
- **Marco desplazado:** un borde de 1.5px corrido en diagonal detrás del video del hero (terracota)
  y de la foto de "Sobre mí" (mostaza).
- **Numeral fantasma:** la cifra de cada métrica repetida en serif enorme al 7% de opacidad.
- **Textura de motas** al 5% sobre las superficies saturadas — el papel del sistema original, sin la
  metáfora literal del corcho.

## Components

### Accordion (`.acc`)
Cuatro ítems del mismo peso y espaciado, cada uno una tarjeta. La cabecera es un `<button>` real
dentro de un `<h3>`, con `aria-expanded` y `aria-controls`. El indicador `+` / `−` a la derecha es
obligatorio. Filete de color que crece a la izquierda del ítem abierto. Un solo ítem abierto por vez.

### Work carousel (`.carousel`)
Sobre fondo tinta. Carril con scroll-snap y clones antes/después para loop infinito; la pieza
centrada va a escala 1 y opacidad 1, las laterales a `.86` / `.3`. Un solo iframe de YouTube por
carrusel, montado recién cuando el desplazamiento se detiene y sólo mientras el carrusel está a la
vista. Autoplay silenciado con badge de sonido.

### Testimonial card
Cita **textual** del cliente, meta ("Cliente · WhatsApp") y la captura real dentro de un `<details>`
plegado. La captura es la prueba, no el elemento principal.

### Form
Campos con caja sobre crema. Cuatro estados: hover, foco (borde terracota + anillo de 3px),
inválido (`aria-invalid` + borde danger + mensaje bajo el campo) y confirmación. El error aparece al
salir del campo y se limpia mientras se corrige.

### Navigation
Header sticky con desenfoque **en un pseudo-elemento, no en el header**: un `backdrop-filter`
convierte a su elemento en bloque contenedor de todo descendiente `position:fixed`, y eso encierra
al cajón del menú mobile dentro de la barra. `section[id]` lleva `scroll-margin-top: 96px`.

### Stripe (`.stripe`)
`<hr>` de 16px con `repeating-linear-gradient` de cuatro bandas de 24px, en dos órdenes de color
(`--a` / `--b`). Marca las transiciones mayores; no se usa dentro de una sección.

## Do's and Don'ts

### Do:
- **Do** envolver el texto de cada `h2` en un `<span>` — es lo que anima el revelado por máscara.
- **Do** alternar la superficie de cada sección respecto de la anterior.
- **Do** verificar el contraste de mostaza según el fondo: sobre tinta sirve para texto chico, sobre
  terracota sólo para texto grande.
- **Do** sumar cualquier efecto de scroll nuevo al orquestador existente, no con un listener propio.
- **Do** usar `minmax(0,1fr)` en toda columna de grid que pueda contener un carril con scroll.

### Don't:
- **Don't** volver a chinches, cintas, corcho, símbolos flotantes ni rotaciones al azar.
- **Don't** poner el serif en párrafos, labels, botones o campos.
- **Don't** animar `width`, `top` o `left` en efectos de scroll — sólo `transform` y `opacity`.
- **Don't** poner texto crema sobre mostaza, ni texto chico en mostaza sobre terracota.
- **Don't** poner `backdrop-filter` sobre un ancestro de un elemento `position:fixed`.
