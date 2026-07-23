# 📚 Tema 4 - Imágenes en HTML

## 📖 Introducción

Las imágenes son uno de los elementos más importantes del desarrollo web. Gracias a ellas es posible hacer que una página sea más atractiva, transmitir información visual y mejorar la experiencia del usuario.

HTML utiliza la etiqueta **`<img>`** para insertar imágenes dentro de una página. Aunque parece una etiqueta sencilla, posee varios atributos fundamentales que permiten controlar su origen, tamaño y accesibilidad.

En este tema aprenderás cómo insertar imágenes, modificar sus dimensiones y utilizarlas como enlaces.

---

# ¿Qué es la etiqueta `<img>`?

La etiqueta `<img>` permite mostrar una imagen dentro de una página web.

A diferencia de muchas etiquetas HTML, **no tiene etiqueta de cierre**, ya que es un elemento vacío.

Su estructura básica es:

```html
<img src="imagen.jpg" alt="Descripción de la imagen">
```

Los atributos más importantes son:

- `src`
- `alt`
- `width`
- `height`

---

# El atributo `src`

```html
<img src="gandalf.jpg">
```

El atributo **`src`** (Source) indica la ubicación del archivo que se desea mostrar.

Puede apuntar a:

- Una imagen local.
- Una carpeta del proyecto.
- Un servidor externo.
- Una URL de Internet.

Ejemplos:

```html
<img src="imagen.jpg">
```

```html
<img src="Assets/img/gandalf.jpg">
```

```html
<img src="https://ejemplo.com/foto.png">
```

Si la ruta es incorrecta, la imagen no podrá cargarse.

---

# El atributo `alt`

```html
<img src="gandalf.jpg"
alt="Gandalf el Gris">
```

El atributo **`alt`** proporciona un texto alternativo que describe la imagen.

Su función es muy importante porque:

- Se muestra cuando la imagen no puede cargarse.
- Es leído por lectores de pantalla para personas con discapacidad visual.
- Ayuda a mejorar el SEO.

Por esta razón, todas las imágenes deberían incluir un atributo `alt` descriptivo.

Ejemplo:

```html
alt="Gato blanco durmiendo sobre un sofá"
```

Es mejor que:

```html
alt="imagen"
```

---

# Cambiar el ancho con `width`

```html
<img
src="gandalf.jpg"
width="400">
```

El atributo `width` define el ancho de la imagen.

El valor se expresa normalmente en píxeles.

Ejemplo:

```html
width="300"
```

significa que la imagen tendrá 300 píxeles de ancho.

Cuando solo se modifica el ancho, el navegador ajusta automáticamente la altura para mantener las proporciones.

---

# Cambiar la altura con `height`

```html
<img
src="gandalf.jpg"
height="400">
```

El atributo `height` establece la altura de la imagen.

Al igual que `width`, suele expresarse en píxeles.

Si únicamente se modifica la altura, el navegador calculará el ancho automáticamente para conservar la proporción de la imagen.

---

# Modificar ancho y alto

También es posible definir ambos valores:

```html
<img
src="gandalf.jpg"
width="300"
height="300">
```

Sin embargo, si las proporciones originales no coinciden, la imagen puede verse deformada.

Por ello, generalmente se recomienda controlar el tamaño mediante CSS.

---

# Utilizar una imagen como enlace

Una imagen puede convertirse en un enlace simplemente colocándola dentro de una etiqueta `<a>`.

Ejemplo:

```html
<a href="https://www.google.com">

<img
src="cat.jpg"
alt="Gato">

</a>
```

En el ejemplo del código:

```html
<a href="https://www.google.com"
target="_blank">

<img src="cat.jpg">

</a>
```

Cuando el usuario hace clic sobre la imagen, será enviado a Google en una nueva pestaña.

---

# Rutas de las imágenes

Existen dos formas principales de acceder a un archivo.

## Ruta relativa

```html
<img src="Assets/img/gandalf.jpg">
```

Hace referencia a un archivo dentro del proyecto.

Es la opción más utilizada.

---

## Ruta absoluta

```html
<img src="https://servidor.com/imagen.jpg">
```

Hace referencia a un archivo alojado en Internet.

Depende de que el servidor permanezca disponible.

---

# Formatos de imagen más comunes

HTML admite numerosos formatos de imagen.

Los más utilizados son:

| Formato | Uso principal |
|----------|---------------|
| JPG / JPEG | Fotografías |
| PNG | Imágenes con transparencia |
| GIF | Animaciones sencillas |
| SVG | Iconos y gráficos vectoriales |
| WebP | Imágenes optimizadas para la web |
| AVIF | Alta calidad con excelente compresión |

Actualmente, **WebP** y **AVIF** son formatos muy recomendables para mejorar el rendimiento de un sitio web.

---

# Buenas prácticas

✔ Utilizar siempre el atributo `alt`.

✔ Mantener las imágenes optimizadas para reducir el tiempo de carga.

✔ Evitar imágenes demasiado grandes.

✔ Preferir formatos modernos como WebP cuando sea posible.

✔ Organizar las imágenes dentro de carpetas como:

```text
Assets/
└── img/
```

✔ Utilizar nombres descriptivos para los archivos.

Ejemplo:

```text
gandalf.jpg
```

Es mejor que:

```text
IMG001.jpg
```

---

# Errores comunes

❌ Escribir una ruta incorrecta.

```html
<img src="imagen.jpg">
```

cuando el archivo realmente se encuentra en otra carpeta.

---

❌ Omitir el atributo `alt`.

```html
<img src="foto.jpg">
```

---

❌ Deformar la imagen modificando ancho y alto sin mantener la proporción.

---

❌ Utilizar imágenes con tamaños excesivos que ralentizan la carga del sitio.

---

# Ejercicio práctico

Crea una página que contenga:

- Una imagen con texto alternativo.
- Una imagen modificando únicamente el ancho.
- Otra modificando únicamente la altura.
- Una imagen que funcione como enlace hacia tu perfil de GitHub.
- Una carpeta llamada:

```text
Assets/img
```

Guarda todas las imágenes dentro de esa carpeta y verifica que las rutas funcionen correctamente.

---

# Resumen

En este tema aprendiste:

- Qué es la etiqueta `<img>`.
- Cómo utilizar el atributo `src`.
- La importancia del atributo `alt`.
- Cómo modificar el ancho con `width`.
- Cómo modificar la altura con `height`.
- Cómo convertir una imagen en un enlace utilizando `<a>`.
- La diferencia entre rutas relativas y absolutas.
- Los formatos de imagen más utilizados en la web.
- Buenas prácticas para trabajar con imágenes en HTML.

Con estos conocimientos ya puedes incorporar imágenes correctamente en tus páginas web, mejorando tanto la apariencia como la accesibilidad y la experiencia de los usuarios.