# Brief: página de enlaces (links.pradomacat.com)

*Documento de contexto para la sesión de construcción. Creado el 25 nov 2026. El archivo `tokens.css` (cara clara) se pasa aparte: es la fuente de los estilos.*

## Objetivo
Una página de enlaces mínima, tipo linktree, para poner en las bios de Instagram y YouTube. Lleva a la gente a los lugares que importan sin que tenga que pensar. **No es la web completa**: `pradomacat.com` sigue siendo la web principal (perfil de programador y sesiones). Esta página es una puerta de entrada rápida.

- **Dominio:** `links.pradomacat.com`
- **Hosting:** GitHub Pages, con archivo `CNAME` en el repo. El DNS está en Cloudflare (registro CNAME del subdominio hacia el usuario de GitHub Pages).
- **Stack:** HTML/CSS/JS vanilla, sin frameworks ni dependencias. Una sola página.
- **Uso principal:** móvil, abierta desde el navegador interno de Instagram o YouTube. Diseño mobile first, carga muy rápida.

## Quién es Fede (lo que se puede decir)
- Nombre de marca: **Federico Prado Macat** (el dominio es pradomacat.com solo por practicidad; el nombre visible siempre es el completo). Se le dice "Fede" en el trato cercano. El wordmark es "Federico Prado Macat" en la serif del sistema.
- Ofrece **sesiones 1:1 de coaching y breathwork** online, en español.
- Está **en formación** en coaching y breathwork. **No decir "certificado" ni "facilitador acreditado"**.
- Tiene un canal de YouTube de meditaciones guiadas (@meditawork) y una app gratuita de respiración (Neyen).
- Es programador, pero en esta página no hace falta mencionarlo salvo un enlace a la web principal.

## Enlaces (en este orden)
| # | Texto del botón | Destino | Tipo |
|---|---|---|---|
| 1 | Reservar una llamada gratuita | https://federico.pradomacat.com/ (o directo al Calendly, URL pendiente de confirmar) | **Primario** (el único) |
| 2 | Sesiones 1:1 de breathwork | https://federico.pradomacat.com/ | Secundario |
| 3 | Practicá con Neyen, la app de respiración | https://neyen.pradomacat.com/ | Secundario |
| 4 | Meditaciones en YouTube | https://www.youtube.com/@meditawork | Secundario |
| 5 | Mi web | https://pradomacat.com/ | Secundario |
| 6 | Escribime | mailto:contacto@pradomacat.com | Texto/enlace discreto en el pie |

**Notas:**
- **Un solo botón primario**, como en el resto del sistema. Los demás son secundarios (pastilla con contorno).
- **Instagram no va por ahora**: la cuenta `@pradomacat` está vacía. Dejar el bloque preparado pero oculto, para activarlo cuando tenga contenido. `@soypradito` está cerrada y no debe aparecer.
- **Buy Me a Coffee no va en esta página.** Decisión del 25 nov: se mezcla con la venta de sesiones. Si se conserva, vive solo en un lugar discreto de Neyen.
- Si el botón 1 y el 2 apuntan al mismo destino, evaluar dejar solo el 1 y no repetir.

## Contenido sugerido
- **Avatar:** la foto de Fede (`/assets/fede.jpg` de la landing; copiarla al repo y optimizarla) con el arco superior de la landing (`--radius-arch`), con texto alternativo descriptivo.
- **Nombre:** "Federico Prado Macat" (serif, protagonista).
- **Frase breve (a elegir con Fede):**
  1. "Un espacio para frenar, respirar y escucharte."
  2. "Sesiones 1:1 de coaching y breathwork online."
  3. Combinar la primera como frase y la segunda como subtítulo pequeño.
- Sin párrafos largos: nombre, una frase, botones y pie.

