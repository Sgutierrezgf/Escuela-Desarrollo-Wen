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

Display: Es el tipo de visualizaciopn que tienen los elementos

Tipos de display

    inline: Estos elementos son los que su caja mide exactamente lo mismo que su contenido. Estos elementos los podemos usar en textos y en lugar de que se agreguen en una nueva línea se agregaran justo al ladito del texto. ❗ Tienen como desventaja que no podemos ponerles márgenes ni tampoco podemos cambiar su tamaño.

    block: Estos elementos ocupan toda la pantalla, por lo que si quieres agregar otro elemento, este se agregará automáticamente abajo. No importa que tengas poco contenido, el elemento sí o sí va a ocupar toda la pantalla.

    inline-block: Esto mezcla lo mejor de ambos mundos. Con este display podemos tener tanto los beneficios de inline como de block, es decir, podemos tener elementos que no ocupen todo el ancho de la pantalla, sino que ocupen solamente lo que su contenido ocupa, pero también vamos a poder darle márgenes y podremos cambiar su tamaño 🤠.

Otros tipos de display
    Flexbox
    CSS Grid

Modelo de caja

    Esto es un tema muy mindblow 🤯. Básicamente porque todo en HTML son cajitas, sí, incluso un texto es una caja. Cuando tú insertas un texto, lo que estás haciendo es que estás insertando una cajita que adentro tiene texto (y lo mismo aplica para cualquier etiqueta). Esta cajita tiene un fondo transparente, pero si tú le pones cualquier fondo usando la propiedad background podrás ver esa cajita. Esta cajita, además de su contenido, tiene estas 3 capas externas que serían el padding, el border y el margin 👇:

    padding: Es básicamente el espaciado que hay entre la caja y el contenido de la caja, es un espaciado interno. Lo solemos usar mucho para permitir que los elementos “respiren”

    border: Es el delineado que le podemos dar a una caja, y un borde puede ser tan grueso como quieras. Simplemente debemos ponerle el grosor, el tipo de borde y el color del borde, por ejemplo, podemos hacer una caja con bordes y líneas intermitentes OwO:

    margin: Este es básicamente el espaciado entre elementos. Es la distancia que podemos dejar de un elemento hacia otro.
    
    Con estas capitas podemos conformar el modelo de caja 

Colapso de margenes

    sucede cuando hay 2 elementos bloque adyancentes
    no sucede cuando flexbox, grid y elementos que no sean adyacentes.

Posicionamiento

    El tema de position es muy interesante porque es prácticamente otra forma que tenemos de posicionar con CSS 👀.

    Usualmente es preferible trabajar con nuestras técnicas de alineamiento comunes como CSS Grid o Flexbox, pero suele haber casos donde sí o sí necesitamos usar position.
    
    El ejemplo más común es con el menú de navegación, que casi siempre solemos verlo en todas las páginas. Aunque también podríamos usarlos si queremos posicionar un elemento con base en otro (aquí es donde intervienen el relative con el absolute), y de hecho esta también es una técnica muy usada cuando se dibuja con CSS 7u7.

    tipos de position

        relative
        absolute
        fixed
        sticky
        static
        initial
        inherital

Z-index y el contexto de apilamiento

    Básicamente son capas que hay una encima de la otra, entonces a medida que vas poniendo más y más estas se van apilando.

    Esto sucede cuando empezamos a hacer uso de position y es ahí en donde entra en juego la propiedad z-index, básicamente porque ahora estamos trabajando en el eje Z. El eje Z es el que va desde la pantalla hacia ti

Propiedades y valores de CSS más usados

    https://cssreference.io

Unidades de medida

    absolutas y relativas

Responsive Design

    Que tu sitio se vea bien en varias medidas de pantalla

¿Qué son las arquitecturas CSS? ¿Para qué sirven?

    Sirven para mantener un orden y una coherencia durante todo el proyecto. Tiene los siguientes objetivos:

    Predecibles: escribir reglas claras.
    Reutilizable: no escribir código redundante.
    Mantenible: que sea fácil de leer y adaptable a los estándares.
    Escalable: que pueda crecer fácilmente sin afectar el rendimiento.
    
    Estos objetivos se deben ver reflejadas en buenas practicas que debe conocer todo el equipo involucrado en el proyecto como:

    Establecer reglas
    Explicar la estructura base
    Establecer estándares de codificación
    Evitar largas hojas de estilo
    Documentación

OOCSS, BEM, SMACSS, ITCSS y Atomic Design

    Las siguiente lecturas sirven para profundizar en cada metodología:

    OOCSS(https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/#top)
    BEM(https://en.bem.info/methodology/)
    SMACSS(https://medium.com/@GreenXIII/organize-your-css-smacss-way-89c087db5092)
    ITCSS(https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)
    Atomic Design(https://bradfrost.com/blog/post/atomic-web-design/)
    How to organize your CSS with OOCSS, BEM & SMACSS(https://intelygenz.medium.com/how-to-organize-your-css-with-oocss-bem-smacss-a2317fa083a7)
