Primero debemos descargar nuestroproyecto en formato .zip
## Instalamos git
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
Lo subimos al repositorio en github (Hay que asegurarnos de estar en la rama que queremos pushear)
```
git push -u origin [main] Puede ser en otra rama
Al hacerlo la primera vez podemos usar -u que le indica que ambos nombres estan vinculados
```
Podemos usar el comando git status para ver el estado
```
git status
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
git branch (* en la que estamos)
```
Fusionar ramas> Primero debemos movernos a la rama ala que mergearemos
```
git checkout rama-base
git merge rama-hija
```
Eliminar rama local
```
git branch -d nombre-de-la-rama
```
Eliminar rama github
```
git push origin --delete nombre-de-la-rama
```
