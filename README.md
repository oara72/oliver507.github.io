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
$ echo "# read me" >> README.md
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
el simbolo * no indica en que branch nos encontramos.

ahora enviamos informacion a este nuevo branch para que se genere.

```
$ echo "# pages-gh" >> README.md
$ git add README.md
$ git commit -m "add a new read me"
$ git push origin -u pages-gh
```
Como se puede observar es importante hacer el push correspondiente con el branch donde nos encontramos.

Ahora vamos al web de Git Hub y en settings buscamos branches > default branch y ponemos por default la branch pages-gh.

Ahora en la terminal hacemos switch nuevamente al branch master.

```
$ git checkout master
```
Ahora creamos un archivo index.html lo adicionamos y borramos el readme.md previamente creado. (en el branch master).

```
$ git add index.html
$ git commit -m "add index"
$ git push origin master
```
Por lo general he tenido muchas complicaciones cuando utilizo el comando *$git add .* (el punto indica que es todo) asi que prefiero adicionar y borrar archivos individualmente.

borramos el readme del branch master

```
$git rm README.md
$git push origin master
```
Listo ahora solo tenemos que ir al sitio web de git hub y en settings > options > change theme y apretar el boton para elegir un tema esto genera un archivo en nuetro repositorio llamado _config.yml.

Ahora vamos al link: Your site is published at ```https://[nombre del usuario].github.io/```


###### Referencias:

1. [Como escribir en este archivo .md (markdown) - English](http://daringfireball.net/projects/markdown/syntax#blockquote).
