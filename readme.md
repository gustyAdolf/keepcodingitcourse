# Práctica del curso de git, gitHub y SourceTree

## Ejercicio 1

-----
**1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?**

Comando: `git reset --hard HEAD~1`

Se utilizó git reset con la opción --hard dado que queríamos modificar la el working copy, 
y HEAD~1 porque estábamos deshaciendo el último cómmit.

-----
**2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

Comando: `git reset --hard f443915`

Donde *f443915* es el Hash del commit (ID del commit), de esta forma
se modifica el working copy y no quedar detached al hacer reset a un commit anterior.

-----
**3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

No, aunque sean diferentes, las ramas styled se creó a partir de la rama master,
por lo tanto el commit hecho después en la rama styled está por delante del commit
de master, por ello se actualizó master sin problemas.

-----
**4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

Si, esto ocurre porque las ramas *htmlfy* y *styled* apuntan a commits diferentes
donde el commit de htmlfy posee una información diferente a la de styled y en la 
que en los dos commits han modificado los mismos archivos, por ello a la hora de mergear,
git no sabe cuál posee la información correcta y se crea un conflicto donde el usuario
decide la información que se queda.

-----
**5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? **

No, ya que master apunta a un commit que se encuentra por detrás, esto es que
el commit que apunta master es padre, abuelo o bisabuelo del commit que apunta
styled, por ello se sabe que la información del commit que apunta styled es 
más reciente que la de master.

-----
**6. ¿Qué comando o comandos utilizaste en el paso 25? **

Comando: `git log --all --decorate --online -graph`

-----
**7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

Si de hecho sólo hay 1 commit que separa el commit que apunta title
al que apunta master, al hacer no fast forward crearía un nuevo commit, 
esto puede ser interesante para que la rama master que apunta a 
un commit, a la hora de hacer merge de otra rama cree un commit 
y mantenga su padre, es decir, que por ejemplo al hacer git reset HEAD~1 
vuelva al commit anterior. Pero esto pasará de igual forma si 
se hace un merge fast forward, ya que sólo hay 1 commit de separación entre la que 
apunta title a la que apunta master, si hubieran 2, si puede ser más interesante 
hacer no fast forward.
 
-----
**8. ¿Qué comando o comandos utilizaste en el paso 27?**

Comando: `git reset HEAD~1`

-----
**9. ¿Qué comando o comandos utilizaste en el paso 28?**

Comando: `git checkout -- git-nuestro.md` 

*No tengo la versión más reciente de git, y no tengo git restore*

-----
**10. ¿Qué comando o comandos utilizaste en el paso 29?**

Comando: `git branch -D title`

-----
**11. ¿Qué comando o comandos utilizaste en el paso 30?**

Comando: `git reset --hard 14b664a`

Donde *14b664a* es el commit ID.

-----
**12. ¿Qué comando o comandos usaste en el paso 32?**

Comando: `git checkout 7545f61`

Donde *7545f61* es el commitID del primer commit

-----
**13. ¿Qué comando o comandos usaste en el punto 33?**

Comando: `git checkout master`

Dado que la rama master está apuntando al estado final,
con ir a master estaríamos, otra forma sería:
`git checkout <commitID estado final>`.

