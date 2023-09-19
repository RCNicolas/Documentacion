# Git

## Contenido

[Términos importantes](#términos-importantes)

[Flujo de trabajo](#flujo-de-trabajo)

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