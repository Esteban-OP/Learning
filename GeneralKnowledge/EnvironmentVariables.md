# Variable de Entorno

Una variable de entorno es un par de clave y valor que se guarda fuera del código del programa, directamente en el sistema operativo o en la plataforma donde se ejecuta. Permiten que una aplicación se entere de datos que cambian según el lugar donde corre.

## ¿Para qué sirven?

- **Separar la configuración del código:** Evita poner datos fijos (como la dirección de una base de datos) dentro del programa. Se puede usar una base de datos local cuando se programa en nuestra computadora, y una base de datos en la nube cuando el programa ya está funcionando para los usuarios.
- **Proteger datos sensibles:** Guardan información privada como contraseñas, claves de API (códigos de acceso a servicios) o tokens de seguridad. Así no se suben por accidente a plataformas públicas como GitHub.
- **Adaptarse al sistema:** Informan al programa sobre rutas del equipo, por ejemplo, dónde están los archivos temporales o cuál es el directorio principal del usuario.

## ¿Cómo se utilizan?

- **En desarrollo local:** Se suelen guardar en un archivo de texto llamado `.env` en la raíz del proyecto. Este archivo nunca se debe subir a Git (se añade al archivo `.gitignore`).
- **En producción:** Se configuran directamente en el panel de control del servidor o de la plataforma de despliegue (como Netlify, Heroku o AWS).
- **En el código:** Cada lenguaje de programación tiene una forma de leerlas:
	- **Python:** os.environ.get('NOMBRE_VARIABLE')
	- **Node.js:** process.env.NOMBRE_VARIABLE
	- **Java:** System.getenv("NOMBRE_VARIABLE")

> [!NOTE]
> Al usar **.env\*** en el `.gitingore`, le decimos a Git que ignore cualquier archivo que empiece con `.env` (como `.env.development` o `.env.production`). Así garantizamos que ninguna credencial de base de datos se suba accidentalmente al repositorio, cumpliendo con las buenas prácticas de seguridad.