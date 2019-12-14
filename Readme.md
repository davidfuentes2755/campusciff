# DAVID FUENTES FERNANDEZ


## Nos creamos nuestra cuenta en GitHub

![imagen1](https://i.imgur.com/eaLgATW.png)

## CREAMOS EL REPOSITORIO EN NUESTRO GITHUB


![imagen2](https://i.imgur.com/7EaPZv9.png)


## CLONAMOS NUESTRO REPOSITORIO
Iniciamos el repositorio git:
~~~~
git init
~~~~

Clonar nuestro repositorio en local:
~~~~
 git clone https://github.com/davidfuentes2755/campusciff.git
~~~~
![imagen2](https://i.imgur.com/WW7Ittg.png)

## Crear Readme.md y sube el archivo en el repositorio


~~~~
touch readme.md
~~~~
git status
~~~~
git add readme.md
~~~~
git status
~~~~
git commit -m "Commit inicial"
~~~~

![imagen3](https://i.imgur.com/BYr6yrm.png)

Subimos al repositorio:

~~~~
git push origin master
~~~~

![imagen4](https://i.imgur.com/x4xlZvm.png)

## Ignorar archivos(Parte 1)

Crear en el repositorio local un fichero privado.txt

~~~~
touch privado.txt
~~~~

Tambien creamos la carpeta "Privada":

~~~~
mkdir privada
~~~~
![imagen6](https://i.imgur.com/TXyJcnN.png)

Editamos el archivo .gitignore

~~~~
nano .gitignore
~~~~
![imagen7](https://i.imgur.com/OyLVquF.png)
![imagen72](https://i.imgur.com/mQxjFrQ.png)



## Ignorar archivos(Parte 2)

Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git:

~~~~
echo "privado.txt" > .gitignore
~~~~
~~~~
echo "/privada" > .gitignore
~~~~
~~~~
git add .
~~~~
~~~~
git commit -m "añadido fichero .gitignore"
~~~~

![imagen8](https://i.imgur.com/d9HNfDX.png)

## Añadir el fichero txt al repositorio local

~~~~
touch 1.txt
git add .
git commit -m "añadido 1.txt"

~~~~

![imagen9](https://i.imgur.com/PyqnQWY.png)

## Crear tag(etiqueta) V 0.1

~~~~
git tag v0.1
~~~~
![image10](https://i.imgur.com/BzR45bn.png)


## Subir el tag V 0.1, subir los cambios al repositorio remoto

~~~~
git push --tag origin master
~~~~
![imagen11](https://imgur.com/LbVxZRd.png)

## Preguntar los nombres de usuario de GitHub a tus compañeros de clase, buscalos y sígueles.Seguir los repositorios de campusciff del resto de tus compañeros


![imagen12a](https://i.imgur.com/nmDIQBV.png)

![imagen12b](https://i.imgur.com/XFW1lU5.png)

## Añadir una estrella a los repositorios de campusciff del resto de tus compañeros

![imagen13a](https://i.imgur.com/jMRr5RY.png)
![imagen13b](https://i.imgur.com/j6uCNaD.png)

## Crear una tabla en el fichero readme.md con la información de varios de tus compañeros de clase

Nombre | Github
-- | --
Miriam | [enlace de github](http://github.com/MIRIAM-GIT)
Rafael |[enlace de github](http://github.com/RuFFuS4)

## Poner a github.com/ como colaborador de campusciff

Nos situamos en el repositorio campusciff y pulsamos en l pestaña "Settings":

![imagen14](https://i.imgur.com/J9z3A5y.png)
Y lo añadimos pulsando en "ADD COLABORATOR":

![imagen14b](https://i.imgur.com/MFNafOt.png)


# ACTIVIDAD AVANZADA GIT-HUB


## Crear una rama V 0.2
~~~~
git branch v0.2
~~~~


## Posiciona la carpeta de trabajo en esa rama

~~~~
git checkout v0.2
~~~~
![imagen](https://i.imgur.com/NTVYAEY.png)


## Añadir fichero 2.txt a la rama V 0.2
~~~~
touch 2.txt
git add .
git commit -m "añadido 2.txt"
~~~~
![imagen2](https://i.imgur.com/0hon3N8.png)

## Crear rama remota v 0.2

Subir los cambios al repositorio
~~~~
git push origin v0.2
~~~~
![imagen3](https://i.imgur.com/tN30P30.png)

## Merge directo

Posicionarse en la rama master
~~~~
git checkout master
~~~~
Hacer un merge de la rama V 0.2 a la rama master 
~~~~
git merge v0.2 -m "merge v0.2 sin conflictos"
~~~~
![imagen4](https://i.imgur.com/WrNDbLa.png)

## Merge con conflicto(1)

En la rama master poner Hola en el fichero 1.txt y hacer commit
~~~~
git checkout master
echo "Hola" >> 1.txt
git add .
git commit -m "hola en 1.txt"
~~~~
![imagen5](https://i.imgur.com/hm6VJ06.png)

## Merge con conflicto(2)

Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit
~~~~
git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "adios en 1.txt"
~~~~
![imagen6](https://i.imgur.com/6XEJe1W.png)

## Merge con conflicto(3)

Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

~~~~
git checkout master
git merge v0.2
git add .
git commit -m "arreglado merge en 1.txt"
~~~~
![imagen7](https://i.imgur.com/v7iKIOs.png)
![imagen8](https://i.imgur.com/2q4KWW6.png)

## Listado de ramas

Lista las ramas con merge y las ramas sin merge
~~~~
git branch --merged
git branch --no-merged
~~~~
![imagen9](https://i.imgur.com/2q4KWW6.png)

## Arreglar conflicto

Arreglar el conflicto anterior y hacer un commit

~~~~
vim 1.txt
~~~~
![imagen10](https://i.imgur.com/BmjtM54.png)
~~~~
git add .
git commit -m "arreglado merge en 1.txt"
~~~~
![imagen11](https://i.imgur.com/rqjmp1E.png)

## Borrar rama

Crear un tag V0.2

~~~~
git tag v0.2
~~~~
![imagen12](https://i.imgur.com/TDRYiKN.png)
Borra la rama V0.2

~~~~
git branch -d v0.2
~~~~
![imagen13](https://i.imgur.com/ZanOKLz.png)

## Listado de cambios

Listar los distintos commits con sus rams y sus tags

~~~~
git config --global alias.list 'log --oneline --decorate --graph --all'
~~~~
![imagen14](https://i.imgur.com/3MIVkVi.png)
~~~~
git list
~~~~
![imagen15](https://i.imgur.com/96WAoOX.png)