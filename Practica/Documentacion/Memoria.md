**TECNICAS DE REPRESENTACION DEL CONOCIMIENTO**

🏫Universidad de Huelva 
📖Representación del conocimiento 
👨‍🎓Pablo Pizarro Sánchez

**INTRODUCCIÓN**

En este documento se procede a explicar el desarrollo de la implementación del problema "Escape de Zurg" en Prolog. Para desarrollarlo se ha tomado el código del problema de https://www.metalevel.at/zurg/ de Markus Triska.

**ESCAPE DE ZURG**

Buzz, Woody, Rex y Hamm tienen que escapar de Zurg. Simplemente tienen que cruzar un último puente antes de ser libres. Sin embargo, el puente es frágil y puede contener como máximo dos de ellos al mismo tiempo. Además, para cruzar el puente se necesita una linterna para evitar trampas y piezas rotas. El problema es que nuestros amigos solo tienen una linterna con una batería que dura solo 60 minutos. Los juguetes necesitan diferentes tiempos para cruzar el puente (en cualquier dirección):

    - Buzz  -> 5 minutos
    - Woody -> 10 minutos
    - Rex   -> 20 minutos
    - Ham   -> 25 minutos
    
Como solo puede haber dos juguetes en el puente al mismo tiempo, no pueden cruzar el puente de una vez. Como necesitan la linterna para cruzar el puente, cada vez que dos han cruzado el puente, alguien tiene que regresar y llevar la linterna a los juguetes del otro lado que aún tienen que cruzar el puente. El problema ahora es: ¿en qué orden pueden los cuatro juguetes cruzar el puente a tiempo (es decir, en 60 minutos) para ser salvados de Zurg?


**PREDICADOS QUE SE UTILIZAN**

* select(+Toy1, +Ls0, -Ls1)
Es cierto si Ls1 unifica con una lista que contiene los elementos de Ls0 sin Toy1.
Esta implementación ya existe en Prolog, pero puesto que no se ha usado en clase, se ha visto la necesidad de explicarla, ya que es una de las que se usan en nuestro problema.

Ejemplo1:

    select(1,[1,2,3],R).
    R = [2, 3] ;
    false.
    
Ejemplo2:

     select(1,[1,2,3,1],R).
    R = [2, 3, 1] ;
    R = [1, 2, 3].
