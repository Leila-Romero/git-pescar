# Clase 02

## Otras formar de colocar en el staging area los archivos(dividir el codigo de un mismo commit en dos partes)

```sh
git add -p # git add --patch
```

* y: agregar el hunk (trocito de codigo) al stage(staging area)
* s: dividir el hunk en varios (automatico)
* n: descarta ese hunk
* e: editar manualmente el hunk (Tengo que comentar la linea que no quiero que pase al staging area con #)
* ?: ayuda/help

## Clonar el repositorio (completo con la historia de todos los commit)

```sh
git clone ruta/url del repo . #El punto es importante para decirle que no cree una carpeta si no que lo baje en el directorio actual
```