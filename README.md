# Pr�ctica de formularios HTML

Abre [validation-form-example/index.html](validation-form-example/index.html) en el navegador; sus estilos est�n en [styles.css](validation-form-example/styles.css). No requiere instalaci�n, compilaci�n ni servidor.

- `input`, `textarea`, `select`/`option` y `button` permiten capturar datos; `label` debe asociarse mediante `for` e `id`.
- `type` define texto, contrase�a, n�mero, radio, checkbox, fecha o correo. Radios del mismo grupo comparten `name`.
- `required`, `min`, `max` y `pattern` restringen los valores; usa `type="email"` para correo en lugar de una expresi�n que limite el dominio a cuatro letras.
- `:valid`, `:invalid` y `:required` permiten mostrar visualmente la validaci�n.
- La validaci�n nativa de env�o requiere un `form` y un bot�n de env�o; el ejemplo actual solo muestra campos individuales. No hay backend ni pruebas automatizadas.

Comprobaci�n manual: deja el nombre vac�o, introduce letras en tel�fono y un correo sin `@`; observa los estilos de validez definidos en CSS. Los archivos `.txt` de la ra�z pertenecen a la pr�ctica de participantes.
