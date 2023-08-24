# Clase 04

# Trabajo colaborativo GIT

## A traves (open source) - Con Pull Request y Fork

## BLAME: sirve para ver quien hizo modificaciones, que hizo, a que hora, etc...

```sh
git blame README.md
git blame <nombre-archivo>
```

## ¿Cual es la diferencia entre fetch y pull?

## FETCH
Me trae la metadata, es decir, me actualiza la informacion dentro de la carpeta .git, pero no aplica los cambios automaticamente. Nos permite ver los cambios que ocurrieron en el remoto y decidir luego que quiero hacer. Si los incorporo todo o parcialmente.

## PULL
Hace primero un fetch y luego trae los cambios automaticamente. Es la combinacion de fetch y pull. Trae la metadata y trae los cambios en las ramas correspondientes. 
 
## GitHub CLI


## GIT CHERRY-PICK


## GIT TAG

```sh
git tag -a v3.0.0 -m "Version 3.0.0" #tag anotado (-a)
```
## Crear un tag en un commit en especifico

```sh
git tag -a v3.0.0 <HASH> -m "Version 3.0.0" #tag anotado (-a)
```

## Listar tags

```sh
git tag
```

## Mostrar informacion del tag

```sh
git show <tag>
git show v3.0.0
```