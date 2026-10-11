# ¿Que es Git?

Git es un sistema de control de versiones.

## Sistemas Centralizados vs Distribuidos

### Sistemas Centralizados (CVCS) 

En un sistema centralizado existe un único servidor central que guarda todo el historial de versiones del proyecto. Aquí es donde los desarrolladores obtienen la última versión del código y guardan cambios (commit). 

- Si el servidor central se cae, nadie puede revisar el historial o hacer commits. 
- La mayoria de operaciones requieren conexión a internet o a la red local. 

### Sistemas Distribuidos (DVCS) 

 En un sistema distribuido como Git o Mercurial cada desarrollador clona el repositorio completo de manera local. Por lo que el desarrollador obtiene todo el historial y archivos, no solo de la version actual. 

- Se pueden hacer commits, crear ramas y revisar el historial de manera offline. 
- Cada clon del repositorio actua como una copia de seguridad del proyecto. 

**Principal diferencia:** El distribuido puede realizar commits de manera local sin necesidad de que exista conexión con el servidor. Cuando el desarrollador quiera compartir sus avances o sincronizar con el equipo ejecuta `git push`. 

