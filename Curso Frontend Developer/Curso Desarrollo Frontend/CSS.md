Anatomía de una declaración CSS: selectores, propiedades y valores

Selector > Es la etiquea de HTML que vamos a trabajar 
    Ejemplo > h1, div, input, button, entre otras etiquetas

Propiedad > Es el estilo que queremos modificar dentro del selector
    Ejemplo > color, posicion, tamaño, entre otros mas

Valor > Es aquel que se le da a la propiedad, toda propidedad tiene un valor
    Ejemplo color puede ser negro, blanco, gris, narajan.

Estructura de declaracion de CSS

h1 {
    color: white;
}


Tipos de selectores: básicos y combinadores

Basicos

    de tipo: Es la etiqueta que queremos modificar, esto modificada todos los selectores del mismo tipo
        Ejemplo: div {...}
    
    de clase: dentro de la etiqueta podemos poner una clase y se le asigna cualquier valor, ejemplo <h1 class='boton'>, ahora se le antepone un . dentro de la estructura de CSS, esto solo modifica la etiqueta que tenga esa clase.
        Ejemplo: .boton{....}
    
    de ID: Funciona igual que el de tipo clase pero se llama id y se antepone un #
        Ejemplo: #boton{....}
    
    de atributo: Modifica los atributos dentro una etiqueta, ejemplo <a href='....'>, modifca el href de la etiqueta.
        Ejemplo: a[herf='']{....}

    universal: Modifica absolutamente todas la etiquetas y de llama con un *
        Ejemplo: *{....}

Combinadores

    Descendientes: En este selector, el que está más a la izquierda es el selector padre y los que están a su derecha serán los selectores hijos,

    Hijo directo: Este caso es similar al anterior, pero ahora solo agarrará a los hijos que este directamente adentro del padre. Recuerda que en el elemento padre nosotros podemos tener más cajitas con más elementos dentro, en este caso, este selector NO agarrará a esos otros elementos

    Elemento adyacente: Básicamente selecciona a la etiqueta que esté debajo de la primera etiqueta 

    General de hermanos: Es similar al adyacente, pero esta vez no solo selecciona al de abajo, sino a cualquiera que esté al mismo nivel que el selector original, es decir, a sus hermanos

    Ejemplo en selectores-2


Tipos de selectores: pseudoclases y pseudoelementos

    Los selectores de pseudoclase son selectores de CSS precedidos por dos puntos. Probablemente estés muy familiarizado con algunos de ellos. Como flotar:

    En el siguiente enlace estan la diferentes pseudoclases que pueden usar y para que sirven cada una

    https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements



Cascada y especificidad en CSS

    CSS(cascading style sheet)

    Especifidad: La especificidad es la manera mediante la cual los navegadores deciden qué valores de una propiedad CSS son más relevantes para un elemento y, por lo tanto, serán aplicados. La especificidad está basada en las reglas de coincidencia que están compuestas por diferentes tipos de selectores CSS.

    Tipos de selectores

        La siguiente lista de tipos de selectores incrementa en función de la especificidad:

        Selectores de tipo (p.e., h1) y pseudo-elementos (p.e., ::before).

        Selectores de clase (p.e., .example), selectores de atributos (p.e., [type="radio"]) y pseudo-clases (p.e., :hover).

        Selectores de ID (p.e., #example).

        El selector universal (*), los combinadores (+, >, ~, ' ', || (en-US)) y la pseudo-clase de negación (:not()) no tienen efecto sobre la especificidad. (Sin embargo, los selectores declarados dentro de :not() si lo tienen.)

        Para más información, visita "Especificidad" en "Cascada y herencia", 
        también puedes visitar: https://specifishity.com

        Los estilos inline añadidos a un elemento (p.e., style="font-weight:bold") siempre sobrescriben a cualquier estilo escrito en hojas de estilo externas, por lo que se puede decir que tienen la mayor especificidad.



    Algunas reglas de oro:

        Busca siempre una manera de emplear la especificidad antes de considerar el uso de !important.

        Usa !important solo en declaraciones específicas de CSS que sobrescriban CSS externo (de librerías externas como Bootstrap o normalize.css).

        Nunca uses !important cuando estés intentando escribir un plugin/mashup.
        
        Nunca uses !important en todo el código CSS.

    
    En lugar de usar !important, considera:

        Hacer un mejor uso de las propiedades en cascada de CSS.

        Usar reglas más específicas. Indicando uno o más elementos antes del elemento que estás seleccionando, la regla se vuelve más específica y gana mayor prioridad:

            <div id="test">
            <span>Text</span>
            </div>

            div#test span { color: green; }
            div span { color: blue; }
            span { color: red; }

        Como un caso especial sin sentido para (2), duplicar selectores simples para aumentar la especificidad cuando no tiene nada más que especificar

            #myId#myId span { color: yellow; }
            .myClass.myClass span { color: orange; }

Tipos de display más usados: block, inline e inline-block