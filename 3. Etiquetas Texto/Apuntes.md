# 📚 Tema 3 - Etiquetas de Texto en HTML

## 📖 Introducción

El contenido textual es el elemento principal de la mayoría de las páginas web. Desde un simple párrafo hasta un artículo completo, HTML ofrece una gran variedad de etiquetas para estructurar, resaltar y dar significado al texto.

En este tema aprenderás las etiquetas más utilizadas para trabajar con texto, conocerás la diferencia entre elementos **en bloque** y **en línea**, y descubrirás la importancia del HTML semántico para crear páginas más accesibles y mejor organizadas.

---

# ¿Qué son las etiquetas de texto?

Las etiquetas de texto permiten mostrar información escrita dentro de una página web.

Gracias a ellas podemos:

- Escribir párrafos.
- Crear títulos.
- Resaltar palabras.
- Insertar citas.
- Mostrar fórmulas matemáticas.
- Crear enlaces.
- Preservar espacios y saltos de línea.

Estas etiquetas son fundamentales en cualquier documento HTML.

---

# La etiqueta `<p>`

```html
<p>Este es un párrafo.</p>
```

Representa un párrafo de texto.

Cada vez que se crea un `<p>`, el navegador agrega un espacio antes y después del contenido.

Ejemplo:

```html
<p>Hola Mundo.</p>

<p>Segundo párrafo.</p>
```

Resultado:

```
Hola Mundo.

Segundo párrafo.
```

Es una de las etiquetas más utilizadas en HTML.

---

# La etiqueta `<b>`

```html
<b>Texto en negrita</b>
```

Muestra el texto en **negrita**, pero únicamente cambia su apariencia visual.

No indica que el contenido sea importante.

---

# La etiqueta `<i>`

```html
<i>Texto en cursiva</i>
```

Muestra el texto en cursiva.

Generalmente se utiliza para:

- Palabras extranjeras.
- Nombres científicos.
- Títulos de obras.
- Expresiones especiales.

---

# La etiqueta `<u>`

```html
<u>Texto subrayado</u>
```

Subraya el contenido.

Actualmente se recomienda utilizarla únicamente cuando el subrayado tenga un significado específico, ya que los usuarios suelen asociarlo con enlaces.

---

# Elementos en bloque

Los elementos en bloque ocupan **todo el ancho disponible** de la página y comienzan en una nueva línea.

Ejemplo:

```html
<p style="background-color: yellow;">
Amarillo
</p>
```

El fondo amarillo ocupará todo el ancho del párrafo.

Algunos ejemplos de elementos en bloque son:

- `<p>`
- `<div>`
- `<section>`
- `<article>`
- `<header>`
- `<footer>`

---

# Elementos en línea

Los elementos en línea solo ocupan el espacio necesario para su contenido.

Ejemplo:

```html
<b>Rojo</b>
<i>Verde</i>
<u>Azul</u>
```

Estos elementos aparecen uno al lado del otro.

Algunos ejemplos son:

- `<b>`
- `<i>`
- `<u>`
- `<a>`
- `<span>`
- `<strong>`
- `<em>`

---

# HTML Semántico

HTML5 recomienda utilizar etiquetas que aporten significado al contenido.

Esto mejora:

- La accesibilidad.
- El SEO.
- La comprensión del código.

---

# La etiqueta `<strong>`

```html
<strong>Importante</strong>
```

Representa texto de **gran importancia**.

Visualmente suele mostrarse en negrita, pero su verdadero propósito es indicar relevancia semántica.

Es preferible utilizar `<strong>` en lugar de `<b>` cuando el contenido sea realmente importante.

---

# La etiqueta `<em>`

```html
<em>Énfasis</em>
```

Representa texto con énfasis.

Generalmente aparece en cursiva.

Debe utilizarse cuando se quiera destacar una palabra por su significado y no solo por cuestiones visuales.

---

# La etiqueta `<br>`

```html
Linea 1<br>
Linea 2
```

Inserta un salto de línea.

No crea un nuevo párrafo, únicamente mueve el contenido a la línea siguiente.

Es útil para:

- Direcciones.
- Poemas.
- Letras de canciones.
- Versos.

No debe utilizarse para separar párrafos.

---

# La etiqueta `<hr>`

```html
<hr>
```

Inserta una línea horizontal.

Representa un cambio de tema o una separación entre secciones del contenido.

No debe utilizarse únicamente como elemento decorativo.

---

# Encabezados `<h1>` hasta `<h6>`

HTML dispone de seis niveles de encabezados.

```html
<h1>Título Principal</h1>
<h2>Subtítulo</h2>
<h3>Encabezado</h3>
```

Su importancia disminuye desde:

```
h1
↓
h2
↓
h3
↓
h4
↓
h5
↓
h6
```

### Recomendaciones

- Utilizar un solo `<h1>` por página.
- Mantener un orden lógico.
- No saltar niveles sin necesidad.

