**TECNICAS DE REPRESENTACION DEL CONOCIMIENTO**

🏫Universidad de Huelva
📖Representación del conocimiento
👨‍🎓Pablo Pizarro Sánchez

**¿Qué es una Representación del Conocimiento?**

* Una representación del conocimiento es fundamentalmente un sustituto, un reemplazo de la cosa misma, utilizado para permitir a una entidad determinar consecuencias pensando en lugar de actuar, es decir, razonando sobre el mundo en lugar de actuando en él.
* Es un conjunto de compromisos ontológicos, es decir, una respuesta a la pregunta: ¿en qué términos debo pensar sobre el mundo?
*Es una teoría parcial del razonamiento inteligente, expresada en términos de tres componentes:

        1. la concepción fundamental de la representación del razonamiento inteligente;
        
        2. el conjunto de inferencias que la representación establece; 
        
        3. el conjunto de inferencias que recomienda.
        
* Es un medio para la computación pragmáticamente eficiente, es decir, el entorno computacional en el que se realiza el pensamiento. Una contribución a esta eficiencia pragmática es la que aporta la orientación que proporciona una representación para organizar la información a fin de facilitar la realización de las inferencias recomendadas.
* Es un medio de expresión humana, es decir, una lengua en la que decimos cosas sobre el mundo.

Vamos a explicar las técnicas más comunes en la representación del conocimiento aplicando inteligencia artificial.

**REDES SEMÁNTICAS**

Las redes semánticas son usadas, entre otras cosas, para representar mapas conceptuales y mentales.
Son grafos dirigidos y etiquetados. Se distinguen en ellos:

* Nodo: es el concepto de objeto o conjunto de objetos junto con los valores de sus propiedades.
* Arco: es la relación o asociación entre nodos. Puede ser de varios tipos:     

                1. parte-de : una clase de objetos es una subclase de otra.
                
                2. es-un: un objeto pertenece a una clase de objetos.
                
                3. relación: entre los conceptos asociados
                
Entre las propiedades de las redes semánticas están que tienen una estructura jerárquica, presentan transitividad y no son monótonas.

Ejemplo de red semántica:

