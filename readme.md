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

![alt text](https://github.com/Pablo942/RC-2020-Pablo-Pizarro-Sanchez/blob/master/Captura1.PNG)

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

Esta técnica representa el conocimiento presentando unas premisas o condiciones y las conclusiones o acciones que de ellas se derivan. 

Su representación suele ser usando IF-THEN. 
Las premisas se colocan a continuación del IF en forma normalmente de tripletas Objeto-Atributo-Valor y utilizando operadores booleanos, mientras que las conclusiones definirán nuevos hechos o realizarán acciones. 

Por ejemplo, podríamos tener la siguiente regla para representar que si hay que ir a trabajar y está lloviendo hay que coger el paraguas: 

        IF “es hora de ir a trabajar” AND “está lloviendo” THEN “tengo que coger el paraguas”.
        
Se distinguen en la lógica varios tipos de herencias:

        1. Herencia simple
        2. Herencia con excepciones
        3. Herencia múltiple
        4. Herencia y cambios
        
Herencia simple con excepciones:
        
![alt text](https://github.com/Pablo942/RC-2020-Pablo-Pizarro-Sanchez/blob/master/Captura2.PNG)

* VENTAJAS

        - Es explícita y condensada
        - Reduce el tiempo de búsqueda
        - Ayuda a evitar repeticiones y compartir conocimiento
        
* DESVENTAJAS

        - No se pueden representar negaciones, disyunciones o cuantificación
        - No se pueden incluir conocimientos procedimentales
        - No hay interpretación estándar
        - Posibilidad de inconsistencia
        - Explosión combinatoria
        
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

![alt text](https://github.com/Pablo942/RC-2020-Pablo-Pizarro-Sanchez/blob/master/Captura3.PNG)

* VENTAJAS

        - Se accede a los datos facilmente
        - Es intuitivo
        - Ayuda a organización de atributos
        
* DESVENTAJAS

        - Muy generalizados
        

