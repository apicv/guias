# Guía para git y GitHub

## Enlaces externos sobre git y GitHub

* [git - la guía sencilla](http://rogerdudler.github.io/git-guide/index.es.html)
* [Introduction to GitHub](https://services.github.com/on-demand/intro-to-github/) (en inglés)
* [Hello World](https://guides.github.com/activities/hello-world/) (en inglés) forma parte de [GitHub Guides](https://guides.github.com/)

## Cómo proponer un cambio (*pull request*)
(no es necesario usar git en tu ordenador; todo esto se puede hacer desde la interfaz web de GitHub)

* Necesitas una [cuenta GitHub](https://github.com/join).
* Haz un *fork* del repositorio (de paso, puedes ponerle una estrella y/o vigilar los cambios).
* Una vez tengas tu *fork*, crea un *branch* con un nombre simple y significativo para el cambio que propones.
* Edita directamente los ficheros que consideres necesario para el cambio que propones (tendrás que hacer *commit* por cada fichero que modifiques).
* Ya puedes crear tu [pull request](https://help.github.com/articles/creating-a-pull-request/). Vete a la carpeta raíz del repositorio y te aparecerá el botón verde que propone la comparación+*pull request*.
* Una vez realizada la petición del cambio, sólo te queda esperar a la revisión de los propietarios del repositorio.
* Una vez integrados los cambios, puedes borrar tu *branch*           .

## Cómo sincronizar tu *fork* con el repositorio original (*upstream*)
(es necesario tener instalado git; todas las operaciones se hacen desde consola; suponemos por defecto que sincronizamos la rama *master*)

* Clonar tu *fork* en el disco duro:
```
$ git clone https://github.com/tu_usuario/repositorio.git
```
* Añadir a la lista de repositorios remotos la dirección de *upstream*:
```
$ git remote add upstream https://github.com/usuario_upstream/repositorio.git
```
* Descargar los cambios de *upstream*:
```
$ git fetch upstream
```
* Cambiar a la rama *master* si no estabas ya:
```
$ git checkout master
```
* Aplicar los cambios que vienen de *upstream*:
```
$ git merge upstream/master
```
* Enviar los cambios a tu *fork* en GitHub:
```
$ git push
```
