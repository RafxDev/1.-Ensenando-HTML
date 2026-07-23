# 📚 Tema 11 - Formularios en HTML

## 📖 Introducción

Los formularios son uno de los elementos más importantes del desarrollo web. Gracias a ellos los usuarios pueden interactuar con una página enviando información como nombres, contraseñas, correos electrónicos, archivos, opiniones, fechas y mucho más.

Prácticamente todos los sitios web utilizan formularios:

- Inicio de sesión.
- Registro de usuarios.
- Buscadores.
- Encuestas.
- Compras en línea.
- Contacto.
- Comentarios.
- Solicitudes.

En este tema aprenderás la estructura básica de un formulario, los principales tipos de campos (`input`), los atributos más utilizados y los controles de selección disponibles en HTML5.

---

# ¿Qué es un formulario?

Un formulario es una sección de una página web que permite al usuario ingresar información para ser procesada posteriormente.

Todo formulario comienza con la etiqueta:

```html
<form>

</form>
```

Dentro de ella se colocan todos los controles que el usuario utilizará.

---

# La etiqueta `<form>`

```html
<form>

</form>
```

Es el contenedor principal del formulario.

En aplicaciones reales suele incluir atributos como:

```html
<form
action="procesar.php"
method="POST">
```

- `action` → indica a dónde se enviarán los datos.
- `method` → define cómo serán enviados (`GET` o `POST`).

En este curso se estudia principalmente la estructura del formulario.

---

# La etiqueta `<label>`

```html
<label for="usuario">

Usuario

</label>
```

Sirve para asociar un texto descriptivo con un campo del formulario.

La relación se establece mediante el atributo:

```html
for=""
```

que debe coincidir con el atributo:

```html
id=""
```

del campo correspondiente.

Ejemplo:

```html
<label for="correo">

Correo

</label>

<input id="correo">
```

Esto mejora:

- La accesibilidad.
- La experiencia del usuario.
- La navegación mediante teclado.

---

# La etiqueta `<input>`

Es el elemento más utilizado en los formularios.

Su estructura básica es:

```html
<input
type="text">
```

Dependiendo del atributo `type`, el navegador mostrará distintos controles.

---

# `type="text"`

```html
<input type="text">
```

Permite escribir texto libre.

Se utiliza para:

- Nombres.
- Usuarios.
- Direcciones.
- Ciudades.

---

# `type="password"`

```html
<input type="password">
```

Oculta el texto ingresado mediante puntos o asteriscos.

Ideal para contraseñas.

---

# `type="checkbox"`

```html
<input type="checkbox">
```

Permite seleccionar varias opciones al mismo tiempo.

Ejemplo:

- HTML
- CSS
- JavaScript
- Python

El usuario puede marcar una, varias o ninguna.

---

# `type="radio"`

```html
<input type="radio">
```

Permite seleccionar únicamente una opción.

Todos los botones que pertenezcan al mismo grupo deben compartir el mismo atributo:

```html
name=""
```

---

# `type="number"`

```html
<input type="number">
```

Solo admite números.

Puede combinarse con:

```html
min
max
step
```

---

# `type="file"`

```html
<input type="file">
```

Permite seleccionar archivos del computador.

Muy utilizado para:

- Fotografías.
- Documentos.
- PDFs.
- Videos.

---

# `type="email"`

```html
<input type="email">
```

Solicita un correo electrónico.

El navegador verifica automáticamente que el formato sea válido.

Ejemplo:

```
usuario@correo.com
```

---

# `type="date"`

```html
<input type="date">
```

Muestra un calendario para seleccionar una fecha.

Puede limitarse utilizando:

```html
min

max
```

---

# Botones del formulario

## Botón Submit

```html
<input
type="submit">
```

Envía toda la información del formulario.

---

## Botón Reset

```html
<input
type="reset">
```

Restablece todos los campos a sus valores originales.

---

## Botón Button

```html
<input
type="button">
```

No realiza ninguna acción por sí mismo.

Normalmente se utiliza junto con JavaScript.

Ejemplo:

```html
<input
type="button"
onclick="alert('Hola')">
```

También puede utilizarse la etiqueta:

```html
<button>

Haz clic

</button>
```

---

# La etiqueta `<textarea>`

```html
<textarea>

</textarea>
```

Permite escribir texto de varias líneas.

Es ideal para:

