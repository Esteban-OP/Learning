# ¿Que son?

Los métodos HTTP son un conjunto de operaciones estándar que indican la acción que un cliente (como un navegador web o una aplicación) desea realizar sobre un recurso en un servidor. En el desarrollo de `APIs REST`, estos métodos se asocian directamente con las operaciones **CRUD** (Create, Read, Update, Delete).

> [!NOTE]
> CRUD son las acciones básicas que se pueden realizar sobre los datos almacenados de forma persistente en un sistema, base de datos o aplicación.

## Métodos HTTP principales

- **GET:** Solicita y obtiene datos de un servidor sin modificar la información.
- **POST:** Envía datos al servidor para crear un nuevo recurso o procesar información.
- **PUT:** Reemplaza por completo un recurso existente con la nueva información enviada.
- **PATCH:** Aplica modificaciones parciales a un recurso sin tener que reescribirlo por completo.
- **DELETE:** Elimina un recurso específico del servidor.


### Otros métodos HTTP

- HEAD: Solicita los mismos encabezados que el método GET, pero sin devolver el cuerpo de la respuesta (útil para verificar si un archivo existe o su tamaño).
- OPTIONS: Describe las opciones de comunicación o qué métodos están permitidos para un recurso específico (muy utilizado con configuraciones de seguridad CORS).
- CONNECT: Establece un túnel hacia el servidor identificado por el recurso.
- TRACE: Realiza una prueba de bucle de retorno para ver qué recibe el servidor a lo largo de la ruta de la petición.

### GET (Leer / Recuperar)

Se usa únicamente para solicitar información de un servidor. No debe alterar el estado de la base de datos (es un método "seguro").

- Petición: GET /api/libros (Obtiene todos los libros)
- Petición: GET /api/libros/123 (Obtiene los detalles del libro con ID 123)
- Cuerpo (Body): No lleva.

### POST (Crear)

Se utiliza para enviar nuevos datos al servidor para crear un recurso subordinado. Si ejecutas la misma petición POST varias veces, crearás múltiples registros.

- Petición: POST /api/libros
- Cuerpo (Body):
```JSON
{
  "titulo": "Cadáver exquisito",
  "autor": "Agustina Bazterrica"
}
```

### PUT (Actualizar / Reemplazar por completo)

Se usa para reemplazar completamente un recurso existente con los datos de la petición. Si el recurso no existe, en algunos diseños de API, PUT puede crearlo. La clave de PUT es la idempotencia: si envías la misma petición 100 veces, el resultado en el servidor será exactamente el mismo que si la envías una vez.

- Petición: PUT /api/libros/123
- Cuerpo (Body): (Debes enviar el objeto completo, incluso lo que no cambió)

```JSON
{
  "id": 123,
  "titulo": "Cadáver exquisito (Edición Especial)",
  "autor": "Agustina Bazterrica"
}
```

### PATCH (Actualización parcial)

A diferencia de PUT, PATCH se utiliza para aplicar modificaciones parciales a un recurso. Solo envías los campos que necesitas cambiar, lo que ahorra ancho de banda y procesamiento.

- Petición: PATCH /api/libros/123
- Cuerpo (Body): (Solo el campo a modificar)

```JSON
{
  "titulo": "Cadáver exquisito (Tapa blanda)"
}
```
### DELETE (Borrar)

Su nombre lo dice todo: solicita al servidor que elimine el recurso especificado. También es un método idempotente; si borras algo y luego intentas borrarlo de nuevo, el estado final (que el recurso ya no exista) sigue siendo el mismo.

- Petición: DELETE /api/libros/123
- Cuerpo (Body): Generalmente no lleva.
