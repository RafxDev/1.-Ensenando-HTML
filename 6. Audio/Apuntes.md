# 📚 Tema 6 - Audio en HTML

## 📖 Introducción

El audio es otro de los recursos multimedia que HTML5 incorporó de forma nativa, permitiendo reproducir música, efectos de sonido, podcasts, narraciones y cualquier otro contenido sonoro sin necesidad de complementos externos.

Gracias a la etiqueta **`<audio>`**, los navegadores modernos pueden reproducir archivos de audio directamente desde una página web, ofreciendo controles integrados y soporte para distintos formatos.

En este tema aprenderás a insertar archivos de audio, utilizar diferentes formatos y proporcionar contenido alternativo para garantizar la compatibilidad con distintos navegadores.

---

# ¿Qué es la etiqueta `<audio>`?

La etiqueta `<audio>` permite reproducir archivos de sonido dentro de una página web.

Su estructura básica es:

```html
<audio src="musica.mp3" controls></audio>
```

Al agregar el atributo `controls`, el navegador mostrará un pequeño reproductor con los controles necesarios para reproducir el audio.

---

# El atributo `src`

```html
<audio src="cancion.mp3"></audio>
```

El atributo **`src`** (Source) indica la ubicación del archivo de audio.

Puede hacer referencia a:

- Un archivo local.
- Una carpeta del proyecto.
- Un servidor remoto.
- Una URL de Internet.

Ejemplo:

```html
<audio src="Assets/audio/musica.mp3"></audio>
```

Si la ruta es incorrecta, el navegador no podrá encontrar el archivo.

---

# El atributo `controls`

```html
<audio controls></audio>
```

Agrega los controles del reproductor.

Generalmente incluyen:

- Reproducir.
- Pausar.
- Barra de progreso.
- Control de volumen.
- Tiempo de reproducción.

Sin este atributo, el usuario no podrá controlar el audio de forma predeterminada.

---

# El atributo `muted`

```html
<audio muted></audio>
```

Inicia la reproducción con el sonido desactivado.

Es útil cuando se desea que el usuario decida cuándo activar el audio.

---

# La etiqueta `<source>`

Aunque es posible utilizar directamente el atributo `src`, la forma recomendada de insertar audio es mediante una o varias etiquetas `<source>`.

Ejemplo:

```html
<audio controls>

<source
src="musica.mp3"
type="audio/mpeg">

</audio>
```

Esta técnica permite ofrecer distintos formatos para mejorar la compatibilidad entre navegadores.

Ejemplo:

```html
<audio controls>

<source src="musica.mp3" type="audio/mpeg">

<source src="musica.ogg" type="audio/ogg">

</audio>
```

El navegador utilizará automáticamente el primer formato que sea compatible.

---

# Contenido alternativo (Fallback)

Es posible incluir contenido entre las etiquetas `<audio>` y `</audio>`.

Este contenido solo aparecerá si el navegador no soporta la reproducción de audio.

Ejemplo:

```html
<audio controls>

<source src="musica.mp3" type="audio/mpeg">

Tu navegador no soporta el elemento de audio.

</audio>
```

También es posible incluir un enlace para descargar el archivo.

```html
<a href="musica.mp3" download>

Descargar audio

</a>
```

---

# Formatos de audio más utilizados

HTML5 admite distintos formatos de audio.

Los principales son:

| Formato | Compatibilidad |
|----------|----------------|
| MP3 | Excelente |
| OGG | Muy buena |
| WAV | Buena, pero archivos más pesados |

### MP3

Es el formato más utilizado debido a su excelente compatibilidad y buena compresión.

### OGG

Formato libre y ampliamente compatible con navegadores modernos.

### WAV

Ofrece una excelente calidad de sonido, aunque genera archivos considerablemente más grandes.

---

# Organización recomendada del proyecto

Una buena organización facilita el mantenimiento del sitio.

Ejemplo:

```text
Proyecto/

├── Assets/
│   ├── audio/
│   ├── img/
│   └── vid/
│
├── index.html
├── style.css
└── script.js
```

Guardar todos los archivos de audio dentro de una carpeta específica ayuda a mantener el proyecto limpio y ordenado.

---

# Otros atributos útiles

Además de `controls` y `muted`, la etiqueta `<audio>` admite otros atributos interesantes.

## `autoplay`

```html
<audio autoplay></audio>
```

Reproduce el audio automáticamente al cargar la página.

Sin embargo, muchos navegadores bloquean esta función si el audio contiene sonido.

---

## `loop`

```html
<audio loop></audio>
```

Hace que el audio vuelva a comenzar automáticamente cuando termina.

---

## `preload`

Permite indicar al navegador cómo debe cargar el archivo antes de reproducirlo.

Ejemplo:

```html
<audio preload="auto"></audio>
```

Valores posibles:

- `none`
- `metadata`
- `auto`

---

# Buenas prácticas

✔ Utilizar siempre el atributo `controls`.

✔ Utilizar `<source>` en lugar de depender únicamente de `src`.

✔ Ofrecer varios formatos cuando sea posible.

✔ Mantener los archivos de audio comprimidos para mejorar la velocidad de carga.

✔ Organizar los archivos dentro de una carpeta `Assets/audio`.

✔ Incluir contenido alternativo (fallback) para navegadores antiguos.

✔ Evitar el uso excesivo de `autoplay`, ya que puede afectar la experiencia del usuario.

---

# Errores comunes

❌ Escribir una ruta incorrecta.

```html
<audio src="musica.mp3">
```

cuando el archivo realmente se encuentra en otra carpeta.

---

❌ Olvidar el atributo `controls`.

El audio estará presente, pero el usuario no podrá reproducirlo fácilmente.

---

❌ Utilizar únicamente un formato poco compatible.

Siempre que sea posible, ofrece más de un formato utilizando varias etiquetas `<source>`.

---

❌ Subir archivos demasiado pesados.

Esto aumenta el tiempo de carga de la página y consume más ancho de banda.

---

# Ejercicio práctico

Crea una página que incluya:

- Un reproductor de audio con controles.
- Un archivo MP3 utilizando el atributo `src`.
- Otro reproductor utilizando la etiqueta `<source>`.
- Un mensaje alternativo para navegadores que no soporten audio.
- Un enlace para descargar el archivo de sonido.
- Un ejemplo utilizando el atributo `loop`.

Organiza los archivos de la siguiente manera:

```text
Assets/

├── audio/
├── img/
└── vid/
```

---

# Resumen

En este tema aprendiste:

- Qué es la etiqueta `<audio>`.
- Cómo utilizar el atributo `src`.
- Para qué sirve el atributo `controls`.
- Cómo funciona el atributo `muted`.
- La importancia de utilizar la etiqueta `<source>`.
- Cómo ofrecer contenido alternativo (fallback).
- Los formatos de audio más utilizados.
- Otros atributos útiles como `autoplay`, `loop` y `preload`.
- Buenas prácticas para organizar y reproducir archivos de audio en una página web.

Con estos conocimientos ya puedes incorporar música, efectos de sonido o narraciones a tus proyectos HTML de forma profesional, manteniendo una buena compatibilidad y ofreciendo una mejor experiencia para los usuarios.