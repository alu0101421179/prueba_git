**Pablo González Martín**

README de prueba

He creado prueba1 desde la rama master, y le he añadido un archivo vacío 1.txt. He hecho commit, y se ha subido todo correctamente al repositorio. Me aparecen ambas ramas, la master sólo con README y prueba1 con README y 1.txt.

Ahora voy a hacer commit deL README modificado, y luego me iré a la rama master y haré git merge prueba1.

Cómo master solo tiene 1 commit y no ha avanzado más desde que cree prueba1, el merge se hará con un Fast Forward, es decir, el puntero de master pasará al commit de prueba1, y ya tendremos en master lo guardado en esa subrama.


CREANDO COMMIT EN MASTER TRAS COMMIT DE SUBRAMA PRUEBA2 PARA VER BIFURCACION

Ahora estoy en subrama prueba2, he creado otro archivo vacío 2.txt, y estoy editando el README. Cuando lo edite, haré un commit desde esta subrama y luego un push. Si yo con la misma me voy a rama master y hago git merge prueba2, pasará lo mismo que antes con prueba1, se hará un merge Fast Forward y simplemente se moverá el puntero de master a este commit, porque master no tiene nuevos commits.

Para probar el otro funcionamiento, haré commit ahora desde prueba2, me iré a master y volveré a añadir una línea al final de este fichero, para que master tenga otro commit nuevo.

Luego haré git merge prueba2, y cuando hagamos git log --graph --all, veremos la bifurcación que se produce para mergear prueba2 al final de mastere, gracias a que master tuvo un commit nuevo antes de mergear prueba2.

