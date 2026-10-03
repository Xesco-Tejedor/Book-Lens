# Book-Lens

Usa la cámara para fotografiar la portada de un libro y obtén su ficha bibliográfica (título, autor, editorial, año, ISBN, temas).

Prototipo de una sola página (`index.html`), sin instalación ni servidor:

1. La foto se reduce en el navegador y se envía a Gemini para leer título, autor e ISBN.
2. Con eso se consulta Open Library (y Google Books como respaldo).
3. También se puede buscar a mano por ISBN, título o autor, sin Gemini.

Demo: https://xesco-tejedor.github.io/Book-Lens/

## Clave de Gemini

La constante `GEMINI_API_KEY` de `index.html` contiene una clave restringida al dominio `xesco-tejedor.github.io` y con cuota limitada. En una web estática la clave es visible: no uses una clave sin restricciones. Para uso local, crea la tuya en https://aistudio.google.com/apikey.
