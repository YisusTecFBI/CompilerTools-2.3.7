CompilerTools 2.3.7 - Herramienta de compilador estándar
========================================================
### Introducción
CompilerTools es una herramienta diseñada para el diseño de un compilador básico en Java. Si bien, no es la herramienta ideal para hacer un compilador con gran cantidad de gramáticas y palabras reservadas, es lo suficientemente intuitivo y funcional para introducirnos en el mundo de los compiladores. Cumple con ser lo bastante didáctico para estudiantes y aficionados al mundo de la programación.  

Características clave:
- Implementa un autocompletador de código en un JTextComponent.
- Extrae los bloques de código del lenguaje inventado para su posterior ejecución.
- Cuenta con una clase para la manipulación de archivos, soportando operaciones como Nuevo, Abrir, Guardar y Guardar Como.
- Se pueden crear errores ya sean Léxicos, Sintácticos, Semánticos o Lógicos.
- Tiene diversas funciones automatizadas que realizan algunas operaciones complejas para la programación del compilador.
- Se pueden crear gramáticas mediante la agrupación de Tokens mediante Producciones.
- Implementa un contador de número de línea en un JTextComponent.
- Cuenta con una función para el coloreo de palabras en un JTextComponent.
- Implementa el almacenamiento de tokens y sus atributos básicos, los cuales son lexema, componente léxico, línea y columna.

Explicaré la función principal de cada clase y cada uno de sus métodos. De igual forma dejaré un [videotutorial](https://www.youtube.com) en el cual explicó mas a detalle el funcionamiento.

### CodeBlock
Clase realizada para la manipulación de bloques de código.
Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>addBCodeBlockChild</span>&#8203;(CodeBlock&nbsp;codeBlockChild)</code></th>
<td>
<div>Función para agregar un bloque de código hijo al bloque de código.</div>
</td>
</tr>
<tr id="i1" class="rowColor">
<td><code>java.util.ArrayList&lt;java.lang.String&gt;</code></td>
<th><code><span>getBlocksOfCodeInOrderOfExec</span>()</code></th>
<td>
<div>Función que retorna un ArrayList de String que representa cada bloque de
 código a ejecutar. En dicho ArrayList se especifica un marcador de inicio y fin de cada bloque de código. El marcador empieza con un caracter ~, seguido de un UUID único y termina con otro caracter ~.
</div>
</td>
</tr>
<tr>
<td><code>java.lang.String</code></td>
<th><code><span>getCode</span>()</code></th>
<td>
<div>Función que retorna el código del bloque.</div>
</td>
</tr>
<tr>
<td><code>java.util.ArrayList&lt;CodeBlock&gt;</code></td>
<th><code><span>getCodeBlockChilds</span>()</code></th>
<td>
<div>Función que retorna los bloques de código hijos.</div>
</td>
</tr>
<tr>
<td><code>static int[]</code></td>
<th><code><span>getPositionOfBothMarkers</span>&#8203;(java.util.ArrayList&lt;java.lang.String&gt;&nbsp;blocksOfCode,
                        java.lang.String&nbsp;marker)</code></th>
<td>
<div>Función que retorna la posición inicial y final de un marcador de bloque
 de código.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>setCode</span>&#8203;(java.lang.String&nbsp;code)</code></th>
<td>
<div>Función para especificar el código del bloque.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>setCodeBlockChilds</span>&#8203;(java.util.ArrayList&lt;CodeBlock&gt;&nbsp;codeBlockChilds)</code></th>
<td>
<div>Función para especificar los bloques de código hijos del bloque de
 código.</div>
</td>
</tr>
</table>

