# Websockets

Un WebSocket es un protocolo de comunicación que permite crear una conexión bidireccion y persistente (abierta en todo momento) entre un navegador o cliente y un servidor web.

## Cómo funciona y diferencias con HTTP tradicional

- **HTTP Tradicional:** El cliente (el navegador) siempre tiene que iniciar la petición ("pedir" datos) y el servidor responde. Si quieres saber si hay algo nuevo, tienes que preguntar una y otra vez (polling).
- **WebSocket:** La comunicación comienza con una petición HTTP normal para "negociar" la conexión (código 101 Switching Protocols), pero a partir de ese momento la conexión se convierte en un canal abierto (socket).
- **Bidireccional y en tiempo real:** Tanto el cliente como el servidor pueden enviarse mensajes el uno al otro en cualquier instante, sin necesidad de abrir y cerrar conexiones continuamente.

## Características principales

- **Protocolos:** Utiliza las direcciones `ws://` para conexiones sin cifrar y `wss://` para conexiones seguras (similar a http y https).
- **Baja sobrecarga:** Una vez establecida la conexión, los mensajes viajan en tramas (frames) con muy poco peso de encabezados comparado con HTTP.
- **Compatibilidad:** Está soportado por la gran mayoría de navegadores modernos y entornos de backend (Node.js, Python, Go, etc.).

## ¿Para qué se utiliza?

Es la tecnología ideal para aplicaciones que requieren intercambio de información instantáneo:
- Chats en línea y aplicaciones de mensajería (tipo WhatsApp Web).
- Videojuegos multijugador en el navegador.
- Sistemas de notificaciones push en vivo.
- Paneles de control (dashboards) financieros o deportivos que actualizan gráficos al instante sin recargar la página.