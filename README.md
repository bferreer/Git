Alumna: Betlem Ferrer

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset –-hard HEAD 1
Deshace el último commit y lo que había en la working copy de manera que todo quede como estaba antes. Nuestro staging área queda vacío.
Se modifica el working copy. Se usa para modificaciones experimentales y al final queremos dejarlo tal y como está.


- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
225403c (HEAD -> styled, master) HEAD@{0}: reset: moving to HEAD~1
9bb70f0 HEAD@{1}: commit: Añado formato a git-nuestro versión 2
225403c (HEAD -> styled, master) HEAD@{2}: checkout: moving from master to styled
225403c (HEAD -> styled, master) HEAD@{3}: commit (initial): Añado texto de git-nuestro versión 1

usuario@BETLEM MINGW64 ~/OneDrive/Documentos/Datos/Bootcamp/Git/REpositorio_practica (styled)
$ git reset --hard 9bb70f0
HEAD is now at 9bb70f0 Añado formato a git-nuestro versión 2

Vuelvo al paso 9bb70f0 que es el que había deshecho antes.


- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
Sí, causa un conflicto porque no se puede hacer. No se puede absorber la rama main.
$ git merge main
merge: main - not something we can merge


- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, me causó un conflicto porque no había salido bien el commit de la versión html del fichero git-nuestro.
Lo he solucionado deshaciendo el add y editando el fichero. Diciéndole lo que quería conservar.
He hecho add y commit de nuevo. 

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, no causó conflictos.
He utilizado: git merge styled desde la rama master

- ¿Qué comando o comandos utilizaste en el paso 25?
 git log --pretty=oneline
 git log --graph

 git log --graph
*   commit d4f5bfe5ccc493d647c27b122dc2ed69d6838733 (HEAD -> master, styled)
|\  Merge: 9bb70f0 236be0c
| | Author: Betlem Ferrer <betlem.ferrer@gmail.com>
| | Date:   Tue Jan 28 01:21:16 2025 +0100
| |
| |     Añado versión html de git-nuestro
| |
| * commit 236be0ca73a06f34e37ba852febf1cd16f09e5a6 (htmlify)
| | Author: Betlem Ferrer <betlem.ferrer@gmail.com>
| | Date:   Tue Jan 28 01:04:28 2025 +0100
| |
| |     Añado etiquetas html a git-nuestro versión 3
| |
* | commit 9bb70f082a5c45ec08abaa7ea18cb9a471c3d855
|/  Author: Betlem Ferrer <betlem.ferrer@gmail.com>
|   Date:   Tue Jan 28 00:29:49 2025 +0100
|
|       Añado formato a git-nuestro versión 2
|
* commit 225403c0885aa8f3d3cb4ffd2bb115f32f67dc13
  Author: Betlem Ferrer <betlem.ferrer@gmail.com>
  Date:   Tue Jan 28 00:24:24 2025 +0100

      Añado texto de git-nuestro versión 1



- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

El merge fast-forward consiste en que el puntero de nuestra rama vaya al mismo sitio donde está el puntero que vamos a absorber.
Y el no fast-forward se usa cuando deseas que el historial sea más explícito, mostrando claramente cuando se fusionaron las ramas. 

- ¿Qué comando o comandos utilizaste en el paso 27?
git reset --hard HEAD o bien git merge --abort.
Lo que nos interesa es no perder los cambios del working copy.

- ¿Qué comando o comandos utilizaste en el paso 28?
No entiendo muy bien la pregunta, pero lo que haría es un git restore git-nuestro.mdgit 


- ¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title


- ¿Qué comando o comandos utilizaste en el paso 30?
git checkout -b title d4f6bfe para volver a crear la rama
Y despues el merge otra vez entre master y title. git merge title desde master. 


- ¿Qué comando o comandos usaste en el paso 32?
$ git checkout 225403c
Note: switching to '225403c'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 225403c Añado texto de git-nuestro versión 1


- ¿Qué comando o comandos usaste en el punto 33?

$ git checkout 84b8313
Previous HEAD position was 225403c Añado texto de git-nuestro versión 1
HEAD is now at 84b8313 Añado el fichero freak

