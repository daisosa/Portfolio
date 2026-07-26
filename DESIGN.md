---
name: Dai Sosa — Portfolio
description: Portfolio freelance de estrategia y creación de contenido, Buenos Aires, Argentina
colors:
  violeta-electrico: "oklch(48% 0.18 310)"
  violeta-electrico-brillante: "oklch(64% 0.16 305)"
  violeta-electrico-frio: "oklch(40% 0.17 288)"
  violeta-electrico-calido: "oklch(44% 0.16 335)"
  lila-suave: "oklch(84% 0.045 300)"
  noche: "oklch(14% 0.012 300)"
  noche-suave: "oklch(18% 0.014 300)"
  papel-crema: "oklch(96.5% 0.012 80)"
  papel-crema-sombreado: "oklch(93% 0.014 80)"
  tinta: "oklch(20% 0.012 300)"
  tinta-atenuada: "oklch(42% 0.03 300)"
typography:
  display:
    fontFamily: "'Instrument Serif', 'Times New Roman', serif"
    fontSize: "clamp(2.6rem, 3rem + 4.6vw, 7.6rem)"
    fontWeight: 400
    lineHeight: 0.98
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "'Instrument Serif', 'Times New Roman', serif"
    fontSize: "clamp(2.2rem, 4.4vw, 4.4rem)"
    fontWeight: 400
    lineHeight: 1.05
  title:
    fontFamily: "'Instrument Serif', 'Times New Roman', serif"
    fontSize: "clamp(1.5rem, 3vw, 2.6rem)"
    fontWeight: 400
    lineHeight: 1.15
  body:
    fontFamily: "'Inter Tight', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "'Inter Tight', 'Helvetica Neue', Arial, sans-serif"
    fontSize: "11px"
    fontWeight: 600
    letterSpacing: "0.18em"
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
    textColor: "{colors.tinta}"
    typography: "{typography.label}"
    padding: "14px 2px"
  chip:
    backgroundColor: "transparent"
    textColor: "{colors.tinta-atenuada}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "6px 12px"
---

# Design System: Dai Sosa — Portfolio

## Overview

**Creative North Star: "El Cuaderno de Estrategia"**

Un cuaderno de trabajo editorial, no un producto de SaaS: numeración de secciones (01, 02, 03…), reglas finas en vez de cajas, y una serif de autor que interrumpe la sans-serif técnica para marcar énfasis, como si alguien subrayara una palabra al escribir a mano. El tono es expresivo, profesional pero cercano — el resplandor violeta y los degradés cinematográficos en las secciones oscuras le dan dramatismo, pero el papel crema y la tipografía contenida en las secciones claras lo devuelven a un registro de estudio, no de discoteca.

El sitio alterna entre dos temperaturas: secciones "papel" (crema, tinta oscura, editorial) y secciones "noche" (violeta-negro, texto claro, más teatral). Ambas comparten la misma tipografía y el mismo lenguaje de reglas finas — es una sola voz con dos iluminaciones distintas, no dos sistemas.

**Key Characteristics:**
- Serif de autor (Instrument Serif) para todo titular y para el énfasis en cursiva; sans técnica (Inter Tight) para todo lo demás.
- Kicker numerado ("01 — Portada") como firma recurrente de navegación editorial.
- Violeta eléctrico como único acento de color; el resto es tinta, papel y noche.
- El sistema nació plano (sin sombra) y ahora combina superficies planas (listas, formularios) con profundidad táctil en las superficies discretas: sombra tibia sobre papel, resplandor violeta sobre noche — ver Elevación.

## Colors

Paleta de dos temperaturas: acento violeta eléctrico + neutros tinta/papel/noche. Un solo acento de color, nunca una paleta multicolor.

