# JWT

Un JSON Web Token (JWT) es un estándar abierto (**RFC 7519**) que permite transmitir información de forma segura entre dos partes como un objeto JSON. Esta información es de confianza porque se encuentra firmada digitalmente y se utiliza principalmente para la autenticación y el control de autorización en aplicaciones web.

## Estructura de un JWT

Un JWT se compone de tres partes separadas por puntos (.), codificadas en Base64Url:
- **Header** (Encabezado): Define el tipo de token (JWT) y el algoritmo de encriptación utilizado para la firma (como HS256 o RS256).
- **Payload** (Carga útil): Contiene las declaraciones o claims (información del usuario, roles, fecha de emisión y tiempo de expiración).
- **Signature** (Firma): Se genera combinando el encabezado, el cuerpo y una clave secreta. Sirve para comprobar que el mensaje no ha sido alterado.

## Para qué sirve
- Autenticación sin estado (Stateless): El servidor no necesita guardar la sesión del usuario en su base de datos. Una vez que el usuario inicia sesión, recibe un JWT que envía en cada petición.
- Propagación de identidad y roles: Permite saber de manera segura quién es el usuario y qué permisos tiene (por ejemplo, si es administrador).
- Inicio de sesión único (SSO): Facilita compartir la autenticación de un usuario entre diferentes dominios o servicios.

## Buenas prácticas de seguridad

- Usar siempre HTTPS: Evita que el token sea interceptado en texto plano durante el viaje.
- Configurar expiración: Asigna un tiempo de vida corto a los tokens para reducir riesgos en caso de robo.
- No guardar datos sensibles: El contenido del Payload se puede decodificar fácilmente, por lo que nunca debes incluir contraseñas