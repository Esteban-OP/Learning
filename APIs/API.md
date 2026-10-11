# API

Una API (Interfaz de Programación de Aplicaciones, por sus siglas en inglés) es un conjunto de reglas y protocolos que permite que dos aplicaciones de software se comuniquen entre sí. Funciona como un mensajero que toma una solicitud de un sistema, le dice a otro sistema lo que necesitas y luego te devuelve la respuesta.

![client-server-api](/APIs/images/Client-server-API.jpg)

## Las APIs en el desarrollo Full-Stack

En el mundo del desarrollo moderno, las APIs son el estándar para separar responsabilidades y conectar sistemas de forma segura:

- **Separación de Frontend y Backend:** Una interfaz web o móvil nunca se conecta directamente a una base de datos Oracle o MySQL por razones de seguridad. En su lugar, el frontend envía una petición a un backend (que puedes tener escrito en Node.js, C# o Python). Ese backend expone una API, valida la petición, consulta la base de datos y devuelve la información, casi siempre empaquetada en formato de texto ligero llamado JSON.

- **Comunicación entre Contenedores:** Cuando trabajas con arquitecturas modernas, es común tener múltiples contenedores de Docker ejecutando distintas partes de un proyecto (un servicio de usuarios, otro de inventario). Como están aislados, se comunican entre sí haciendo peticiones a sus respectivas APIs.

- **Consumo de servicios externos:** Si tu proyecto necesita procesar un pago o enviar un correo automático, no programas esos sistemas complejos desde cero. Simplemente consumes la API de empresas como Stripe o SendGrid; les envías los datos necesarios y sus servidores hacen el trabajo pesado.

## Flujo de Petición HTTP a Base de Datos

Paso a paso de la comunicación entre Cliente, API Backend y Base de Datos.

<a href="https://htmlpreview.github.io/?https://github.com/Esteban-OP/Learning/blob/main/APIs/interactive_visual_API.html" target="_blank">Click Aqui</a>