## Pasos a seguir
Primero debemos descargar nuestroproyecto en formato .zip
Instalamos git
```
sudo apt install git
```
Creamos el repositorio en github y generamos un token concediendole permisos
Copiamos el token y lo usaremos para el primer push
Credenciales de git (opcional)
```
git config --global user.name [nombre]
git config --global user.email [email]
git config --global credential.helper store

```
Git init en la carpeta donde queremos crear el repositorio
```
git init
```
Vincular repositorio a github
```
git remote add origin https://github.com/usuario/repositorio.git
```
Preparamos los archivos para el commit
```
git add .
```
Realizamos el commit
```
git commit -m "primer commit"
```
Lo subimos al repositorio en github (Hay que asegurarnos de estar en la rama que queremos pushear) mejor sin el -u
```
git push origin [main] (Puede ser en otra rama)
```
Asegurarnos de que esta actualizada con la remota SIEMPRE antes de hacer cualquier cosa o merges
```
git pull origin main
```
Añadimos ramas
```
git branch nombre-de-la-rama
```
Si queremos crearla y movernos a ella 
```
git checkout -b nombre-de-la-rama (se puede usar switch -c)
```
Y vemos todas las ramas con el comando
```
git branch -r / -a (local y online)
git branch (en la que estamos)
```
Hacemos todos los cambios y creamos todas las ramas que queramos. Luego de eso se vuelven a añadir y se hace el commit en cada una, seguido de un merge a la rama que queramos en el momento necesario.
Fusionar ramas> Primero debemos movernos a la rama ala que mergearemos (no ff para que no se haga fast forward)
```
git checkout rama-base
git merge --no-ff rama-hija
```

## RESUMEN
Una vez creadas nuestras ramas, al hacer modificaciones en alguna rama, demebos mantenernos en la misma y:
```
git status (para ir verificando el estado)
git add [archivo o todo .]
git commit -m "mensaje"

```
Una vez realizado eso nos movemos a la rama a la que queremos mergear esos cambios y siempre un pull para que este actualizada
```
git checkout [rama]
git pull origin [rama]
```
Aqui hacemos el merge y modificamos el mensaje del commit si queremos
```
git merge --no-ff [rama]
```
Podemos ir revisando todas las acciones con el comando:
```
git log --graph --oneline --all --decorate
```
Hacemos el push para que se suban los cambios y un pull opcional para mantener todo actualizado
```
git push origin [rama]
git pull origin [rama]
```
## Otros comandos
Ver estado de repositorio o rama actual
```
git status
```
Ver esquema de logs en git
```
git log --oneline --graph --all
```


Sincronizar main en caso de estar desincronizado
```
git fetch origin
```
Deshacer commit sin perder cambios
```
git reset --soft HEAD~1
```
Deshacer merge 
```
git merge --abort --> sin commit
git reset --hard HEAD~1  --> sin hacer push
git revert -m 1 <hash_del_commit_de_merge>  ->despues de commit y push
```
Eliminar rama local
```
git branch -d nombre-de-la-rama
```
Eliminar rama github
```
git push origin --delete nombre-de-la-rama
```
Para ver diferencias si hay conflictos 
```
git diff
```
