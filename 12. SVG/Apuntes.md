# 📚 Tema 12 - Imágenes SVG en HTML

## 📖 Introducción

Las imágenes **SVG (Scalable Vector Graphics)** son un formato gráfico basado en **XML** que permite representar dibujos, iconos e ilustraciones mediante instrucciones matemáticas en lugar de píxeles.

A diferencia de formatos como **JPG** o **PNG**, una imagen SVG puede ampliarse o reducirse infinitamente sin perder calidad. Por esta razón, los SVG se utilizan ampliamente en el desarrollo web moderno para logotipos, iconos, ilustraciones, gráficos y elementos de interfaces.

En este tema aprenderás qué es un SVG, cómo funciona y cómo utilizarlo dentro de una página HTML.

---

# ¿Qué es un SVG?

SVG significa:

**Scalable Vector Graphics**
(Gráficos Vectoriales Escalables)

Es un estándar desarrollado por el **W3C** para representar gráficos mediante código XML.

Ejemplo muy simple:

```html
<svg width="100" height="100">

<circle
cx="50"
cy="50"
r="40"
fill="red"/>

</svg>
```

El navegador interpreta ese código y dibuja un círculo rojo.

---

# ¿Qué significa que sea vectorial?

Una imagen vectorial no está formada por píxeles.

Está formada por:

- Líneas.
- Curvas.
- Coordenadas.
- Figuras geométricas.
- Operaciones matemáticas.

Por eso puede escalarse sin perder definición.

Por ejemplo:

- Un icono SVG puede verse perfectamente tanto a **32 px** como a **3000 px**.

---

# Diferencia entre SVG y PNG/JPG

| SVG | PNG / JPG |
|------|-----------|
| Vectorial | Basado en píxeles |
| No pierde calidad al ampliar | Pierde calidad al ampliarse |
| Se puede editar mediante código | Normalmente requiere un editor de imágenes |
| Peso muy pequeño en iconos | Generalmente más pesado |
| Ideal para logotipos e iconos | Ideal para fotografías |

---

# La etiqueta `<svg>`

Todo gráfico SVG comienza con:

```html
<svg>

</svg>
```

Este elemento define el área donde se dibujará la imagen.

En el ejemplo del curso se utilizan atributos como:

```html
<svg
width="300"
height="300"
viewBox="0 0 1024 1024">
```

---

# El atributo `width`

```html
width="300"
```

Define el ancho del gráfico.

Puede expresarse en:

- píxeles (`px`)
- porcentajes (`%`)
- otras unidades CSS

---

# El atributo `height`

```html
height="300"
```

Define la altura del SVG.

---

# El atributo `viewBox`

```html
viewBox="0 0 1024 1024"
```

Es uno de los atributos más importantes.

Define el sistema de coordenadas interno del dibujo.

Su estructura es:

```
viewBox="x y ancho alto"
```

Gracias a él, el navegador puede escalar correctamente la imagen.

---

# El atributo `fill`

```html
fill="#000000"
```

Controla el color de relleno de las figuras.

Puede utilizar:

- Colores por nombre.
- RGB.
- HEX.
- HSL.

Ejemplo:

```html
fill="red"
```

o

```html
fill="#00AEEF"
```

---

# La etiqueta `<path>`

La mayoría de los iconos SVG utilizan la etiqueta:

```html
<path>
```

Dentro de ella existe un atributo llamado:

```html
d=""
```

Ese atributo contiene cientos o miles de coordenadas que describen la figura.

Ejemplo:

```html
<path
d="M10 10 L50 50">
```

No es necesario escribir estos datos manualmente.

Generalmente son generados por programas de diseño o descargados desde repositorios de iconos.

---

# El atributo `d`

```html
d="..."
```

Es el "mapa" que indica al navegador cómo dibujar la figura.

Contiene instrucciones como:

- M → mover
- L → línea
- C → curva
- A → arco
- Z → cerrar figura

Aunque puede parecer complejo, normalmente no es necesario editarlo manualmente.

