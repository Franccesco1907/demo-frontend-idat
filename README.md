# Práctica de formularios HTML

Abre [validation-form-example/index.html](validation-form-example/index.html) en el navegador; sus estilos están en [styles.css](validation-form-example/styles.css). No requiere instalación, compilación ni servidor.

- `input`, `textarea`, `select`/`option` y `button` permiten capturar datos; `label` debe asociarse mediante `for` e `id`.
- `type` define texto, contraseña, número, radio, checkbox, fecha o correo. Radios del mismo grupo comparten `name`.
- `required`, `min`, `max` y `pattern` restringen los valores; usa `type="email"` para correo en lugar de una expresión que limite el dominio a cuatro letras.
- `:valid`, `:invalid` y `:required` permiten mostrar visualmente la validación.
- La validación nativa de envío requiere un `form` y un botón de envío; el ejemplo actual solo muestra campos individuales. No hay backend ni pruebas automatizadas.

Comprobación manual: deja el nombre vacío, introduce letras en teléfono y un correo sin `@`; observa los estilos de validez definidos en CSS. Los archivos `.txt` de la raíz pertenecen a la práctica de participantes.
