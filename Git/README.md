# Git

## Contenido

[Términos importantes](#términos-importantes)

[Flujo de trabajo](#flujo-de-trabajo)

[Comandos](#comandos)

[Merge]()

[Cherry pick]()

[Pull Request (PR)]()

[Releases en GitHub]()

* * *

Git es un **Software de control de versiones** que registra los cambio realizados sobre un archivo o conjunto de archivos a lo largo del tiempo.

Permite **gestionar distintas versiones** de un mismo archivo, pudiendo volver a una version anterior o a una mas reciente cuando sea necesario.

## **Términos Importantes**


**Repositorio** Lugar donde guardamos y administramos nuestros archivos

* Locales: Son aquellos que se crean de forma “local” en nuestro PC, y que no necesariamente son compartidos.
* Remotos: Son aquellos que se encuentran alojados en algún servidor externo y que puede ser accedido desde cualquier lugar. Un ejemplo puede ser Git-Hub.

**Ramas** Las ramas pueden ser definidas como “punteros” para cada uno de loa cambios o versiones que queremos armar de un proyecto o desarrollo.

* cada rama representa una Linea independiente de desarrollo.
* Git cuenta con una rama principal master/main de la cual parten todas las demás ramas.

**Commit**: Instantánea de cambios en el tiempo.

**Staging Area**: Área para preparar cambios antes de confirmar.

**Clonar**: Copiar un repositorio remoto localmente.

**Pull**: Obtener cambios del repositorio remoto.

**Push**: Enviar cambios al repositorio remoto.

## Flujo de trabajo

El flujo de *Git*, consta de tres estados locales, es decir en la computadora donde se esta trabajando y uno más de forma remota cuando accedemos al código centralizado en plataformas como GitHub, Gitlab, Bitbucket, etc.

Dichos estados son ***modified***, ***staged***, ***committed*** y ***remote***. A cada uno de ellos le corresponde un área de trabajo:

1. **Working Directory:** Es el área correspondiente al estado **modified** y es la carpeta local de tu computadora donde almacenas los archivos de tu proyecto.
  
2. **Staging Area:** Es el área correspondiente al estado **staged** también se le llama **index** por que es el área donde git indexa y agrega los cambios realizados en los archivos previos a comprometerlos en su registro.
  
3. **Local Repository:** Es el área correspondiente al estado **committed**, donde los cambios ya se han registrado en el repositorio de *git* también se le llama **HEAD** por que indica en qué cambio se encuentra el puntero del repositorio.
  
4. **Remote Repository:** Es el área correspondiente al estado **remote** y es el directorio remoto donde almacenamos los archivos del proyecto en alguna plataforma web como GitHub, GitLab, Bitbucket. Git denomina ***o*rigin** al repositorio remoto.

## Comandos 

### **Comandos básicos de Linux**
  
      # Navegación de directorios
      ls            # Lista los archivos y directorios en el directorio actual
      pwd           # Muestra la ruta completa del directorio actual
      cd <directorio>  # Cambia el directorio actual al directorio especificado
      cd ..         # Retrocede un nivel en la jerarquía de directorios
      
      # Manipulación de archivos y directorios
      touch <archivo>  # Crea un archivo vacío con el nombre especificado
      mkdir <directorio>  # Crea un nuevo directorio
      cp <origen> <destino>  # Copia archivos o directorios
      mv <origen> <destino>  # Mueve o renombra archivos o directorios
      rm <archivo>   # Elimina un archivo
      rm -r <directorio>  # Elimina un directorio y su contenido recursivamente
      
      # Visualización de contenido
      cat <archivo>  # Muestra el contenido completo de un archivo
      more <archivo>  # Muestra el contenido de un archivo página por página
      less <archivo>  # Muestra el contenido de un archivo con navegación interactiva
      head <archivo>  # Muestra las primeras líneas de un archivo
      tail <archivo>  # Muestra las últimas líneas de un archivo
      
      # Edición de archivos de texto
      nano <archivo>  # Abre un editor de texto en la terminal
      vi <archivo>    # Abre el editor de texto Vi en la terminal
      
      # Gestión de procesos
      ps             # Muestra una lista de procesos en ejecución
      top            # Muestra una lista dinámica de procesos y su uso de recursos
      kill <PID>     # Termina un proceso utilizando su ID de proceso (PID)
      
      # Gestión de usuarios y permisos
      who            # Muestra una lista de usuarios conectados
      useradd <nombre-usuario>  # Crea un nuevo usuario
      passwd <nombre-usuario>   # Cambia la contraseña de un usuario
      chmod <permisos> <archivo>  # Cambia los permisos de un archivo o directorio
      
      # Red
      ping <host>    # Prueba la conectividad con un host
      ifconfig       # Muestra información sobre interfaces de red
      ssh <usuario>@<host>  # Inicia una conexión SSH a un host remoto
      
      # Paquetes y actualizaciones
      sudo apt-get update  # Actualiza la lista de paquetes disponibles (en sistemas basados en Debian/Ubuntu)
      sudo apt-get install <paquete>  # Instala un paquete (en sistemas basados en Debian/Ubuntu)
      sudo yum update  # Actualiza los paquetes (en sistemas basados en CentOS/RHEL)
      
      # Ayuda
      man <comando>  # Muestra el manual de un comando específico
      <comando> --help  # Muestra información de ayuda para un comando específico
      
      # Salida de la terminal
      exit           # Cierra la sesión actual de la terminal
  
### **Comandos Git**
  
      # Configuración inicial
      git config --global user.name "Tu Nombre"         # Configura tu nombre de usuario
      git config --global user.email "tu@email.com"    # Configura tu correo electrónico
      
      # Crear y clonar repositorios
      git init                   # Inicializa un nuevo repositorio Git en el directorio actual
      git clone <url>            # Clona un repositorio remoto en tu máquina local
      
      # Trabajo con ramas
      git branch                  # Lista todas las ramas locales
      git branch <nombre-rama>    # Crea una nueva rama
      git checkout <nombre-rama>  # Cambia a una rama específica
      git checkout -b <nombre-rama>  # Crea y cambia a una nueva rama
      git merge <nombre-rama>     # Fusiona una rama en la rama actual
      git branch -d <nombre-rama> # Elimina una rama local
      
      # Trabajo con cambios
      git status                 # Muestra el estado actual de los archivos
      git add <archivo>          # Agrega un archivo al área de preparación (staging)
      git add .                  # Agrega todos los archivos al área de preparación
      git commit -m "Mensaje"    # Crea un nuevo commit con los cambios en el área de preparación
      git reset HEAD <archivo>   # Quita un archivo del área de preparación
      git reset --soft HEAD~1    # Deshace el último commit pero mantiene los cambios
      git reset --hard HEAD~1    # Deshace el último commit y los cambios
      
      # Historial y diferencias
      git log                    # Muestra el historial de commits
      git log --oneline          # Muestra el historial de commits en una línea
      git diff                   # Muestra las diferencias entre el directorio de trabajo y el área de preparación
      git diff <commit1> <commit2>  # Muestra las diferencias entre dos commits
      git blame <archivo>        # Muestra quién modificó cada línea en un archivo
      
      # Repositorios remotos
      git remote -v              # Lista los repositorios remotos configurados
      git remote add <nombre> <url>  # Agrega un repositorio remoto
      git push <nombre-rama> <nombre-rama-remota>  # Sube cambios a un repositorio remoto
      git pull <nombre-rama-remota> <nombre-rama-local>  # Obtiene cambios de un repositorio remoto
      
      # Resolución de conflictos
      git fetch                  # Obtiene cambios del repositorio remoto sin fusionar
      git diff <rama-remota>/<nombre-rama>..<nombre-rama-local>  # Muestra diferencias entre ramas locales y remotas
      git merge <rama-remota>/<nombre-rama>   # Fusiona los cambios remotos en la rama local
      # (Resolución manual de conflictos si es necesario)
      git merge --no-ff <branch> # Este comando fusiona la rama especificada en la rama actual, pero siempre genera una confirmación de fusión (incluso si se trata de una fusión con avance rápido). Esto resulta útil para documentar todas las fusiones que tienen lugar en tu repositorio.
      
      # Etiquetas (tags)
      git tag                    # Lista las etiquetas
      git tag -a <nombre-tag> -m "Mensaje"  # Crea una etiqueta anotada
      git push origin <nombre-tag>  # Sube una etiqueta al repositorio remoto
      
      #-------------------------------------------------------------------------------------------------------------------
      
      # Historia avanzada
      git reflog                  # Muestra un registro detallado de todas las operaciones realizadas en el repositorio
      git log --graph             # Muestra un gráfico de ramas en el historial de commits
      git log --author=<nombre>   # Filtra los commits por autor
      git log --since=<fecha>     # Filtra los commits desde una fecha específica
      git log <archivo>           # Muestra el historial de un archivo específico
      git log -S<string>          # Muestra el historial de cambios que incluyen una cadena específica
      
      # Reescribir la historia
      git rebase <rama>           # Reorganiza los commits de la rama actual sobre la rama especificada
      git commit --amend          # Modifica el commit más reciente
      git rebase -i <commit>      # Interactivo: Reescribe la historia de los commits anteriores
      
      # Submódulos
      git submodule init          # Inicializa submódulos en un repositorio
      git submodule update        # Actualiza los submódulos a la versión especificada
      git submodule foreach       # Ejecuta comandos en cada submódulo
      
      # Refs y etiquetas
      git show-ref                # Muestra referencias (refs) disponibles
      git tag -l "patrón*"        # Lista etiquetas que coinciden con un patrón
      git verify-tag <nombre-tag> # Verifica la firma GPG de una etiqueta
      
      # Stash
      git stash                   # Guarda temporalmente los cambios no comprometidos
      git stash list              # Lista todas las entradas del stash
      git stash apply <stash>     # Aplica un stash específico
      git stash drop <stash>      # Elimina un stash específico
      
      # Búsqueda
      git grep <patrón>           # Busca en los archivos coincidencias con un patrón
      git bisect                  # Ayuda a encontrar el commit que introdujo un problema
      
      # Revertir cambios
      git revert <commit>         # Crea un nuevo commit que deshace los cambios de un commit anterior
      
      # Trabajo colaborativo
      git cherry-pick <commit>    # Aplica los cambios de un commit específico en la rama actual
      git rebase -i <commit>      # Reorganiza y edita commits antes de compartirlos
      git fetch --prune           # Elimina referencias a ramas eliminadas en el repositorio remoto
      
      # Hooks
      # Personaliza el comportamiento de Git utilizando scripts en la carpeta .git/hooks/
  
  | `git init` | Inicializa un nuevo repositorio |
  | --- | --- |
  | `git clone <URL>` | Clona un repositorio remoto. |
  | `git status` | Muestra el estado actual de los archivos. |
  | `git log` | Muestra el historial de commits. |
  | `git add <archivo>` | Agrega cambios al área de preparación. |
  | `git commit -m "Mensaje"` | Guarda los cambios con un mensaje descriptivo. |
  | `git push` | Envía cambios al repositorio remoto. |
  | `git pull` | Obtiene cambios del repositorio remoto. |
  | `git branch` | Crea un rama o muestra las ramas que hay |
  | `git branch -m <name1 name2>` | cambia el nombre de la rama 1 por la rama 2 |
  | `git branch -d <name>` | Elimina la rama |
  | `git checkout <rama>` | Cambia a una rama específica. |
  | `git checkout <name>` | se posiciona en una rama especifica |
  | `git diff <name1 name2>` | conocer diferencias que existen entre dos ramas |
  | `git merge <rama>` | Fusiona una rama con la rama actual. |
  | `git merge <origin destino>` | Carga en la rama destino lo de la rama de origin, debe estar posicionado en la rama a actualizar para hacer el merge |
  | `git commit --amend` | Modificar el commit anterior |
  | `git rebase - HEAD~#` | Modificar varios commit anteriores al ultimo |
  
### **Configurando Git por primera vez**
  
      git --version
      git config --global user.name "Jonathan MirCha"
      git config --global user.email jonmircha@gmail.com
      git config --global user.ui true
      git config --global init.defaultBranch main
      git config --list
      # asignando visual studio code como editor de configuración de git
      git config --global core.editor "code --wait"
      git config --global -e
      # para estandarizar los saltos de línea en windows
      git config --global core.autocrlf true
      # para estandarizar los saltos de línea en linux/mac
      git config --global core.autocrlf input
      # ver todas las opciones de la configuración en la terminal
      git config -h
      # ver todas las opciones de la configuración en el navegador
      git help config
  
 **Inicializar Git en un directorio local**
  
      mkdir carpeta
      cd carpeta
      touch README.md
      touch .gitignore
      git init
      code .
  
### **Flujo de trabajo / Repositorio Remoto**
  
      # agregar los cambios de un archivo al staged
      git add archivo/directorio
      # agregar todos los cambios de todos los archivos al staged
      git add .
      
      # los cambios son comprometidos en el repositorio
      # debes escribir el mensaje del cambio
      # cuando se abra el archivo de configuración
      # al terminar guarda y cierra el archivo
      # para que los cambios tengan efecto
      git commit
      # es un shortcut del comando anterior
      # escribes y confirmas el mensaje del cambio en un sólo paso
      git commit -m "mensaje descriptivo del cambio"
      
      # se agrega el origen remoto de tu repositorio de GitHub
      git remote add origin https://github.com/usuario/repositorio.git
      # la primera vez que vinculamos el repositorio remoto con el local
      git push -u origin master
      # para las subsecuentes actualizaciones, sino cambias de rama
      git push
      
      #para descargar los cambios del repositorio remoto al local
      git pull