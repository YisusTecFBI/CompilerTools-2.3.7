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

<section role="region">
    <ul>
        <li><a>
            </a>
            <h3>Detalles de métodos</h3>
            <a id="getCode()">
            </a>
            <ul>
                <li>
                    <h4>getCode</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>String El código del bloque</dd>
                    </dl>
                </li>
            </ul>
            <a id="setCode(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>setCode</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>code</code> - El código que se desea que contenga el bloque</dd>
                    </dl>
                </li>
            </ul>
            <a id="getCodeBlockChilds()">
            </a>
            <ul>
                <li>
                    <h4>getCodeBlockChilds</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>ArrayList&lt;CodeBlock&gt; ArrayList de bloques de código</dd>
                    </dl>
                </li>
            </ul>
            <a id="setCodeBlockChilds(java.util.ArrayList)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>setCodeBlockChilds</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>codeBlockChilds</code> - ArrayList de bloques de código hijos</dd>
                    </dl>
                </li>
            </ul>
            <a id="addBCodeBlockChild(compilerTools.CodeBlock)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>addBCodeBlockChild</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>codeBlockChild</code> - El bloque de código que se desea agregar como hijo</dd>
                    </dl>
                </li>
            </ul>
            <a id="getBlocksOfCodeInOrderOfExec()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getBlocksOfCodeInOrderOfExec</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>ArrayList&lt;String&gt; Un ArrayList de String de los bloques de
                            código en orden de ejecución</dd>
                    </dl>
                </li>
            </ul>
            <a id="getPositionOfBothMarkers(java.util.ArrayList,java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getPositionOfBothMarkers</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>blocksOfCode</code> - Los bloques de código que se desean analizar</dd>
                        <dd><code>marker</code> - El marcador que se desea buscar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>int[] Un arreglo de enteros de dos dimensiones que contiene ambas
                            posiciones</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

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

<section role="region">
    <ul>
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Detalles de métodos</h3>
            <a id="Open()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>Open</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Retorna verdadero si abrió el archivo exitosamente, falso
                            en caso contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="Save()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>Save</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Retorna verdadero si el archivo fue guardado
                            exitosamente, falso en caso contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="SaveAs()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>SaveAs</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Retorna verdadero si el archivo fue guardado
                            exitosamente, falso en caso contrario</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

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

<section role="region">
    <ul>
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Detalles de métodos</h3>
            <a id="getLine()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getLine</h4>
                    <dl>
                        <dt><span class="returnLabel">Retorna:</span></dt>
                        <dd>int Número que representa la línea</dd>
                    </dl>
                </li>
            </ul>
            <a id="getColumn()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getColumn</h4>
                    <dl>
                        <dt><span class="returnLabel">Retorna:</span></dt>
                        <dd>int Número que representa la columna</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

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
                              javax.swing.text.JTextComponent&nbsp;jTextComponent,
                              java.lang.Runnable&nbsp;function)</code></th>
<td>
<div>Función para implementar el método de autocompletado de código en un
 JTextComponent, mostrando un JPopupMenu que contendrá todas la palabras
 coincidentes con lo que se ha escrito. Dicho JPopupMenu se activará al presionar CTRL + SPACE.</div>
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

