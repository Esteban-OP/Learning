# JSON (JavaScript Object Notation) 

Es un formato de texto ligero y estándar utilizado para estructurar, almacenar y transportar datos. Aunque su sintaxis está inspirada en JavaScript, es completamente independiente del lenguaje; puede ser generado y procesado por prácticamente cualquier lenguaje de programación moderno (Python, Java, C#, PHP, etc.).

## ¿Para qué sirve?

Su función principal es actuar como el puente de comunicación universal entre diferentes sistemas informáticos. En el desarrollo de software, se utiliza principalmente para:

- Comunicación en aplicaciones Fullstack (APIs): Es el formato estándar para enviar información entre el cliente (el frontend o navegador) y el servidor (el backend). Si un usuario llena un formulario en una página web, esos datos se convierten a JSON antes de viajar por internet hacia la base de datos.

- Archivos de configuración: Herramientas de desarrollo, editores de código y frameworks utilizan archivos .json para guardar sus ajustes (por ejemplo, el archivo package.json en proyectos de Node.js).

- Almacenamiento de bases de datos: Las bases de datos NoSQL (como MongoDB) almacenan la información estructurada en documentos que son esencialmente idénticos a JSON.

## ¿Cómo se estructura?

JSON organiza la información utilizando pares de `clave` y `valor`. Las "claves" son siempre cadenas de texto entre comillas, y los "valores" pueden ser textos, números, booleanos (true o false), arreglos (listas) u otros objetos.

Se utilizan llaves `{}` para delimitar un **objeto** y corchetes `[]` para delimitar **listas**.

## ¿Por qué este formato es tan popular?

- Legible por humanos: Al estar basado en texto y usar una estructura limpia, es muy fácil de leer a simple vista sin necesidad de software especial.

- Rápido para las máquinas: Analizar (parsear) un archivo JSON para convertirlo en variables utilizables consume muy pocos recursos computacionales.

- Ligero: Al no tener etiquetas de cierre voluminosas (a diferencia de formatos más antiguos como XML), los archivos pesan menos, lo que hace que las transferencias de red sean más rápidas.