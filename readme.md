#Ejercicio 1 **git, gitHub y Sourcetree**

11 -Deshacer el último commit (perdiendo los cambios realizados en el working copy)
	Aplicamos un git reset --hard HEAD~1 para borrar el contenido del working copy

12 -Rehacer el último commit (el que acabamos de deshacer)
	Aplicamos un git reglog para identificar al commit al que queremos despalzarnos	
	Aplicamos un git chekout <identificador>
	Al recuperar este punto, me ha dado el error de que estaba en deatached HEAD.
	después de un montón de pruebas decido crear una rama styled2, pongo como activa styled y hago un
	merge sobre styled y en el status todo ok y en working copy vueve a aparecer el fichero con los
	cambios realizados.
13 -Hacer un merge con 'master' (styled absorve a master)
	ponemos como rama activa la styled y hacemos un git merge master.
	al aplicar la instrucción nos informa de "Alreadu up-to-date"
19 -Hecemos una verificación de la branch activa, nos situamos en styled como activa
	desde esta rama hacemos un merge y nos salta un conflicto.
	editamos el fichero resultante del merge y borramos las lineas que consideramos y según
	marca el enunciado de este apartado. Hacemosun git add y a continuaciín un commit.
21 -Cambiamos a branch master con git checkout y provocamos un merge fast-forward sin conflicto. 

25 -Dibujar el diagrama
	creamos un alias con git --global config alias.graph "log --graph --decorate --pretty=oneline"

26 -Ejecutamos un git branch para verificar que estamos en la rama master y ejecutamos
	git merge --no-ff title
	No hay conflicto y ejecutamos el git status y procedemos a hacer el add y el commit

27 -Deshacer el merge (sin perder los cambios en el working copy)
	para esta tarea aplicaremos un git reset HEAD~1 y así retrocedemos un commit 
	si hacemos un git status, nos aparece el fichero git-nuestro.md en estado modified

28 -Descartar los cambios
	para descartar los cambios ejecutamos el comando git checkout git-nuestro.md
	verificamos en nuestro working copy el contenido de nuestro fichero y ha desaparecido el título
	que conseguimos a través del merge anterior.

29 -Eliminar la rama title
	Ejecutamos el comando git branch -D title y a continuación consultamos el estado de las branch
	y title ha desaparecido.

30 -Rehacer el merge que hemos deshecho
	En este apartado he tenido mucha dificultad para entender que estaba pasando y porque el 
	git checkout <Id> me ponía siempre en un "detached HEAD" y no conseguia pasar a la branch master.
	voy a investigar más
	Al final en la recuperación de este punto, he decidido crear una branch nueva master2 y recuperar
	el detached en ella, y al final he provocado un merge con la master. Creo que no es la solución
	pero se me termina el tiempo para presentar la práctica y es lo único que he sabido hacer.

32 -Volver al commit inicial cuando se creó el poema
	Llegamos con un git reset <id>
	despues de probar e investigar ha sido lo único que me ha funcionado

33 -Volver al estado final, cuando pusimos titulo al poema

	vovlemos con un git reset al número de identificador.

	 