<section role="region">
    <ul>
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Method Detail</h3>
            <a id="clearDataInTable(javax.swing.JTable)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>clearDataInTable</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>table</code> - La tabla que se desea limpiar</dd>
                    </dl>
                </li>
            </ul>
            <a id="addRowDataInTable(javax.swing.JTable,java.lang.Object[])">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>addRowDataInTable</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>table</code> - La tabla a la que se desea agregar el renglón</dd>
                        <dd><code>rowData</code> - El arreglo de objetos que sea desea agregar como renglón;
                            cada posición representa una columna</dd>
                    </dl>
                </li>
            </ul>
            <a id="insertAsteriskInName(javax.swing.JFrame,javax.swing.text.JTextComponent,java.lang.Runnable)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>insertAsteriskInName</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>jFrame</code> - JFrame del cual se desea modificar el título durante una
                            edición</dd>
                        <dd><code>jTextComponent</code> - JTextComponent que se tomará como referencia de
                            edición</dd>
                        <dd><code>function</code> - Función que se ejecutará al cambiar el título del JFrame
                            durante la edición de un archivo</dd>
                    </dl>
                </li>
            </ul>
            <a id="centerWord(java.lang.String,java.lang.String,java.lang.String,int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>centerWord</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>word</code> - La cadena que se desea centrar</dd>
                        <dd><code>charLeft</code> - El caracter con el que se desea rellenar el lado
                            izquierdo</dd>
                        <dd><code>charRight</code> - El caracter con el que se desea rellenar el lado derecho</dd>
                        <dd><code>quantity</code> - El tamaño total de la cadena resultante</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>String La cadena centrada con caracteres a la izquierda y derecha</dd>
                    </dl>
                </li>
            </ul>
            <a id="formatString(java.lang.String,java.lang.String,java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>formatString</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>str</code> - La cadena en la cual se desea hacer el remplazo</dd>
                        <dd><code>format</code> - La cadena a remplazar</dd>
                        <dd><code>replace</code> - La cadena de remplazo</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>String La cadena original con el remplazo realizado</dd>
                    </dl>
                </li>
            </ul>
            <a id="colorTextPane(java.util.ArrayList,javax.swing.JTextPane,java.awt.Color)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>colorTextPane</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>textsColor</code> - El ArrayList de textos de color</dd>
                        <dd><code>jtpCode</code> - El JTextPane en el cual se desea cambiar el color de los
                            caracteres</dd>
                        <dd><code>originalColor</code> - El color por defecto de aquellos caracteres que no
                            estén dentro del rango</dd>
                    </dl>
                </li>
            </ul>
            <a id="setLineNumberOnJTextComponent(javax.swing.text.JTextComponent,int,java.awt.Color)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>setLineNumberOnJTextComponent</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>jTextComponent</code> - el JTextComponent en el cual se desea mostrar los
                            números de línea</dd>
                        <dd><code>minimumDisplayDigits</code> - La cantidad mínima de espacios de dígitos
                            mostradas en el numerador</dd>
                        <dd><code>color</code> - El color del número de línea actual en la que se esté
                            posicionado</dd>
                    </dl>
                </li>
            </ul>
            <a id="isLetter(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>isLetter</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>letter</code> - La letra que se desea analizar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Verdadero si la cadena es una letra, falso en caso
                            contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="isWord(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>isWord</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>word</code> - La palabra que se desea analizar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Verdadero si la cadena es una palabra, falso en caso
                            contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="isDigit(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>isDigit</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>digit</code> - El dígito que se desea analizar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Verdadero si la cadena es un dígito, falso en caso
                            contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="isNumber(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>isNumber</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>number</code> - El número que se desea analizar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Verdadero si la cadena es un número, falso en caso
                            contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="isSpace(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>isSpace</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>space</code> - El espacio que se desea analizar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Verdadero si la cadena es un espacio vacío, falso en caso
                            contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="isSpaceOrSaltLine(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>isSpaceOrSaltLine</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>space</code> - El espacio que se desea analizar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Verdadero si la cadena es un espacio vacío o salto de
                            línea, falso en caso contrario</dd>
                    </dl>
                </li>
            </ul>
            <a
                id="setAutocompleterJTextComponent(java.lang.String[],javax.swing.text.JTextComponent,java.lang.Runnable)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>setAutocompleterJTextComponent</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>words</code> - Las palabras clave de las cuales se buscarán coincidencias</dd>
                        <dd><code>jTextComponent</code> - El JtextComponent del que se desea implementar el
                            método de autocompletado</dd>
                        <dd><code>function</code> - La función que se desea ejecutar después de seleccionar
                            cualquier palabra clave del JPopupMenu</dd>
                    </dl>
                </li>
            </ul>
            <a id="splitCodeInCodeBlocks(java.util.ArrayList,java.lang.String,java.lang.String,java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>splitCodeInCodeBlocks</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>tokens</code> - El ArrayList de tokens resultante del análisis léxico</dd>
                        <dd><code>blockInitiator</code> - El bloque o lexema iniciador de bloque de código</dd>
                        <dd><code>blockTerminator</code> - El bloque o lexema terminador de bloque de código</dd>
                        <dd><code>sentenceTerminator</code> - El bloque o lexema terminador de sentencia</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>CodeBlock El bloque de código principal con sus bloques y
                            subbloques de código</dd>
                    </dl>
                </li>
            </ul>
            <a id="sortErrorsByLineAndColumn(java.util.ArrayList)">
                <!--   -->
            </a>
            <ul class="blockListLast">
                <li>
                    <h4>sortErrorsByLineAndColumn</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>errors</code> - El ArrayList de errores</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

