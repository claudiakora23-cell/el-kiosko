# El Kiosko · Landing page

Landing page de **El Kiosko**, agencia de marketing en Málaga. Servicios (solo estos cuatro): Branding, Diseño y desarrollo web, Social media & content, y SEO. Se escribe con K, como en el rótulo de la ilustración. Una sola página, sin build: HTML, CSS y JS en `index.html`.

## Archivos
- `index.html`: toda la página (estilos y scripts en línea), con documento HTML completo (`<!doctype>`, `<head>` con metadatos Open Graph y `canonical`).
- `kiosko-lineas.png`: la ilustración del kiosko en líneas claras sobre fondo transparente; es la que usa el hero (sin filtros ni fundidos, para que el fondo sea idéntico al de la página en cualquier móvil). Se generó a partir de `kiosko.jpg` (negro sobre blanco), que se queda como imagen para compartir en redes (`og:image`) y datos de Google.
- `aviso-legal.html`, `privacidad.html`, `cookies.html` + `legal.css`: páginas legales (con `noindex`). Titular: persona física con nombre comercial El Kiosko.
- `_version-*/`: copias de versiones anteriores; no se publican.

Se publica con GitHub Pages: https://claudiakora23-cell.github.io/el-kiosko/

## Identidad
- Colores (tokens en `:root`): `--ink #0B0B0B` negro profundo, `--bone #F6F5F0` blanco roto, `--accent #A78BFA` lavanda, `--mute #A0A0A0` gris neutro.
- Secciones claras con la clase `.light`, que redefine los tokens (los pilares Criterio/Rigor/Cercanía y Compromisos).
- Tipografías (Google Fonts): Montserrat para títulos y etiquetas, Inter para textos.
- Las palabras destacadas en los títulos usan `.serif`: Montserrat cursiva en lavanda.
- Las etiquetas de sección van entre corchetes: `[ Servicios ]`.
- Los textos están en español de España (tuteo) y el tono es cercano pero profesional.
- Contacto: elkioskoagency@gmail.com · Instagram @kiosko.agency. Sin teléfono ni LinkedIn.

## Estructura
1. Hero: titular y kiosko con cuatro pizarras de kiosko sobre el dibujo (`.vit`, con `data-svc` = web | branding | redes | seo): tablero negro con marco metálico, cada una a su altura. Web, Branding y Social media cuelgan del toldo con cadenas (largo en `--cord`) y se balancean; SEO es de caballete (`.vit--easel`) en el suelo y apenas se mece. Posición y tamaño en variables del `style` (`--x` centro, `--y` arriba, `--w`, `--ar`, `--fs`, `--tilt`). Al pasar el ratón se despliega la pizarra grande `.vit__info` (en táctil, al tocar); los subservicios están en el objeto `SVC` del script.
2. Marquesina con velocidad ligada al scroll.
3. Agencia: manifiesto con palabras que se iluminan y tres pilares.
4. Servicios (claro): filas con relleno al pasar el ratón.
5. Método: 4 fases con columna fija; un raíl lavanda se llena al bajar, la fase centrada en pantalla se ilumina (`.step.on`) y el indicador `#phase` muestra cuál es.
6. Sectores: scroll horizontal fijado (solo en escritorio) y tarjeta final "Tu marca, aquí".
7. Planes: tres tarjetas `.plan` fijas (sticky) que se apilan al bajar (negra, lavanda y blanca); la de debajo se encoge y oscurece según `--c`, que calcula el script. El contenido está en el HTML.
8. Compromisos (claro), Preguntas (acordeón), Contacto (formulario con consentimiento de privacidad) y footer con datos de contacto, enlaces legales y "KIOSKO" gigante.

Animaciones: revelado por líneas (`.reveal .line`) con IntersectionObserver, preloader 000→100, cursor propio (punto que crece y se vuelve lavanda sobre lo pulsable) y nav que se oculta. Todo respeta `prefers-reduced-motion`.

Los datos sin rellenar llevan la clase `.tbd` (se ven marcados en lavanda).

## Pendiente
- Calle y número del domicilio en `aviso-legal.html`, `privacidad.html` y los datos estructurados de `index.html`.
- Formulario conectado con FormSubmit (`formsubmit.co/ajax/elkioskoagency@gmail.com`); la primera vez hay que activarlo desde el email que llega al Gmail.
- Dominio propio (cuando lo haya, cambiar la URL de GitHub Pages en `index.html` y `aviso-legal.html`).
