<!-- Oliver Alexander
Web Developer
January 28th, 2017. -->

# Comenzar un web pages en github

Voy a describir detalladamente cuales fueron los pasos para crear este web de repositorios.

primero comenzar por crear el repositorio, para esto ir al sitio github crear repositorio y copiar el enlace ssh. 

abro la terminal y me dirigo con cd (como en linux) al sitio donde quiero clonar el repositorio.

una vez en la carpeta raiz donde vamos a instalar el repositorio escribimos.

```
$ git clone git@github.com:[nombre-de-usuario]/[nombre-de-usuario].github.io.git
```
Este comando genera o nos trae el repositorio que hemos creado en sitio de github. nos dirigimos con cd dentro de La carpeta la cual está en blanco porque no le hemos dados intrucción de init ni tiene ningun archivo.

ahora empezamos a crear nuestra web con los siguientes comandos.

```
$ git init
$ echo "#read me" >> README.md
$ git add README.md
$ git commit -m "first commit"
$ git push origin -u master
```
Es importante seguir la secuencia de comandos uno por uno para que no tire error. Si revisas el web de github veras que hay un branch llamado master que contiene el archivo README.md

Esta parte es importante pues hemos creado el branch llamado "master" que es el Default para iniciar el repositorio, pero lo que queremos es que cuando nos dirigamos ahi aparezca un index.html que podamos manipular desde nuestra terminal.

los branch son snaptshot o sea una instantanea que define como es el branch por Default y del cual se van a copiar los siguientes branchs que eventualmente generemos.

bien ahora vamos a crear un branch llamado "pages-gh" (indistinto igual se puede llamar carrito).

```
$ git branch pages-gh
$ git fetch
$ git checkout pages-gh
```
El ultimo comando nos hara un switch al branch pages-gh

para verificar que estamos ahi usa el comando.
```
$ git branch 
```
el simbolo * no indica

# Referencias:

1. [Como escribir en este archivo .md (markdown) - English](http://daringfireball.net/projects/markdown/syntax#blockquote).
