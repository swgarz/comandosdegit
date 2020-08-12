
## comando para instalar git en linux
    sudo apt-get install git

## Pasos para iniciar un proyecto y tu primer commit

  git init (repositorio local, laptop)
  
  git add (archivo.txt o punto para agregar todos los archivos)
  
  git commit -m "mensaje para identificar este cambio de otros"
  
  git remote add origin https://github.com/swgarz/nombredetuproyectoengithub.git
  
  git push -u origin master (empujas del repositorio local (laptop) al repositorio remote (github)
  
## Configuracion global de git

  git config --list (muestra toda la configuracion global de git)
  
  git config --global user.name "tu nombre aqui"
  
  git config --global user.email "tu email aqui"

   

## Comandos de git

  git show (todos los cambios historicos hechos, para salir: dos puntos + q + enter)
  
  git log (todos los cambios historicos hechos, para salir: dos puntos + q + enter)
  
  git status (ver el estado en que se encuentra tu stage, se le llama asi cuando se han agregado a la ram (en verde) y esperan ser empujados al repositorio. Aparecerán en rojo si no están agregados al stage)
  
  git push (enviar del repositorio local al repositorio remoto(github))
  
  git pull (si estás trabajando en equipo o iniciaste sesión en algun otro dispositivo y ya te encuentras en tu máquina local, git pull == traer cambios)
  
  git rm --cached (tu archivo.txt) - quita el cambio del stage y ahora con git status lo verás en verde.
  
  git diff (primer commit que se quiere comparar) (segundo commit que se quiere comparar), los commits podemos visualizarlos con git log, diff si utiliza para    comparar cambios. 
  
  git diff -> compara lo del stage y lo untracked, que no se agregó con add.
  
  git reset (commit al que queremos regresar) --hard (este comando nos regresa al commit que queramos pero BORRA TODO, PRECAUCION si es lo que quieres) 'git log para ver los commits a donde queremos regresar'
  
  git checkout (commit) (archivo) -> cambias de rama solo con un achivo especifico, despues git add . y despues commit
  
  git merge (ramasecundaria) -> Tienes que estar en master y hacer git merge para traerte los cambios a master de otra rama (branch) si tienes conflictos los arreglas yendote al editor de texto y seleccionado lo que mejor te convenga, despues haces git add. después git commit y no es necesario hacer git merge de nuevo el merge estará listo.
  
  git log --graph -> te muestra las ramas (branch) graficamente
  
  git log --all --graph --decorate --oneline -> muestra grafica de todos los logs
  
  git show-branch --all-> muestra todas las ramas y hacia donde apuntan
  
  #### los tags son útiles en github para ver versiones y regresar al código
  
  git tag -a (tag que aparecerá en github) -m "mensaje" (hash) -> después hacer un pull y enseguida git push origin master --tags
  
  git tag -d (nombre del tag) -> borrarás el tag
  
  git push origin :refs/tags/nombredetagborradoenlocal -> borra el tag en github
  
  #### crear un alias para no escribir comando tan largo
  alias nombrequequieres = git log --all --graph --decorate --oneline -> podría ser cualquier otro comando
  
  
## generar llaves, pública y privada para conectarse por ssh a github
    ssh-keygen -t rsa -b 4096 -C 
    
   le das enter, despues entender otra vez, hasta que te genere las llaves. Deja las llaves por default en la carpeta de tu usuario y en .ssh
   
   eval $(ssh-agent -s) ->para checar que el proceso de ssh está corriendo
   
   #### agregar email a la carpeta ssh para agregar identidad
   
   ssh-add /home/usuario/.ssh/id_rsa
   
   #### cambiar de https a ssh
   
   git remote -v -> para ver que los dos origins están con https
   
   git remote set-url origin git@github.com:(copialo de clone en tu repositorio)
   
   #### hacer un pull request a un proyecto open source
   
   debes hacer un fork del proyecto en donde quieres contribuir (proyecto open source), ahora realizas tus cambios en tu repositorio, el fork que hiciste, github    entiende que ese proyecto está forkeado asi que una ves que trabajaste en tus cambios, haces commit y lo empujas hacia tu repositorio (add,commit,push) cuando    todo esté listo, harás un pull request desde tu fork, listo! solo debes esperar que lo acepten o algun comentario para feedback del proyecto.
   