### Grammar
Clase que sirve para realizar la agrupación de Tokens en un ArrayList de Producciones junto con la agregación de Errores de la agrupación deseada. La clase utiliza el manejo de índices, expresiones regulares y el uso de parámetros como referencia y valor. Por defecto, al iniciar se crean 'n' producciones de 'n' cantidad de tokens recibidos como parámetro. Es decir, que cada Producción contendrá un solo Token. Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>activateMessages</span>()</code></th>
<td>
<div>Función para activar los mensajes informativos en consola.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>activateValidations</span>()</code></th>
<td>
<div>Función para activar las validaciones internas de la clase.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>delete</span>&#8203;(java.lang.String&nbsp;nameProduction)</code></th>
<td>
<div>Función para eliminar una producción de manera silenciosa.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>delete</span>&#8203;(java.lang.String[]&nbsp;namesProduction)</code></th>
<td>
<div>Función para eliminar un conjunto de producciones de manera silenciosa.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>delete</span>&#8203;(java.lang.String[]&nbsp;namesProduction,
      int&nbsp;errorNumber)</code></th>
<td>
<div>Función para eliminar un conjunto de producciones y especificar el número
 de error de dichas producciones eliminadas.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span class="memberNameLink">delete</span>&#8203;(java.lang.String[]&nbsp;namesProduction,
      int&nbsp;errorNumber,
      java.lang.String&nbsp;errorMsg)</code></th>
<td>
<div>Función para eliminar un conjunto de producciones y especificar el número
 y mensaje de error de dichas producciones eliminadas.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>delete</span>&#8203;(java.lang.String&nbsp;nameProduction,
      int&nbsp;errorNumber)</code></th>
<td class="colLast">
<div class="block">Función para eliminar una producción y especificar el número de error de
 dicha producción eliminada.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>delete</span>&#8203;(java.lang.String&nbsp;nameProduction,
      int&nbsp;errorNumber,
      java.lang.String&nbsp;errorMsg)</code></th>
<td>
<div>Función para eliminar una producción y especificar el número y mensaje de
 error de dicha producción eliminada.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>disableMessages</span>()</code></th>
<td>
<div>Función para desactivar los mensajes informativos en consola.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>disableValidations</span>()</code></th>
<td>
<div>Función para desactivar las validaciones internas de la clase.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>finalLineColumn</span>()</code></th>
<td>
<div>Método para indicar que el error de la agrupación debe de mostrar la
 línea y columna final de la producción indicada.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>group</span>&#8203;(java.lang.String&nbsp;nameProduction,
     java.lang.String&nbsp;expReg,
     java.lang.String[]&nbsp;conmponents,
     boolean&nbsp;stopAtFirstOcurrence,
     int&nbsp;errorNumber,
     java.lang.String&nbsp;errorMsg,
     int&nbsp;indexComponent,
     java.util.ArrayList&lt;Production&gt;&nbsp;production)</code></th>
<td>
<div>Función que realiza la agrupación de Tokens en Producciones.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>initialLineColumn</span>()</code></th>
<td>
<div >Método para indicar que el error de la agrupación debe de mostrar la
 línea y columna inicial de la producción indicada.</div>
