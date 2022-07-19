¿Qué es HTML y CSS? ¿Para qué sirven?

HTML --> Lenguaje de marcado de hipertexto
            Codigo que ayuda a estructurar una pagina web(El esqueleto).

CSS --> Hojas de estilo de cascada
            Lenguaje que le da vida al HTML(Colores, tama;os, ubicaciones y mas)

Motores de renderizado
    Pasar archivos a pixeles en pantalla

    El navegador hace 5 pasos

        1. Pasa los archivos a objetos
        2. Calcula el estilo correspondiente a cada nodo DOM
        3. Calcula las dimensiones de cada nodo y donde va en la pantalla
        4. Pinta las diferentes cajas
        5. Toma las capas y los convierte en una imagen para mostrar en pantalla


Anatomía de un documento HTML y sus elementos

¿Qué es una etiqueta? 🤔
Básicamente una etiqueta representa un elemento de nuestro HTML. ¿Recuerdas cuando te dije que trabajar con HTML era decirle al navegador que agregue cualquier cosa que nosotros queramos? Bueno, eso se lo decimos por medio de etiquetas 7u7.
.
Como ya sabes, una etiqueta representa cualquier cosa que nosotros queramos agregar, pero esta etiqueta también puede tener atributos, pero… ¿Qué son los atributos? ¡Inventémonos una etiqueta! La etiqueta michi 👇:

<michi>Retax</michi>

Imagina que nuestra etiqueta inventada es capaz de pintar un michi en nuestra página web, ¡pero un michi puede ser de distintas formas! Por ejemplo, podemos tener michis blancos, negros, con rayitas, grandes, pequeños, tranquilos, etc. Entonces esas características las podríamos definir con los atributos, por ejemplo:

<michi color="blanco" con-rayitas="sí" tamaño="pequeño" posicion="acostado">Retax</michi>

❗ La etiqueta <michi> no existe en HTML, fue usada para fines prácticos, no intente usarla.

En HTML tenemos algunas etiquetas que pueden actuar como cajas, ¡sí!, puedes imaginártelas como cajitas. Entonces ahí dentro podemos meter más etiquetas HTML (y sí, así como las cajas de Amazon, también puedes meter cajas dentro de otras cajas 😏)

Por ejemplo, la etiqueta <section> puede actuar como una caja, ¡pero la etiqueta <ul> también puede actuar como una caja! ¿Por qué tenemos tantas cajas? 🤔 Bueno, es aquí donde entra el HTML semántico, lo cual lo verás en la próxima clase 👀👉

HTML semantico

    La semántica hace referencia al significado de las palabras y al significado de las oraciones, por ejemplo, cuando leemos un texto coherente, que utiliza palabras y oraciones adecuadas y que le dan sentido a lo que leemos.

    De igual forma, HTML nos brinda una serie de etiquetas con mayor significado, para cada parte, sección, o elemento de nuestra página, y que, aunque en la práctica no generen un resultado distinto al de usar una etiqueta <div> como contenedor para todo, pueden darle mayor significado a nuestro código, así como algunas otras ventajas.

    Etiquetas con significado
    ayuda a tu sitio a ser accesible
    mejora tu posicionamiento SEO
    codigo mas claro


Etiquetas de HTML más usadas

ETIQUETAS INICIALES O DE RAÍZ

    <!DOCTYPE html> Indica al navegador que el documento está basado en el estándar HTML5.

    <html> </html> Representa la raíz de un documento HTML. Todos los demás elementos de la estructura HTML deben ser recogidos dentro de estas etiquetas.

METADATOS DEL DOCUMENTO

    <head> </head> Representa una colección de metadatos acerca del documento, incluyendo enlaces a, o definiciones de, scripts y hojas de estilo. El resto de etiquetas de metadatos, irán recogidas dentro de las etiquetas de apertura y cierre del head. Importante explicar que estos metadatos del documento, es información para el navegador y no contenido que será visible en la página web. A excepción de la etiqueta <title> que veremos a continuación.
    <title> </title> Etiqueta usada para definir el título de la página web.
    <link> Se usa para enlazar recursos externos al documento HTML. El ejemplo más común son las hojas de estilos CSS.
    <meta> Etiqueta usada para definir otros metadatos que no se pueden definir con una etiqueta HTML especifica. Por ejemplo para definir el autor del sitio, o la descripción del mismo.
    <style> </style> Etiquetas usadas para introducir código CSS en línea, es decir, en el propio documento HTML.

ETIQUETAS DE SECCIONES O PARA ESTRUCTURAR EL HTML

    <body> </body> Al contrario que la etiqueta de metadatos <head>, todo lo que quieras mostrar en la página web debe ir recogido dentro de las etiquetas de apertura y cierre de <body>. Este contenido será el que se muestre en la web.
    <nav> </nav> Usadas para definir el contenido que será la sección de navegación de la web.
    <main> </main> Se usa para definir el contenido principal del documento. Solamente puede existir uno por documento.
    <section> </section> Define una sección del documento
    <article> </article> Define contenido independiente de la web.
    <aside> </aside> Dentro de estas etiquetas suele alojarse el contenido adicional de la web. Suele ser contenido relacionado con la web pero de poca importancia
    <h1>,<h2>,<h3>,<h4>,<h5>,<h6> Son etiquetas HTML muy importantes, ya que son usadas para jerarquizar el contenido de la web. Las etiquetas se usan para explicar brevemente el contenido que irá a continuación.
    <header> </header> Se usan para definir la cabecera la página web. Suele contener el logotipo, menú de navegación, etc.
    <footer> </footer> Usadas para definir el pie de página.

