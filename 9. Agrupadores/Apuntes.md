# 📚 Tema 9 - Agrupadores en HTML (`<div>` y `<span>`)

## 📖 Introducción

A medida que una página web crece, es necesario organizar el contenido para facilitar su diseño, mantenimiento y manipulación mediante CSS y JavaScript.

Para ello, HTML proporciona dos etiquetas muy importantes conocidas como **agrupadores**:

- **`<div>`** → Elemento en bloque.
- **`<span>`** → Elemento en línea.

Aunque ambas permiten agrupar contenido, cada una tiene un propósito diferente dependiendo del tipo de elementos que se deseen organizar.

En este tema aprenderás cuándo utilizar cada una y cuáles son sus diferencias.

---

# ¿Qué es un agrupador?

Un agrupador es una etiqueta cuya función principal es reunir uno o varios elementos HTML para tratarlos como una sola unidad.

Esto permite:

- Aplicar estilos CSS.
- Manipular contenido con JavaScript.
- Organizar mejor la estructura del documento.
- Facilitar el mantenimiento del código.

Los agrupadores **no aportan significado semántico** al contenido; simplemente sirven como contenedores.

---

# La etiqueta `<div>`

```html
<div>

</div>
```

La etiqueta `<div>` es un contenedor de tipo **bloque**.

Esto significa que ocupa todo el ancho disponible y comienza siempre en una nueva línea.

Puede contener prácticamente cualquier elemento HTML, por ejemplo:

- Encabezados.
- Párrafos.
- Imágenes.
- Enlaces.
- Formularios.
- Otras etiquetas `<div>`.

---

# Ejemplo de uso

```html
<div>

<h2>Título</h2>

<p>Contenido.</p>

<img src="foto.jpg">

<a href="#">Más información</a>

</div>
```

En el código del ejemplo se agrupan varios elementos relacionados dentro de un único `<div>`.

Esto permite aplicar estilos a todo el conjunto mediante CSS.

---

# ¿Para qué se utiliza `<div>`?

Es una de las etiquetas más utilizadas en desarrollo web.

Se emplea para crear:

- Contenedores.
- Tarjetas (Cards).
- Barras laterales.
- Secciones.
- Cuadrículas (Grid).
- Diseños con Flexbox.
- Componentes de interfaces.

La mayoría de los diseños modernos están construidos utilizando numerosos elementos `<div>` combinados con CSS.

---

# Características de `<div>`

- Es un elemento **en bloque**.
- Ocupa todo el ancho disponible.
- Puede contener otros elementos HTML.
- Puede anidarse dentro de otros `<div>`.
- No posee significado semántico.

---

# La etiqueta `<span>`

```html
<span>

</span>
```

La etiqueta `<span>` es un contenedor **en línea**.

Solo ocupa el espacio necesario para mostrar su contenido.

Generalmente se utiliza para modificar una pequeña parte de un texto.

---

# Ejemplo de uso

```html
<p>

Mi color favorito es

<span style="color:red">

rojo

</span>

</p>
```

Resultado:

Mi color favorito es **rojo**.

En el ejemplo del código se utiliza `<span>` para agrupar una fecha y aplicar estilos de manera independiente.

---

# ¿Para qué se utiliza `<span>`?

Normalmente se emplea para:

- Cambiar el color de una palabra.
- Aplicar una fuente distinta.
- Resaltar parte de un texto.
- Manipular fragmentos mediante JavaScript.

No debe utilizarse para agrupar grandes cantidades de contenido.

---

# Características de `<span>`

- Es un elemento **en línea**.
- Solo ocupa el espacio necesario.
- Puede contener texto y otros elementos en línea.
- No rompe la línea del documento.
- No posee significado semántico.

---

# Diferencias entre `<div>` y `<span>`

| `<div>` | `<span>` |
|----------|----------|
| Elemento en bloque | Elemento en línea |
| Ocupa todo el ancho disponible | Solo ocupa el espacio necesario |
| Ideal para grandes estructuras | Ideal para pequeñas partes del texto |
| Puede contener casi cualquier elemento HTML | Generalmente contiene texto o elementos en línea |
| Muy utilizado para el diseño de páginas | Muy utilizado para aplicar estilos específicos |

---

# Ejemplo comparativo

### Utilizando `<div>`

```html
<div>

<h2>Artículo</h2>

<p>Contenido...</p>

</div>
```

Se crea un bloque completo.

---

### Utilizando `<span>`

```html
<p>

Este texto contiene una

<span>

palabra destacada

</span>

</p>
```

Solo se modifica una parte del texto.

---

# Relación con CSS

Los agrupadores son especialmente útiles cuando se combinan con CSS.

Ejemplo:

```html
<div class="card">

<h2>Título</h2>

<p>Contenido</p>

</div>
```

```css
.card{

background: white;

padding:20px;

border-radius:10px;

}
```

Gracias a esto es posible diseñar componentes reutilizables.

---

# Relación con JavaScript

También permiten manipular contenido mediante JavaScript.

Ejemplo:

```html
<span id="contador">

0

</span>
```

JavaScript puede modificar ese valor dinámicamente.

---

# Buenas prácticas

✔ Utilizar `<div>` para organizar grandes bloques de contenido.

✔ Utilizar `<span>` únicamente para modificar pequeñas partes del texto.

✔ Agregar clases (`class`) o identificadores (`id`) cuando sea necesario aplicar estilos o scripts.

✔ Mantener una estructura ordenada y con buena indentación.

✔ Utilizar etiquetas semánticas (`<section>`, `<article>`, `<header>`, etc.) cuando representen mejor el contenido, reservando `<div>` para casos donde no exista una etiqueta semántica adecuada.

---

# Errores comunes

❌ Utilizar `<span>` para contener grandes secciones de una página.

---

❌ Construir toda una página utilizando únicamente `<div>` cuando existen etiquetas semánticas más apropiadas.

---

❌ Crear demasiados niveles de `<div>` innecesarios, dificultando la lectura del código.

---

# Ejercicio práctico

Construye una página que contenga:

- Un `<div>` representando una tarjeta de presentación.
- Dentro del `<div>` agrega:
  - Un título.
  - Un párrafo.
  - Una imagen.
  - Un enlace.

Después crea un párrafo donde una sola palabra esté dentro de un `<span>` y aplícale un color diferente mediante CSS.

---

# Resumen

En este tema aprendiste:

- Qué son los agrupadores en HTML.
- Cómo utilizar la etiqueta `<div>`.
- Cómo utilizar la etiqueta `<span>`.
- La diferencia entre elementos en bloque y elementos en línea.
- Cuándo utilizar cada uno de estos contenedores.
- Cómo combinarlos con CSS y JavaScript.
- Buenas prácticas para mantener un código limpio y organizado.

Con estos conocimientos ya puedes organizar el contenido de tus páginas web de forma más eficiente, preparando la estructura necesaria para aplicar estilos, crear diseños modernos y manipular elementos mediante JavaScript.