### Directory
Clase para la manipulación de archivos de código. Las operaciones que se pueden realizar son las siguientes: Nuevo, Abrir, Guardar, Guardar Como y Salir. El código se podrá visualizar en el JTextComponent especificado. De la misma manera, si el título del JFrame contiene un asterisco (lo cual indica que el código actual está siendo modificado), hará las operaciones correspondientes. Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>Exit</span>()</code></th>
<td>
<div>Función que, en dado caso de que exista un archivo o código siendo modificado, le preguntará si desea guardar los cambios realizados.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>New</span>()</code></th>
<td>
<div>Función para crear una nueva edición de código. Reseteará el título del JFrame y el contenido del JTextComponent. Si existe algún archivo o código siendo modificado, le preguntará si desea guardar los cambios realizados.</div>
</td>
</tr>
<tr>
<td><code>boolean</code></td>
<th><code><span>Open</span>()</code></th>
<td>
<div>Función para abrir un archivo de código.  Pondrá de título del JFrame el nombre del archivo, además de poner el contenido de dicho archivo en el JTextComponent. Si existe algún archivo o código siendo modificado, le preguntará si desea guardar los cambios.</div>
</td>
</tr>
<tr>
<td><code>boolean</code></td>
<th><code><span>Save</span>()</code></th>
<td>
<div>Función para guardar los cambios realizados en un archivo de código. Si el archivo no ha sido creado, desplegará el explorador de archivos para elegir el nombre y ubicación del nuevo archivo que usted desea crear. Si ya existe un archivo con el mismo nombre en la misma ubicación, le preguntará si desea remplazarlo. En caso de que ya exista, guardará los cambios en el archivo y quitará el asterisco del título del JFrame.</div>
</td>
</tr>
<tr>
<td><code>boolean</code></td>
<th><code><span>SaveAs</span>()</code></th>
<td>
<div>Función que guardará como un nuevo archivo el código que esté siendo
 modificado o creado. Se desplegará el explorador de archivos para elegir la ubicación y el nombre del nuevo archivo. Si existe un archivo con el mismo nombre y ubicación, este será remplazado.</div>
</td>
</tr>
</table>

### ErrorLSSL
Clase que sirve para almacenar un error ya sea Léxico, Sintáctico, Semántico o Lógico. Se guarda la siguiente información: el número de error, la descripción, la producción de tokens a almacenar, y un booleano que indica si desea mostrar la línea/columna inicial o final de la producción. Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getColumn</span>()</code></th>
<td>
<div>Método para obtener la columna donde se encuentra el error.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getLine</span>()</code></th>
<td>
<div>Método para obtener la línea donde se encuentra el error.</div>
</td>
</tr>
</table>

### Functions
Clase creada para la ejecución de funciones que son de utilidad en un compilador estándar. Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>addRowDataInTable</span>&#8203;(javax.swing.JTable&nbsp;table,
                 java.lang.Object[]&nbsp;rowData)</code></th>
<td>
<div>Método para agregar un arreglo de objetos como renglón a una tabla</div>
</td>
</tr>
<tr>
<td><code>static java.lang.String</code></td>
<th><code><span>centerWord</span>&#8203;(java.lang.String&nbsp;word,
          java.lang.String&nbsp;charLeft,
          java.lang.String&nbsp;charRight,
          int&nbsp;quantity)</code></th>
<td>
<div>Método para centrar una cadena entre caracteres especificados a la
 izquierda y derecha.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>clearDataInTable</span>&#8203;(javax.swing.JTable&nbsp;table)</code></th>
<td>
<div>Método para eliminar todos los renglones de una tabla.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>colorTextPane</span>&#8203;(java.util.ArrayList&lt;TextColor&gt;&nbsp;textsColor,
             javax.swing.JTextPane&nbsp;jtpCode,
             java.awt.Color&nbsp;originalColor)</code></th>
<td>
<div>Función que colorea los caracteres de un JTextPane que estén dentro de un
 rango de un determinado color.</div>
</td>
</tr>
<tr>
<td><code>static java.lang.String</code></td>
<th><code><span>formatString</span>&#8203;(java.lang.String&nbsp;str,
            java.lang.String&nbsp;format,
            java.lang.String&nbsp;replace)</code></th>
<td>
<div>Método que realiza el remplazo de una cadena por otra cadena, con la
 condición de que no esté precedida de el caracter de escape '\'.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>insertAsteriskInName</span>&#8203;(javax.swing.JFrame&nbsp;jFrame,
                    javax.swing.text.JTextComponent&nbsp;jTextComponent)</code></th>
