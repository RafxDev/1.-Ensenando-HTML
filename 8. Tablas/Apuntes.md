# 📚 Tema 8 - Tablas en HTML

## 📖 Introducción

Las tablas son uno de los elementos más útiles de HTML para organizar información en filas y columnas. Son ideales para mostrar datos estructurados como horarios, listas de estudiantes, inventarios, reportes financieros, estadísticas y cualquier información tabular.

Antes de HTML5 era común utilizar tablas para diseñar páginas web completas, pero actualmente **las tablas deben utilizarse únicamente para representar datos**, mientras que el diseño de la página debe realizarse con CSS.

En este tema aprenderás cómo crear tablas, organizar filas y columnas, utilizar encabezados y personalizar grupos de columnas.

---

# ¿Qué es una tabla?

Una tabla es una estructura formada por filas y columnas que permite organizar información de manera clara.

En HTML, una tabla se crea utilizando la etiqueta:

```html
<table>

</table>
```

Dentro de ella se agregan las filas y las celdas.

---

# Estructura básica de una tabla

Una tabla sencilla tiene la siguiente estructura:

```html
<table>

<tr>

<td>Dato 1</td>
<td>Dato 2</td>
<td>Dato 3</td>

</tr>

</table>
```

Visualmente:

| Dato 1 | Dato 2 | Dato 3 |

---

# La etiqueta `<table>`

```html
<table>

</table>
```

Es el contenedor principal de toda la tabla.

Dentro de esta etiqueta se colocan:

- Filas (`<tr>`)
- Encabezados (`<th>`)
- Celdas (`<td>`)
- Grupos de columnas (`<colgroup>`)

---

# La etiqueta `<tr>`

```html
<tr>

</tr>
```

Representa una fila (**Table Row**).

Cada fila puede contener varias celdas.

Ejemplo:

```html
<tr>

<td>Pedro</td>
<td>21</td>

</tr>
```

---

# La etiqueta `<td>`

```html
<td>Contenido</td>
```

Representa una celda de datos (**Table Data**).

Cada `<td>` corresponde a una columna dentro de la fila.

Ejemplo:

```html
<tr>

<td>HTML</td>

<td>CSS</td>

<td>JavaScript</td>

</tr>
```

Resultado:

| HTML | CSS | JavaScript |

---

# La etiqueta `<th>`

```html
<th>Nombre</th>
```

Representa una celda de encabezado (**Table Header**).

Por defecto el navegador la muestra:

- En negrita.
- Centrada.

Se utiliza para identificar el contenido de cada columna o fila.

Ejemplo:

```html
<tr>

<th>Nombre</th>

<th>Edad</th>

</tr>
```

Resultado:

| Nombre | Edad |

---

# La etiqueta `<colgroup>`

```html
<colgroup>

</colgroup>
```

Permite agrupar columnas para aplicar estilos de manera conjunta.

Dentro de ella se utilizan etiquetas `<col>`.

Ejemplo:

```html
<colgroup>

<col style="background-color: gray;">

<col>

<col>

</colgroup>
```

En el ejemplo del código, la primera columna aparece con un color de fondo diferente gracias a este elemento.

---

# La etiqueta `<col>`

```html
<col>
```

Representa una columna dentro del grupo de columnas.

Generalmente se utiliza para aplicar estilos como:

- Color de fondo.
- Ancho.
- Bordes.

No contiene información, únicamente sirve para configurar la apariencia de una columna.

---

# Ejemplo completo

```html
<table>

<tr>

<th>Nombre</th>

<th>Edad</th>

</tr>

<tr>

<td>Pedro</td>

<td>21</td>

</tr>

<tr>

<td>Ana</td>

<td>20</td>

</tr>

</table>
```

Resultado:

| Nombre | Edad |
|---------|------|
| Pedro | 21 |
| Ana | 20 |

---

# Estilos básicos con CSS