</td>
</tr>
<tr>
<td ><code>void</code></td>
<th><code><span>loopForFunExecUntilChangeNotDetected</span>&#8203;(java.lang.Runnable&nbsp;function)</code></th>
<td>
<div>Método que ejecutará una función de forma indefinida hasta que el tamaño
 de producciones deje de disminuir.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>show</span>()</code></th>
<td>
<div class="block">Función para imprimir en consola las gramáticas o producciones de tokens.</div>
</td>
</tr>
</table>

<section role="region">
    <ul>
        <li><a
                id="group(java.lang.String,java.lang.String,java.lang.String[],boolean,int,java.lang.String,int,java.util.ArrayList)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>group</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>nameProduction</code> - El nombre de la nueva producción</dd>
                        <dd><code>expReg</code> - La expresión regular con la que debe coincidir los nombres
                            (componentes) de las producciones a agrupar</dd>
                        <dd><code>conmponents</code> - Los componentes de la expresión regular. Si no se
                            especifican se obtienen de forma automática, pero consume más tiempo de
                            procesamiento</dd>
                        <dd><code>stopAtFirstOcurrence</code> - Indicamos si deseamos que la agrupación se
                            detenga en la primera ocurrencia</dd>
                        <dd><code>errorNumber</code> - El número de error en caso de que dicha agrupación sea
                            un error</dd>
                        <dd><code>errorMsg</code> - El mensaje de error en caso de que dicha agrupación sea
                            un error</dd>
                        <dd><code>indexComponent</code> - El índice del componente o producción del que
                            deseamos hacer referencia en el error</dd>
                        <dd><code>production</code> - ArrayList de Producciones donde deseamos guardar las
                            agrupaciones realizadas</dd>
                    </dl>
                </li>
            </ul>
            <a id="loopForFunExecUntilChangeNotDetected(java.lang.Runnable)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>loopForFunExecUntilChangeNotDetected</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>function</code> - La función que se ejecutará de forma indefinida</dd>
                    </dl>
                </li>
            </ul>
            <a id="delete(java.lang.String,int,java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>delete</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>nameProduction</code> - El nombre de la producción que se desea eliminar</dd>
                        <dd><code>errorNumber</code> - El número de error</dd>
                        <dd><code>errorMsg</code> - El mensaje de error</dd>
                    </dl>
                </li>
            </ul>
            <a id="delete(java.lang.String[],int,java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>delete</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>namesProduction</code> - El arreglo de nombres de producciones que se
                            desean eliminar</dd>
                        <dd><code>errorNumber</code> - El número de error</dd>
                        <dd><code>errorMsg</code> - El mensaje de error</dd>
                    </dl>
                </li>
            </ul>
            <a id="delete(java.lang.String,int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>delete</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>nameProduction</code> - El nombre de la producción que se desea eliminar</dd>
                        <dd><code>errorNumber</code> - El número de error</dd>
                    </dl>
                </li>
            </ul>
            <a id="delete(java.lang.String[],int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>delete</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>namesProduction</code> - El arreglo de nombres de producciones que se
                            desean eliminar</dd>
                        <dd><code>errorNumber</code> - El número de error</dd>
                    </dl>
                </li>
            </ul>
            <a id="delete(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>delete</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>nameProduction</code> - El nombre de la producción que se desea eliminar</dd>
                    </dl>
                </li>
            </ul>
            <a id="delete(java.lang.String[])">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>delete</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>namesProduction</code> - El nombre de las producciones que se desean
                            eliminar</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

