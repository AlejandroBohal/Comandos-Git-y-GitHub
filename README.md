# Comandos de Git y GitHub

## Comandos básicos

* **Quitar error de CRLF:** git config core.autocrlf true

* **Ver historial de commits:** git log

* **Configurar nombre de usuario:** git config --global user.name "_El nombre aca_"

* **Configurar email de usuario:** git config --global user.email "_El email aca_"

* **Restaurar la última versión de un archivo:** git checkout -- .

* **Crear repositorio local:** git init

* **Subir al “escenario” todos los archivos:** git add .

* **Tomar una fotografía al “escenario”:** git commit -m “_El mensaje aca_”

* **Crear comando simplificado de git status:** git config --global alias.s "status -s -b"

* **Saber los archivos que han sido modificados:** git status

* **Saber los archivos que han sido modificados de manera simplificada:** git status -s

* **Quitar todos los archivos .xml del "escenario":** git reset *.xml

* **Agregar todos los archivos al "escenario" menos los .xml:**  
git add -A  
git reset *.xml

* **Otros comandos importantes:** 
![1](https://github.com/sebastianfrasic/Comandos-Git-y-GitHub/blob/master/Imagenes/1.jpg)

* **Configurar un alias para git log con detalles:** git config --global alias.lg "log --oneline --decorate --all --graph"

* **Comando abreviado de git log con detalles:** git lg

* **Ver los cambios que hubo en los archivos:** git diff

* **Quitar archivos del escenario:** git reset HEAD README.md

* **Deshacer cambios:** git checkout – README.md

* **Cambiar el mensaje del commit:** git commit --amend -m "Nuevo Mensaje"

## Comandos para viajar en el tiempo

* **Devolverse a un commit sin borrar todo:** git reset –mixed _HashDelCommit_

* **Devolverse a un commit borrando todo:** git reset –hard _HashDelCommit_

* **Ver todos los registros hechos en el repositorio:** git reflog

### Modificar archivos mediante git

* **Cambiar el nombre de un archivo:** git mv _nombreAntiguo_ _nombreNuevo_

* **Eliminar un archivo:** git rm _nombreDelArchivo_

### Modificar archivos fuera de git

* **Actualizar y agregar cambios:**  
git add -u
git add -A
git commit -m “El mensaje aca”

## Ramas

### Fast-Forward

* **Crear nueva rama:** git branch _NombreDeLaRama_

* **Cambiarse de rama:** git checkout _NombreDeLaRama_

* **Comparar cambios entre ramas:** git diff _Rama1_ _Rama2_

* **Unir una rama con la rama master: (Se debe estar en la rama master)** git merge _NombreDeLaRama_

* **Eliminar una rama: (Es buena práctica eliminar la rama después de un merge)** git branch -d _NombreDeLaRama_

#### Unión automática

* **Crear y moverse a una nueva rama:** git checkout -b _NombreDeLaRama_

#### Ramas con Github

* **Eliminar ramas remotas:** git push origin :_rama-a-eliminar_

* **Limpiar ramas en Github:** git remote prune origin

## Tags

* **Crear nuevo tag:** git tag _NombreDelTag_   ó   git tag -a _TagID_ -m "_Mensaje del Tag_"

* **Eliminar un tag:** git tag -d _TagID_

* **Subir todos los tags a Github:** git push –tags

## Stash: Toma algunos archivos y los coloca en un área temporal, que después puedo agregar/quitar de mi proyecto. (Solo se usa en casos de emergencia)

•	Crear nuevo Stash (Se agrega a la pila de Stashes):
git stash 
•	Eliminar un tag:
git stash list
•	Eliminar último elemento de la pila de Stashes:
git stash pop
•	Eliminar todas las entradas en el Stash:
git stash clear
•	Insertar mensajes en un Stash:
git stash save “Mensaje aca”

 



Rebase:
 


¿Qué hace el Rebase?
 

  
 

•	Unir dos commits:
git rebase -i HEAD~#DeCommitsQueQuieroUnit
Luego, en el editor VI, en lugar de “pick” colocar “s” o “squash”. Y cambiar lo que sea necesario.

•	Cambiar el nombre a un commit:
git rebase -i HEAD~#DeCommitsQueQuieroUnit
Luego, en el editor VI, en lugar de “pick” colocar “r” o “reword”. Y cambiar lo que sea necesario.
