# API REST

Una API REST (Representational State Transfer) es el tipo de API más utilizado en el desarrollo web moderno. No es una tecnología en sí, sino una arquitectura o conjunto de reglas sobre cómo se debe diseñar la comunicación.

La regla de oro de REST es que todo gira en torno a recursos. Piensa en un recurso como un sustantivo o una tabla en tu base de datos (por ejemplo: usuarios, productos, pedidos). Para interactuar con estos recursos, REST utiliza los verbos estándar del protocolo HTTP.

![api-rest-model](/APIs/images/rest-api-model.jpg)

## Características Clave de REST

- **No guarda estado (Stateless):** El servidor no recuerda peticiones anteriores. Cada petición (request) que hace el cliente debe contener toda la información necesaria para que el servidor la entienda (por ejemplo, el token de autenticación del usuario). Esto hace que las APIs REST sean muy escalables y fáciles de desplegar en contenedores de Docker.

- **Usa URLs como identificadores:** Cada recurso tiene una dirección única.

- **Se comunica en JSON:** Aunque REST puede devolver datos en texto plano o XML, el estándar actual de la industria es responder con objetos JSON, ya que lenguajes como JavaScript (tanto en el frontend como en Node.js) los procesan de forma nativa e inmediata.

## Los Métodos HTTP (El equivalente al CRUD)

Cuando diseñas un sistema (por ejemplo, con Node.js o Python) y lo conectas a una base de datos (como MySQL u Oracle), utilizas **operaciones CRUD** (Create, Read, Update, Delete). En REST, estas operaciones se mapean directamente a métodos HTTP:

| Método HTTP | Operación CRUD |¿Qué hace? (Ejemplo con /usuarios) | 
| --- | --- | --- |
| GET | Leer (Read) | Obtiene información. GET /usuarios/1 devuelve los datos del usuario 1. No modifica nada en la base de datos. |
| POST | Crear (Create) | Envía datos nuevos. POST /usuarios con un JSON crea un nuevo usuario. |
| PUT | Actualizar (Update) | Reemplaza un recurso por completo. PUT /usuarios/1 sobreescribe toda la información del usuario 1. |
| PATCH | Actualizar parcial | Modifica solo una parte. PATCH /usuarios/1 cambia solo el correo, dejando el resto intacto. | 
| DELETE | Borrar (Delete) | Elimina un recurso. DELETE /usuarios/1 borra al usuario 1 de la base de datos. |