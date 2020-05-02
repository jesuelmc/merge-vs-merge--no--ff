# GIT MERGE VS GIT MERGE --NO--FF
Al desarrollar con git  es frecuente usar ramas, estas son un conjunto de *commits* ordenados cronológicamente.  
Lo usual es manejar una rama principal a la cual se le denomina **master** y varias ramas de desarrollo .

---
## Git merge
A medida que se va trabajando viene la tarea de unir 2 ramas, de este modo se procede con la fusion o tambien conocido como **merge**. El trabajo de git merge es combinar multiples series de commits para obtener una sola, esto se puede realizar de varias maneras dependiendo a los casos que se tenga en el estado de los commits en las ramas. Aunque al final el resultado a obtener es practicamente el mismo.

Al momento de utilizar  git merge se procede a revisar los commits que encabezan ambas ramas y el commit base que se tiene en commun, de esto los 2 resultdados mas comunes es:  
> Que la rama **B** contenga en su totalidad el contenido de la rama **A** por lo que se opta por el metodo *fast forward*

![ff](https://i.ibb.co/HBzQxnf/ff.png)

> Que la rama **B** no contenga todos los commits pertenecientes a la  rama **A** por lo que procede en modo recursivo o 3 ways
![3w](https://i.ibb.co/HpzS1ZS/3w.png)

## Git merge --no--ff
Es una opcion que se tiene al momento de hacer merge, este viene a ser la confirmacion de que se realice el merge creando un nuevo commit **(NC)**, sin importar que se pueda realizar por el metodo de *fast forward*

![noff](https://i.ibb.co/R9kP0jc/noff.png)

## Concluciones
La opcion `git merge --no--ff` es utilizada para asegurarse que la rama no sufra cambios mediante la creacion de un nuevo commit, de esta manera aseguramos la integridad de la rama en caso de que se vaya ha necesitar en algun futuro. Aunque si es una rama descartable no exite problema si solamente se utiliza un `git merge`