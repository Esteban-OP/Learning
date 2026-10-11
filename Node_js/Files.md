# package.json

Es el corazón de cualquier proyecto moderno de **JavaScript**. Se puede interactuar directamente con este archivo (o mediante comandos que lo modifican).

- **Identidad:** Contiene los metadatos del proyecto (nombre, versión, descripción, autor).

- **Comandos:** Define los scripts que se usaran en la terminal (ej. npm run dev, npm test, npm run build).

- **Dependencias:** Lista las librerías que el proyecto necesita para funcionar (dependencies) y para el desarrollo (devDependencies).

- **Versiones flexibles:** Aquí las versiones de las librerías suelen escribirse con símbolos como ^ o ~ (ej. "express": "^4.17.1"). Esto le dice a npm: "Instala esta versión, pero si hay actualizaciones menores que no rompan el código, instálalas también".

# package-lock.json

- Su **propósito principal** es la reproducibilidad. Si subes tu código a un repositorio y otro desarrollador lo clona, npm leerá el package-lock.json para descargar exactamente el mismo código que tienes tú, byte por byte.

- Este archivo es generado y gestionado automáticamente por npm cada vez que se instala o actualiza un paquete. No se debe editar manualmente.

- **Versiones estáticas:** Mientras que el package.json es flexible, el package-lock.json bloquea las versiones. Guarda el número exacto de la versión instalada (ej. "4.17.3").

- **Árbol profundo:** No solo guarda la versión exacta de las herramientas que se instalaron manualmente, sino también las versiones exactas de las dependencias que usan las dependencias ya instaladas.