### Production
Clase realizada para el almacenamiento de un grupo de tokens, especificando el nombre de la agrupación y la línea/columna inicial y final de la misma. Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>addTokens</span>&#8203;(Production&nbsp;prod)</code></th>
<td>
<div>Método para agregar los tokens de otra producción.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getColumn</span>()</code></th>
<td>
<div>Método para obtener la columna inicial de la producción.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getFinalColumn</span>()</code></th>
<td>
<div>Método para obtener la columna final de la producción.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getFinalLine</span>()</code></th>
<td>
<div>Método para obtener la línea final de la producción.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getLine</span>()</code></th>
<td>
<div>Método para obtener la línea inicial de la producción.</div>
</td>
</tr>
<tr>
<td><code>java.lang.String</code></td>
<th><code><span>getName</span>()</code></th>
<td>
<div>Método para obtener el nombre de la producción.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getSizeTokens</span>()</code></th>
<td>
<div>Retorna la cantidad de tokens que almacena la producción.</div>
</td>
</tr>
<tr>
<td><code>java.util.ArrayList&lt;Token&gt;</code></td>
<th><code><span>getTokens</span>()</code></th>
<td>
<div>Método para obtener el ArrayList de tokens de la producción.</div>
</td>
</tr>
<tr>
<td><code>java.lang.String</code></td>
<th><code><span>lexemeRank</span>&#8203;(int&nbsp;i)</code></th>
<td>
<div>Método para obtener el lexema de un determinado token en la posición i
 (acepta índices negativos).</div>
</td>
</tr>
<tr>
<td><code>java.lang.String</code></td>
<th><code><span>lexemeRank</span>&#8203;(int&nbsp;i,
          int&nbsp;j)</code></th>
<td>
<div>Retorna los lexemas concatenados de los tokens que estén entre la
 posición i y j (acepta índices negativos).</div>
</td>
</tr>
<tr>
<td><code>java.lang.String</code></td>
<th><code><span>lexicalCompRank</span>&#8203;(int&nbsp;i)</code></th>
<td>
<div>Método para obtener el componente léxico de un determinado token en la
 posición i (acepta índices negativos).</div>
</td>
</tr>
<tr id="i11">
<td><code>java.lang.String</code></td>
<th><code><span>lexicalCompRank</span>&#8203;(int&nbsp;i,
               int&nbsp;j)</code></th>
<td>
<div>Retorna los componentes léxicos concatenados de los tokens que estén
 entre la posición i y j (acepta índices negativos).</div>
</td>
</tr>
<tr>
<td><code>boolean</code></td>
<th><code><span><a>nameEqualTo</a></span>&#8203;(java.lang.String&nbsp;name)</code></th>
<td>
<div>Método para saber si el nombre de la producción es igual a otra cadena.</div>
</td>
</tr>
<tr>
<td><code>boolean</code></td>
<th><code><span><a>nameEqualTo</a></span>&#8203;(java.lang.String[]&nbsp;names)</code></th>
<td>
<div>Método para saber si el nombre de la producción es igual a alguna de las
 cadenas dentro del arreglo.</div>
</td>
</tr>
<tr>
<td><code>void</code></td>
<th><code><span>setName</span>&#8203;(java.lang.String&nbsp;name)</code></th>
<td>
<div>Método para cambiar el nombre de la producción.</div>
</td>
</tr>
<tr>
<td><code>Token</code></td>
<th><code><span>tokenRank</span>&#8203;(int&nbsp;i)</code></th>
<td>
<div>Método para obtener un determinado token que está en la posición i
 (acepta índices negativos).</div>
</td>
</tr>
<tr>
<td><code>java.util.ArrayList&lt;Token&gt;</code></td>
<th><code><span>tokenRank</span>&#8203;(int&nbsp;i,
         int&nbsp;j)</code></th>
<td>
<div>Retorna un ArrayList que contiene los tokens que estén entre la posición
 i y j (acepta índices negativos).</div>
</td>
</tr>
</table>

