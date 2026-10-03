# Book-Lens

Usa la cámara para fotografiar la portada de un libro y obtén su ficha bibliográfica (título, autor, editorial, año, ISBN, temas).

Prototipo de una sola página (`index.html`), sin instalación ni servidor:

1. La foto se reduce en el navegador y se envía a Gemini para leer título, autor e ISBN.
2. Con eso se consulta Open Library (y Google Books como respaldo).
3. También se puede buscar a mano por ISBN, título o autor, sin Gemini.

Demo: https://xesco-tejedor.github.io/Book-Lens/

## Gemini y la clave

La clave de Gemini no está en el código público. La página llama a un pequeño servidor intermedio (proxy) que guarda la clave como secreto; su URL va en la constante `GEMINI_PROXY_URL` de `index.html`. Para uso local puedes poner tu propia clave (https://aistudio.google.com/apikey) en `GEMINI_API_KEY`, sin subirla a ningún repositorio. Sin proxy ni clave, la búsqueda por ISBN, título o autor sigue funcionando.

El modo "Lomos" lee varios libros de una foto de estantería y busca cada uno en Open Library. La lectura de lomos puede fallar: revisa siempre los resultados.
