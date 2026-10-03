# Book-Lens

Usa la cámara para fotografiar la portada de un libro y obtén su ficha bibliográfica (título, autor, editorial, año, ISBN, temas).

Prototipo de una sola página (`index.html`), sin instalación ni servidor:

1. La foto se reduce en el navegador y se envía a Gemini para leer título, autor e ISBN.
2. Con eso se consulta Open Library (y Google Books como respaldo).
3. También se puede buscar a mano por ISBN, título o autor, sin Gemini.

Demo: https://xesco-tejedor.github.io/Book-Lens/

## Clave de Gemini

El reconocimiento de portadas necesita una clave de la API de Gemini en la constante `GEMINI_API_KEY` de `index.html`. En una web estática esa clave es visible para cualquiera que abra el código fuente, así que debe ser una clave propia con restricción de sitio web (HTTP referrer) y cuota limitada en Google Cloud. Crea la tuya en https://aistudio.google.com/apikey. Sin clave, la búsqueda por ISBN, título o autor sigue funcionando.
