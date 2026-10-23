# El Kiosko · Landing page

Landing page de **El Kiosko**, agencia de marketing. Servicios (solo estos cuatro): Branding, Diseño y desarrollo web, Social media & content, y SEO. Se escribe con K, como en el rótulo de la ilustración. Una sola página, sin build: HTML, CSS y JS en `index.html`.

## Archivos
- `index.html`: toda la página (estilos y scripts en línea).
- `kiosko.jpg`: ilustración lineal del kiosko (negro sobre blanco). En la web se invierte con `filter: invert(1)` y `mix-blend-mode: screen` para verse en blanco sobre negro.

`index.html` no lleva `<!doctype>`, `<html>`, `<head>` ni `<body>`: se publica como Artifact de Claude, que añade ese esqueleto. Abierto en local con doble clic también funciona.

## Identidad
- Colores (tokens en `:root`): `--ink #0B0B0B` negro profundo, `--bone #F6F5F0` blanco roto, `--accent #A78BFA` lavanda, `--mute #A0A0A0` gris neutro.
- Secciones claras con la clase `.light`, que redefine los tokens (los pilares Criterio/Rigor/Cercanía y Compromisos).
- Tipografías (Google Fonts): Montserrat para títulos y etiquetas, Inter para textos.
- Las palabras destacadas en los títulos usan `.serif`: Montserrat cursiva en lavanda.
- Las etiquetas de sección van entre corchetes: `[ Servicios ]`.
- Los textos están en español de España (tuteo) y el tono es cercano pero profesional.

## Estructura
1. Hero: titular y kiosko con cuatro vitrinas sobre el dibujo (`.vit`, con `data-svc` = web | branding | redes | seo): la puerta de la izquierda, el escaparate central, la vitrina de la derecha y el mostrador. Al pasar el ratón la vitrina se abre y despliega su panel `.vit__info` (en táctil, al tocar); los subservicios están en el objeto `SVC` del script.
2. Marquesina con velocidad ligada al scroll.
3. Agencia: manifiesto con palabras que se iluminan y tres pilares.
4. Servicios (claro): filas con relleno al pasar el ratón.
5. Método: 4 fases con columna fija; un raíl lavanda se llena al bajar, la fase centrada en pantalla se ilumina (`.step.on`) y el indicador `#phase` muestra cuál es.
6. Sectores: scroll horizontal fijado (solo en escritorio) y tarjeta final "Tu marca, aquí".
7. Planes: tres tarjetas `.plan` fijas (sticky) que se apilan al bajar (negra, lavanda y blanca); la de debajo se encoge y oscurece según `--c`, que calcula el script. El contenido está en el HTML.
8. Compromisos (claro), Preguntas (acordeón), Contacto (formulario) y footer con "KIOSKO" gigante.

Animaciones: revelado por líneas (`.reveal .line`) con IntersectionObserver, preloader 000→100, cursor propio (punto que crece y se vuelve lavanda sobre lo pulsable) y nav que se oculta. Todo respeta `prefers-reduced-motion`.

## Pendiente
- Email real (ahora `hola@elkiosko.agency`, inventado).
- Conectar el formulario a un servicio de envío (ahora es de demostración).