### Primary
- **Violeta Eléctrico** (`oklch(48% 0.18 310)`): el acento funcional — línea de progreso de scroll, punto del proceso, selección de texto, fondo de botones al hover. Úsalo con moderación; es el color que la mirada debe encontrar, no el que la satura.
- **Violeta Eléctrico Brillante** (`oklch(64% 0.16 305)`): variante más luminosa del mismo acento — cursor a medida, línea de progreso, dot decorativo. Para acentos puntuales sobre fondo oscuro.
- **Violeta Eléctrico Frío** (`oklch(40% 0.17 288)`) y **Violeta Eléctrico Cálido** (`oklch(44% 0.16 335)`): los dos extremos del degradé de fondo en las secciones "noche" (hero, contacto). Nunca se usan como color de texto o de control; son exclusivamente atmósfera de fondo.

### Secondary
- **Lila Suave** (`oklch(84% 0.045 300)`): color reservado para la cursiva de énfasis dentro de titulares sobre fondo oscuro (`<em>` del hero) y para el subtítulo inmediatamente debajo. No se usa en botones, links ni controles — es puramente tipográfico.

### Neutral
- **Papel Crema** (`oklch(96.5% 0.012 80)`): fondo por defecto de las secciones claras (marcas, proceso, servicios, sobre mí).
- **Papel Crema Sombreado** (`oklch(93% 0.014 80)`): variante ligeramente más oscura para diferenciar la sección de testimonios del resto del papel.
- **Tinta** (`oklch(20% 0.012 300)`): color de texto por defecto sobre papel.
- **Tinta Atenuada** (`oklch(42% 0.03 300)`): texto secundario sobre papel (kickers, meta-datos, etiquetas) — un color sólido, no una opacidad sobre tinta, para mantener el contraste WCAG AA (~7.7:1 sobre papel crema).
- **Noche** (`oklch(14% 0.012 300)`) y **Noche Suave** (`oklch(18% 0.014 300)`): fondo de las secciones oscuras (hero, trabajo, contacto) y su variante para paneles internos (marco de foto).

### Named Rules
**La Regla de un Solo Acento.** El violeta es el único color con significado; todo lo demás es tinta, papel o noche. Si hace falta un segundo color para diferenciar algo, se resuelve con tipografía o espaciado, no con otro tono.

## Typography

**Display Font:** Instrument Serif (con Times New Roman de respaldo)
**Body/Label Font:** Inter Tight (con Helvetica Neue, Arial de respaldo)

**Character:** Una serif de autor, editorial y ligeramente clásica, interrumpe una sans técnica y neutra. La serif es la voz que habla — sube de tamaño, se pone en cursiva para enfatizar; la sans es la voz que organiza — kickers, navegación, meta-datos, siempre en mayúscula y tracking abierto.

### Hierarchy
- **Display** (400, `clamp(2.6rem, 3rem + 4.6vw, 7.6rem)`, line-height 0.98): titular del hero únicamente. La cursiva dentro del display usa Lila Suave.
- **Headline** (400, `clamp(2.2rem, 4.4vw, 4.4rem)`, line-height ~1.05): título de cada sección numerada ("Selección de proyectos", "En qué puedo ayudarte").
- **Title** (400, `clamp(1.5rem, 3vw, 2.6rem)` a `clamp(18px, 1.6vw, 22px)` según el componente): nombres de proyecto, título de servicio, encabezado de paso de proceso.
- **Body** (400, 16px, line-height 1.5): párrafos y copy general.
- **Label** (600, 11px, tracking 0.18em, uppercase): kickers numerados, tags de servicio, links de navegación y footer.

### Named Rules
**La Regla del Kicker Numerado.** Cada sección principal abre con "NN — Nombre" en Label. Es la firma de navegación del sistema; no se usa este patrón para nada que no sea el inicio de una sección de primer nivel.

## Layout

