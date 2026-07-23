# 📚 Tema 1 - Las Etiquetas del `<head>`

## 📖 Introducción

Toda página web comienza con una estructura básica. Dentro de ella existe una sección muy importante llamada **`<head>`**, cuya función es proporcionar información sobre el documento al navegador.

Los elementos que se encuentran dentro del `<head>` normalmente **no son visibles para el usuario**, pero son esenciales para que la página funcione correctamente, sea compatible con diferentes dispositivos y pueda ser encontrada por los motores de búsqueda como Google.

En este tema aprenderás las etiquetas más importantes que pueden encontrarse dentro del `<head>` y cuál es su propósito.

---

# ¿Qué es la etiqueta `<head>`?

La etiqueta `<head>` es un contenedor que almacena información del documento HTML.

Dentro de ella se incluyen:

- Metadatos.
- Título de la página.
- Hojas de estilo (CSS).
- Iconos del sitio.
- Scripts (en algunos casos).
- Configuraciones para navegadores.

Su estructura básica es:

```html
<head>

</head>
```

---

# ¿Qué son los metadatos?

Los **metadatos** son datos que describen otros datos.

En HTML sirven para proporcionar información sobre la página al navegador, buscadores y otros servicios.

Los metadatos se escriben utilizando la etiqueta:

```html
<meta>
```

La mayoría de las etiquetas `<meta>` no tienen etiqueta de cierre.

---

# `<meta charset="UTF-8">`

```html
<meta charset="UTF-8">
```

Define la codificación de caracteres utilizada por la página.

La codificación **UTF-8** permite utilizar prácticamente todos los caracteres existentes:

- Letras
- Números
- Símbolos
- Emojis
- Caracteres especiales
- Tildes
- Ñ

Es una de las etiquetas más importantes de cualquier documento HTML.

---

# `<meta http-equiv="X-UA-Compatible">`

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

Le indica a Internet Explorer que utilice su motor de renderizado más moderno disponible.

Actualmente casi no se utiliza porque Internet Explorer fue descontinuado, pero durante muchos años fue una práctica habitual.

---

# `<meta name="viewport">`

```html
<meta
name="viewport"
content="width=device-width, initial-scale=1.0">
```

Esta etiqueta hace que la página sea adaptable a dispositivos móviles.

### width=device-width

Hace que el ancho de la página sea igual al ancho del dispositivo.

### initial-scale=1.0

Indica que el nivel inicial de zoom será del 100%.

Sin esta etiqueta, muchos teléfonos mostrarían la página demasiado pequeña.

---

# `<title>`

```html
<title>Document</title>
```

Define el nombre que aparecerá en:

- La pestaña del navegador.
- Los marcadores.
- Los resultados de Google.
- Historial del navegador.

Ejemplo:

```
Mi Primera Página Web
```

---

# `<meta name="author">`

```html
<meta name="author" content="RafxDev">
```

Permite indicar quién es el autor del sitio.

Es útil para documentar proyectos.

---

# `<meta name="description">`

```html
<meta
name="description"
content="Esta es una página de ejemplo">
```

Describe brevemente el contenido del sitio.

Esta descripción suele aparecer en los resultados de búsqueda de Google.

Una buena descripción mejora el SEO.

---

# `<meta name="keywords">`

```html
<meta
name="keywords"
content="HTML, CSS, Programación">
```

Permite indicar palabras clave relacionadas con la página.

Actualmente Google prácticamente no utiliza esta etiqueta para posicionamiento, aunque otros buscadores sí pueden considerarla.

---

# `<meta http-equiv="refresh">`

```html
<meta
http-equiv="refresh"
content="5;url=https://www.google.com">
```

Permite actualizar automáticamente la página o redirigir al usuario después de cierto tiempo.

En este ejemplo:

- Espera 5 segundos.
- Envía al usuario a Google.

También puede usarse únicamente para refrescar la página.

Ejemplo:

```html
<meta http-equiv="refresh" content="10">
```

Actualizaría la página cada diez segundos.

---

# `<meta http-equiv="cookie">`

```html
<meta
http-equiv="cookie"
content="name=value">
```

Antiguamente algunos navegadores permitían establecer cookies mediante una etiqueta meta.

Actualmente este método prácticamente no se utiliza.

Las cookies modernas se administran mediante:

- JavaScript
- El servidor
- Encabezados HTTP

---

# `<link rel="stylesheet">`

```html
<link rel="stylesheet" href="style.css">
```

Conecta un archivo CSS con nuestra página HTML.

Gracias a esta etiqueta podemos separar:

- El contenido (HTML).
- El diseño (CSS).

Esta es una de las etiquetas más utilizadas en desarrollo web.

---

# `<link rel="icon">`

```html
<link
rel="icon"
href="favicon.ico"
type="image/x-icon">
```

Define el icono que aparece en la pestaña del navegador.

Este pequeño icono recibe el nombre de **Favicon**.

Generalmente mide:

- 16×16 px
- 32×32 px
- 48×48 px

---

# `<script>`

```html
<script src="script.js"></script>
```

Carga un archivo JavaScript externo.

Normalmente se coloca al final del `<body>` para que la página cargue primero el contenido antes de ejecutar el código JavaScript.

---

# Orden recomendado del `<head>`

Generalmente se recomienda el siguiente orden:

```html
<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Mi Página</title>

<meta name="author" content="Autor">

<meta name="description" content="Descripción">

<link rel="stylesheet" href="style.css">

<link rel="icon" href="favicon.ico">

</head>
```

No es obligatorio, pero facilita la lectura y mantenimiento del código.

---

# Buenas prácticas

✔ Siempre utilizar `UTF-8`.

✔ Agregar la etiqueta `viewport`.

✔ Escribir un título descriptivo.

✔ Incluir una buena descripción.

✔ Mantener separados HTML, CSS y JavaScript.

✔ Utilizar un favicon para dar identidad al sitio.

✔ Evitar el uso de `refresh` salvo casos específicos.

✔ No depender de `keywords` para mejorar el SEO.

---

# Ejercicio práctico

Crea una página HTML que incluya:

- Un título personalizado.
- Tu nombre como autor.
- Una descripción.
- Tres palabras clave.
- Un favicon.
- Un archivo CSS.
- Un archivo JavaScript.

Comprueba que el título aparezca correctamente en la pestaña del navegador.

---

# Resumen

En este tema aprendiste:

- Qué es la etiqueta `<head>`.
- Qué son los metadatos.
- Cómo configurar la codificación de caracteres.
- Cómo adaptar una página a dispositivos móviles.
- Cómo agregar un título.
- Cómo definir el autor y la descripción.
- Cómo mejorar la organización del proyecto utilizando CSS y JavaScript externos.
- Cómo agregar un favicon.
- Buenas prácticas para estructurar correctamente el `<head>`.

Con estos conocimientos ya puedes construir la cabecera de una página HTML de forma profesional.