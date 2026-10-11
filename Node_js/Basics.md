# ¡Que es?

Node.js es un entorno de ejecución de código abierto y multiplataforma que permite ejecutar código JavaScript fuera del navegador (en servidores, ordenadores locales o scripts).

### Características principales

- **No es un lenguaje ni un framework:** Es un entorno que toma el lenguaje JavaScript y le da los recursos necesarios para funcionar en el sistema operativo.
- **Motor V8:** Está construido sobre el motor V8 de Google Chrome, el cual compila JavaScript a código de máquina para ofrecer una alta velocidad de ejecución.
- **Asíncrono y orientado a eventos:** Usa un modelo de entrada/salida (E/S) no bloqueante. Esto significa que puede atender miles de peticiones simultáneas sin que una tarea lenta detenga todo el sistema.
- **NPM (Node Package Manager):** Viene con un gestor de paquetes que incluye el ecosistema de librerías de código abierto más grande del mundo.

### ¿Para qué sirve?

- **Desarrollo Backend:** Crear servidores web y APIs robustas.
- **Aplicaciones en tiempo real:** Ideal para chats, videojuegos o servicios con [WebSockets](../GeneralKnowledge/Websockets.md).
- **Herramientas de línea de comandos (CLI) y automatización:** Para compilar código, ejecutar scripts o gestionar tareas del sistema.

## Inicializar el proyecto Node.js

En la terminal, ejecutar el comando `npm init -y`.

**¿Por qué hacemos esto?**

Node.js es el entorno que permite ejecutar JavaScript en una computadora (fuera del navegador). El comando npm init -y crea un archivo llamado package.json. Este archivo es como el "acta de nacimiento" del backend; allí se registrarán todas las librerías de terceros que instales para que tu proyecto funcione.

## Instalar las dependencias (Librerías)

En ocasiones necesitamos instalar librerias especificas dependiendo de lo que necesitemos en nuestro proyecto.

Ejemplo de comando comun:

`npm install express pg dotenv cors`

**¿Por qué estos paquetes específicos?**

- **express:** Es el marco de trabajo (framework) que facilita enormemente la creación de APIs REST y el manejo de solicitudes HTTP (GET, POST, etc.).

- **pg:** Es el "driver" o conductor que le enseña a Node.js cómo hablar el idioma específico de PostgreSQL.

- **dotenv:** Permite que tu código lea las variables secretas que guardaste en el archivo .env.development.

- **cors:** Es una medida de seguridad. Por defecto, los navegadores bloquean las peticiones que van de un puerto a otro (ej. del frontend en el puerto 5173 al backend en el 3000). CORS le da permiso al frontend para comunicarse con la API.