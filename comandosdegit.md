
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
  
  