ETIQUETAS PARA LA AGRUPACIÓN DE CONTENIDO

    <p> </p> Etiqueta usada para escribir párrafos de texto.
    <hr> Etiqueta utilizada para «romper» entre dos secciones de una web. Usada comúnmente como separador.
    <pre> </pre> Usada para pegar texto manteniendo el pre formato propio del texto.
    <blockquote> </blockquote> Se usan para indicar que el contenido es texto citado.
    <ol> </ol> Etiquetas para crear una lista ordenada
    <ul> </ul> Etiquetas para crear una lista des-ordenada
    <li> </li> Etiquetas que recogen el contenido de un elemento de una lista, sea ordenada o no.
    <dl> </dl> Usada para crear una lista de definiciones.
    <dt> </dt> Representa un término definido por la siguiente etiqueta <dd>
    <dd> </dd> Se usa para definir los términos listados antes que él.
    <figure> </figure> Indica una figura ilustrada como parte del documento HTML5.
    <figcaption> </figcaption> Utilizada para definir la leyenda de una figura.
    <div> </div> Etiqueta común utilizada para crear un contenedor genérico.

ETIQUETAS SEMÁNTICAS PARA TEXTO

    <a> </a> Etiqueta utilizada para crear hiperenlaces en el documento HTML
    <strong> </strong> Etiqueta para definir una palabra o conjunto de ellas como importantes. Tiene una fuerte importancia en el SEO de la página.
    <small> </small> Utilizada para dejar un comentario aparte, del tipo una nota de derechos de autoría, u otros textos que no son esenciales para la comprensión del documento.
    <cite> </cite> Para indicar el título de una obra
    <sub> </sub> y <sup> </sup> Etiquetas utilizadas para representar un subíndice o superíndice.
    <mark> </mark> Usada para resaltar texto
    <span> </span> Etiqueta HTML sin ningún significado específico. Se usa conjuntamente con los atributos «class» o «id» para atribuirle ciertas características.
    <br> Etiqueta utilizada para crear un salto de línea

ETIQUETAS PARA INCRUSTAR CONTENIDO

    <img> Etiqueta para «pintar» una imagen en la página web.
    <iframe> </iframe> Es una etiqueta que sirve para anidar otro documento HTML dentro del documento principal.
    <embed> Usada para integrar una aplicación o contenido interactivo externo que no suele ser HTML.
    <object> </object> Utilizada llamar a un recurso externo de la web. Este recurso será tratado como una imagen, o un recurso externo para ser procesado por un plugin.
    <video> </video> Se usa para reproducir video en la página web junto a sus archivos de audio y capciones asociadas.
    <audio> </audio> Usada para cargar en una web un archivo de audio o stream de audio.
    <source> Permite a autores especificar recursos multimedia alternativos para las etiquetas de <video> o <audio>
    <svg> </svg> Se usa para llamar a una imagen vectorizada.
    ETIQUETAS PARA LA CREACIÓN DE TABLAS
    <table> </table> Etiquetas de apertura y cierre de una tabla. El resto de etiquetas de la tabla han de ir siempre recogidas entre estas dos etiquetas.
    <caption> </caption> Usada para indicar el título de la tabla.
    <colgroup> </colgroup> Etiqueta utilizada para agrupar dos o más columnas de una tabla.
    <tbody> </tbody> Usada para describir los datos concretos de una tabla.
    <thead> </thead> Indica el bloque de filas que describen las etiquetas de las columnas de la tabla.
    <tfoot> </tfoot> Indica los bloques de filas que describen los resúmenes, o datos totales de una columna de una tabla.
    <tr> </tr> Se usa para indicar una fila de celdas de una tabla.
    <td> </td> Usada para definir una celda de una tabla.
    <th> </th> Etiqueta que se usa para definir el encabezado de una celda

ETIQUETAS PARA LA CREACIÓN DE FORMULARIOS

    <form> </form> Etiqueta de apertura y cierre de un formulario de una página web. El resto de etiquetas de formulario deben ir siempre recogidas entre estas etiquetas de apertura y cierre de formulario.
    <fieldset> </fieldset> Etiqueta que representa un conjunto o agrupación de elementos de un formulario. «Pinta» un recuadro alrededor de las etiquetas que estén contenidas dentro del <fieldset>
    <legend> </legend> Etiqueta ligada a <fieldset>. Indica el título del <fieldset>
    <label> </label> Se usa para definir el nombre o título de un control del formulario.
    <input> Pinta un campo de introducción de datos para el usuario. Es de las principales etiquetas de un formulario.
    <button> </button> Etiqueta utilizada para representar un botón en el formulario.
    <select> </select> Input que permite una selección entre un conjunto de opciones.
    <option> </option> Etiqueta ligada a <select>. Permite añadir diferentes opciones al <select>
    <textarea> </textarea> Añade un campo al usuario para que pueda introducir texto en unas líneas máximas de texto que el desarrollador puede definir.

Mas informacion sobre las etiquetas

https://htmlreference.io