# Comandos básicos

## Configuración

|                |Comando                          |
|----------------|-------------------------------|
|Verificar versión|`git --version`|
|Saber más sobre un comando específico|`git help "comando"`            |
|Nombre global|`git config --global user.name "Nombre"`|
|Email global|`git config --global user.email "nuestro@email.com"`|
|Ver configuración global|`git config --global -e`|

Al realizar estas configuraciones ya no tendríamos que configurar los usuarios de git cada vez que realicemos **commits** o hagamos **push**.

## Iniciando un proyecto

|                |Comando                          |
|----------------|-------------------------------|
|Inicializar un repositorio|`git init`|

## Verificar estado de los archivos

|                |Comando                          |
|----------------|-------------------------------|
|Verificar cambios que se han realizado|`git status`|
|Ver directamente los archivos que tuvieron cambios|`git status -s`|
|Ver directamente los archivos con cambios junto con la rama actual|`git status -s -b`|

## Agregar o quitar archivos antes del commit

|                |Comando                          |
|----------------|-------------------------------|
|Agregar todos los archivos|`git add .`|
|Agregar todos los archivos que se modificaron|`git add -A`|
|Agregar todos los archivos con cierta extensión en el directorio actual|`git add *.png`|
|Agregar todos los archivos con cierta extensión de **TODO** el proyecto|`git add "*.png"`|
|Agregar todos los archivos|`git add --all`|
|Agregar todos los archivos en una carpeta con cierta extensión|`git add pdfs/*.pdf`|

## Revertir commit

|                |Comando                          |
|----------------|-------------------------------|
|Quitar del stage archivos con cierta extensión|`git reset *.xml`|
|Quitar del stage archivo en específico|`git reset HEAD "archivo"`|
|Quitar del stage archivo que tenía commit|`git reset --soft HEAD^`|

## Revisar cambios que hemos hecho

|                |Comando                          |
|----------------|-------------------------------|
|Ver cambios que se hicieron en los archivos|`git diff`|
|Ver cambios que se hicieron en los archivos incluso estando en el stage|`git diff --staged`|

## Guardar commits

|                |Comando                          |
|----------------|-------------------------------|
|Guardar los cambios|`git commit -m "Mensaje"`|
|Agregar todos los archivos al state y hacer el commit en una línea|`git commit -am "Mensaje"`|

Se recomienda hacer commits específicos, esto permitirá hacer **checkouts** más fácilmente sin necesidad de afectar otras secciones de nuestro código que están bien.

## Modificar commit

|                |Comando                          |
|----------------|-------------------------------|
|Modificar mensaje de commit (sin haber hecho push)|`git commit --amend -m "Mensaje correcto"`|

## Revertir cambios

|                |Comando                          |
|----------------|-------------------------------|
|Regresar los cambios al último commit|`git checkout -- .`|
|Regresar los cambios al último commit de cierto archivo|`git checkout -- "archivo"`|

## Ver historial de commits

|                |Comando                          |
|----------------|-------------------------------|
|Ver commits (orden descendiente)|`git log`|
|Hacer log con hash (id) corto|`git log --oneline`|
|Hacer log con hash (id) corto en forma de listado|`git log --oneline --decorate --all --graph`|

## Crear alias

|                |Comando                          |Ejemplo|
|----------------|-------------------------------|-------------------------------|
|Crear alias|`git config --global alias."alias" "codigo"`|`git config --global alias.lg "log --oneline --decorate --all --graph"`|
|Otro ejemplo|`git config --global alias."alias" "codigo"`|`git config --global alias.s "status -s -b"`|
|Ver alias que hemos creado|`git config --global -e`|Sin ejemplo|
|Ver listado de datos globales y alias|`git config --global -l`|Sin ejemplo|

Estos alias se crean con el fin de simplificar las instrucciones que le damos a Git.

## Errores

|                |Comando                          |
|----------------|-------------------------------|
|Si se presenta problema con el CRLF|`git config core.autocrlf true`|
|Si se presenta problema de warning: LF will be replaced by CRLF|`git config core.autocrlf true`|
