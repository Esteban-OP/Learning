# CI/CD

El CI/CD (`Continuous Integration / Continuous Deployment`) es un conjunto de prácticas y herramientas de automatización que permite a los equipos de desarrollo de software compilar, probar y lanzar actualizaciones de código de forma rápida, frecuente y segura.


## Componentes del CI/CD

- **CI** - Integración Continua (Continuous Integration): Los desarrolladores fusionan su código en un repositorio compartido varias veces al día. Cada cambio activa automáticamente una serie de compilaciones y pruebas unitarias para detectar errores de forma temprana.

- **CD** - Entrega Continua (Continuous Delivery): Tras pasar las pruebas de CI, el código se empaqueta de forma automática y queda listo para ser desplegado en un entorno de pruebas o producción. Requiere una aprobación manual para lanzar los cambios a los usuarios finales.

- **CD** - Despliegue Continuo (Continuous Deployment): Es el siguiente nivel del CD. Una vez que el código supera todas las pruebas automáticas, se envía directamente al entorno de producción sin intervención humana.

## Principales Beneficios

- Detección temprana de errores: Los fallos se encuentran al momento de integrar el código y no cuando el software ya está terminado.
- Mayor velocidad: Permite lanzar nuevas funciones y correcciones a diario o semanalmente, en lugar de cada varios meses.
- Menor riesgo: Al hacer cambios pequeños y constantes, es mucho más fácil identificar y revertir problemas.
- Menos trabajo manual: Se automatizan las tareas repetitivas de compilación, testeo y despliegue, lo que libera tiempo para los programadores.