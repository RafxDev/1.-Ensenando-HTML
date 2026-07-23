# 📚 Tema 2 - Las Etiquetas del `<body>`

## 📖 Introducción

Después de conocer la estructura del `<head>`, es momento de aprender la segunda parte más importante de un documento HTML: el **`<body>`**.

Todo lo que el usuario puede ver e interactuar dentro de una página web se encuentra en esta sección. Aquí se agregan textos, imágenes, enlaces, formularios, videos, botones y todas las demás estructuras que conforman un sitio web.

Además, HTML5 introdujo una serie de **etiquetas semánticas** que permiten organizar mejor el contenido, facilitando tanto el desarrollo como la accesibilidad y el posicionamiento en buscadores (SEO).

En este tema conocerás las principales etiquetas que forman la estructura del `<body>`.

---

# ¿Qué es la etiqueta `<body>`?

La etiqueta `<body>` contiene todo el contenido visible de una página web.

Su estructura básica es:

```html
<body>

</body>
```

Dentro de ella se colocan todos los elementos que el usuario verá al abrir el sitio.

Por ejemplo:

- Encabezados
- Párrafos
- Imágenes
- Videos
- Formularios
- Botones
- Tablas
- Menús
- Enlaces

Todo ello pertenece al cuerpo del documento.

---

# ¿Qué son las etiquetas semánticas?

Antes de HTML5 era muy común construir páginas utilizando únicamente etiquetas como:

```html
<div>
```

Esto hacía que el código fuera difícil de interpretar.

HTML5 introdujo etiquetas con significado propio, conocidas como **etiquetas semánticas**, las cuales indican claramente cuál es la función de cada parte del documento.

Por ejemplo:

- Encabezado
- Menú de navegación
- Contenido principal
- Barra lateral
- Pie de página

Esto mejora:

- La organización del código.
- La accesibilidad.
- El SEO.
- El mantenimiento del proyecto.

---

# La etiqueta `<header>`

```html
<header>

</header>
```

Representa el encabezado de una página o de una sección.

Generalmente contiene:

- El logotipo.
- El nombre del sitio.
- El menú principal.
- Un buscador.
- Información introductoria.

Ejemplo:

```html
<header>

<h1>Mi Página Web</h1>

</header>
```

Normalmente aparece en la parte superior del sitio.

---

# La etiqueta `<nav>`

```html
<nav>

</nav>
```

Representa una sección destinada a la navegación.

Dentro de ella suelen colocarse los enlaces más importantes del sitio.

Ejemplo:

```html
<nav>

<a href="#">Inicio</a>

<a href="#">Productos</a>

<a href="#">Contacto</a>

</nav>
```

No todos los grupos de enlaces necesitan estar dentro de un `<nav>`, únicamente aquellos que representan la navegación principal.

---

# La etiqueta `<section>`

```html
<section>

</section>
```

Representa una sección temática del contenido.

Cada sección agrupa información relacionada entre sí.

Ejemplo:

```html
<section>

<h2>Noticias</h2>

</section>
```

Un sitio puede tener múltiples secciones.

---

# La etiqueta `<article>`

```html
<article>

</article>
```

Representa un contenido independiente que puede entenderse por sí solo.

Ejemplos:

- Una noticia.
- Una publicación de blog.
- Un comentario.
- Un producto.
- Una receta.

En el ejemplo del código aparecen dos artículos dentro de una misma sección:

```html
<section>

<article></article>

<article></article>

</section>
```

Cada artículo puede contener su propio título, imágenes y contenido.

---

# La etiqueta `<aside>`

```html
<aside>

</aside>
```

Representa contenido secundario o complementario al contenido principal.

Se utiliza para mostrar información como:

- Publicidad.
- Noticias relacionadas.
- Enlaces recomendados.
- Biografía del autor.
- Widgets.
- Redes sociales.

Generalmente se ubica en uno de los laterales de la página.

---

# La etiqueta `<footer>`

```html
<footer>

</footer>
```

Representa el pie de página.

Normalmente contiene información como:

- Derechos de autor.
- Información de contacto.
- Redes sociales.
- Políticas de privacidad.
- Avisos legales.
- Enlaces adicionales.

Ejemplo:

```html
<footer>

<p>Derechos reservados</p>

</footer>
```

Puede existir un `<footer>` para toda la página o para una sección específica.

---

# Estructura básica de una página HTML5

Una estructura semántica sencilla suele verse así:

```html
<body>

<header>

<nav>

</nav>

</header>

<section>

<article>

</article>

</section>

<aside>

</aside>

<footer>

</footer>

</body>
```

Cada elemento cumple una función específica y ayuda a mantener el código organizado.

---

# Ventajas de utilizar etiquetas semánticas

Utilizar etiquetas semánticas ofrece numerosos beneficios:

- Código más limpio y fácil de leer.
- Mejor organización del contenido.
- Mayor accesibilidad para lectores de pantalla.
- Mejor posicionamiento en buscadores (SEO).
- Facilita el mantenimiento del proyecto.
- Permite que otros desarrolladores comprendan rápidamente la estructura del sitio.

---

# Buenas prácticas

✔ Utilizar un solo `<header>` principal por página cuando sea posible.

✔ Colocar los enlaces principales dentro de `<nav>`.

✔ Agrupar contenido relacionado usando `<section>`.

✔ Utilizar `<article>` únicamente cuando el contenido tenga sentido por sí mismo.

✔ Reservar `<aside>` para información complementaria.

✔ Agregar siempre un `<footer>` con información relevante del sitio.

✔ Mantener una estructura ordenada y fácil de leer.

---

# Ejercicio práctico

Construye una página que contenga:

- Un encabezado con el nombre del sitio.
- Un menú de navegación con cuatro enlaces.
- Una sección llamada "Noticias".
- Dos artículos con un título y un párrafo.
- Una barra lateral con enlaces recomendados.
- Un pie de página con el texto:

```text
© 2026 Tu Nombre. Todos los derechos reservados.
```

Observa cómo cada parte de la página queda claramente organizada gracias a las etiquetas semánticas.

---

# Resumen

En este tema aprendiste:

- Qué es la etiqueta `<body>`.
- La importancia de las etiquetas semánticas.
- El uso de `<header>`.
- Cómo funciona `<nav>`.
- Para qué sirve `<section>`.
- Cuándo utilizar `<article>`.
- El propósito de `<aside>`.
- La función del `<footer>`.
- Cómo estructurar correctamente una página HTML5.

Con estas etiquetas ya puedes crear la estructura base de prácticamente cualquier sitio web moderno, organizando el contenido de forma clara, profesional y fácil de mantener.