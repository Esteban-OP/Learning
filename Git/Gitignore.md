# Git Ignore

## ¿Que es?

El archivo `.gitignore` sirve para indicarle a Git qué archivos o carpetas del proyecto no debe rastrear ni subir al repositorio.

## ¿Para qué se utiliza?

- **Mantener el repositorio limpio:** Evita que se suban archivos pesados, temporales o generados automáticamente.
- **Proteger información sensible:** Impide compartir contraseñas, claves privadas, tokens de API o archivos de variables de entorno (como `.env`).
- **Evitar dependencias innecesarias:** Excluye carpetas que se pueden reinstalar fácilmente, como node_modules en JavaScript o entornos virtuales en Python.
- **Ignorar configuraciones locales:** Deja fuera archivos creados por el editor de código o sistema operativo (por ejemplo, .DS_Store en Mac).

> [!TIP]
> Se pueden generar plantillas automáticas y seguras según el lenguaje de programación o framework en plataformas como `gitignore․io`.