<section role="region">
    <ul>
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Method Detail</h3>
            <a id="getName()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getName</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>String Nombre de la producción</dd>
                    </dl>
                </li>
            </ul>
            <a id="getTokens()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getTokens</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>ArrayList&lt;Token&gt; El ArrayList de tokens</dd>
                    </dl>
                </li>
            </ul>
            <a id="getLine()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getLine</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int La línea inicial</dd>
                    </dl>
                </li>
            </ul>
            <a id="getColumn()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getColumn</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int La columna inicial</dd>
                    </dl>
                </li>
            </ul>
            <a id="getFinalLine()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getFinalLine</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int La línea final</dd>
                    </dl>
                </li>
            </ul>
            <a id="getFinalColumn()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getFinalColumn</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int La columna final</dd>
                    </dl>
                </li>
            </ul>
            <a id="getSizeTokens()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getSizeTokens</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int Cantidad de tokens</dd>
                    </dl>
                </li>
            </ul>
            <a id="addTokens(compilerTools.Production)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>addTokens</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>prod</code> - La producción de la que se desea extraer los tokens para
                            agregarlos</dd>
                    </dl>
                </li>
            </ul>
            <a id="lexemeRank(int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>lexemeRank</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>i</code> - La posición del token del que se desea extraer el lexema</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>String El lexema del token</dd>
                    </dl>
                </li>
            </ul>
            <a id="lexicalCompRank(int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>lexicalCompRank</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>i</code> - La posición del token del que se desea extraer el componente
                            léxico</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>String El componente léxico del token</dd>
                    </dl>
                </li>
            </ul>
            <a id="tokenRank(int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>tokenRank</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>i</code> - La posición del token que se desea obtener</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>Token El token</dd>
                    </dl>
                </li>
            </ul>
            <a id="lexemeRank(int,int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>lexemeRank</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>i</code> - posición inicial del rango</dd>
                        <dd><code>j</code> - posición final del rango</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>String Los lexemas concatenados</dd>
                    </dl>
                </li>
            </ul>
            <a id="lexicalCompRank(int,int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>lexicalCompRank</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>i</code> - posición inicial del rango</dd>
                        <dd><code>j</code> - posición final del rango</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>String Los componentes léxicos concatenados</dd>
                    </dl>
                </li>
            </ul>
            <a id="tokenRank(int,int)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>tokenRank</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>i</code> - posición inicial del rango</dd>
                        <dd><code>j</code> - posición final del rango</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>ArrayList&lt;Token&gt; El ArrayList de tokens dentro del rango</dd>
                    </dl>
                </li>
            </ul>
            <a id="nameEqualTo(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>nameEqualTo</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>name</code> - La cadena que se desea comparar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Retorna verdadero si el nombre es igual a la otra cadena,
                            falso en caso contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="nameEqualTo(java.lang.String[])">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>nameEqualTo</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>names</code> - El arreglo de cadenas que se desea comparar</dd>
                        <dt><span>Retorna:</span></dt>
                        <dd>boolean Retorna verdadero si el nombre es igual a alguna de las
                            cadenas, falso en caso contrario</dd>
                    </dl>
                </li>
            </ul>
            <a id="setName(java.lang.String)">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>setName</h4>
                    <dl>
                        <dt><span>Parámetros:</span></dt>
                        <dd><code>name</code> - El nuevo nombre de la producción</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

### TextColor
Clase para el almacenamiento del índice de inicio, tamaño y color de una cadena. Las funciones o métodos que contiene son los siguientes:
<table>
<tr>
<th>Modificador y tipo</th>
<th>Método</th>
<th>Descripción</th>
</tr>
<tr>
<td><code>java.awt.Color</code></td>
<th><code><span>getColor</span>()</code></th>
<td>
<div>Función para obtener el color de la cadena.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getSize</span>()</code></th>
<td>
<div>Función para obtener el tamaño de la cadena.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getStart</span>()</code></th>
<td>
<div>Función para obtener el índice de inicio de la cadena.</div>
</td>
</tr>
</table>

### Token
Clase para almacenar los atributos de un token (lexema, componente léxico, línea y columna). Las funciones o métodos que contiene son los siguientes:
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
<div>Método para obtener el número de columna del token.</div>
</td>
</tr>
<tr>
<td><code>java.lang.String</code></td>
<th><code><span>getLexeme</span>()</code></th>
<td>
<div>Función para obtener el lexema del token.</div>
</td>
</tr>
<tr>
<td ><code>java.lang.String</code></td>
<th><code><span>getLexicalComp</span>()</code></th>
<td>
<div>Función para obtener el componente léxico del token.</div>
</td>
</tr>
<tr>
<td><code>int</code></td>
<th><code><span>getLine</span>()</code></th>
<td>
<div>Función para obtener el número de línea del token.</div>
</td>
</tr>
</table>
