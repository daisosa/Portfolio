# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Marcas y negocios (consumo masivo, emprendimientos y marcas personales) que buscan estrategia y creación de contenido para destacar en un mercado saturado.

## Mode

Experience.

El sitio prioriza una experiencia visual memorable por encima de una interfaz convencional. El trabajo y el contenido deben guiar la navegación mediante movimiento, ritmo y una presentación editorial, sin comprometer la usabilidad.

## Brand Voice

Estratégica, creativa y dinámica.

El tono debe ser profesional, cercano y difícil de ignorar ("un-ignorable"). Debe transmitir que el contenido es un sistema con propósito, no una colección de publicaciones aisladas.

## Product Purpose

Portfolio freelance de Daiana "Dai" Sosa para conseguir clientes de estrategia y creación de contenido.

El mensaje central es directo y verificable: Dai hace estrategia de contenido, guiones y edición de video para marcas y creadores, con más de cuatro años de trabajo y clientes reales detrás. La propuesta de valor se enuncia en el titular; el diagnóstico, la línea editorial y la optimización aparecen como el método (sección Proceso), no como el gancho.

Se descartó el mensaje anterior ("nunca fue tan fácil crear contenido, nunca fue tan difícil destacar") por genérico: no decía qué hace Dai, para quién ni cómo, y es una construcción intercambiable con la de cualquier otro perfil del rubro.

## Positioning

El contenido se trata como un sistema con propósito (diagnóstico + línea editorial + producción), no como piezas o decisiones de publicación aisladas.

Cuatro líneas de servicio ofrecidas:

- Estrategia de contenido.
- Guiones.
- Edición.
- Acompañamiento creativo continuo.

## Operating Context

- Freelance solista, sin equipo fijo. Modalidad principal: por proyecto.
- Una de las cuatro líneas de servicio ("Acompañamiento creativo") es seguimiento mensual continuo; coexiste con la modalidad principal por proyecto.
- Proceso de trabajo declarado en el sitio: Diagnosticar → Pensar → Escribir → Optimizar.
- Ubicada en Buenos Aires, Argentina.
- Vías de contacto: formulario del sitio, email y WhatsApp (+54 9 11 3504-6576).
- El footer no incluye enlaces de Instagram o LinkedIn (pendiente de definir). El bloque está escrito y comentado en `index.html`: sólo hay que descomentarlo y completar las URLs.

## Capabilities and Constraints

- Sitio estático de una sola página (`index.html`) desarrollado únicamente con HTML, CSS y JavaScript vanilla.
- Sin backend ni framework.
- Sin sistema de build.
- El formulario valida en el cliente y abre el cliente de correo mediante `mailto:`; no existe envío directo desde el navegador.
- Sin CMS: cualquier modificación de contenido requiere editar el HTML.

## Brand Commitments

- Nombre: "Dai Sosa" (Daiana Sosa).
- Ya existe un sistema visual completo (paleta, tipografía y componentes) implementado en `index.html`. Si se desea documentarlo formalmente, utilizar `DESIGN.md`.

## Evidence on Hand

- Clientes confirmados para la sección "Marcas que confiaron en mi trabajo" (logos reales en `assets/logos/`):
  - URV
  - Airo
  - Arakina
  - Brahma
  - Bulldog
  - Café Martínez
  - Cozy
  - Henry
  - Incamed
  - Oregon
  - Otaku
  - Porto
  - Timeleft
  - Tumm
- Testimonios: 6 capturas reales de clientes en `assets/testimonios/01.jpeg`–`06.jpeg`. En el sitio se muestran como cita textual (transcripción literal de la captura, sin nombre porque las capturas no lo exponen) con la captura original disponible en un `<details>` plegado. Ninguna cita puede editarse para "mejorarla": el texto tiene que coincidir con la captura.
- Los 12 videos de los carruseles (Mis ediciones / Mis guiones) son Shorts de YouTube reales; se cambian reemplazando `data-id` y `data-video` en cada `<li class="carousel-item">` — no se suben archivos de video al repo (límite de tamaño de GitHub). El video del hero usa el mismo mecanismo (`[data-hero-media]`).
- Email de contacto: `mambocreativook@gmail.com`.

## Product Principles

- El contenido es un sistema, no piezas aisladas.
- Toda propuesta parte de diagnóstico, estrategia y línea editorial.
- La prueba social siempre debe ser real; nunca inventar clientes, testimonios, métricas o resultados.
- El posicionamiento debe reflejar que Dai trabaja como freelancer independiente, nunca como una agencia.
- El sitio debe seguir funcionando como un hosting 100 % estático.

## Design Principles

- La experiencia debe sentirse editorial, viva y dinámica.
- El trabajo de Dai debe ser el protagonista de la interfaz.
- Priorizar narrativa visual, ritmo, movimiento y jerarquía antes que componentes genéricos.
- Buscar una estética memorable sin sacrificar claridad ni velocidad de navegación.

## Anti-References

Evitar:

- Estética "AI Beige" o interfaces genéricas.
- Componentes excesivamente estándar con bordes redondeados y sombras planas por defecto.
- Diseños que parezcan dashboards, templates o landing pages intercambiables.
- Páginas excesivamente estáticas, clínicas o similares a un documento de texto.

## Accessibility & Inclusion

No existen requerimientos específicos adicionales más allá de las buenas prácticas ya implementadas:

- Contraste WCAG AA.
- Formularios correctamente etiquetados.
- Landmarks semánticos.
- Navegación clara y accesible.