---

# La etiqueta `<pre>`

```html
<pre>

Texto
    con espacios
        preservados

</pre>
```

Conserva exactamente:

- Espacios.
- Tabulaciones.
- Saltos de línea.

Es muy útil para mostrar:

- Código.
- Diagramas.
- Arte ASCII.
- Configuraciones.

---

# La etiqueta `<blockquote>`

```html
<blockquote>

Texto citado

</blockquote>
```

Representa una cita extensa proveniente de otra fuente.

Generalmente el navegador la muestra con sangría.

---

# La etiqueta `<q>`

```html
<q>Una cita.</q>
```

Se utiliza para citas cortas dentro de un párrafo.

El navegador suele agregar automáticamente comillas.

También puede utilizarse el atributo:

```html
cite=""
```

para indicar el origen de la cita.

---

# El atributo `lang`

```html
<q lang="ja">
時間は万能な薬だ
</q>
```

Indica el idioma del contenido.

Esto ayuda a:

- Lectores de pantalla.
- Traductores.
- Navegadores.
- Motores de búsqueda.

Algunos ejemplos:

```
es
en
fr
de
ja
it
pt
```

---

# La etiqueta `<sup>`

```html
x<sup>2</sup>
```

Representa un superíndice.

Se utiliza en:

- Matemáticas.
- Potencias.
- Notación científica.
- Referencias.

Ejemplo:

```
a² + b² = c²
```

---

# La etiqueta `<sub>`

```html
H<sub>2</sub>O
```

Representa un subíndice.

Se utiliza principalmente en:

- Fórmulas químicas.
- Expresiones científicas.

Ejemplo:

```
CO₂
H₂O
NH₃
```

---

# La etiqueta `<abbr>`

```html
<abbr title="Organización Mundial de la Salud">
OMS
</abbr>
```

Define una abreviatura.

Cuando el usuario coloca el cursor sobre ella, aparece una descripción.

Es muy útil para:

- Siglas.
- Acrónimos.
- Unidades de medida.

---

# La etiqueta `<a>`

La etiqueta `<a>` crea enlaces.

Su estructura básica es:

```html
<a href="URL">
Texto
</a>
```

---

## Abrir un enlace en otra pestaña

```html
<a href="https://github.com"
target="_blank">
GitHub
</a>
```

El atributo:

```html
target="_blank"
```

abre el enlace en una nueva pestaña del navegador.

---

## Enlaces de correo

```html
<a href="mailto:correo@ejemplo.com">
Enviar correo
</a>
```

Al hacer clic, se abrirá el cliente de correo predeterminado del usuario.

---

## Enlaces telefónicos

```html
<a href="tel:+1234567890">
Llamar
</a>
```

Son especialmente útiles en dispositivos móviles, ya que permiten iniciar una llamada directamente.

---

# Buenas prácticas

✔ Utilizar `<strong>` en lugar de `<b>` cuando el texto sea importante.

✔ Utilizar `<em>` en lugar de `<i>` cuando exista énfasis.

✔ No abusar del `<br>` para separar contenido.

✔ Mantener un solo `<h1>` por documento.

✔ Utilizar `<blockquote>` para citas largas y `<q>` para citas cortas.

✔ Agregar el atributo `lang` cuando se escriba contenido en otro idioma.

✔ Utilizar `<abbr>` para explicar abreviaturas poco conocidas.

✔ Crear enlaces descriptivos en lugar de escribir textos como "Haz clic aquí".

---

# Ejercicio práctico

Crea una página que contenga:

- Un título principal.
- Tres subtítulos.
- Dos párrafos.
- Un texto importante usando `<strong>`.
- Un texto con énfasis usando `<em>`.
- Una cita corta y una cita larga.
- Una fórmula matemática usando `<sup>`.
- Una fórmula química usando `<sub>`.
- Una abreviatura con `<abbr>`.
- Un enlace a una página web.
- Un enlace de correo electrónico.
- Un enlace telefónico.

Comprueba que cada etiqueta cumpla correctamente su función.

---

# Resumen

En este tema aprendiste:

- Qué son las etiquetas de texto.
- Cómo crear párrafos con `<p>`.
- La diferencia entre `<b>`, `<strong>`, `<i>` y `<em>`.
- Qué son los elementos en bloque y en línea.
- Cómo insertar saltos de línea y separadores con `<br>` y `<hr>`.
- El uso correcto de los encabezados `<h1>` a `<h6>`.
- Cómo preservar espacios con `<pre>`.
- La diferencia entre `<blockquote>` y `<q>`.
- Cómo utilizar superíndices y subíndices.
- El uso de abreviaturas con `<abbr>`.
- Cómo crear distintos tipos de enlaces con `<a>`.

Con estas etiquetas ya puedes estructurar y dar significado al contenido textual de una página web de forma clara, accesible y profesional.