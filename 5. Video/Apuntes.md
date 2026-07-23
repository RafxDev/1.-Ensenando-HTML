# 📚 Tema 5 - Videos en HTML

## 📖 Introducción

Los videos son uno de los recursos multimedia más utilizados en el desarrollo web. Permiten mostrar tutoriales, presentaciones, demostraciones de productos, clases, animaciones y mucho más.

Desde HTML5 ya no es necesario utilizar tecnologías externas como Flash para reproducir videos. Gracias a la etiqueta **`<video>`**, los navegadores modernos pueden reproducir contenido multimedia de forma nativa.

En este tema aprenderás a insertar videos, configurar sus controles, utilizar varios formatos y mostrar una imagen de portada antes de su reproducción.

---

# ¿Qué es la etiqueta `<video>`?

La etiqueta `<video>` permite reproducir archivos de video directamente en una página web.

Su estructura más básica es:

```html
<video src="video.mp4" controls></video>
```

El navegador mostrará un reproductor con controles para que el usuario pueda reproducir el contenido.

---

# El atributo `src`

```html
<video src="joel.mp4"></video>
```

El atributo **`src`** indica la ubicación del archivo de video.

Puede apuntar a:

- Un archivo local.
- Una carpeta del proyecto.
- Un servidor remoto.
- Una URL de Internet.

Ejemplo:

```html
<video src="Assets/vid/video.mp4"></video>
```

Si la ruta es incorrecta, el video no podrá reproducirse.

---

# El atributo `controls`

```html
<video controls></video>
```

Agrega los controles del reproductor.

Entre ellos:

- Reproducir.
- Pausar.
- Barra de progreso.
- Control de volumen.
- Pantalla completa.
- Velocidad de reproducción (según el navegador).

Sin este atributo, el usuario no podrá controlar el video de forma predeterminada.

---

# El atributo `autoplay`

```html
<video autoplay></video>
```

Hace que el video comience automáticamente al cargar la página.

Sin embargo, los navegadores modernos suelen bloquear la reproducción automática si el video tiene sonido.

Por ello, normalmente se utiliza junto con el atributo:

```html
muted
```

---

# El atributo `muted`

```html
<video muted></video>
```

Inicia el video sin sonido.

Es especialmente útil cuando se combina con `autoplay`, ya que muchos navegadores solo permiten la reproducción automática de videos silenciados.

---

# Los atributos `width` y `height`

Permiten definir el tamaño del reproductor.

Ejemplo:

```html
<video
width="600"
height="400">
</video>
```

Generalmente es recomendable controlar las dimensiones mediante CSS para obtener un diseño más flexible.

---

# Utilizar la etiqueta `<source>`

Una forma más recomendable de insertar videos es utilizando la etiqueta `<source>`.

Ejemplo:

```html
<video controls>

<source
src="joel.mp4"
type="video/mp4">

</video>
```

Esto permite agregar varios formatos para mejorar la compatibilidad entre navegadores.

Ejemplo:

```html
<video controls>

<source src="video.mp4" type="video/mp4">

<source src="video.webm" type="video/webm">

</video>
```

El navegador utilizará el primer formato compatible.

---

# Contenido alternativo (Fallback)

Es posible agregar contenido entre las etiquetas `<video>` y `</video>`.

Este contenido solo se mostrará si el navegador no soporta la reproducción de video.

Ejemplo:

```html
<video controls>

<source src="video.mp4" type="video/mp4">

<p>

Tu navegador no soporta videos.

</p>

</video>
```

También es una buena práctica ofrecer un enlace para descargar el archivo.

```html
<a href="video.mp4" download>

Descargar video

</a>
```

---

# El atributo `poster`

```html
<video
poster="gandalf.jpg">
```

Define una imagen que se mostrará antes de reproducir el video.

Funciona como una miniatura o portada.

Ejemplo:

```html
<video
controls
poster="portada.jpg">

<source src="video.mp4">

</video>
```

Es muy útil para hacer el contenido más atractivo visualmente.

---

# Formatos de video más utilizados

Los navegadores modernos admiten varios formatos.

Los principales son:

| Formato | Compatibilidad |
|----------|----------------|
| MP4 | Excelente |
| WebM | Muy buena |
| OGG | Limitada |

Actualmente, **MP4 (H.264)** es el formato más utilizado debido a su amplia compatibilidad.

---

# Organización recomendada del proyecto

Una estructura ordenada facilita el mantenimiento del sitio.

Ejemplo:

```text
Proyecto/

├── Assets/
│   ├── img/
│   ├── vid/
│   └── audio/
│
├── index.html
├── style.css
└── script.js
```

Guardar los videos dentro de una carpeta específica ayuda a mantener el proyecto organizado.

---

# Buenas prácticas

✔ Utilizar siempre el atributo `controls`, salvo que exista un reproductor personalizado.

✔ Evitar abusar de `autoplay`, ya que puede resultar molesto para los usuarios.

✔ Combinar `autoplay` con `muted` cuando sea necesario.

✔ Utilizar el atributo `poster` para mostrar una portada atractiva.

✔ Incluir contenido alternativo (fallback) para navegadores antiguos.

✔ Ofrecer un enlace de descarga cuando el video sea importante.

✔ Optimizar el tamaño del archivo para reducir el tiempo de carga.

✔ Utilizar formatos compatibles como MP4 o WebM.

---

# Errores comunes

❌ Escribir una ruta incorrecta en `src`.

```html
<video src="video.mp4">
```

cuando el archivo realmente se encuentra en otra carpeta.

---

❌ Olvidar el atributo `controls`.

El video se cargará, pero el usuario no tendrá controles para reproducirlo o pausarlo.

---

❌ Utilizar `autoplay` con sonido.

Muchos navegadores bloquearán automáticamente la reproducción.

---

❌ Subir videos demasiado pesados.

Esto aumenta considerablemente el tiempo de carga de la página.

---

# Ejercicio práctico

Crea una página que incluya:

- Un video con controles.
- Reproducción automática sin sonido.
- Una imagen de portada utilizando `poster`.
- Un mensaje alternativo para navegadores que no soporten videos.
- Un enlace para descargar el archivo de video.
- Dos etiquetas `<source>` con formatos diferentes (si dispones de ellos).

Organiza el proyecto utilizando la siguiente estructura:

```text
Assets/

├── img/
└── vid/
```

---

# Resumen

En este tema aprendiste:

- Qué es la etiqueta `<video>`.
- Cómo utilizar el atributo `src`.
- Para qué sirve `controls`.
- Cómo funciona `autoplay`.
- La utilidad del atributo `muted`.
- Cómo modificar el tamaño del reproductor.
- El uso de la etiqueta `<source>`.
- Cómo agregar contenido alternativo (fallback).
- Cómo utilizar una imagen de portada con `poster`.
- Los formatos de video más utilizados.
- Buenas prácticas para incorporar videos en una página web.

Con estos conocimientos ya puedes integrar videos de forma profesional en tus proyectos HTML, ofreciendo una mejor experiencia de usuario y una mayor compatibilidad entre navegadores.