Contenedor centrado con `max-width: 1440px` y padding lateral fluido (`--gutter`, `clamp(20px, 5vw, 64px)`). Ritmo vertical entre secciones controlado por un único token (`--section-y`, `clamp(72px, 11vw, 168px)`) — toda sección respira el mismo aire, sin excepciones ad hoc. Sin grid de columnas global: cada componente define su propia grilla local cuando la necesita (fila de servicio: `90px 1fr auto`; header: logo/nav/toggle). Responsive en tres quiebres (1180px, 860px, 600px), mobile-first en la lógica de contenido aunque el CSS esté escrito desktop-first.

## Elevation & Depth

**Estado actual (implementado):** ya no es un sistema puramente plano — se extendió profundidad más allá de testimonios, con dos vocabularios según la superficie de fondo:

- **Sobre papel** (fondo claro): sombra oscura tibia (`rgba(20,10,40,...)`). Usada en la tarjeta de testimonio (flota + rotación tipo Polaroid, se "endereza" al hover) y ahora también en el CTA principal (botón lleno, ver Components).
- **Sobre noche** (fondo oscuro): una sombra oscura es invisible contra un fondo casi negro, así que la profundidad se resuelve con un resplandor violeta claro en vez de una sombra oscura — misma regla ("nunca gris neutro"), adaptada a que el tono deba ser más claro que el fondo, no más oscuro. Usada en los marcos de trabajo (`.work-frame`).

Separación general entre bloques sigue resolviéndose con espacio y líneas finas (`--line-on-light` / `--line-on-dark`, 1px al 14% de opacidad) — la sombra es para superficies que "flotan" como objetos, no para separar secciones o listas continuas (ver Do's and Don'ts).

### Shadow Vocabulary
- **ambient-card** (`box-shadow: 0 24px 48px -24px rgba(20,10,40,.18)`): reposo, superficie clara que flota (testimonios, CTA principal).
- **lifted-card** (`box-shadow: 0 32px 60px -20px rgba(20,10,40,.24–.5)`): hover/activo de la misma superficie clara.
- **ambient-glow-dark** (`box-shadow: 0 24px 48px -16px rgba(161,90,207,.25)`): reposo, superficie oscura que flota (marcos de trabajo).
- **lifted-glow-dark** (`box-shadow: 0 28px 64px -12px rgba(161,90,207,.4)`): hover/activo de la misma superficie oscura.

### Named Rules
**La Regla de la Sombra Tibia.** Ninguna sombra es gris neutro: sobre papel se tiñe de violeta-tinta oscuro (`rgba(20,10,40,...)`); sobre noche se invierte a un resplandor violeta claro (`rgba(161,90,207,...)`) porque una sombra oscura no se ve contra un fondo oscuro. Nunca `rgba(0,0,0,...)` ni un gris neutro genérico en ningún caso.
**La Regla de Superficie Flotante.** La sombra/resplandor se reserva para componentes que son objetos discretos con espacio alrededor (cards con `gap`, botones). No se aplica a filas de una lista continua (ej. el acordeón de servicios) — ahí la profundidad se resuelve con el invertido de color que ya existe al hover, no con `box-shadow`, para evitar el efecto "tarjeta fantasma" de una sombra que choca contra el borde del vecino.

## Shapes

Radios casi rectos: `--radius-soft` (2px) en los marcos de imagen es la única esquina "curva" real del sistema — todo lo demás es o bien recto (botones, inputs, contenedores) o completamente circular (`50%`: dots, cursor, iconos de proceso) o pill (`100px`: chips de servicio). No hay un radio intermedio tipo "8px/12px card": el sistema evita deliberadamente el lenguaje de tarjeta redondeada genérica. Bordes: solo hairlines de 1px en `--line-on-light`/`--line-on-dark`; nunca un borde de color sólido grueso.

## Components

Carácter general: **táctil y cálido** — la dirección confirmada se aleja de la austeridad puramente editorial de botones sin relieve hacia controles con más superficie, más peso y una sensación más "tocable", sin perder la tipografía como protagonista.

