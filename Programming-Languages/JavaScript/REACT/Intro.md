# ¿Qué Es React?

React es una biblioteca de JavaScript de código abierto, mantenida principalmente por Meta (anteriormente Facebook) y una vasta comunidad de desarrolladores. A diferencia de un framework completo (como Angular), React hace una sola cosa: construir interfaces de usuario (UI).

El propósito principal de React es hacer que la creación de interfaces interactivas sea un proceso lógico, predecible y altamente eficiente. Lo logra mediante 2 conceptos principales:

- **Arquitectura basada en componentes:** React te permite dividir la interfaz de usuario en piezas independientes y reutilizables llamadas `componentes`. En lugar de construir una página web entera de golpe, construyes pequeños componentes (un botón, una barra de búsqueda, un menú) y los combinas para formar aplicaciones complejas.

- **El DOM Virtual (Virtual DOM):** Modificar lo que el usuario ve en el navegador (el DOM real) es un proceso lento en términos de rendimiento informático. React soluciona esto manteniendo una copia ligera del DOM en la memoria de la computadora. Cuando los datos cambian, React actualiza esta copia primero, calcula matemáticamente las diferencias exactas con la versión anterior, y luego actualiza solamente esas piezas específicas en la pantalla real.