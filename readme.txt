Clase #1
* Instalar Git 

Clase #2 
* Editores de Código y archivos de texto plano

Clase #3 
* Introducción a la terminal y línea de comandos

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

- Volver en el tiempo y eliminar todo hasta el commit elegido: git reset <numero del commit> --hard
-
