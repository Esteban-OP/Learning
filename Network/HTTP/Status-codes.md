# Codigos de Estado

Los códigos de estado HTTP son respuestas estandarizadas que el servidor devuelve al cliente para indicarle el resultado de la petición. Se dividen en cinco familias principales según su primer dígito (1xx a 5xx).

> [!NOTE]
> Para el desarrollo de `APIs`, las familias 2xx (Éxito), 4xx (Error del Cliente) y 5xx (Error del Servidor) son las principales por lo que solo se incluyen las mas comunes.

## 2xx: Respuestas Exitosas

Indican que el servidor recibió, entendió y procesó la petición correctamente.

- `200 OK`: La petición se realizó con éxito. Es la respuesta estándar para peticiones `GET` (al devolver datos) y, a menudo, para `PUT` o `PATCH` (al devolver el objeto actualizado).

- `201 Created`: La petición tuvo éxito y como resultado se creó un nuevo recurso. Es la respuesta estándar que debes devolver tras un `POST` exitoso.

- `204 No Content`: La petición se completó con éxito, pero el servidor no tiene información adicional para enviar en el cuerpo (body) de la respuesta. Se utiliza típicamente para respuestas a peticiones `DELETE`.

## 4xx: Errores del Cliente

Indican que hubo un problema con la petición enviada por el cliente (navegador, aplicación o Postman). El servidor no la procesará hasta que el cliente la corrija.

- `400 Bad Request`: La petición está mal formulada. Puede deberse a un JSON mal estructurado en el cuerpo o a parámetros faltantes que el servidor requiere para entender la solicitud.

- `401 Unauthorized`: El cliente debe autenticarse para obtener la respuesta. Ocurre cuando no envías un token de autenticación (como un [JWT](/GeneralKnowledge/JSON/JWT.md)) o el que envías ha expirado.

- `403 Forbidden`: El cliente está autenticado (el servidor sabe quién es), pero no tiene los permisos necesarios para realizar esa acción sobre ese recurso en particular.

- `404 Not Found`: El servidor no puede encontrar el recurso solicitado. Ocurre si la URL del endpoint está mal escrita o si se busca un ID que no existe en la base de datos (ej. GET /api/libros/999 y el libro 999 no existe).

- `422 Unprocessable Entity`: La petición tiene el formato correcto (el JSON es válido), pero contiene errores de validación de negocio. Por ejemplo, enviar un correo electrónico con un formato inválido o un precio negativo.

## 5xx: Errores del Servidor

Indican que el cliente envió una petición válida, pero el servidor falló al intentar procesarla debido a un error interno o de infraestructura.

- `500 Internal Server Error`: Error genérico ("crash" en el backend). Ocurre por una excepción no controlada en el código del servidor, como intentar leer una propiedad de un objeto nulo o un error de sintaxis en el entorno de producción.

- `502 Bad Gateway`: El servidor está actuando como una puerta de enlace (proxy) y recibió una respuesta inválida del servidor que está detrás (por ejemplo, si Nginx no puede comunicarse con tu aplicación Node.js).

- `503 Service Unavailable`: El servidor no está listo para manejar la petición. Generalmente indica que está sobrecargado, en mantenimiento, o que la base de datos está caída.