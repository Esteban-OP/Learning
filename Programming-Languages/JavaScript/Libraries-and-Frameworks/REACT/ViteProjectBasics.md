# Crear un proyeccto React con Vite

Abrir la terminal en la carpeta donde se guardara el proyecto y ejecutar:

`npm create vite@latest mi-primer-react -- --template react`

Luego entrar a la carpeta e instalar las dependencias base:

`cd mi-primer-react`

`npm install`

Vite generará automáticamente una estructura. La estructura relevante es esta:

```text
mi-primer-react/
├── index.html           <-- El punto de entrada del navegador
├── package.json         <-- Las dependencias y scripts de tu proyecto
├── src/
│   ├── main.jsx         <-- Monta la aplicación React en el HTML
│   ├── App.jsx          <-- Tu componente principal
│   ├── Greeting.jsx     <-- El nuevo componente que vas a crear
│   └── index.css        <-- Estilos globales (opcional)
```