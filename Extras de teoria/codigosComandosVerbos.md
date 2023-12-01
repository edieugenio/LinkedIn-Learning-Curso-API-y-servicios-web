## Códigos de respuesta FTP

El primer dígito se utiliza para indicar el resultado de la comunicación: 

- 2yz - respuesta Éxito
- 4yz o 5yz - No hay respuesta
- 1yz o 3yz - Un error o una respuesta incompleta

El segundo dígito define la clase de error:

- x0z - Error de sintaxis
- x1z - Respuesta a las solicitudes de información
- x2z - Respuesta al control y conexiones de datos
- x3z - Respuestas sobre autenticación
- x4z - No definido.
- x5z - Códigos de estados del sistema de archivos del servidor.

El tercer dígito del código de respuesta se utiliza para proporcionar detalles adicionales para cada una de las categorías definidas por el segundo dígito.

## Comandos y códigos SMTP

**Comandos SMTP**

- HELO, para abrir una sesión con el servidor
- EHLO, para abrir una sesión, en el caso de que el servidor soporte extensiones.
- MAIL FROM, para indicar quien envía el mensaje
- RCPT TO, para indicar el destinatario del mensaje
- DATA, para indicar el comienzo del mensaje, éste finalizará cuando haya una línea únicamente con un punto.
- QUIT, para cerrar la sesión
- RSET Aborta la transacción en curso y borra todos los registros.
- SEND Inicia una transacción en la cual el mensaje se entrega a una terminal.
- SOML El mensaje se entrega a un terminal o a un buzón.
- SAML El mensaje se entrega a un terminal y a un buzón.
- VRFY Solicita al servidor la verificación de todo un argumento.
- EXPN Solicita al servidor la confirmación del argumento.
- HELP Permite solicitar información sobre un comando.
- NOOP No decir nada, se emplea para mantener la sesión abierta
- TURN Solicita al servidor que intercambien los papeles (el servidor hace de cliente y el cliente de servidor).

**Códigos de respuesta SMTP:**

De los tres dígitos del código numérico, el primero indica la categoría de la respuesta, estando definidas las siguientes categorías:

- 2XX, la operación solicitada ha sido concluida con éxito
- 3XX, la orden ha sido aceptada, pero el servidor esta pendiente de que el cliente le envíe nuevos datos para terminar la operación
- 4XX, para una respuesta de error
- 5XX, para indicar una condición de error permanente, por lo que no debe repetirse la orden

## Comandos y códigos HTTP

Códigos de respuestas del servidor: 

- Códigos con formato 1xx: Respuestas informativas. Indica que la petición ha sido recibida y se está procesando.
- Códigos con formato 2xx: Respuestas correctas. Indica que la petición ha sido procesada correctamente.
- Códigos con formato 3xx: Respuestas de redirección. Indica que el cliente necesita realizar más acciones para finalizar la petición.
- Códigos con formato 4xx: Errores causados por el cliente. Indica que ha habido un error en el procesado de la petición a causa de que el cliente ha hecho algo mal.
- Códigos con formato 5xx: Errores causados por el servidor. Indica que ha habido un error en el procesado de la petición a causa de un fallo en el servidor.

## Verbos HTTP

**GET:**  Solicita un recurso al servidor. 

**HEAD**: Pide un recurso al servidor pero sólo su cabecera y no su cuerpo. 

**POST**: Envía datos para ser procesados al servidor. Normalmente se utilizan para crear nuevos recursos. 

**PUT**: Se utiliza para actualizar contenidos en el servidor. 

**DELETE**: Borra un recurso específicado del servidor. 

**TRACE**: Pide datos al servidor que se le hayan enviado previamente. Se utiliza para depurar y ver la información que añaden algunos servidores intermedios. 

**OPTIONS**: Devuelve los métodos (o verbos)  HTTP que el servidor soporta. 

**CONNECT**: Se utiliza para saber si tenemos acceso al servidor. 

**PATCH**: Realiza la misma función que PUT pero sobreescribe completamente el recurso.