## Diseño
- **Cara clara del sistema** (misma que la web de sesiones), para que se vea como parte de la misma marca. No usar `tokens-dark.css`.
- Cargar `tokens.css` y escribir `styles.css` usando **solo variables**: ni colores, ni tamaños, ni radios, ni sombras escritos a mano.
- Tono: **cálido y sereno**. Fondo crema (`--color-bg`), aura suave de celeste y durazno como en el inicio de la landing (decorativa, sin texto encima), terracota solo en detalles pequeños.
- **Tipografía:** serif para el nombre y la frase; sans de sistema para los botones. Sin fuentes externas.
- **Layout:** una columna centrada, ancho máximo estrecho (usar `--container-narrow` o menos), botones a todo el ancho en móvil, alto `--btn-height` (48px).
- **Botones:** los del sistema (`--btn-*`): pastilla, borde 1,5px, peso 500. Separación cómoda entre ellos para tocar con el pulgar.
- **Movimiento:** aparición suave con `--ease-out` y `--duration-reveal` (opcional), y hover con `--duration-fast`. Respetar `prefers-reduced-motion`: sin animación si el sistema lo pide.
- **Sombras:** casi ninguna, como en el resto del sistema.

## Accesibilidad
- Contraste mínimo 4,5:1 en todo texto (los tokens ya lo cumplen; no introducir colores nuevos).
- Foco visible en todos los enlaces (`--color-focus`).
- Un solo `h1` ("Federico Prado Macat"), `lang="es"`, estructura semántica (`main`, lista `ul` de enlaces).
- Zonas de toque de al menos 44px.
- Enlaces con texto claro, sin emojis como único contenido. Si se usa icono, con texto visible al lado.

## SEO y metadatos
- `<title>`: "Federico Prado Macat · Coaching y breathwork online" (ajustable).
- `meta description` corta y sin afirmaciones de salud.
- Open Graph y Twitter card con la foto o una imagen de marca (1200×630).
- `theme-color`: `#faf6f0`.
- **`noindex` por ahora**, igual que `federico.pradomacat.com`, hasta que las webs estén lanzadas. Se quita al lanzar. Confirmar con Fede.
- Favicon simple con la inicial o el wordmark.

## Lo que NO puede aparecer
- Afirmaciones de salud o curación ("sana", "trata", "reemplaza terapia") ni efectos sobre ansiedad, insomnio, etc.
- Promesas de resultado o garantías.
- Títulos que no tiene ("certificado", "acreditado").
- Testimonios inventados, urgencia falsa o contadores.
- Enlace a `@soypradito` (cuenta cerrada).

## Privacidad y legal
- La página **no debe usar cookies ni analíticas** de terceros por defecto. Si más adelante se agrega analítica, habría que actualizar el texto de privacidad y revisar el aviso de cookies (RGPD/LSSI, Fede vive en España).
- Pie mínimo: contacto (`contacto@pradomacat.com`), "© 2026 Federico Prado Macat" y un enlace a la política de privacidad de la web de sesiones cuando exista.
- Si se mide clics, hacerlo sin cookies (por ejemplo, parámetros UTM en los destinos) y solo si Fede lo pide.

## Requisitos técnicos
- Estructura simple:
  ```
  index.html
  styles.css
  tokens.css        (copia del de la landing, sin modificar)
  CNAME             (links.pradomacat.com)
  assets/           (foto optimizada, og-image, favicon)
  ```
- Imágenes optimizadas (foto en WebP/JPG ligero con tamaños adecuados).
- Sin JavaScript obligatorio: la página funciona sin él. JS solo para detalles opcionales (animación de entrada).
- HTTPS activo en GitHub Pages; verificar que el CNAME y el DNS resuelvan.
- Probar en móvil real y en el navegador interno de Instagram/YouTube si es posible.

## Criterio de "terminado"
- Se ve bien y se toca bien en móvil (320px en adelante) y en escritorio.
- Pasa revisión de contraste y de teclado.
- Sin colores ni tamaños escritos a mano: todo viene de `tokens.css`.
- Los enlaces apuntan a los destinos correctos.
- `links.pradomacat.com` responde por HTTPS.

## Pendientes que decide Fede
- [ ] URL de Calendly (si el botón 1 va directo a reservar, en lugar de a la web).
- [ ] Frase de presentación (opciones arriba).
- [ ] ¿Mantener `noindex` hasta el lanzamiento?
- [ ] Activar el bloque de Instagram cuando `@pradomacat` tenga contenido.
