# Clase 04

# Trabajo colaborativo GIT

## A traves (open source) - Con Pull Request y Fork

1.Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original)

2.Me clono el fork desde mi cuenta github

3.Trabajo normalmente. Subo los cambios (A repo propio)

4.Me voy al proyecto original en el apartado Pull Request. Creo un nuevo Pull Request. Algunas veces aparece en mi repo la posibilidad Pull Request.

## Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.

1.Voy a la cuenta del proyecto original y me copio la url del repositorio

2.Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

```sh
git remote add upstream <url-del-repositorio-original>
```
```sh
git remote -v
```
3.Me traigo los cambios del repositorio original a mi repo local

```sh
git pull upstream main
```
4.Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

```sh
git push
```
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
<https://cli.github.com/>

## GIT CHERRY-PICK

Me permite traerme un commit o conjunto de commit de una rama en particular a otra rama

git cherry-pick Me incluye los commit extremos seleccionados

git cherry-pick ^.. No me incluye los extremos. Los bordes

git cherry-pick ..

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

## Subir todos los tags al repo remoto

```sh
git push --tags
```

## Subir un tag en especifico al repo remoto

```sh
git push origin v0.0.0
git push origin <version-del-tag>
```