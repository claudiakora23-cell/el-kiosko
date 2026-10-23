# El Kiosko · Landing page

Landing page de **El Kiosko**, agencia de marketing (páginas web, branding y redes sociales). Se escribe con K, como en el rótulo de la ilustración. Una sola página, sin build: HTML, CSS y JS en `index.html`.

## Archivos
- `index.html`: toda la página (estilos y scripts en línea).
- `kiosko.jpg`: ilustración lineal del kiosko (negro sobre blanco). En la web se invierte con `filter: invert(1)` y `mix-blend-mode: screen` para verse en blanco sobre negro.

`index.html` no lleva `<!doctype>`, `<html>`, `<head>` ni `<body>`: se publica como Artifact de Claude, que añade ese esqueleto. Abierto en local con doble clic también funciona.

## Identidad
- Colores (tokens en `:root`): `--ink #0B0B0B` negro profundo, `--bone #F6F5F0` blanco roto, `--accent #A78BFA` lavanda, `--mute #A0A0A0` gris neutro.
- Secciones claras con la clase `.light`, que redefine los tokens (Servicios y Compromisos).
- Tipografías (Google Fonts): Montserrat para títulos y etiquetas, Inter para textos y Caveat para la tiza de las pizarras.
- Las palabras destacadas en los títulos usan `.serif`: Montserrat cursiva en lavanda.
- Las etiquetas de sección van entre corchetes: `[ Servicios ]`.
- Los textos están en español de España (tuteo) y el tono es cercano pero profesional.

## Estructura
1. Hero: titular, kiosko y tres pizarras (`.board`, con `data-svc` = web | branding | redes). Al pulsar una se abre `#sheet` con animación FLIP; los subservicios están en el objeto `SVC` del script.
2. Marquesina con velocidad ligada al scroll.
3. Agencia: manifiesto con palabras que se iluminan y tres pilares.
4. Servicios (claro): filas con relleno al pasar el ratón.
5. Método: 4 fases con columna fija.
6. Sectores: scroll horizontal fijado (solo en escritorio) y tarjeta final "Tu marca, aquí".
7. Planes: selector tipo canales de TV (CH 01–03) con estática; datos en `plans`.
8. Compromisos (claro), Preguntas (acordeón), Contacto (formulario) y footer con "KIOSKO" gigante.

Animaciones: revelado por líneas (`.reveal .line`) con IntersectionObserver, preloader 000→100, cursor propio y nav que se oculta. Todo respeta `prefers-reduced-motion`.

## Pendiente
- Email real (ahora `hola@elkiosko.agency`, inventado).
- Conectar el formulario a un servicio de envío (ahora es de demostración).
- El título de "Método" está en verde `#3DDC84`; falta decidir si pasa a lavanda o blanco.