En el ejemplo del código se utiliza CSS para mejorar la apariencia de la tabla.

### `border-collapse`

```css
table{
    border-collapse: collapse;
}
```

Une los bordes de las celdas para evitar líneas dobles.

---

### `border`

```css
border: 2px solid gray;
```

Agrega un borde alrededor de la tabla o de las celdas.

---

### `padding`

```css
padding: 10px 20px;
```

Añade espacio entre el contenido y los bordes de cada celda.

Hace que la tabla sea mucho más legible.

---

### `background-color`

```css
background-color: gray;
```

Permite cambiar el color de fondo de una fila, columna o encabezado.

En el ejemplo se utiliza para destacar los encabezados de la tabla.

---

### `letter-spacing`

```css
letter-spacing: 1px;
```

Aumenta la separación entre caracteres.

Se utiliza únicamente con fines estéticos.

---

### `font-size`

```css
font-size: 0.8rem;
```

Modifica el tamaño del texto de la tabla.

---

# ¿Cuándo utilizar tablas?

Las tablas deben utilizarse para mostrar datos organizados.

Ejemplos:

- Horarios escolares.
- Inventarios.
- Reportes financieros.
- Listas de estudiantes.
- Resultados deportivos.
- Estadísticas.
- Calificaciones.

No deben utilizarse para construir el diseño general de una página web.

---

# Buenas prácticas

✔ Utilizar `<th>` para los encabezados.

✔ Organizar correctamente las filas mediante `<tr>`.

✔ Aplicar estilos utilizando CSS.

✔ Mantener una estructura clara y ordenada.

✔ Utilizar tablas únicamente para datos tabulares.

✔ Agrupar columnas con `<colgroup>` cuando sea necesario.

---

# Errores comunes

❌ Utilizar tablas para diseñar toda una página web.

Actualmente esto se considera una mala práctica.

---

❌ Colocar texto directamente dentro de `<table>`.

Incorrecto:

```html
<table>

Hola

</table>
```

Correcto:

```html
<table>

<tr>

<td>Hola</td>

</tr>

</table>
```

---

❌ No utilizar encabezados (`<th>`).

Los encabezados ayudan tanto a la accesibilidad como a la comprensión de la información.

---

# Etiquetas avanzadas (HTML5)

Aunque no aparecen en este ejemplo, HTML también ofrece otras etiquetas muy útiles para tablas:

| Etiqueta | Función |
|----------|---------|
| `<thead>` | Agrupa el encabezado de la tabla. |
| `<tbody>` | Agrupa el cuerpo principal. |
| `<tfoot>` | Agrupa el pie de la tabla. |
| `<caption>` | Agrega un título descriptivo a la tabla. |

Estas etiquetas mejoran la organización y la accesibilidad.

---

# Ejercicio práctico

Crea una tabla que represente las calificaciones de cinco estudiantes.

Debe incluir:

- Nombre.
- Edad.
- Curso.
- Nota final.
- Estado (Aprobado o Reprobado).

Después:

- Agrega encabezados utilizando `<th>`.
- Cambia el color del encabezado con CSS.
- Utiliza `border-collapse`.
- Aplica `padding` a todas las celdas.
- Colorea una columna utilizando `<colgroup>`.

---

# Resumen

En este tema aprendiste:

- Qué es una tabla en HTML.
- Cómo utilizar la etiqueta `<table>`.
- Cómo crear filas mediante `<tr>`.
- Cómo agregar celdas utilizando `<td>`.
- La función de los encabezados `<th>`.
- Cómo agrupar columnas con `<colgroup>` y `<col>`.
- Cómo mejorar la apariencia de una tabla utilizando CSS.
- Cuándo es apropiado utilizar tablas y cuándo no.
- Buenas prácticas para organizar información tabular.

Con estos conocimientos ya puedes crear tablas profesionales para mostrar información organizada, clara y fácil de interpretar en cualquier página web.