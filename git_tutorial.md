# Tutorial básico de git

## Básicos

**Saber el estado de las cosas**

`git status`

**Saber cuántas ramas hay y en cuál estoy**

`git branch`

## Cambios

**Añadir cambios de archivos modificados**

`git add -p`

**Añadir archivos nuevos**

`git add nombre-del-archivo`

**Grabar en la historia los archivos añadidos con git add**

`git commit -m "mensaje de commit"`

**Deshacer el último commit**

`git reset --soft HEAD~1`

* si no se quieren dejar los cambios de ese commit cambiar `--soft` por `--hard`.
* se puede cambiar el uno por otro número para deshacer más commits.
* `HEAD^` es equivalente a `HEAD~1`.

## Ramas

**Crea una nueva rama**

`git branch nombre-de-la-rama`

**Cambiar de rama**

`git checkout nombre-de-la-rama`

**Unir cambios de la rama mencionada a la rama en la que estamos**

`git merge nombre-de-la-rama-a-unir`

## Repositorios remotos

**Ver la lista de repositorios remotos asociados a este proyecto**

`git remote -v`

**Añadir un nuevo repositorio remoto**

`git remote add nombre-del-demoto url-del-remoto`

* Por ejemplo cuando contribuyes a un proyecto de código abierto es útil añadir un remoto de nombre `upstream` que tenga la URL del repositorio original (del que hiciste fork)

**Crear una imagen de nuestra rama en el repositorio remoto (primer push)**

`git push -u origin nombre-de-la-rama`

**Subir los cambios de la rama actual a su imagen remota**

`git push`

**Bajar cambios del proyecto original**

`git pull upstream master`

* Para esto hay que estar en la rama máster
* si el comando falla quizá sea por que `upstream` no está definido, caso en el cual puedes usar el comando de esta lista para _añadir un nuevo repositorio remoto_ (está más arriba).

## Cosas lindas

**Ver una lista bonita de cambios**

`git log --graph --decorate --oneline  --all para ver una lista de cambios`
