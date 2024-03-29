# Clase 02

## PATCHED: Otras formar de colocar en el staging area los archivos(dividir el codigo de un mismo commit en dos partes)

```sh
git add -p # git add --patch
```

* y: agregar el hunk (trocito de codigo) al stage(staging area)
* s: dividir el hunk en varios (automatico)
* n: descarta ese hunk
* e: editar manualmente el hunk (Tengo que comentar la linea que no quiero que pase al staging area con #)
* ?: ayuda/help

## CLONE: Clonar el repositorio (completo con la historia de todos los commit)

```sh
git clone ruta/url del repo . #El punto es importante para decirle que no cree una carpeta si no que lo baje en el directorio actual
```
## .GITIGNORE: me permite descartar archivos que no quiero que formen parte del repositorio.
Para eso tengo que crear en general un archivo nuevo llamado ".gitignore" y colorcarle el nombre de carpeta y/o archivo que quiero que ignore

## AMEND: Me permite corregir el ultimo commit ya creado o agregarle mas informacion a ese mismo que puse en el codigo y no quiero crear otro commit
```sh
git commit --amend -m "Vuelvo a escribir el commit"
```

## GITKEEP: Me permite seguir carpetas vacias
Git no versiona carpetas. Si yo quisiera que git siga una carpeta tengo que crear un archivo llamado por la comunidad .gitkeep

## REMOTE: Me permite agregar la url del repositorio remoto(github) en el local para luego subir los cambios

```sh
git remote add origin <url-del-repositorio-remoto>
```
> Visualizar si mi repo local tiene remotos
```sh
git remote
git remote -v #para mostrarme mas detalles
```
## COMMIT --AM: Esto me permite realizar un commit, si mi proyecto esta en el repo remoto y no tengo que utilizar git add . ###Solo Sirve si en el git status aparece mi archivo modified:

```sh
git commit -am <mensaje>
git commit -am "Agrego data sobre el git remote"
```
> Luego para llevar este commit al remoto utilizo el push
```sh
git push
```

# GIT BRANCHES (Ramas)

## Crear ramas

```sh
git branch <nombre-rama>
git branch nb
```

## Listar ramas

```sh
git branch
```

## Moverme a una rama (cambiar de rama)

```sh
git switch <nombre-rama>
git switch nb
```

## Para cambiar entre las ultimas 2 ramas

```sh
git switch -
```

## Para traer lo que hay en la rama creada (nb) a la rama principal (main). Tenemos que estar parados en la rama principal a la hora de ejecutar este comando.

```sh
git merge <nombre-rama-a-traer>
git merge nb
```

## Borro una rama que ya no voy a utilizar

```sh
git branch -d <nombre-de-la-rama>
git branch -d nb
git branch -D nb # Si le pongo la "D" mayuscula le estoy diciendo que lo borre porque estoy segura
```

## Creo una rama y me muevo a ella

```sh
git switch -c <nombre-rama>
git switch -c dev
```

## Subir una rama al repo remoto

```sh
git push origin <nombre-rama>
git push origin dev
```

## Para listar las ramas del remoto

```sh
git branch -
```

## Para listar todas las ramas (locales y remotas)

```sh
git branch -a
```

## Para listar las ramas del remoto

```sh
git branch -r
```
