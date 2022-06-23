# git init
Inicializar el repositorio en la carpeta donde estemos posicionados

# git config --global user.name/email
Configurar quien somos en el repositorio

# git status
Estado del repositorio actual con todos los commit que estan en staging y los untracked files. 

# git rm --cached/force
Remueve el archivo del staging. Básicamente le dice a Git que deje de trackear el historial de cambios de estos archivos,
por lo que pasaran a un estado untracked.
git rm --force: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

# git reset --soft/hard
Devuelve en el tiempo con los cambios todavia en staging para el proximo commit. 
Hard devuelve absolutamente todo y reversa cambios. 

# git rm vs git reset
Git rm lo elimina mas solo tenemos que volver en el tiempo para recuperar el ultimo commit. 
git reset nos ayuda a volver en el tiempo. Pero no como git checkout que nos deja ir, mirar, pasear y volver. Con git reset volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás.

# git reset HEAD
git reset HEAD: Este es el comando para sacar archivos del área de staging. No para borrarlos ni nada de eso,
solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y
los incluyamos de nuevo en staging con git add, por supuesto.
El ultimo commit, es considerado **HEAD**
--------------------------------------------------------------------------------------------------------------------------------------------------
# git add
Pasamos del directorio de trabajo, a la zona de "preparacion" o staging para que sean enviados al repositorio local. 

# git commit
Pasamos de la zona de "preparacion" o staging al repositorio local. 

# git clone *url*
Se trae una copia de los archivos del repositorio remoto al repositorio local y el directorio de trabajo. 

# git push 
Enviamos todo del repositorio local al repositorio remoto. 

# git fetch
Trae documentos del repositorio remoto al local sin crear copias en mi directorio de trabajo. 
con **git merge** combino este documento del repositorio local con mi directorio de trabajo. 

# git merge
Este funciona en la rama donde este, sea la principal o una secundaria. 
Despues de esto, los cambios de las ramas que se mencionen en el commit se combinan junto
A los cambios de la rama actual para formar un archivo unificado. 

# git pull
Combina fetch y merge. 

# branches
Creamos una nueva rama con copias de la rama principal que podemos modificar mas los cambios no estaran reflejados alli. 

# conflictos
Estos ocurren cuando se modifican las mismas lineas de codigo. Cuando esto sucede, se deben de solucionar aceptando
o rechazando cambios al codigo realizados en las otras ramas. 
Despues de hacer esto, el cambio conflictivo sigue en la otra rama a la que se le pidio merge. 

# git pull origin master --allow-unrelated-histories
Esto se debe de hacer cuando en el repositorio existen archivos que no tenemos nosotros.
