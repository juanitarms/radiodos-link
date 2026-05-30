# Radio Dos · Link in bio

Página del link de la biografía de Instagram de [@radiodos993](https://instagram.com/radiodos993):
una grilla con las últimas notas, donde cada placa lleva a la nota completa en
[radiodos.com.ar](https://www.radiodos.com.ar).

La actualiza **sola** el bot de aprobación ([radiodos-ig-publisher](https://github.com/juanitarms/radiodos-ig-publisher)):
cada vez que se aprueba una nota, sube la placa a `img/` y agrega la entrada a
`posts.json` por la API de GitHub. La página lee `posts.json` en el navegador y arma la grilla.

## Estructura

| Archivo | Qué es |
|---------|--------|
| `index.html` | La página (estática; lee `posts.json` y arma la grilla). |
| `posts.json` | Las últimas notas (`{id, image, url, title, volanta, date}`), la más nueva primero. La escribe el bot. |
| `img/<id>.png` | Las placas. Las sube el bot; se mantienen sólo las últimas ~60. |
| `logo.png` | Logo de Radio Dos. |
| `.nojekyll` | Para que GitHub Pages sirva los archivos tal cual. |

No se edita a mano: lo maneja el bot. Para servirla se usa GitHub Pages (o, más adelante,
un dominio propio tipo `link.radiodos.com.ar` apuntando acá — sin cambiar nada del código).