- Comentarios.
- Opiniones.
- Mensajes.
- Descripciones.

---

# La etiqueta `<select>`

```html
<select>

</select>
```

Crea una lista desplegable.

Cada opción se define mediante:

```html
<option>
```

Ejemplo:

```html
<select>

<option>

Colombia

</option>

</select>
```

---

# La etiqueta `<option>`

Representa una opción dentro del menú desplegable.

Puede utilizar:

```html
selected
```

para aparecer seleccionada por defecto.

Ejemplo:

```html
<option selected>

Seleccione

</option>
```

---

# La etiqueta `<optgroup>`

```html
<optgroup
label="Europa">
```

Permite organizar las opciones en grupos.

Ejemplo:

```
Europa

España

Francia

Italia
```

Hace que listas largas sean mucho más fáciles de utilizar.

---

# Atributos importantes de los formularios

## `placeholder`

```html
placeholder="Escribe aquí"
```

Muestra un texto de ayuda dentro del campo.

---

## `value`

```html
value="Texto"
```

Define un valor inicial.

---

## `readonly`

```html
readonly
```

El usuario puede leer el contenido pero no modificarlo.

---

## `disabled`

```html
disabled
```

Desactiva completamente el campo.

No puede seleccionarse ni enviarse.

---

## `required`

```html
required
```

Hace obligatorio completar el campo antes de enviar el formulario.

---

## `maxlength`

```html
maxlength="10"
```

Establece la cantidad máxima de caracteres.

---

## `minlength`

```html
minlength="5"
```

Define la cantidad mínima de caracteres.

---

## `pattern`

```html
pattern="[A-Za-z]{5,10}"
```

Permite validar el contenido mediante expresiones regulares.

En el ejemplo:

- Solo letras.
- Entre 5 y 10 caracteres.

---

## `min`

```html
min="1"
```

Valor mínimo permitido.

---

## `max`

```html
max="100"
```

Valor máximo permitido.

---

## `multiple`

```html
multiple
```

Permite seleccionar varios archivos en un mismo campo.

---

# Buenas prácticas

✔ Utilizar siempre `<label>` para identificar cada campo.

✔ Asignar un `id` único a cada control.

✔ Utilizar `required` cuando un dato sea obligatorio.

✔ Agregar `placeholder` para orientar al usuario.

✔ Validar la información utilizando atributos como `pattern`, `min`, `max` o `maxlength`.

✔ Agrupar opciones mediante `<optgroup>` cuando existan muchas alternativas.

✔ Utilizar el tipo de `input` adecuado para cada dato.

---

# Errores comunes

❌ No utilizar etiquetas `<label>`.

❌ Repetir el mismo `id` en varios elementos.

❌ Utilizar `type="text"` para datos que deberían ser `email`, `date` o `number`.

❌ No validar la información ingresada.

❌ Abusar de campos obligatorios (`required`) innecesariamente.

---

# Ejercicio práctico

Construye un formulario de registro que incluya:

- Nombre de usuario.
- Contraseña.
- Correo electrónico.
- Edad.
- Fecha de nacimiento.
- País.
- Lenguajes de programación conocidos (checkbox).
- Lenguaje principal (radio).
- Campo para comentarios.
- Carga de un archivo.
- Botones **Enviar**, **Reiniciar** y un botón que muestre un mensaje usando JavaScript.

Después:

- Haz obligatorio el correo.
- Limita el nombre entre 5 y 15 caracteres.
- Restringe la edad entre 10 y 100 años.
- Permite subir varios archivos.

---

# Resumen

En este tema aprendiste:

- Qué es un formulario.
- Cómo utilizar la etiqueta `<form>`.
- La función de `<label>`.
- Los principales tipos de `<input>`.
- Cómo crear listas desplegables con `<select>`.
- Cómo organizar opciones con `<optgroup>`.
- Cómo utilizar `<textarea>`.
- Los botones `submit`, `reset` y `button`.
- Los atributos más importantes de validación (`required`, `readonly`, `disabled`, `pattern`, `maxlength`, `min`, `max`, `multiple`, entre otros).
- Buenas prácticas para construir formularios modernos y accesibles.

Con estos conocimientos ya puedes crear formularios completos y funcionales, capaces de recopilar información de los usuarios de forma organizada, validada y preparada para ser procesada por aplicaciones web.