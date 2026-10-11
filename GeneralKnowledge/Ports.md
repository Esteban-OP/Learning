# Listado de puertos comunes

## Puerto 3000

El puerto 3000 es un puerto de red que se utiliza de forma predeterminada para el desarrollo de aplicaciones web locales, especialmente en entornos con Node.js, React, Next.js y servidores Express.

### ¿Para qué sirve?

- **Desarrollo local:** Los programadores lo usan para probar sus sitios web o aplicaciones en su propia computadora (`localhost:3000`) antes de subirlos a internet.
- **Evitar conflictos:** Se eligió este número porque rara vez interfiere con los servicios estándar del sistema operativo.

### Problemas comunes y soluciones

- **Puerto ya ocupado ("Port already in use"):** Ocurre cuando intentas iniciar un proyecto y otra aplicación ya está usando el puerto 3000. Se puede solucionar buscando y cerrando el proceso desde la terminal mediante comandos.
- **Seguridad:** No es recomendable dejar el puerto 3000 expuesto directamente a internet en servidores de producción sin medidas de protección adecuadas.