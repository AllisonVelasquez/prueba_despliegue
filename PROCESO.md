Primero debemos descargar nuestroproyecto en formato .zip
## Instalamos git
```
sudo apt install git
```
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
Lo subimos al repositorio en github
```
git push -u origin [main] Puede ser en otra rama
```

