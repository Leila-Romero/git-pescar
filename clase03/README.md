# Clase 03

# GIT MERGE
Para fusionar las ramas tengo que utilizar el comando **git merge**
IMPORTANTE: Tengo que estar en la rama destino de los cambios que quiero traerme
Si quiero fusionar la rama **tarea-footer** en la rama **main** tengo que estar en la rama **main** y ejecutar el comando **git merge tarea-footer**

```sh
git merge <rama-que-quiero-traerme>
git merge tarea footer
```

> Si no estan disponibles los integrantes del equipo que estuvieron trabajando tengo que abortar la fusion.

```sh
git merge --abort
```

## Tipos de fusiones

* Fast-fodward (no hay ningun conflicto, se hace de manera automatica)
* Recursivo (ort-strategy) (No hay ningun conflicto, se hace de manera automatica)
* Manual (Conflictos y vamos a tener que resolverlos manualmente indicandole a git que lo hicimos con un nuevo commit)


## GIT STASH
Permite registrar temporalmente los cambios que aun no fueron comiteados (guardados dentro del repo) (Cambios que estan en el WORKING DIRECTORY o STAGING AREA) guardarlos para dentro de un area temporal paraseguir trabajando luego.
Los stash solo quedan local (estan almacenados dentro de la carpeta .git)


### Crear un stash

```sh
git stash 
```
### Listar los stash

```sh
git stash list
```
### Para recuperar el ultimo stash guardado. No puede recuperar todos los guardados en la lista unicamente el ultimo. Elimina ese stash de la lista.

```sh
git stash pop
```

### Recuperar todos los stash guardados en la lista o el que yo quiera tener. No elimina el stash de la lista.

```sh
git stash apply stash@{1}
git stash apply stash@{2}
git stash apply stash@{3}
```

### Para eliminar un stash 

```sh
git stash drop stash stash@{1}
git stash drop stash stash@{2}
git stash drop stash stash@{3}
```

