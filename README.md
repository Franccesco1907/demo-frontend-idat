# FRONTEND TEORÍA

### 1. ¿Qué es un formulario HTML?

Un formulario HTML es un elemento fundamental en el desarrollo web que permite a los usuarios ingresar datos y enviarlos al servidor para su procesamiento. Los formularios son esenciales para interactuar con los visitantes de un sitio web, ya que permiten la entrada de información como texto, números, selecciones y más. Los formularios se crean utilizando una combinación de etiquetas HTML y se definen mediante el elemento `<form>`.

```html
<form action="procesar.php" method="post">
  <!-- Elementos del formulario se colocan aquí -->
  <input type="text" name="nombre" placeholder="Nombre">
  <input type="submit" value="Enviar">
</form>
```

### 2. Etiquetas de formulario

Las etiquetas de formulario son elementos HTML utilizados para crear diferentes tipos de controles y campos en un formulario. Algunas de las etiquetas más comunes incluyen:

#### `<input>`
La etiqueta `<input>` se utiliza para crear campos de entrada en formularios. Puede tener varios tipos, que se describen en detalle a continuación.

#### `<label>`
La etiqueta `<label>` se utiliza para proporcionar etiquetas descriptivas para los campos de entrada. Mejora la accesibilidad y la usabilidad de un formulario.

```html
<label for="nombre">Nombre:</label>
<input type="text" id="nombre" name="nombre">
```

#### `<textarea>`
La etiqueta `<textarea>` se utiliza para crear áreas de texto de múltiples líneas en formularios, como comentarios o mensajes largos.

```html
<textarea name="comentario" rows="4" cols="50"></textarea>
```

#### `<select>` y `<option>`
Las etiquetas `<select>` y `<option>` se utilizan para crear listas desplegables (selects) en las que los usuarios pueden seleccionar una opción de una lista predefinida.

```html
<select name="color">
  <option value="rojo">Rojo</option>
  <option value="verde">Verde</option>
  <option value="azul">Azul</option>
</select>
```

#### `<button>`
La etiqueta `<button>` se utiliza para crear botones personalizados en formularios, que pueden ser utilizados para enviar el formulario o realizar otras acciones mediante JavaScript.

```html
<button type="submit">Enviar</button>
```

### 3. Tipos de input

Los campos de entrada (`<input>`) son esenciales en los formularios, y pueden tener varios tipos que determinan el tipo de dato que se espera. Algunos de los tipos de input más comunes son:

#### Texto (`type="text"`)
Este tipo se utiliza para campos de texto de una sola línea, como nombres, direcciones de correo electrónico o contraseñas.

```html
<input type="text" name="nombre" placeholder="Nombre">
```

#### Contraseña (`type="password"`)
El tipo "password" se utiliza para campos de contraseña y oculta los caracteres ingresados para proteger la información.

```html
<input type="password" name="clave" placeholder="Contraseña">
```

#### Número (`type="number"`)
El tipo "number" se utiliza para campos que requieren valores numéricos, como edades o cantidades.

```html
<input type="number" name="edad" min="0" max="100">
```

#### Radio (`type="radio"`)
Los botones de opción (`<input type="radio">`) permiten a los usuarios seleccionar una opción de una lista de opciones mutuamente excluyentes.

```html
<input type="radio" name="genero" value="masculino"> Masculino
<input type="radio" name="genero" value="femenino"> Femenino
```

#### Casilla de verificación (`type="checkbox"`)
Las casillas de verificación (`<input type="checkbox">`) permiten a los usuarios seleccionar múltiples opciones de una lista.

```html
<input type="checkbox" name="intereses" value="deportes"> Deportes
<input type="checkbox" name="intereses" value="lectura"> Lectura
```

#### Fecha (`type="date"`)
El tipo "date" se utiliza para seleccionar una fecha específica a partir de un calendario interactivo.

```html
<input type="date" name="fecha_nacimiento">
```

Estos son solo algunos ejemplos de etiquetas de formulario y tipos de input en HTML. La combinación de estas etiquetas y tipos de input te permite crear formularios interactivos y personalizados para tu sitio web. Es importante comprender cómo funcionan y cómo se combinan para lograr la funcionalidad deseada en tu frontend.

### 1. Validaciones de formulario y atributos de validación

La validación de formularios es un proceso esencial para garantizar que los datos ingresados por los usuarios sean precisos y cumplan con ciertos criterios antes de ser enviados al servidor. HTML5 introduce una serie de atributos que facilitan la validación de formularios sin necesidad de escribir JavaScript personalizado. Algunos atributos de validación comunes incluyen:

#### `required`
El atributo `required` se agrega a un campo de entrada para indicar que el usuario debe proporcionar un valor antes de enviar el formulario. Esto es útil para campos obligatorios.

```html
<input type="text" name="nombre" required>
```

#### `min` y `max`
Los atributos `min` y `max` se utilizan para establecer valores mínimo y máximo para campos numéricos. Por ejemplo, para establecer una edad mínima de 18 años:

```html
<input type="number" name="edad" min="18">
```

#### `pattern`
El atributo `pattern` permite definir un patrón de expresión regular que debe coincidir con el valor del campo de entrada. Esto es útil para validar formatos específicos, como números de teléfono o códigos postales.

```html
<input type="text" name="telefono" pattern="[0-9]{10}">
```

### 2. Patrones de validación

Los patrones de validación se definen utilizando expresiones regulares en el atributo `pattern`. Aquí hay algunos ejemplos comunes de patrones de validación:

- **Número de teléfono en formato de 10 dígitos (EE. UU.):**

```html
<input type="text" name="telefono" pattern="[0-9]{10}">
```

- **Dirección de correo electrónico:**

```html
<input type="email" name="email">
```
Opcional:
```html
<input type="text" name="email" pattern="[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}">
```

- **Código postal de Estados Unidos (5 dígitos o 5 dígitos + extensión de 4 dígitos):**

```html
<input type="text" name="codigo_postal" pattern="\d{5}(-\d{4})?">
```

### 3. Pseudo clases de validación

Las pseudo clases de validación en CSS son útiles para aplicar estilos a elementos del formulario basados en su estado de validación. Algunas pseudo clases de validación comunes son:

#### `:valid`
La pseudo clase `:valid` se aplica a elementos de formulario que han pasado la validación. Por ejemplo, un campo de entrada con un formato de correo electrónico válido:

```css
input:valid {
  border-color: green;
}
```

#### `:invalid`
La pseudo clase `:invalid` se aplica a elementos de formulario que no han pasado la validación. Por ejemplo, un campo de entrada con un correo electrónico incorrecto:

```css
input:invalid {
  border-color: red;
}
```

#### `:required`
La pseudo clase `:required` se aplica a elementos de formulario que tienen el atributo `required`. Puedes utilizarlo para resaltar campos obligatorios:

```css
input:required {
  font-weight: bold;
}
```

Estas son algunas de las herramientas que puedes utilizar para implementar la validación de formularios en HTML y aplicar estilos basados en el estado de validación utilizando CSS. La validación de formularios es esencial para mejorar la experiencia del usuario y garantizar que los datos ingresados sean precisos y confiables.
