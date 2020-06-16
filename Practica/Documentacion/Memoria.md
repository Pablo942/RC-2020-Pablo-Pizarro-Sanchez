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


**SOLUCION EN PROLOG**

Para representar el estado del entorno, utilizamos un término estado de la forma (T, Ls, Rs) , donde:
    
    T: número entero que denota el tiempo empleado hasta ahora.
    Ls: lista de juguetes que se encuentran actualmente en el  lado izquierdo
    Rs: lista de juguetes que están actualmente en el  lado derecho
    
Inicialmente, todos los juguetes estarán en el  lado izquierdo y necesitarán cruzar el puente para llegar al  lado derecho . ç
Tenemos dos estados importantes:

    Estado inicial: (0, [buzz, woody, rex, hamm], []) todos están en el lado izquierdo y nadie en el derecho.
    Estado final: (_, [], _) todos los juguetes están en el lado derecho, y por tanto, ninguno en el lado izquierdo.  
    
El objetivo del problema es obtener una secuencia de movimientos que nos lleven desde estado inicial al estado final.

Para eso tenemos dos tipos de movimientos:

    left_to_right(Toy1, Toy2), que significa que Toy1 y Toy2 se mueven de izquierda a derecha
    right_to_left(Toy), que significa que Toy se mueve de derecha a izquierda
    
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

* moves_(state(+T0, +Ls0, -Rs0)

Es cierto si Rs0 unifica con una lista que contiene los que se encuentran a la derecha del puente.
