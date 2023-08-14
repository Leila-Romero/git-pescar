# Clase 01

## Extensiones Visual studio code 

* Git Lens
* Git Graph
* Material Icon Theme

## Verificar que tengo instalado Git

```sh
git --version #git -v
```

## Configurar el nombre y el mail para poder realizar commits (foto)

```sh
git config --global user.name "Leila Romero"
git config --global user.email "leilaromero1502@gmail.com"
```

## Para abrir el archivo en el navegador de todos los comandos

```sh
git config --help
```

## Para saber si tengo los datos bien cargados anteriores

```sh
git config --global --get-regexp user
```

## Para quitar algun dato cargado

```sh
git config --global --unset user.nombre del dato a borrar(email,name)
```

## Para inicializar un repositorio de git
* Esto me crea el repositorio de git. Se crea una carpeta .git(oculta)

```sh
git init
```

## Para saber el estado de los archivos

```sh
git status
```


## Areas posibles en las que pueden estar los archivos

* Working Directory (Directorio de trabajo) donde se van agredando, borrando archivos durante el desarrollo.

* Staging Area (Area de control de cambios) se agregan los archivos para darle seguimiento y posteriormente sacarles una foto(commit)

* Local Repo (Area de validacion de cambios, donde se registran las modificaciones realizadas) donde van a estar todas las fotos (commit) que vaya sacando.


## Estados de los archivos

* Untracked (Sin seguimiento)=> Archivos que no se agregaron al index/stage y por consecuente no se les da seguimiento.
* Staged => Archivos que fueron agregados al index/stage area y cuyos cambios van a ser incorporados al repositorio.
* Unmodified => Archivos que se encuentran en el repositorio y que no fueron modificados (con respecto al repositorio).
* Modified => Archivos que se encuentran en el repositorio pero difieren con lo que se encuentra actualmente en el directorio de trabajo (Working directory).


## Para pasar un archivo del Working Directory al Staging Srea

```sh
git add nombre-archivo
git add clase.01/README.md
```

## Para pasar del Staging Area al Local Repo

```sh
git commit -m "mensaje descriptivo del contenido del commit"
git commit -m "Esto es mi primer commit!"
```

## Para ver la diferencia entre el Working Directory y el Local Repo al agregar algo cuando ya esta en el Local Repo

```sh
git diff # Para salir del comando si la consola queda bloqueada es presionar la letra "q"
```

## Me devuelve todos los commit que tengo

```sh
git log
git log --oneline # Me devuelve la info mas simplificada de los commit
```