![alt text](https://github.com/Pablo942/RC-2020-Pablo-Pizarro-Sanchez/blob/master/Teoria/Captura1.PNG)

Objetivo de la red semántica: 
Su objetivo es desarrollar una estructura para generar datos que se puedan interpretar desde un ordenador. De esta forma pueden ser compartidos y representados por personas y además por herramientas automatizadas.

* VENTAJAS 

Ofrecen una gran potencia, ya que: 

        - Son una forma natural de representació
        - Transmiten de manera bastante transparente
        - Son fácilmente comprensibles. 
        
* DESVENTAJAS 

Contamos con poca flexibilidad.

**LÓGICA**

La lógica consiste en un lenguaje de representación basado en condiciones y reglas. Tiene una sintaxis y una semántica bien definidas, y usa reglas de inferencia.
   
        Los Lunes y Miércoles voy a la casa de Juan para cenar
        Lógica: ∀SX.((es_Lunes(X) V ES_Miercoles(X)) ->
                Cenar(Yo, CasaDe(Juan),X))
                
En cuanto a la sintaxis y la semántica, tenemos ciertas características:

* Sintaxis:
        
        - Reglas para construir oraciones lógicas
        - Simbología que se puede usar
        - Cómo podremos combinar los símbolos
        
* Semántica
        
        - Como interpretamos en la Lógica las oraciones
        - Asignar un significado a cada oración
        
* VENTAJAS
        
        - Los lenguajes de programación están basados en la lógica
        - La lógica ayuda al razonamiento.
        
* DESVENTAJAS
        
        - En ocasiones, poco eficiente.
        
**FRAMES O MARCOS**

Es una técnica de representación muy similar a la utilizada en la programación orientada a objetos. 

* Consta de class frames, similares a las clases, que representan conjuntos de objetos con características similares. Características :
        
        - Conceptos o situaciones genéricas
        - Se describen por un conjunto de propiedades

* A partir de ellas se crean las instance frames que representan elementos concretos de esa clase. Por ejemplo, podríamos tener el marco de clase “Persona” y la instancia “Juan”. Características :
        
        - Objetos concretos o individuos
        - Relacionados con un marco clase
        - Heredan propiedades

* Existe también la posibilidad, a diferencia de en las redes semánticas, de definir lo que se llaman facets sobre estos slots, de forma que se les aporte comportamiento procedural. Por ejemplo, sobre un slot edad podríamos añadir el facet “if-changed”, para comprobar el valor introducido.

Ejemplo de marco:

![alt text](https://github.com/Pablo942/RC-2020-Pablo-Pizarro-Sanchez/blob/master/Teoria/Captura3.PNG)

* VENTAJAS

        - Se accede a los datos facilmente
        - Es intuitivo
        - Ayuda a organización de atributos
        
* DESVENTAJAS

        - Muy generalizados
        
        
**REGLAS**

Esta técnica representa el conocimiento presentando unas premisas o condiciones y las conclusiones o acciones que de ellas se derivan. 

Su representación suele ser usando IF-THEN. 
Las premisas se colocan a continuación del IF en forma normalmente de tripletas Objeto-Atributo-Valor y utilizando operadores booleanos, mientras que las conclusiones definirán nuevos hechos o realizarán acciones. 

Por ejemplo, podríamos tener la siguiente regla para representar que si hay que ir a trabajar y está lloviendo hay que coger el paraguas: 

        IF “es hora de ir a trabajar” AND “está lloviendo” THEN “tengo que coger el paraguas”.

* VENTAJAS DE LAS REGLAS DE PRODUCCION
        
        Permiten representar el conocimiento en forma adecuada para los ordenadores
        Modularizan pedazos de conocimiento
        Permiten el desarrollo incremental
        Las decisiones son entendibles y explicables
        Abren nuevas posibilidades computacionales(paralelismo)
        Permiten interacciones no planeadas y utiles

* DESVENTAJAS DE LAS REGLAS DE PRODUCCION

        No hay fundamento para decidir que problemas tiene solución  
        Escalamiento sin perder entendimiento / eficiencia
        Permiten interacciones no planeadas y no deseadas
        No saben cuando romper sus propias reglas
        No tienen acceso al razonamiento que hay detrás de las reglas
        Inadecuadas para describir conocimiento declarativo
        
**OTRAS TECNICAS**

* Tripletas Objeto-Atributo-Valor: 

Se utilizan para representar hechos acerca de objetos y sus atributos, especificando el valor de un atributo para un determinado objeto. 

Por ejemplo, para representar que el coche es rojo, se tendría una tripleta Coche-Color-Rojo. 

Típicamente estas tripletas se representan en forma de grafos, utilizando una elipse para el objeto, un cuadrado para el valor, y una flecha o arco dirigido entre ambos elementos representando el atributo.

* Lógica difusa 

Representa conocimiento impreciso o ambiguo. 

Ejemplo, la expresión “Juan es viejo”, en comparación con “Juan es joven” o “Juan es de mediana edad”, puede no ser sencilla de representar con otras técnicas, ya que la edad es algo gradual, no se pasa de ser joven un día a ser de mediana edad al siguiente. 

Esta ténica lo que permite es definir funciones de membresía que asignan un valor entre 0 y 1 a cada valor. Así por ejemplo, la función de membresía de edad, asignaría un 1 a joven si la persona tiene 10 años, pero este valor iría decreciendo conforme aumentase la edad hasta llegar a 0, pero teniendo en cuenta que antes de eso se habría ido incrementando el valor de membresía de “mediana edad” e incluso de “viejo”, pudiendo haber edades como los 45, en los que se podría decir que con una persona es joven con un 0.2, vieja con un 0.2 y de mediana edad con un 0.6.


**BIBLIOGRAFÍA**

Para la elaboración de este documento se han utilizado los documentos de las siguientes fuentes:

* https://www.cs.us.es/cursos/ia2-2003/temas/tema-03.pdf
* https://ccc.inaoep.mx/~emorales/Cursos/InteligenciaArtificial/Acetatos/logregrel.pdf
* https://www.dsi.unive.it/~atorsell/AI/mod1-07-knowledge.pdf
* https://www.ecured.cu/T%C3%A9cnicas_de_Representaci%C3%B3n_de_Conocimiento#T.C3.A9cnicas
* http://www.cs.us.es/~fsancho/?e=172
