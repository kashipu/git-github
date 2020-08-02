Clase #1
* Instalar Git 

Clase #2 
* Editores de Código y archivos de texto plano

Clase #3 
* Introducción a la terminal y línea de comandos

- Muestra el directorio donde estamos: pwd

- Para ir al Home cmd: $ cd / 
- Mostrar todos los archivos incluso los ocultos y los ponga en una lista: $ ls -al
- Devolverme una carpeta: $ cd .. o solo cd 
- Crear una carpeta: $ mkdir <nombre de la carpeta>
- Crear un Archivo: $ touch <nombre y extención del archivo>
- Mostrar contenido de algún archivo: $ cat <nombre del archivo>
- Mostrar historial de comandos de la consola: $ history
- Ir a un comando anterior del historial: $ !72-> <numero del comando en el histoy>
- Borrar un archivo: $ rm <nombre del archivo>

Clase #4 
* Crear un repositorio

- Iniciar git: $ git init
- Añadir al stagign: $ git add <nombre del archivo>
- Añadir al stagign: $ git add . Todos los archivos
- Quitar del stagign: $ git rm --cached <nombre del archivo>
- Crear el primer Commit: $ git commit -m "Mensaje del commit"
- Mover o renombrar un archivo: $ git mv <-f> ... <archivo> <archivo renombrado>
- Mover o renombrar un archivo: $ git mv <-f> ... <archivo> <archivo renombrado> ej ($ git mv -f movimiento.txt test.txt)
- Ver todos los commits: $ git log

Clase #5 
* Volver en el tiempo en nuestro repositorio

- Volver en el tiempo y eliminar todo hasta el commit elegido: $ git reset <numero del commit> --hard
- Volver en el tiempo con git checkout: $ git checkout <numero del commit o tag>
- Volver a los ultimos cambios: $ git checkout master
- Sacar los archivos del Staging: $ Git reset HEAD /o/ $ git restore --staged readme.txt

Clase #6 
* Flujo de trabajo básico con un repositorio remoto

- Algunos comandos utiles 
    * Te muestra el id commit y el título del commit. $ git log --oneline
    * Te muestra donde se encuentra el head point en el log. $ git log --decorate
    * Muestra los cambios brevemente: git log --stat
    * Muestra los cambios en las lineas de los archivos que se hicieron en determinado commit: git log -p-
    * Muestra los cambios que ha realizado determinado usuario: $ git shortlog 
    * Muestra el tag y los mensajes del los commits: git log --graph --oneline --decorate
    * Muestra los commits donde se le han hecho cambios a determinado archivo: $ git log index.html

Clase #7 
* Introducción a las ramas o branches de Git

- Introducción a GNU nano 
- Salir de NANO: F2
- Me muestra en que lugar estoy y que cambios se hicieron: $ git show
- Crear una rama: $ git branch <rama1> o nombre de la rama que queramos Crear
- Moverse a una rama: $ git checkout <nombre de la rama>


Clase #8 
* Uso de GitHub