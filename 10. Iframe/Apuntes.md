# 📚 Tema 10 - Iframes en HTML

## 📖 Introducción

En muchas ocasiones es necesario mostrar contenido que no pertenece directamente a nuestra página web, como un video de YouTube, un mapa de Google Maps, una canción de SoundCloud o incluso otra página web.

Para ello, HTML proporciona la etiqueta **`<iframe>`**, que permite **incrustar contenido externo** dentro de una página.

El término **iframe** significa **Inline Frame** (marco en línea), ya que crea una ventana donde se carga otro documento HTML o contenido proporcionado por un servicio externo.

En este tema aprenderás cómo utilizar iframes, sus principales atributos y algunas de sus aplicaciones más comunes.

---

# ¿Qué es un `<iframe>`?

La etiqueta `<iframe>` permite mostrar una página web o un recurso externo dentro de otra página HTML.

Su estructura básica es:

```html
<iframe src="https://ejemplo.com"></iframe>
```

El navegador crea un marco independiente donde se carga el contenido indicado en el atributo `src`.

---

# El atributo `src`

```html
<iframe src="https://ejemplo.com"></iframe>
```

El atributo **`src`** indica la dirección del contenido que se desea mostrar.

Puede apuntar a:

- Otra página web.
- Un video.
- Un mapa.
- Un reproductor de música.
- Un documento PDF.
- Una aplicación web.

---

# Modificar el tamaño

Los atributos `width` y `height` permiten definir las dimensiones del iframe.

Ejemplo:

```html
<iframe
src="https://ejemplo.com"
width="600"
height="400">
</iframe>
```

También es posible controlar el tamaño mediante CSS.

---

# El atributo `allowfullscreen`

```html
allowfullscreen
```

Permite que el contenido incrustado pueda visualizarse en pantalla completa.

Es muy utilizado en:

- YouTube.
- Vimeo.
- Presentaciones.
- Reproductores multimedia.

---

# El atributo `loading`

```html
loading="lazy"
```

Indica al navegador que cargue el iframe únicamente cuando el usuario se acerque a él.

Esto mejora el rendimiento de la página.

Valores posibles:

- `lazy`
- `eager`

Actualmente se recomienda utilizar `lazy` cuando el contenido no sea visible inmediatamente.

---

# El atributo `referrerpolicy`

```html
referrerpolicy="strict-origin-when-cross-origin"
```

Controla la información que el navegador envía al sitio web externo sobre el origen de la solicitud.

Se utiliza principalmente por motivos de privacidad y seguridad.

---

# El atributo `allow`

```html
allow="autoplay; encrypted-media"
```

Permite habilitar determinadas funciones dentro del iframe.

Algunas opciones comunes son:

- `autoplay`
- `clipboard-write`
- `encrypted-media`
- `fullscreen`
- `gyroscope`
- `picture-in-picture`

Cada servicio define qué permisos son necesarios.

---

# Incrustar un video de YouTube

Uno de los usos más frecuentes de `<iframe>` es insertar videos de YouTube.

Ejemplo:

```html
<iframe
width="560"
height="315"
src="https://www.youtube.com/embed/ID_DEL_VIDEO"
allowfullscreen>
</iframe>
```

### ¿Cómo obtener el código?

1. Abrir el video en YouTube.
2. Hacer clic en **Compartir**.
3. Seleccionar **Insertar**.
4. Copiar el código HTML generado.

Este método garantiza una mayor compatibilidad.

---

# Incrustar música de SoundCloud

SoundCloud también permite insertar reproductores mediante iframes.

Ejemplo:

```html
<iframe
src="https://w.soundcloud.com/player/...">
</iframe>
```

Generalmente el propio sitio genera automáticamente el código necesario.

---

# Mostrar otra página web

También es posible cargar una página web completa.

Ejemplo:

```html
<iframe
src="https://www.google.com">
</iframe>
```

Sin embargo, muchas páginas modernas **no permiten ser incrustadas** debido a políticas de seguridad.

Por ello, es normal que algunos sitios no se muestren correctamente dentro de un iframe.

---

# Incrustar Google Maps

Google Maps ofrece una forma muy sencilla de insertar mapas.

Ejemplo:

```html
<iframe
src="https://www.google.com/maps/embed?...">
</iframe>
```

### Obtener el código

1. Buscar una ubicación en Google Maps.
2. Seleccionar **Compartir**.
3. Elegir **Insertar un mapa**.
4. Copiar el código HTML.

Esta es una de las formas más utilizadas para mostrar ubicaciones en sitios web.

---

# Otros usos comunes de `<iframe>`

Los iframes permiten incrustar muchos tipos de contenido.

Algunos ejemplos son:

- Videos de YouTube.
- Mapas de Google Maps.
- Música de SoundCloud.
- Presentaciones.
- Formularios externos.
- Documentos PDF.
- Calendarios.
- Publicaciones de redes sociales.
- Aplicaciones web.

---

# Ventajas de utilizar iframes

- Fácil integración de contenido externo.
- No es necesario descargar los recursos.
- Permite reutilizar servicios de terceros.
- Reduce el trabajo de desarrollo.
- Mantiene el contenido actualizado automáticamente.

---

# Desventajas

- Dependen del servicio externo.
- Algunas páginas bloquean los iframes por seguridad.
- Pueden afectar el rendimiento si se utilizan en exceso.
- Requieren conexión a Internet para cargar el contenido.

---

# Buenas prácticas

✔ Utilizar únicamente contenido proveniente de sitios confiables.

✔ Configurar correctamente el tamaño del iframe.

✔ Utilizar `loading="lazy"` cuando sea posible.

✔ Permitir únicamente los permisos necesarios mediante `allow`.

✔ Utilizar `allowfullscreen` en videos.

✔ Verificar que el contenido incrustado sea responsive para dispositivos móviles.

---

# Errores comunes

❌ Intentar incrustar páginas que no permiten el uso de iframes.

---

❌ Utilizar demasiados iframes en una misma página, afectando el rendimiento.

---

❌ No establecer dimensiones, provocando problemas en el diseño.

---

❌ Conceder permisos innecesarios mediante el atributo `allow`.

---

# Ejercicio práctico

Crea una página que contenga:

- Un video de YouTube incrustado.
- Un reproductor de SoundCloud.
- Un mapa de Google Maps con la ubicación de tu ciudad.
- Un iframe con `loading="lazy"`.
- Un iframe con `allowfullscreen`.

Después, intenta incrustar una página web cualquiera y observa si permite o no ser mostrada dentro del iframe.

---

# Resumen

En este tema aprendiste:

- Qué es la etiqueta `<iframe>`.
- Cómo utilizar el atributo `src`.
- Cómo modificar el tamaño con `width` y `height`.
- El propósito de `allowfullscreen`.
- Cómo mejorar el rendimiento con `loading="lazy"`.
- La función del atributo `allow`.
- Qué hace `referrerpolicy`.
- Cómo incrustar videos de YouTube.
- Cómo insertar reproductores de SoundCloud.
- Cómo mostrar mapas de Google Maps.
- Las ventajas y limitaciones del uso de iframes.
- Buenas prácticas para integrar contenido de terceros.

Con estos conocimientos ya puedes incorporar recursos externos en tus páginas web de forma segura y profesional, aprovechando servicios como YouTube, Google Maps y otras plataformas compatibles con `iframe`.