# Respuesta a las preguntas de la Practica 1 (git)


### Deshacer el ultimo commit (perdiendo cambios en working copy)

`git reset --hard`


### Rehacer el ultimo commit (deshaciendo cambio de la pregunta anterior)

`git reflog`

se consigue entonces el hash de ese commit en particular

`git reset --hard <hash de ultimo commit>`

el proceso se hace todavia mejor si se utilizan tags (particularmente utilizo un sistema de tags v#.#)

y con este sistema, seria tan sencillo como hacer

`git reset --hard <tag de la version>`

### Hacer un merge con rama 'master'

`git merge master`


### Hacer merge de 'htmlify' en 'styled'

Habra conflictos, debido a que README.md es diferente

`git merge htmlify`

Y efectivamente, hay conflictos, se resuelven de acuerdo a como indica el ejercicio


### Merge con 'styled' desde 'master'

    git checkout master
    git merge styled


### Diagrama de git

`git log --graph`


### Merge 'no fast forward' de 'title' en 'master'

`git merge title --no-ff`


### Deshacer merge sin perder cambios en working copy

`git reset`


### Descartar los cambios de la pregunta anterior

`git restore`


### Elminar rama 'title'

`git branch -d title`


### Rehacer merge que se hizo en las preguntas anteriores

En este caso, simplemente se utiza el reflog (como se hizo anteriormente)

`git reflog`

se consigue entonces el hash de ese commit en particular

`git reset --hard <hash>`

el proceso se hace todavia mejor si se utilizan tags (particularmente utilizo un sistema de tags v#.#)


### Volver al commit inicial

Una forma es con `git log --reverse` en la rama principal, pero yo personalmente he utilizalo el tag v0.0

Por tanto, lo hago como `git reset --hard v0.0`


### Volver a cuando se puso titulo al poema

La rama title ahora esta detatched, se puede recuperar la informacion con reflog y buscando cuidadosamente el commit concreto

`git reflog`

se consigue entonces el hash de ese commit en particular

`git reset --hard <hash>`