### Buttons
- **Editorial (secundario):** sin relleno, solo regla superior e inferior de 1px en `currentColor` (`.btn-editorial`). Hover reduce opacidad a .7 y desplaza el ícono con `transform: translateX(8px)`. Reservado a acciones secundarias.
- **Táctil (CTA principal):** `.hero-cta` y `.finale-submit` — pill (`border-radius: 100px`), fondo Violeta Eléctrico, texto Papel Crema, sombra `ambient-card`, padding generoso (`18px 32px`). Hover pasa a Violeta Eléctrico Brillante, se levanta (`translateY(-3px)`) y la sombra crece a `lifted-card`. Es la variante "táctil y cálido" para las dos acciones de conversión del sitio (agendar/enviar) — el resto de los botones se queda en editorial.

### Chips
- **Style:** sin relleno, borde de 1px en `currentColor`, texto en Tinta Atenuada, `border-radius: 100px` (`.service-extra span`).
- **State:** no tienen variante seleccionada/no-seleccionada — son puramente informativos, no interactivos.

### Cards
- **Trabajo (`.work-card`):** marco de imagen `9/16` con radio `--radius-soft`, sombra `ambient-glow-dark` en reposo (resplandor violeta, no sombra oscura — el fondo de la sección es casi negro), `lifted-glow-dark` + `translateY(-4px)` al hover.
- **Testimonio (`.testimonial-card`):** sombra `ambient-card`/`lifted-card` + rotación aleatoria (±1.4°/1.6°) tipo Polaroid disperso sobre una mesa. Sigue siendo la referencia de "cómo se ve la profundidad" sobre papel.
- **Fila de servicio (`.service-row`):** deliberadamente sin sombra — es una lista continua con divisores hairline, no una tarjeta discreta; la profundidad al hover se resuelve invirtiendo a fondo Noche/texto Papel Crema, no con `box-shadow` (ver Regla de Superficie Flotante en Elevation).

### Inputs / Fields
- **Style:** sin caja — solo `border-bottom` implícito vía el patrón general de líneas finas, label en Label por encima del campo.
- **Focus:** cambia `border-color` a Violeta Eléctrico Brillante (`outline:none` con reemplazo explícito, no eliminación silenciosa del foco).

### Navigation
- **Style:** links en Label, subrayado que se revela de izquierda a derecha al hover (`::after` con `right:0`). En mobile, drawer de pantalla completa sobre Noche con el mismo tratamiento de link, activado por un botón hamburguesa de 44×44px.

## Do's and Don'ts

### Do:
- **Do** usar Violeta Eléctrico como único acento con significado; todo lo demás son neutros de tinta/papel/noche.
- **Do** teñir cualquier sombra nueva del mismo violeta-tinta oscuro (`rgba(20,10,40,...)`) sobre papel, o del resplandor violeta claro (`rgba(161,90,207,...)`) sobre noche — nunca gris neutro.
- **Do** usar el kicker numerado (`NN — Nombre`, Label) solo para el inicio de una sección de primer nivel.
- **Do** reservar la variante táctil (fondo sólido + sombra) para el CTA principal y las cards discretas (trabajo, testimonios); el resto de los botones se queda editorial.
- **Do** resolver la profundidad de listas continuas (fila de servicio) con el invertido de color al hover, no con `box-shadow`.

### Don't:
- **Don't** introducir un segundo color de acento — el sistema es deliberadamente mono-acento.
- **Don't** usar radios intermedios tipo "8px card" — el vocabulario de forma es recto, circular o pill, nada entre medio.
- **Don't** apagar el foco visible (`outline:none`) sin un reemplazo de contraste equivalente (ver Focus en Inputs).
- **Don't** aplicar `box-shadow` a una fila de una lista continua con divisores hairline — choca contra el borde del vecino ("tarjeta fantasma"); usar el invertido de color en su lugar.
- **Don't** confundir "más profundidad" con sombras grises genéricas de UI kit — toda sombra nueva sigue la Regla de la Sombra Tibia.
