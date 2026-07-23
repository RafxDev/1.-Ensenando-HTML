# 📚 Tema 7 - Listas en HTML

## 📖 Introducción

Las listas son una de las herramientas más utilizadas en HTML para organizar información de manera clara y ordenada. Se emplean para crear menús de navegación, listas de tareas, catálogos de productos, índices, recetas, instrucciones y muchos otros elementos presentes en una página web.

HTML ofrece distintos tipos de listas según la forma en que se desea presentar la información:

- **Listas desordenadas** (`<ul>`)
- **Listas ordenadas** (`<ol>`)
- **Elementos de lista** (`<li>`)
- **Listas anidadas** (listas dentro de otras listas)

En este tema aprenderás a utilizar cada una de ellas y a personalizar su numeración.

---

# ¿Qué es una lista?

Una lista es un conjunto de elementos relacionados entre sí.

Cada elemento de una lista se representa mediante la etiqueta:

```html
<li>
```

La forma en que esos elementos se muestran dependerá del tipo de lista que se utilice.

---

# La etiqueta `<ul>` (Lista desordenada)

La etiqueta `<ul>` crea una lista cuyos elementos no siguen un orden específico.

Cada elemento aparece acompañado por un símbolo (viñeta).

Su estructura es:

```html
<ul>

<li>Elemento 1</li>
<li>Elemento 2</li>
<li>Elemento 3</li>

</ul>
```

Ejemplo:

```html
<ul>
    <li>Leche</li>
    <li>Pan</li>
    <li>Huevos</li>
</ul>
```

Resultado:

- Leche
- Pan
- Huevos

Las listas desordenadas son ideales para mostrar información donde el orden no es importante.

---

# La etiqueta `<ol>` (Lista ordenada)

La etiqueta `<ol>` crea una lista numerada.

Cada elemento recibe automáticamente un número.

Ejemplo:

```html
<ol>
    <li>Despertar</li>
    <li>Desayunar</li>
    <li>Trabajar</li>
</ol>
```

Resultado:

1. Despertar
2. Desayunar
3. Trabajar

Este tipo de lista se utiliza cuando el orden de los elementos sí es importante.

---

# La etiqueta `<li>`

```html
<li>Elemento</li>
```

Representa un elemento individual dentro de una lista.

Puede utilizarse tanto en listas ordenadas como desordenadas.

Ejemplo:

```html
<ul>

<li>HTML</li>

<li>CSS</li>

<li>JavaScript</li>

</ul>
```

---

# Listas anidadas

Es posible colocar una lista dentro de otra.

Esto permite representar categorías y subcategorías.

Ejemplo:

```html
<ul>

<li>

Frutas

<ul>

<li>Manzanas</li>

<li>Bananas</li>

</ul>

</li>

</ul>
```

En el ejemplo del código se observa cómo una lista principal contiene otras listas, tanto ordenadas como desordenadas.

Las listas anidadas son muy utilizadas para:

- Menús.
- Árboles de directorios.
- Categorías.
- Índices.
- Estructuras jerárquicas.

---

# El atributo `start`

Las listas ordenadas pueden comenzar desde un número específico.

Ejemplo:

```html
<ol start="5">

<li>Tarea</li>

<li>Tarea</li>

</ol>
```

Resultado:

5. Tarea

6. Tarea

Es útil cuando una lista continúa desde otra previamente mostrada.

---

# El atributo `type`

Permite modificar el tipo de numeración de una lista ordenada.

## Letras mayúsculas

```html
<ol type="A">
```

Resultado:

A.

B.

C.

---

## Letras minúsculas

```html
<ol type="a">
```

Resultado:

a.

b.

c.

---

## Números romanos mayúsculos

```html
<ol type="I">
```

Resultado:

I.

II.

III.

---

## Números romanos minúsculos

```html
<ol type="i">
```

Resultado:

i.

ii.

iii.

---

## Numeración tradicional

```html
<ol type="1">
```

Resultado:

1.

2.

3.

Este es el valor predeterminado.

---

# El atributo `reversed`

```html
<ol reversed>
```

Hace que la numeración se muestre en orden descendente.

Ejemplo:

```html
<ol reversed>

<li>Uno</li>

<li>Dos</li>

<li>Tres</li>

</ol>
```

Resultado:

3. Uno

2. Dos

1. Tres

Es útil para mostrar clasificaciones o conteos regresivos.

---

# ¿Cuándo utilizar cada tipo de lista?

### Utiliza `<ul>` cuando:

- El orden no sea importante.
- Se trate de una lista de elementos.
- Muestres opciones de navegación.
- Enumeres características.

Ejemplos:

- Lista de compras.
- Menú principal.
- Ingredientes.

---

### Utiliza `<ol>` cuando:

- Exista un orden específico.
- Se describan pasos.
- Se expliquen procedimientos.
- Se muestren clasificaciones.

Ejemplos:

- Tutoriales.
- Recetas.
- Manuales.
- Instrucciones.

---

# Buenas prácticas

✔ Utilizar `<ul>` únicamente cuando el orden no importe.

✔ Utilizar `<ol>` para procesos paso a paso.

✔ Mantener una correcta indentación en listas anidadas.

✔ Evitar crear demasiados niveles de anidación para no dificultar la lectura.

✔ Escribir elementos de lista claros y descriptivos.

✔ Utilizar atributos como `type`, `start` o `reversed` solo cuando realmente sean necesarios.

---

# Errores comunes

❌ Colocar elementos que no sean `<li>` directamente dentro de una lista.

Incorrecto:

```html
<ul>

<p>Elemento</p>

</ul>
```

Correcto:

```html
<ul>

<li>Elemento</li>

</ul>
```

---

❌ Utilizar listas ordenadas cuando el orden no tiene importancia.

---

❌ Crear listas excesivamente profundas y difíciles de leer.

---

# Ejercicio práctico

Crea una página que contenga:

- Una lista desordenada con cinco frutas.
- Una lista ordenada con los pasos para preparar una taza de café.
- Una lista anidada que represente las carpetas de un proyecto.
- Una lista ordenada que comience desde el número 10.
- Una lista utilizando letras mayúsculas.
- Otra utilizando números romanos.
- Una lista en orden inverso utilizando `reversed`.

---

# Resumen

En este tema aprendiste:

- Qué son las listas en HTML.
- Cómo crear listas desordenadas con `<ul>`.
- Cómo crear listas ordenadas con `<ol>`.
- El uso de la etiqueta `<li>`.
- Cómo construir listas anidadas.
- Cómo modificar la numeración mediante `start`.
- Cómo utilizar diferentes estilos de numeración con `type`.
- Cómo invertir el orden utilizando `reversed`.
- Las buenas prácticas para organizar información mediante listas.

Con estos conocimientos ya puedes estructurar información de forma clara y organizada, una habilidad fundamental para construir menús, índices, formularios, catálogos y muchos otros componentes de una página web.