---

# El atributo `xmlns`

```html
xmlns="http://www.w3.org/2000/svg"
```

Indica que el documento pertenece al espacio de nombres SVG.

Es recomendable mantenerlo cuando se copia un SVG desde otra fuente.

---

# El atributo `version`

```html
version="1.1"
```

Indica la versión del estándar SVG utilizada.

---

# La etiqueta `<g>`

```html
<g>

</g>
```

Representa un grupo de elementos.

Sirve para organizar varias figuras y aplicar estilos o transformaciones de manera conjunta.

En los SVG descargados suele utilizarse para agrupar distintos componentes del dibujo.

---

# ¿Dónde conseguir SVG?

Existen numerosos sitios donde descargar iconos e ilustraciones vectoriales.

En este curso se utiliza:

**SVG Repo**

https://www.svgrepo.com/

Este sitio ofrece miles de iconos gratuitos que pueden descargarse como archivos SVG o copiar directamente como código HTML.

También existen otras plataformas populares como:

- Heroicons.
- Font Awesome.
- Tabler Icons.
- Bootstrap Icons.

---

# Ventajas del formato SVG

- Escalado infinito sin perder calidad.
- Muy ligero para iconos.
- Editable mediante código.
- Compatible con CSS.
- Compatible con JavaScript.
- Permite crear animaciones.
- Ideal para diseño responsive.

---

# Desventajas

- No es recomendable para fotografías.
- Algunos SVG muy complejos pueden contener mucho código.
- Requiere comprender XML si se desea editar manualmente.

---

# SVG y CSS

Una de las mayores ventajas es que pueden modificarse utilizando CSS.

Ejemplo:

```css
svg{

width:200px;

}
```

o

```css
path{

fill:red;

}
```

Esto permite cambiar colores sin modificar la imagen original.

---

# SVG y JavaScript

También pueden manipularse mediante JavaScript.

Es posible:

- Cambiar colores.
- Rotarlos.
- Escalarlos.
- Animarlos.
- Crear gráficos interactivos.

Por esta razón los SVG son muy utilizados en aplicaciones modernas.

---

# Buenas prácticas

✔ Utilizar SVG para iconos y logotipos.

✔ Mantener el atributo `viewBox`.

✔ Descargar SVG únicamente desde sitios confiables.

✔ Optimizar los SVG cuando sean muy grandes.

✔ Utilizar CSS para modificar colores siempre que sea posible.

---

# Errores comunes

❌ Eliminar el atributo `viewBox`, provocando que el gráfico se deforme al cambiar de tamaño.

---

❌ Utilizar SVG para fotografías.

Los formatos JPG o WebP son más adecuados.

---

❌ Editar manualmente el atributo `d` sin conocer su funcionamiento.

---

# Ejercicio práctico

1. Descarga dos iconos desde **SVG Repo**.

2. Agrégalos a una página HTML utilizando la etiqueta `<svg>`.

3. Cambia su tamaño mediante `width` y `height`.

4. Modifica el color utilizando el atributo `fill`.

5. Intenta cambiar el color mediante CSS.

---

# Resumen

En este tema aprendiste:

- Qué es un gráfico SVG.
- La diferencia entre imágenes vectoriales y de mapa de bits.
- Cómo utilizar la etiqueta `<svg>`.
- La función de `viewBox`.
- Cómo funcionan `width` y `height`.
- Qué hace el atributo `fill`.
- La importancia de la etiqueta `<path>` y del atributo `d`.
- Cómo agrupar elementos mediante `<g>`.
- Dónde descargar iconos SVG.
- Las ventajas de utilizar gráficos vectoriales en el desarrollo web.
- Cómo modificar SVG utilizando CSS y JavaScript.

Con estos conocimientos ya puedes incorporar iconos e ilustraciones vectoriales en tus proyectos web, obteniendo imágenes ligeras, escalables y fáciles de personalizar, una práctica muy común en el desarrollo frontend moderno.