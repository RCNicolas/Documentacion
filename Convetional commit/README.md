# Conventional commit

### Estructura de un conventional commit

Los commits en un proyecto Git pueden seguir convenciones para facilitar la comprensión y el seguimiento del historial. Una convención popular es la de "Conventional Commits", que ayuda a estandarizar los mensajes de commit.

    <tipo>[ámbito opcional]: <descripción>
    
    [cuerpo opcional]
    
    [nota(s) al pie opcional(es)]

## Ámbito

El campo ámbito es opcional y sirve para dar información contextual como por ejemplo indicar el nombre de la feature(Carpeta, archivo o area) a la que afecta el commit.

### Descripción

Breve descripción del cambio cumpliendo lo siguiente:

* usa imperativos, en tiempo presente: “añade” mejor que “añadido” o “añadidos”
* la primera letra siempre irá en minúscula
* no escribir un punto al final

## Cuerpo

Es opcional y debería tener más información que la descripción. Debería usar el mismo tono imperativo que la descripción.

## Nota al pie

Es opcional. Siempre se utiliza para indicar cambios que rompan la compatibilidad de la versión actual (Breaking Changes) aunque también están permitidos otros formatos que sigan la convención de [git trailer format](https://git-scm.com/docs/git-interpret-trailers)

Si el pie de página indica un Breaking Change, el formato deberá ser el siguiente:

`BREAKING CHANGE: <description>`

También se utilizan para etiquetar a los project managers para la revision del mismo

* **Tipos**
  
  ### Conventional commit mas comunes
  
  | fix | Arregla un problema en el Código fuente |
  | --- | --- |
  | feat | Insertar algo nuevo ya sea código fuente o archivos |
  | refactor | - Se ha mejorado el código fuente |
  
  * Se han movido las carpetas
  * Modificación de los comentarios de código fuenteLimpiado, organizado, mejorado || realce | Se ha creado una nueva version del documento “tag” || docs | http://README.md se han realizado cambios en la documentación del repositorio || chore | - Dar formato al código fuente
  * Se ha cambiado la ruta de un fichero o endpoint arreglar formateo del código, actualizar una versión || style | Cambios a la apariencia de la web “archivos html o CSS” || BREAKING CHANGE | Se utiliza en la nota para especificar lo que sucedió en el código, si modificas funciones o Apis los demás commit o desarrolladores les causarán errores por las modificación realizadasNota: es importante si utilizas este tipo es obligatorio colocar el símbolo ! para tener en cuenta este commit. |

### Emojis en Conventional Commits

Los Conventional Commits también pueden incluir emojis para dar un contexto visual rápido sobre el tipo de commit y su propósito. Aquí hay algunos ejemplos de emojis comunes y cuándo se deben usar:

* **Emojis**
  * 🚀 `:rocket:` `feat` Utiliza este emoji para commits que introducen nuevas características emocionantes.
  * 🐛 `:bug:` `fix` Añade este emoji cuando corrijas errores o problemas.
  * 📝 `:memo:` `docs` Úsalo para commits relacionados con cambios en la documentación, como actualizaciones de README o comentarios de código.
  * 🎨 `:art:` `style` Utiliza este emoji para cambios en el formato o estilo del código sin modificar su funcionalidad.
  * ♻️ `:recycle:` `refactor` Usa este emoji para commits que realizan mejoras en el código sin agregar nuevas características ni corregir errores.
  * ✅ `:white_check_mark:` `test` Agrega este emoji para commits relacionados con pruebas y casos de prueba.
  * 🔧 `:wrench:` `chore` Utilízalo para tareas de mantenimiento, actualizaciones de dependencias y cambios menores o actualizar archivos de configuración.
  * 🔥 `:fire:` `remove` Para commits que eliminan código o recursos no utilizados.
  * ⬆️ `:arrow_up:` `upgrade` Úsalo cuando actualices bibliotecas, frameworks o dependencias del proyecto.
  * ⚡ `:zap:` Mejora el rendimiento.
  * 🚑 `:ambulance:` Revisión crítica.
  * ✨ `:sparkles:` Introducir nuevas características.
  * 💄 `:lipstick:` Agregue o actualice la interfaz de usuario y los archivos de estilo.
  * 🎉 `:tada:` Comenzar un proyecto.
  * 🔒 `:lock:` Solucionar problemas de seguridad.
  * 🏷️ `:bookmark:` Etiquetas de lanzamiento / versión
  * 🚨 `:rotating_light:` Corregir advertencias del compilador.
  * 🚧 `:construction:` Trabajo en curso.
  * 🔨 `:hammer:` Agregar o actualizar scripts de desarrollo.
  * ✏️ `:pencil2:` Corregir errores tipográficos.
  * 🚚 `:truck:` Mover o cambiar el nombre de los recursos (archivos, rutas).
  * 💥 `:boom:` Introducir cambios de ultima hora.
  * 💡 `:bulb:` Agregar o actualizar comentarios en el código.
  * 🍻 `:beers:` Escribe código borracho.
  * 💬 `:speech_balloon:` Agregar o actualizar texto y literales.
  * 👥 `:busts_in_silhouette:` Agregar o actualizar colaboradores.
  * 🚸 `:children_crossing:` Mejorar la experiencia de usuario.
  * 📱 `:iphone:` Trabajar en el diseño responsive.
  * ⚗️ `:alembic:` Realizar experimentos.
  * 💫 `:dizzy:` Agregar o actualizar animaciones y transiciones.