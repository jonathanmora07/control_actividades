1. Explica la diferencia entre Git y GitHub
Git es un sistema de control de versiones distribuido que funciona de manera local en tu computadora. Se encarga de rastrear los cambios en los archivos y administrar el historial de versiones de un proyecto.

GitHub es un servicio basado en la nube que aloja repositorios de Git. Facilita la colaboración en equipo, el respaldo en la nube y la gestión de proyectos de software.

2. Explica para qué sirve .gitignore
El archivo .gitignore le especifica a Git qué archivos o carpetas debe ignorar intencionalmente en un proyecto. Esto evita incluir en el control de versiones archivos temporales, credenciales sensibles, configuraciones de entorno local o dependencias descargables.

3. Explica por qué .venv no debe almacenarse normalmente en GitHub
La carpeta .venv contiene el entorno virtual de Python con todos sus paquetes compilados e instalados localmente. No debe subirse a GitHub porque:

Depende de la plataforma: Los binarios instalados pueden no funcionar en otros sistemas operativos o configuraciones.

Peso innecesario: Contiene cientos de archivos y megabytes de dependencias que saturan el repositorio.

Redundancia: En su lugar, se utiliza un archivo requirements.txt para que cualquier colaborador pueda recrear el entorno fácilmente.

4. Explica para qué sirve requirements.txt
requirements.txt es un archivo de texto que enumera todas las librerías externas de Python necesarias para ejecutar un proyecto, junto con sus versiones exactas. Permite a otros desarrolladores (o servidores de despliegue) instalar rápidamente todas las dependencias mediante el comando pip install -r requirements.txt.

5. Explica la diferencia entre Stage, Commit y Push
Stage (Staging Area): Es la etapa donde marcas o seleccionas qué cambios específicos deseas incluir en la próxima versión o "fotografía" del proyecto (git add).

Commit: Es el registro local guardado del estado de tu proyecto en un momento determinado, acompañado de un mensaje descriptivo (git commit -m "...").

Push: Es la acción de enviar tus commits locales al repositorio remoto alojado en GitHub (git push).

6. Explica por qué un repositorio puede tener varios commits antes de realizar un push
Un repositorio puede acumular varios commits locales antes de un push porque los commits representan pequeñas unidades lógicas de trabajo completado localmente. Guardar múltiples commits de manera local te permite:

Trabajar e iterar sin necesidad de conexión a internet.

Mantener un historial detallado y atómico de tus avances antes de hacer públicos o definitivos esos cambios en el servidor remoto.

Comandos Git para registrar el cambio (6º Commit) y subirlo a GitHub
Para agregar estas respuestas a tu archivo, registrar el commit y subirlo, ejecuta los siguientes comandos en tu terminal: 

# 1. Agregar las respuestas al archivo correspondiente (o guarda el archivo manualmente)
# 2. Pasar el archivo a la zona de Stage
git add parte_4/parte_4.md

# 3. Crear el sexto commit con un mensaje descriptivo
git commit -m "docs: responde cuestionario de la parte 4 sobre Git, GitHub y entorno Python"

# 4. Enviar los cambios al repositorio remoto en GitHub
git push origin main

