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
- Borrar una rama git branch -D <nombre de la rama>
- Crear una rama: $ git branch <rama1> o nombre de la rama que queramos Crear
- Moverse a una rama: $ git checkout <nombre de la rama>


Clase #8 
* Uso de GitHub

- Crear un repositorio en GitHub
- Añadir un origen remoto: $ git remote add origin <link del repositorio en GitHub>
- Enviar todos los cambios al repositorio remoto: git push origin master
- Traer los cambios del origen remoto: git pull origin master
- Fusionar cambios del origen remoto y local: git pull origin master --allow-unrelated-histories

Clase #9 
* Crear llave SSH

- Comando para crear llave: $ ssh-keygen -t rsa -b 4096 -C "correoElectronico"
- Verificar que el servicio de ssh esta corriendo en la máquina: $ eval $(ssh-agent -s)
- Agregar la llave a ese servicio ~
                                -- el simbolo ~ es solo un atajo al home o directorio raíz  
- ssh-add ~/.ssh/id.rsa
- colocar la llave publica en GitHub
- cambiar el origen en git repolocal: $ git remote set-url origin 

clase #10 
*Flujo de trabajo
-Traer ramas: $git pull origin <nombre de rama> 

clase #11
*Git Rebase: reorganizando el trabajo realizado

rebase solo para repos locales

Git stash guardar cambios 
git stash pop para  tomar en cuenta los cambios que he hecho 
git stash drop para no tomar en cuenta los cambios que he hecho 

Git clean 

* Prueba y muestra los archivos que va a borrar
git clean --dry-run 

* git clean -f  
Elimina todo los archivos que no estan trackeados 


* Git Cherry-pick 
TRAE UN COMMIT DE OTRA RAMA 

* GIT AMEND 
* añadir cambios al commit anterior 
    git commit --amend


* Git reset y reflog solo caso de emergencia 

git reflog / muestra todos los heads de algun momento 

encuentras el HEAD@{1} al que quieras volver " git reset --HARD tag del commit"

¿Qué pasa cuando todo se rompe y no sabemos qué está pasando? Con git reset HashDelHEAD nos devolveremos al estado en que el proyecto funcionaba.

git reset --soft HashDelHEAD te mantiene lo que tengas en staging ahí.
git reset --hard HashDelHEAD resetea absolutamente todo incluyendo lo que tengas en staging.
git reset es una mala práctica, no deberías usarlo en ningún momento; debe ser nuestro último recurso.


git grep para buscar palabras repetidas 

git grep <palabra> / encuentra la palabra 
git grep -n <palabra> / encuentra la palabra con la linea donde está
git grep -c <palabra> / cuenta la cantidad de veces que está escrita 

buscar en los commits / git log -S <palabra>

Comandos recursivos 

git shortlog -sn = muestra cuantos commit han hecho cada miembros del equipo.
git shortlog -sn --all = muestra cuantos commit han hecho cada miembros del equipo hasta los que han sido eliminado
git shortlog -sn --all --no-merge = muestra cuantos commit han hecho cada miembros quitando los eliminados sin los merges
git blame ARCHIVO = muestra quien hizo cada cosa linea por linea
git COMANDO --help = muestra como funciona el comando.
git blame ARCHIVO -Llinea_inicial,linea_final= muestra quien hizo cada cosa linea por linea indicándole desde que linea ver ejemplo -L35,50
**git branch -r **= se muestran todas las ramas remotas
git branch -a = se muestran todas las ramas tanto locales como remotas