1. Tienes que modificar la escena 5 de Hamlet en el fichero scene-5.txt. En dicha escena Hamlet encuentra al fantasma de su padre. Añade este texto al fichero:
> Ghost: 
> My hour is almost come,
> When I to sulphurous and tormenting flames
> Must render up myself.
He creado una carpeta en el escritorio, he entrado en ella y he inicializado un repositorio con "git init".
Luego he clonado este repositorio con "git pull git@github.com:IESJacaranda/deshaciendo-cambios-y-gestion-de-ramas-SaludQ.git".
Después he modificado el fichero con "nano scene-5.txt" y he añadido el texto.
2. Añade scene-5.txt al área de preparación.
git add scene-5.txt
3. Haz un commit con los cambios con un buen mensaje de commit.
git commit -m "un buen mensaje de commit"
4. Modifica las palabras del fantasma. Aquí tienes una sugerencia divertida:
> Ghost: 
> My hour is almost come,
> When I to sulphurous and tormenting balloons
> Must render up myself.
con "nano scene-5.txt"
5. Devuelve el fichero al estado del último commit.
git reset --soft 6efbab7
6. Cambia el nombre de LARRY por LAERTES en los ficheros scene-3.txt y scene-7.txt.
nano scene-3.txt y con crtl+w crtl+r
nano scene-7.txt y con crtl+w crtl+r
7. Añade los ficheros al área de preparación usando un único comando git.
git add scene-3.txt scene-7.txt
8. Vamos a cometer un error a propósito. Borra cualquier línea del fichero scene-2.txt.
nano scene-2.txt
9. Añade scene-2.txt al área de preparación.
git add scene-2.txt
10. Comprueba el estado del repositorio. 
git status
11. Devuelve scene-2.txt al directorio de trabajo.
git rm --cached scene-2.txt
12. Haz un commit para guardar los cambios realizados en el nombre de Larry por Laertes.
git commit -m "cambiando LARRY por LAERTES" scene-3.txt scene-7.txt
13. Busca el primer commit que has hecho y vuelve a dicho commit. Indica como has buscado el commit anterior y como has vuelto a él.
git log --oneline
git reset --mixed 6efbab7
14. Crea una nueva rama llamada **reinventando_hamlet**
git branch reinventando_hamlet
15. Cámbiate a dicha rama
git checkout reinventando_hamlet
16. Mejora la escena 2 como creas conveniente.
nano scene-2.txt
17. Haz un commit con los cambios con un mensaje adecuado.
git commit -m "un mensaje adecuado 2"
18. Vuelve a la rama master.
git checkout master
19. Elimina la rama **reinventando_halet**
git branch -d reinventando_hamlet
20. Crea una nueva rama, modifica algo en la rama master, haz commit y llévate los cambios a la rama que has creado.
git branch nueva_rama
nano scene-2.txt
git commit -m "nuevo commit" scene-2.txt
git pull
21. Provoca un conflicto entre la rama master y la rama que has creado (indica lo que has hecho). Une la rama a la rama master resolviendo el conflicto.
nano scene-2.txt (en master)
git checkout rama_nueva
nano scene-2.txt (en rama)
desde la principal, git merge rama_nueva (forzamos lo de la principal)
