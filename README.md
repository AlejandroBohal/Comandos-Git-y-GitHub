# Comandos de Git y GitHub

## Comandos básicos

* **Quitar error de CRLF:** git config core.autocrlf true

* **Ver historial de commits:** git log

* **Configurar nombre de usuario:** git config --global user.name "__El nombre aca__"

* **Configurar email de usuario:** git config --global user.email "__El email aca__"

* **Restaurar la última versión de un archivo:** git checkout -- .

* **Crear repositorio local:** git init

* **Subir al “escenario” todos los archivos:** git add .

* **Tomar una fotografía al “escenario”:** git commit -m “__El mensaje aca__”

* **Crear comando simplificado de git status:** git config --global alias.s "status -s -b"

* **Saber los archivos que han sido modificados:** git status

* **Saber los archivos que han sido modificados de manera simplificada:** git status -s

* **Quitar todos los archivos .xml del "escenario":** git reset *.xml

* **Agregar todos los archivos al "escenario" menos los .xml:**  
git add -A  
git reset *.xml

## Otros comandos importantes

* **Configurar un alias para git log con detalles:** git config --global alias.lg "log --oneline --decorate --all --graph"

* **Comando abreviado de git log con detalles:** git lg

* **Ver los cambios que hubo en los archivos:** git diff

* **Quitar archivos del escenario:** git reset HEAD README.md

* **Deshacer cambios:** git checkout – README.md

* **Cambiar el mensaje del commit:** git commit --amend -m "Nuevo Mensaje"

## Comandos para viajar en el tiempo

* **Devolverse a un commit sin borrar todo:** git reset –mixed __HashDelCommit__

* **Devolverse a un commit borrando todo:** git reset –hard __HashDelCommit__

* **Ver todos los registros hechos en el repositorio:** git reflog

### Modificar archivos mediante git

* **Cambiar el nombre de un archivo:** git mv __nombreAntiguo__ __nombreNuevo__

* **Eliminar un archivo:** git rm __nombreDelArchivo__

Modificar archivos fuera de git:
•	Actualizar y agregar cambios:
git add -u
git add -A
git commit -m “El mensaje aca”

Ramas:
 



Merge/Uniones:
Fast-Forward:
•	Crear nueva rama:
git branch NombreDeLaRama

•	Cambiarse de rama:
git checkout NombreDeLaRama

•	Comparar cambios entre ramas:
git diff Rama1 Rama2

•	Unir una rama con la rama master: (Se debe estar en la rama master)
git merge NombreDeLaRama

•	Eliminar una rama: (Es buena práctica eliminar la rama después de un merge)
git branch -d NombreDeLaRama

Unión automática:
•	Crear y moverse a una nueva rama:
git checkout -b NombreDeLaRama


Tags:
•	Crear nuevo tag:
git tag NombreDelTag
ó   git tag -a TagID -m "Mensaje del Tag"
•	Eliminar un tag:
git tag -d TagID



Stash: Toma algunos archivos y los coloca en un área temporal, que después puedo agregar/quitar de mi proyecto. (Solo se usa en casos de emergencia).
 

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


 
GitHub:
•	Subir todos los tags a Github:
git push –tags

•	Eliminar ramas remotas:
git push origin :rama-a-eliminar

•	Limpiar ramas en Github:
git remote prune origin