<td>
<div>Método para colocar el asterisco al final del título del JFrame durante
 la edición de un archivo.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>insertAsteriskInName</span>&#8203;(javax.swing.JFrame&nbsp;jFrame,
                    javax.swing.text.JTextComponent&nbsp;jTextComponent,
                    java.lang.Runnable&nbsp;function)</code></th>
<td>
<div>Método para colocar el asterisco al final del título del JFrame durante
 la edición de un archivo.</div>
</td>
</tr>
<tr>
<td><code>static boolean</code></td>
<th><code><span>isDigit</span>&#8203;(java.lang.String&nbsp;digit)</code></th>
<td>
<div>Método para saber si una cadena es un dígito.</div>
</td>
</tr>
<tr>
<td><code>static boolean</code></td>
<th><code><span>isLetter</span>&#8203;(java.lang.String&nbsp;letter)</code></th>
<td>
<div>Método para saber si una cadena es una letra.</div>
</td>
</tr>
<tr>
<td><code>static boolean</code></td>
<th><code><span>isNumber</span>&#8203;(java.lang.String&nbsp;number)</code></th>
<td>
<div>Método para saber si una cadena es un número.</div>
</td>
</tr>
<tr>
<td><code>static boolean</code></td>
<th><code><span>isSpace</span>&#8203;(java.lang.String&nbsp;space)</code></th>
<td>
<div>Método para saber si una cadena es un espacio vacío.</div>
</td>
</tr>
<tr>
<td><code>static boolean</code></td>
<th><code><span>isSpaceOrSaltLine</span>&#8203;(java.lang.String&nbsp;space)</code></th>
<td>
<div>Método para saber si una cadena es un espacio vacío o salto de línea.</div>
</td>
</tr>
<tr>
<td><code>static boolean</code></td>
<th><code><span>isWord</span>&#8203;(java.lang.String&nbsp;word)</code></th>
<td>
<div>Método para saber si una cadena es una palabra.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>setAutocompleterJTextComponent</span>&#8203;(java.lang.String[]&nbsp;words,
                              javax.swing.text.JTextComponent&nbsp;jTextComponent)</code></th>
<td>
<div>Función para implementar el método de autocompletado de código en un
 JTextComponent, mostrando un JPopupMenu que contendrá todas la palabras
 coincidentes con lo que se ha escrito.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>setAutocompleterJTextComponent</span>&#8203;(java.lang.String[]&nbsp;words,
                              javax.swing.text.JTextComponent&nbsp;jTextComponent,
                              java.lang.Runnable&nbsp;function)</code></th>
<td>
<div>Función para implementar el método de autocompletado de código en un
 JTextComponent, mostrando un JPopupMenu que contendrá todas la palabras
 coincidentes con lo que se ha escrito.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>setLineNumberOnJTextComponent</span>&#8203;(javax.swing.text.JTextComponent&nbsp;jTextComponent)</code></th>
<td>
<div>Método que muestra los números de línea en un JTextComponent.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>setLineNumberOnJTextComponent</span>&#8203;(javax.swing.text.JTextComponent&nbsp;jTextComponent,
                             int&nbsp;minimumDisplayDigits,
                             java.awt.Color&nbsp;color)</code></th>
<td>
<div>Método que muestra los números de línea en un JTextComponent.</div>
</td>
</tr>
<tr>
<td><code>static void</code></td>
<th><code><span>sortErrorsByLineAndColumn</span>&#8203;(java.util.ArrayList&lt;ErrorLSSL&gt;&nbsp;errors)</code></th>
<td>
<div>Método para ordenar un ArrayList de errores por número de línea y
 columna.</div>
</td>
</tr>
<tr>
<td><code>static CodeBlock</code></td>
<th><code><span>splitCodeInCodeBlocks</span>&#8203;(java.util.ArrayList&lt;Token&gt;&nbsp;tokens,
                     java.lang.String&nbsp;blockInitiator,
                     java.lang.String&nbsp;blockTerminator,
                     java.lang.String&nbsp;sentenceTerminator)</code></th>
<td>
<div>Función que divide el bloque de código principal en bloques y subbloques
 de código, tomando en cuenta tanto el lexema o bloque iniciador de
 código, el lexema o bloque terminador de código, y el lexema o bloque
 terminador de sentencia.</div>
</td>
</tr>
</table>
