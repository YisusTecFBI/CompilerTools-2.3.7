CompilerTools 2.3.7 - Herramienta de compilador estándar
========================================================
### Introducción
CompilerTools es una herramienta creada para el diseño de un compilador básico en Java. Si bien, no es la herramienta ideal para hacer un compilador con gran cantidad de gramáticas y palabras reservadas, es lo suficientemente intuitivo y funcional para introducirnos en el mundo de los compiladores. Cumple con ser lo bastante didáctico para estudiantes y aficionados al mundo de la programación.  

Características clave:
- Implementa un autocompletador de código en un JTextComponent.
- Extrae los bloques de código del lenguaje inventado para su posterior ejecución.
- Cuenta con una clase para la manipulación de archivos, soportando operaciones como Nuevo, Abrir, Guardar y Guardar Como.
- Se pueden crear errores ya sean Léxicos, Sintácticos, Semánticos o Lógicos.
- Tiene diversas funciones automatizadas que realizan algunas operaciones complejas para la programación del compilador.
- Se pueden crear gramáticas mediante la agrupación de Tokens a través de Producciones.
- Implementa un contador de número de línea en un JTextComponent.
- Cuenta con una función para el coloreo de palabras en un JTextComponent.
- Implementa el almacenamiento de tokens y sus atributos básicos, los cuales son lexema, componente léxico, línea y columna.

Explicaré la función principal de cada clase y cada uno de sus métodos. De igual forma dejaré un [videotutorial](https://youtu.be/AHGe8l_yG6s) en el cual explicó más a detalle el funcionamiento.

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
<td><code>static boolean</code></td>
<th><code><span>isMarker</span>&#8203;(java.lang.String&nbsp;marker)</code></th>
<td>
<div>Función para saber si una cadena es un marcador.</div>
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
	    <a id="isMarker(java.lang.String)">
    		<!--   -->
	     </a>
	    <ul>
    		<li>
        	    <h4>isMarker</h4>
        	    <dl>
            		<dt><span>Parámetros:</span></dt>
            		<dd><code>marker</code> - El marcador que se desea analizar</dd>
            		<dt><span>Retorna:</span></dt>
            		<dd>boolean Verdadero si la cadena es un marcador, falso en caso
                	contrario</dd>
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
<div>Método para agregar un arreglo de objetos como renglón a una tabla.</div>
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
             javax.swing.JTextPane&nbsp;jTextPane,
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
            <h3>Detalles de métodos</h3>
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
                        <dd><code>jTextPane</code> - El JTextPane en el cual se desea cambiar el color de los
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
                        <dd><code>jTextComponent</code> - El JTextComponent del que se desea implementar el
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
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Detalles de métodos</h3>
         <a
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
                            deseamos hacer referencia en el error (acepta índices negativos)</dd>
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
            <h3>Detalles de métodos</h3>
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
                        <dd><code>i</code> - posición inicial del rango (acepta índices negativos)</dd>
                        <dd><code>j</code> - posición final del rango (acepta índices negativos)</dd>
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
                        <dd><code>i</code> - posición inicial del rango (acepta índices negativos)</dd>
                        <dd><code>j</code> - posición final del rango (acepta índices negativos)</dd>
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
                        <dd><code>i</code> - posición inicial del rango (acepta índices negativos)</dd>
                        <dd><code>j</code> - posición final del rango (acepta índices negativos)</dd>
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

<section role="region">
    <ul>
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Detalles de métodos</h3>
            <a id="getStart()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getStart</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int Índice de inicio</dd>
                    </dl>
                </li>
            </ul>
            <a id="getSize()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getSize</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>int El tamaño de la cadena</dd>
                    </dl>
                </li>
            </ul>
            <a id="getColor()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getColor</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>Color El Color de la cadena</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

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

<section role="region">
    <ul>
        <li><a id="method.detail">
                <!--   -->
            </a>
            <h3>Detalles de métodos</h3>
            <a id="getLexeme()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getLexeme</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>String El lexema</dd>
                    </dl>
                </li>
            </ul>
            <a id="getLexicalComp()">
                <!--   -->
            </a>
            <ul>
                <li>
                    <h4>getLexicalComp</h4>
                    <dl>
                        <dt><span>Retorna:</span></dt>
                        <dd>String El componente léxico</dd>
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
                        <dd>int El número de línea</dd>
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
                        <dd>int El número de columna</dd>
                    </dl>
                </li>
            </ul>
        </li>
    </ul>
</section>

### Ejemplo de uso
Procederemos a crear varios tokens y agregarlos a un ArrayList de tipo Token:

````java
        // Declaramos los tokens, pasando como parámetro el lexema, componente léxico, línea y columna
        Token tk1 = new Token("(", "PARENTESIS_A", 3, 41);
        Token tk2 = new Token(")", "PARENTESIS_C", 5, 13);
        Token tk3 = new Token("color", "TIPO_DATO", 9, 36);
        // Agregamos los tokens a un ArrayList de tipo Token
        ArrayList<Token> tokens = new ArrayList<>();
        tokens.add(tk1);
        tokens.add(tk2);
        tokens.add(tk3);
````

Declararemos un ArrayList de tipo ErrorLSSL para guardar los errores resultantes de las agrupaciones de gramáticas que haremos más adelante:


````java
        // ArrayList de ErrorLSSL
        ArrayList<ErrorLSSL> errores = new ArrayList<>();
````

A continuación, empezaremos a hacer las agrupaciones de nuestras gramáticas. Crearemos un objeto de tipo Grammar:

````java
        // Creamos el objeto de tipo Grammar, pasando como parámetro el ArrayList de Tokens y el ArrayList de errores
        Grammar gramatica = new Grammar(tokens, errores);
        // Mostramos las gramáticas o conjunto de producciones creadas
        gramatica.show();
````

Lo anterior nos generará una salida en consola:

````
**** Mostrando gramáticas ****

....................................................................................................
Produccion(PARENTESIS_A, 3, 41, 3, 41, [
Token((, PARENTESIS_A, 3, 41)])

....................................................................................................
Produccion(PARENTESIS_C, 5, 13, 5, 13, [
Token(), PARENTESIS_C, 5, 13)])

....................................................................................................
Produccion(TIPO_DATO, 9, 36, 9, 36, [
Token(color, TIPO_DATO, 9, 36)])
````

Como podrá observar, nos generó 3 producciones, estas producciones a su vez contienen un solo Token. El nombre de la producción es el mismo que el nombre del token que almacena. El primer parámetro es el nombre de la producción, la línea inicial, columna inicial, línea final, columna final y el arreglo de tokens. En este caso, tanto la línea/columna inicial y final son las mismas ya que solo contiene un solo Token. En caso de haber más tokens en la Producción, la línea/columna inicial de la Producción será igual a la línea/columna del primer Token; siguiendo la misma lógica, la línea/columna final será igual a la línea/columna del último Token.

Realizaremos las agrupaciones de nuestros tokens. Supongamos que inventamos una nueva gramática donde debe haber un paréntesis que abre y que cierra al inicio, seguido de un tipo de dato. Debemos tener claro que el objeto Grammar que creamos anteriormente realizará las agrupaciones de Tokens de acuerdo al orden en el que estén en el ArrayList que recibió como parámetro. Haremos la agrupación de la siguiente manera:

````java
        /* Hacemos una agrupación, pasando como parámetro el nombre de la nueva producción,
        seguido de la expresión regular
         */
        gramatica.group("FUNCION", "PARENTESIS_A PARENTESIS_C TIPO_DATO");
````

Si mostramos nuevamente la gramática, generará la siguiente salida en consola:

````
....................................................................................................
**** Agrupación 1 "FUNCION" realizada con éxito ****
Cantidad de componentes: 3
La cantidad de producciones se redujo de 3 a 1


**** Mostrando gramáticas ****

....................................................................................................
Produccion(FUNCION, 3, 41, 9, 36, [
Token((, PARENTESIS_A, 3, 41),
Token(), PARENTESIS_C, 5, 13),
Token(color, TIPO_DATO, 9, 36)])
````
Como podrá darse cuenta, la clase Grammar nos mostrará información de la agrupación que haya realizado, así como la reducción de producciones que hayan ocurrido. Al final podremos observar que se generó una sola producción con 3 tokens. La expresión regular que usamos en el paso anterior es muy sencilla, pero soporta cualquier expresión sin importar su complejidad, dándonos el total control de agrupaciones que queramos realizar.

Ahora bien, puede ser que nosotros estemos intentando meter una expresión regular incorrecta:

````java
gramatica.group("FUNCION", "PARENTESIS_A PARENTESIS_C TIPO_DATO )*");
````

En consecuencia, en consola veremos lo siguiente:

````
....................................................................................................
**** Agrupación 1 "FUNCION" no realizada****
Δ Resuelva los errores a continuación descritos Δ:
1. Formato de expresión regular inválido: Unmatched closing ')' near index 35
PARENTESIS_A PARENTESIS_C TIPO_DATO )*
                                   ^

**** Mostrando gramáticas ****

....................................................................................................
Produccion(PARENTESIS_A, 3, 41, 3, 41, [
Token((, PARENTESIS_A, 3, 41)])

....................................................................................................
Produccion(PARENTESIS_C, 5, 13, 5, 13, [
Token(), PARENTESIS_C, 5, 13)])

....................................................................................................
Produccion(TIPO_DATO, 9, 36, 9, 36, [
Token(color, TIPO_DATO, 9, 36)])
````
Como podremos observar, no se realizó ninguna agrupación de Tokens. De igual manera, vemos que la agrupación 1 no fue realizada por un formato de expresión regular inválido. Usted tiene que asegurarse de que las expresiones regulares introducidas sean correctas para poder obtener la agrupación deseada. Ahora bien, las validaciones internas que hace la clase Grammar consumen tiempo de procesamiento. Si al final usted ya ha verificado que ninguna expresión regular o parámetro es incorrecto, podemos desactivar las validaciones mediante el siguiente método:

````java
        // Desactivamos las validaciones internas de la clase
        gramatica.disableValidations();
````
Precaución: Si usted desactiva las validaciones y alguna agrupación contiene algún parámetro incorrecto, se nos generará un error en tiempo de ejecución. Supongamos que no corregimos la expresión regular y aun así desactivamos las validaciones:

````java
        // Desactivamos las validaciones internas de la clase
        gramatica.disableValidations();

        /* Hacemos una agrupación, pasando como parámetro el nombre de la nueva producción,
        seguido de la expresión regular
         */
        gramatica.group("FUNCION", "PARENTESIS_A PARENTESIS_C TIPO_DATO)*");
````

Por lo tanto, tendremos un error en tiempo de ejecución, deteniendo por completo la ejecución de nuestro programa:

````
....................................................................................................
Exception in thread "main" java.util.regex.PatternSyntaxException: Unmatched closing ')' near index 32
PARENTESIS_APARENTESIS_CTIPO_DATO)*
                                ^
	at java.base/java.util.regex.Pattern.error(Pattern.java:2027)
	at java.base/java.util.regex.Pattern.compile(Pattern.java:1786)
	at java.base/java.util.regex.Pattern.<init>(Pattern.java:1428)
	at java.base/java.util.regex.Pattern.compile(Pattern.java:1068)
	at java.base/java.util.regex.Pattern.matches(Pattern.java:1173)
	at java.base/java.lang.String.matches(String.java:2024)
	at compilerTools.Grammar.group(Grammar.java:186)
	at compilerTools.Grammar.group(Grammar.java:399)
	at NewClass.main(NewClass.java:36)
/home/yisus/snap/netbeans/common/52/executor-snippets/run.xml:111: The following error occurred while executing this line:
/home/yisus/snap/netbeans/common/52/executor-snippets/run.xml:68: Java returned: 1
BUILD FAILED (total time: 0 seconds)
````

Las impresiones en consola de las agrupaciones realizadas también consumen tiempo de procesamiento. Aunque no ejecutemos el método show(), estás seguirán mostrándose:
````
....................................................................................................
**** Agrupación 1 "FUNCION" realizada con éxito ****
Cantidad de componentes: 3
La cantidad de producciones se redujo de 3 a 1
````

Lo único que tenemos que hacer, es mandar a llamar el siguiente método para que no muestre los mensajes informativos de las agrupaciones a realizar:
````java
        // Desactivamos los mensajes informativos de las agrupaciones
        gramatica.disableMessages();
        /* Hacemos una agrupación, pasando como parámetro el nombre de la nueva producción,
        seguido de la expresión regular
         */
        gramatica.group("FUNCION", "PARENTESIS_A PARENTESIS_C TIPO_DATO");
````

Lo anterior no generará ninguna salida en consola.

Para el siguiente ejemplo, introduciremos nuevos tokens:
````java
        // Declaramos los tokens
        Token tk1 = new Token("FUNCION", "FUNCION", 1, 94);
        Token tk2 = new Token("FUNCION", "FUNCION", 2, 56);
        Token tk3 = new Token("FUNCION", "FUNCION", 3, 65);
        Token tk4 = new Token("{", "LLAVE_A", 4, 24);
        Token tk5 = new Token("{", "LLAVE_A", 5, 76);
        Token tk6 = new Token("{", "LLAVE_A", 6, 45);
        Token tk7 = new Token("FUNCION", "FUNCION", 7, 65);
        Token tk8 = new Token("}", "LLAVE_C", 8, 15);
        Token tk9 = new Token("}", "LLAVE_C", 9, 43);
        Token tk10 = new Token("}", "LLAVE_C", 10, 13);
        // Agregamos los tokens a un ArrayList de tipo Token
        ArrayList<Token> tokens = new ArrayList<>();
        tokens.add(tk1);
        tokens.add(tk2);
        tokens.add(tk3);
        tokens.add(tk4);
        tokens.add(tk5);
        tokens.add(tk6);
        tokens.add(tk7);
        tokens.add(tk8);
        tokens.add(tk9);
        tokens.add(tk10);
        // ArrayList de ErrorLSSL
        ArrayList<ErrorLSSL> errores = new ArrayList<>();

        // Creamos el objeto de tipo Grammar, pasando como parámetro el ArrayList de Tokens y el ArrayList de errores
        Grammar gramatica = new Grammar(tokens, errores);
````

Supongamos que deseamos meter los siguientes tokens en una sola agrupación:

````java
        Token tk4 = new Token("{", "LLAVE_A", 4, 24);
        Token tk5 = new Token("{", "LLAVE_A", 5, 76);
        Token tk6 = new Token("{", "LLAVE_A", 6, 45);
        Token tk7 = new Token("FUNCION", "FUNCION", 7, 65);
        Token tk8 = new Token("}", "LLAVE_C", 8, 15);
        Token tk9 = new Token("}", "LLAVE_C", 9, 43);
        Token tk10 = new Token("}", "LLAVE_C", 10, 13);
````

Tenemos diferentes maneras de hacerlo. La primera es con una expresión regular:

````java
        gramatica.group("FUNCION","(LLAVE_A)+ FUNCION (LLAVE_C)+");
````

La segunda forma, es con el método loopForFunExecUntilChangeNotDetected, el cual se ejecutará de forma indefinida hasta que no se detecte ningún cambio en la cantidad de producciones. Agruparemos de forma indefinida una llave que abre, seguido de alguna producción con el nombre de 'FUNCION' y que termine con una llave que cierra:
````java
	gramatica.loopForFunExecUntilChangeNotDetected(() -> {
            gramatica.group("FUNCION", "LLAVE_A FUNCION LLAVE_C");
        });
````

Ambas formas generan la siguiente salida en consola:

````
**** Mostrando gramáticas ****

....................................................................................................
Produccion(FUNCION, 1, 94, 1, 94, [
Token(FUNCION, FUNCION, 1, 94)])

....................................................................................................
Produccion(FUNCION, 2, 56, 2, 56, [
Token(FUNCION, FUNCION, 2, 56)])

....................................................................................................
Produccion(FUNCION, 3, 65, 3, 65, [
Token(FUNCION, FUNCION, 3, 65)])

....................................................................................................
Produccion(FUNCION, 4, 24, 10, 13, [
Token({, LLAVE_A, 4, 24),
Token({, LLAVE_A, 5, 76),
Token({, LLAVE_A, 6, 45),
Token(FUNCION, FUNCION, 7, 65),
Token(}, LLAVE_C, 8, 15),
Token(}, LLAVE_C, 9, 43),
Token(}, LLAVE_C, 10, 13)])
````

Explicaremos de que otra manera podemos manipular las agrupaciones. Al observar una expresión regular, nosotros por intuición sabemos que expresión regular genera una sola cadena, por lo tanto, solo podrá cumplirse con una cadena. Sin embargo, la clase Grammar eso no lo sabe. Podemos hacer que haga una agrupación ya sea solamente en la primera ocurrencia o no. Por defecto no lo hace, pero nosotros podemos especificarlo en el método group. Por ejemplo, supongamos que deseamos agrupar una llave que abre, seguido de una función y que termina con una o más llaves que cierran. La agrupación se hace de la siguiente manera:

````java
        gramatica.group("FUNCION","LLAVE_A FUNCION (LLAVE_C)+");
````

Lo anterior mostrará lo siguiente en consola:
````
**** Mostrando gramáticas ****

....................................................................................................
Produccion(FUNCION, 1, 94, 1, 94, [
Token(FUNCION, FUNCION, 1, 94)])

....................................................................................................
Produccion(FUNCION, 2, 56, 2, 56, [
Token(FUNCION, FUNCION, 2, 56)])

....................................................................................................
Produccion(FUNCION, 3, 65, 3, 65, [
Token(FUNCION, FUNCION, 3, 65)])

....................................................................................................
Produccion(LLAVE_A, 4, 24, 4, 24, [
Token({, LLAVE_A, 4, 24)])

....................................................................................................
Produccion(LLAVE_A, 5, 76, 5, 76, [
Token({, LLAVE_A, 5, 76)])

....................................................................................................
Produccion(FUNCION, 6, 45, 10, 13, [
Token({, LLAVE_A, 6, 45),
Token(FUNCION, FUNCION, 7, 65),
Token(}, LLAVE_C, 8, 15),
Token({, LLAVE_C, 9, 43),
Token(}, LLAVE_C, 10, 13)])
````

Ahora bien, supongamos que deseamos que la agrupación la haga hasta la primera ocurrencia. Mandaremos un parámetro adicional booleano llamado stopAtFirstOcurrence en true:

````java
        gramatica.group("FUNCION", "LLAVE_A FUNCION (LLAVE_C)+", true);
````

De esa manera, tendremos lo siguiente en consola:

````
**** Mostrando gramáticas ****

....................................................................................................
Produccion(FUNCION, 1, 94, 1, 94, [
Token(FUNCION, FUNCION, 1, 94)])

....................................................................................................
Produccion(FUNCION, 2, 56, 2, 56, [
Token(FUNCION, FUNCION, 2, 56)])

....................................................................................................
Produccion(FUNCION, 3, 65, 3, 65, [
Token(FUNCION, FUNCION, 3, 65)])

....................................................................................................
Produccion(LLAVE_A, 4, 24, 4, 24, [
Token({, LLAVE_A, 4, 24)])

....................................................................................................
Produccion(LLAVE_A, 5, 76, 5, 76, [
Token({, LLAVE_A, 5, 76)])

....................................................................................................
Produccion(FUNCION, 6, 45, 8, 15, [
Token({, LLAVE_A, 6, 45),
Token(FUNCION, FUNCION, 7, 65),
Token(}, LLAVE_C, 8, 15)])

....................................................................................................
Produccion(LLAVE_C, 9, 43, 9, 43, [
Token({, LLAVE_C, 9, 43)])

....................................................................................................
Produccion(LLAVE_C, 10, 13, 10, 13, [
Token(}, LLAVE_C, 10, 13)])
````

Como puede observar, solamente agrupó una llave que cierra, ya que en si la agrupación cumple con la expresión regular, pero se detuvo en la primera ocurrencia. Esta funcionalidad solamente es útil si desea ahorrar tiempo de procesamiento en aquellas agrupaciones que solamente se cumplirán con una sola cadena.

A continuación describiremos la manera de como generar errores sintácticos. Un error sintáctico se genera al encontrarse una gramática que no esté reconocida por el lenguaje. Supongamos que deseamos agrupar una llave que abre, seguido de una función, una llave que cierra y que termina con punto y coma. Para ello, nuevamente introduciremos nuevos tokens:

````java
        // Declaramos los tokens
        Token tk1 = new Token("{", "LLAVE_A", 1, 23);
        Token tk2 = new Token("FUNCION", "FUNCION", 2, 12);
        Token tk3 = new Token("}", "LLAVE_C", 3, 16);
        Token tk4 = new Token("{", "LLAVE_A", 5, 22);
        Token tk5 = new Token("FUNCION", "FUNCION", 6, 23);
        Token tk6 = new Token("}", "LLAVE_C", 7, 65);
        Token tk7 = new Token(";", "PUNTO_COMA", 8, 13);
        // Agregamos los tokens a un ArrayList de tipo Token
        ArrayList<Token> tokens = new ArrayList<>();
        tokens.add(tk1);
        tokens.add(tk2);
        tokens.add(tk3);
        tokens.add(tk4);
        tokens.add(tk5);
        tokens.add(tk6);
        tokens.add(tk7);
	
	// ArrayList de ErrorLSSL
        ArrayList<ErrorLSSL> errores = new ArrayList<>();

        // Creamos el objeto de tipo Grammar, pasando como parámetro el ArrayList de Tokens y el ArrayList de errores
        Grammar gramatica = new Grammar(tokens, errores);
````

A continuación, haremos la agrupación anteriormente descrita:

````java
        gramatica.group("FUNCION_COMPLET", "LLAVE_A FUNCION LLAVE_C PUNTO_COMA");
````

Al mostrar las gramáticas, nos mostrará lo siguiente en consola:

````
**** Mostrando gramáticas ****

....................................................................................................
Produccion(LLAVE_A, 1, 23, 1, 23, [
Token({, LLAVE_A, 1, 23)])

....................................................................................................
Produccion(FUNCION, 2, 12, 2, 12, [
Token(FUNCION, FUNCION, 2, 12)])

....................................................................................................
Produccion(LLAVE_C, 3, 16, 3, 16, [
Token(}, LLAVE_C, 3, 16)])

....................................................................................................
Produccion(FUNCION_COMPLET, 5, 22, 8, 13, [
Token({, LLAVE_A, 5, 22),
Token(FUNCION, FUNCION, 6, 23),
Token(}, LLAVE_C, 7, 65),
Token(;, PUNTO_COMA, 8, 13)])
````

Podemos observar que solo un grupo de producciones cumplieron con la expresión regular. A los grupos de producciones o tokens anteriores solamente les faltó un punto y coma al final. Como eso es básicamente un error sintáctico, agruparemos dicha expresión y guardaremos el error en el ArrayList de errores. Entonces, después de nuestra primera agrupación de sintaxis correcta, haremos una segunda agrupación para la sintaxis incorrecta:

````java
        // Agrupación con sintaxis correcta
        gramatica.group("FUNCION_COMPLET", "LLAVE_A FUNCION LLAVE_C PUNTO_COMA");

        /* Agrupación con sintaxis incorrecta, pasando como parámetro el nombre de la nueva producción,
           la expresión regular, el número de error y el mensaje de error 
         */
        gramatica.group("FUNCION_COMPLET", "LLAVE_A FUNCION LLAVE_C",
                1, "Error sintáctico {}: Falta el punto y coma al final de la función [#, %]");
````

Lo anterior realizará las siguientes agrupaciones:
````
**** Mostrando gramáticas ****

....................................................................................................
Produccion(FUNCION_COMPLET, 1, 23, 3, 16, [
Token({, LLAVE_A, 1, 23),
Token(FUNCION, FUNCION, 2, 12),
Token(}, LLAVE_C, 3, 16)])

....................................................................................................
Produccion(FUNCION_COMPLET, 5, 22, 8, 13, [
Token({, LLAVE_A, 5, 22),
Token(FUNCION, FUNCION, 6, 23),
Token(}, LLAVE_C, 7, 65),
Token(;, PUNTO_COMA, 8, 13)])
````

¿Dónde quedó el error? El error fue almacenado en el ArrayList de errores que pasamos como parámetro. A continuación, imprimiremos en consola del ArrayList de errores:

````java
        // Mostramos en consola el ArrayList de errores
        System.out.println(errores);
````

Lo anterior muestra lo siguiente en consola:

````
[Error sintáctico 1: Falta el punto y coma al final de la función [1, 23]]
````
Si observamos bien, la línea y columna que nos está indicando el error es la inicial. Si queremos que nos indique la línea y columna final haremos lo siguiente. Antes de iniciar las agrupaciones de errores, mandaremos a llamar el método finalLineColumn. Después de hacer la agrupación del error, mandamos a llamar el método initialLineColumn para volver a mostrar la línea/columna inicial.

````java
 	// Hacemos que en las agrupaciones de errores nos muestre la línea/columna final
        gramatica.finalLineColumn();
        /* Agrupación con sintaxis incorrecta, pasando como parámetro el nombre de la nueva producción,
           la expresión regular, el número de error y el mensaje de error 
         */
        gramatica.group("FUNCION_COMPLET", "LLAVE_A FUNCION LLAVE_C",
                1, "Error sintáctico {}: Falta el punto y coma al final de la función [#, %]");
        // Hacemos que en las agrupaciones de errores nos muestre la línea/columna inicial nuevamente
        gramatica.initialLineColumn();
	
	// Mostramos en consola el ArrayList de errores
        System.out.println(errores);
````

Al ejecutar lo anterior, nos mostrará lo siguiente en consola:
````
[Error sintáctico 1: Falta el punto y coma al final de la función [3, 16]]
````
Vemos entonces que ahora nos mostró la línea/columna final de la producción agrupada.

Imaginemos que cambiamos la estructura de la agrupación. En vez de que el punto y coma vaya al final, haremos que tengan que ser dos los que tengan que ir antes y después de la producción FUNCION:
````java
// Declaramos los tokens
        Token tk1 = new Token("{", "LLAVE_A", 5, 22);
        Token tk2 = new Token(";", "PUNTO_COMA", 6, 13);
        Token tk3 = new Token("FUNCION", "FUNCION", 6, 23);
        Token tk4 = new Token(";", "PUNTO_COMA", 6, 36);
        Token tk5 = new Token("}", "LLAVE_C", 8, 65);

        // Agregamos los tokens a un ArrayList de tipo Token
        ArrayList<Token> tokens = new ArrayList<>();
        tokens.add(tk1);
        tokens.add(tk2);
        tokens.add(tk3);
        tokens.add(tk4);
        tokens.add(tk5);
        // ArrayList de ErrorLSSL
        ArrayList<ErrorLSSL> errores = new ArrayList<>();

        // Creamos el objeto de tipo Grammar, pasando como parámetro el ArrayList de Tokens y el ArrayList de errores
        Grammar gramatica = new Grammar(tokens, errores);

        // Agrupación con sintaxis correcta
        gramatica.group("FUNCION_COMPLET", "LLAVE_A PUNTO_COMA FUNCION PUNTO_COMA LLAVE_C");
````
Ahora bien, sabemos que todas las producciones (LLAVE_A, LLAVE_C, FUNCION, PUNTO_COMA) son de un solo token. Pero, ¿y si fueran de más de 100000 tokens cada una? EL mostrar el error inicial o final no es suficiente, sino que tenemos que hacer referencia a un componente. Si queremos indicar el componente, añadimos un parámetro más llamado indexComponent. El índice del componente del que haremos referencia será el de FUNCION. El siguiente código hará la agrupación del error en caso de que falte un PUNTO_COMA antes de FUNCION:

````java
        // Hacemos que en las agrupaciones de errores nos muestre la línea/columna inicial
        gramatica.initialLineColumn();
        /* Agrupación con sintaxis incorrecta, pasando como parámetro el nombre de la nueva producción,
           la expresión regular, el número de error, el mensaje de error y el componente de referencia 
         */
        gramatica.group("FUNCION_COMPLET", "LLAVE_A FUNCION PUNTO_COMA LLAVE_C",
                1, "Error sintáctico {}: Falta el punto y coma antes de la función [#, %]", 1);
````

Lo anterior nos mostraría lo siguiente en consola:

````
[Error sintáctico 1: Falta el punto y coma antes de la función [6, 23]]
````
El siguiente código hará la agrupación del error en caso de que falte un PUNTO_COMA después de FUNCION:

````java
	// Hacemos que en las agrupaciones de errores nos muestre la línea/columna final
        gramatica.finalLineColumn();
        /* Agrupación con sintaxis incorrecta, pasando como parámetro el nombre de la nueva producción,
           la expresión regular, el número de error, el mensaje de error y el componente de referencia 
         */
        gramatica.group("FUNCION_COMPLET", "LLAVE_A PUNTO_COMA FUNCION LLAVE_C",
                2, "Error sintáctico {}: Falta el punto y coma después de la función [#, %]", -2)
````

Después, nos mostraría lo siguiente en consola:
````
[Error sintáctico 2: Falta el punto y coma después de la función [6, 23]]
````
Si observamos bien, tanto el error sintáctico 1 y 2 están en la misma línea/columna debido a que la producción FUNCION está compuesta de un solo token. Si estuviera compuesta de más tokens, nos mostrará ya sea la línea/columna inicial/final en su respectivo caso. 

También podemos eliminar aquellas producciones o grupos de tokens que deseemos descartar. Mandaremos a llamar la función delete, la cual nos permite eliminar una producción ya sea de forma silenciosa o bien, agregando un mensaje de error. Supongamos que deseamos eliminar el punto y coma, argumentando que es un caracter inválido en nuestro lenguaje:

````java
	// Eliminamos cualquier producción con el nombre de PUNTO_COMA
        gramatica.delete("PUNTO_COMA", 2, "Error sintáctico {}: Caracter inválido [#, %]");
        // Mostramos en consola el ArrayList de errores
        System.out.println(errores);
````

Lo anterior nos mostrará lo siguiente en consola:

````
....................................................................................................
**** Se realizaron 1 eliminaciones de producciones llamadas "PUNTO_COMA" ****
La cantidad de producciones se redujo de 7 a 6

[Error sintáctico 2: Caracter inválido [8, 13]]
````

A continuación explicaremos como guardar nuestras agrupaciones en un ArrayList. Tomaremos como ejemplo los siguientes grupos de tokens:

````java
	// Declaramos los tokens
        Token tk1 = new Token("número", "TIPO_DATO", 1, 94);
        Token tk2 = new Token("$hola", "IDENTIFICADOR", 2, 56);
        Token tk3 = new Token("=", "OP_ASIG", 3, 65);
        Token tk4 = new Token("56", "VALOR", 4, 24);
        Token tk5 = new Token("flotante", "TIPO_DATO", 5, 76);
        Token tk6 = new Token("$kilometros", "IDENTIFICADOR", 6, 45);
        Token tk7 = new Token("=", "OP_ASIG", 7, 65);
        Token tk8 = new Token("45.78", "VALOR", 8, 15);
        // Agregamos los tokens a un ArrayList de tipo Token
        ArrayList<Token> tokens = new ArrayList<>();
        tokens.add(tk1);
        tokens.add(tk2);
        tokens.add(tk3);
        tokens.add(tk4);
        tokens.add(tk5);
        tokens.add(tk6);
        tokens.add(tk7);
        tokens.add(tk8);
````

Supongamos que deseamos agrupar aquellos tokens o producciones que inician con un tipo de dato, seguido de un identificador, un operador de asignación y un valor:

````java
        gramatica.group("IDENT_COMPLET", "TIPO_DATO IDENTIFICADOR OP_ASIG VALOR");
````

Lo anterior mostrará lo siguiente en consola:

````
....................................................................................................
**** Agrupación 1 "IDENT_COMPLET" realizada con éxito ****
Cantidad de componentes: 4
La cantidad de producciones se redujo de 8 a 2


**** Mostrando gramáticas ****

....................................................................................................
Produccion(IDENT_COMPLET, 1, 94, 4, 24, [
Token(número, TIPO_DATO, 1, 94),
Token($hola, IDENTIFICADOR, 2, 56),
Token(=, OP_ASIG, 3, 65),
Token(56, VALOR, 4, 24)])

....................................................................................................
Produccion(IDENT_COMPLET, 5, 76, 8, 15, [
Token(flotante, TIPO_DATO, 5, 76),
Token($kilometros, IDENTIFICADOR, 6, 45),
Token(=, OP_ASIG, 7, 65),
Token(45.78, VALOR, 8, 15)])
````

Ahora bien, supongamos que nosotros deseamos guardar esas producciones en un ArrayList de tipo Producción. Lo que tenemos que hacer primero es crear el ArrayList. Después, pasar dicho ArrayList como parámetro en el método group. Al final, imprimiremos dicho ArrayList:


````java
 	// Declaramos un ArrayList de tipo Producción para guardar los identificadores
        ArrayList<Production> identificadores = new ArrayList<>();

        gramatica.group("IDENT_COMPLET", "TIPO_DATO IDENTIFICADOR OP_ASIG VALOR", identificadores);

	// Mostramos el ArrayList
        for (Production ident : identificadores) {
            System.out.println("-".repeat(20));
            System.out.println(ident);
            System.out.println("-".repeat(20));
        }
````

Lo anterior mostrará lo siguiente en consola:

````
--------------------
Produccion(IDENT_COMPLET, 1, 94, 4, 24, [
Token(número, TIPO_DATO, 1, 94),
Token($hola, IDENTIFICADOR, 2, 56),
Token(=, OP_ASIG, 3, 65),
Token(56, VALOR, 4, 24)])
--------------------
--------------------
Produccion(IDENT_COMPLET, 5, 76, 8, 15, [
Token(flotante, TIPO_DATO, 5, 76),
Token($kilometros, IDENTIFICADOR, 6, 45),
Token(=, OP_ASIG, 7, 65),
Token(45.78, VALOR, 8, 15)])
--------------------
````
Ya hemos guardado nuestros identificadores en un ArrayList. Podemos acceder fácilmente a los tokens y a su vez, acceder ya sea al número de línea/columna, lexema o componente léxico del mismo. Primeramente mostraremos los tokens de ambas producciones:

````java
        for (Production ident : identificadores) {
            ArrayList<Token> tks = ident.getTokens();
            for (Token tk : tks) {
                System.out.println(tk);
            }
            System.out.println("-".repeat(20));
        }
````

Lo anterior mostrará lo siguiente en consola:

````
Token(número, TIPO_DATO, 1, 94)
Token($hola, IDENTIFICADOR, 2, 56)
Token(=, OP_ASIG, 3, 65)
Token(56, VALOR, 4, 24)
--------------------
Token(flotante, TIPO_DATO, 5, 76)
Token($kilometros, IDENTIFICADOR, 6, 45)
Token(=, OP_ASIG, 7, 65)
Token(45.78, VALOR, 8, 15)
--------------------
````

Puede darse el caso de que solo queramos algunos datos y no todo el token. Para ello, podemos usar los métodos lexemeRank, lexicalCompRank ó tokenRank, los cuales nos permiten acceder a un determinado rango de tokens y/o sus atributos. Por ejemplo, podemos creas un HashMap para almacenar el nombre del identificador y su valor para crear una tabla de identificadores. Lo haremos de la siguiente manera:

````java
        // Creamos un HashMap para guardar los identificador y sus valores
        HashMap<String, String> identifiers = new HashMap<>();

        for (Production ident : identificadores) {
            String tipo_dato = ident.lexemeRank(0);
            String identificador = ident.lexemeRank(1);
            String valor = ident.lexemeRank(-1);
            // Mostramos los lexemas extraídos
            System.out.println(String.format("El identificador %s de tipo %s es igual a %s", identificador, tipo_dato, valor));
            // Guardamos la llave y el valor en nuestro HashMap
            identifiers.put(identificador, valor);
        }

        // Mostramos en consola nuestro HashMap
        System.out.println(String.format("\n%s", identifiers));
````

Lo anterior mostrará lo siguiente en consola:

````
El identificador $hola de tipo número es igual a 56
El identificador $kilometros de tipo flotante es igual a 45.78

{$kilometros=45.78, $hola=56}
````

Una parte importante de todo compilador aparte del análisis léxico, sintáctico, semántico o lógico es que sea totalmente funcional. Debe de existir alguna manera en la que podamos acceder a cada una de las sentencias de forma individual para su posterior ejecución. Para hacer lo anterior, nos apoyaremos de la Clase CodeBlock y Functions. Supongamos que tenemos los siguientes Tokens:
````java
       	// Declaramos los tokens
        Token tk1 = new Token("SENTENCIA", "SENTENCIA", 1, 94);
        Token tk2 = new Token(";", "PUNTO_COMA", 1, 95);
        Token tk3 = new Token("SENTENCIA", "SENTENCIA", 2, 56);
        Token tk4 = new Token(";", "PUNTO_COMA", 2, 57);
        Token tk5 = new Token("SENTENCIA", "SENTENCIA", 3, 65);
        Token tk6 = new Token(";", "PUNTO_COMA", 3, 66);
        Token tk7 = new Token("{", "LLAVE_A", 4, 24);
        Token tk8 = new Token("SENTENCIA", "SENTENCIA", 5, 76);
        Token tk9 = new Token(";", "PUNTO_COMA", 5, 77);
        Token tk10 = new Token("SENTENCIA", "SENTENCIA", 6, 45);
        Token tk11 = new Token(";", "PUNTO_COMA", 6, 46);
        Token tk12 = new Token("{", "LLAVE_A", 7, 65);
        Token tk13 = new Token("SENTENCIA", "SENTENCIA", 8, 15);
        Token tk14 = new Token(";", "PUNTO_COMA", 8, 16);
        Token tk15 = new Token("}", "LLAVE_C", 9, 23);
        Token tk16 = new Token("SENTENCIA", "SENTENCIA", 10, 15);
        Token tk17 = new Token(";", "PUNTO_COMA", 10, 16);
        Token tk18 = new Token("}", "LLAVE_C", 11, 45);
        Token tk19 = new Token("SENTENCIA", "SENTENCIA", 12, 94);
        Token tk20 = new Token(";", "PUNTO_COMA", 12, 95);
	
        // Agregamos los tokens a un ArrayList de tipo Token
        ArrayList<Token> tokens = new ArrayList<>();
        tokens.add(tk1);
        tokens.add(tk2);
        tokens.add(tk3);
        tokens.add(tk4);
        tokens.add(tk5);
        tokens.add(tk6);
        tokens.add(tk7);
        tokens.add(tk8);
        tokens.add(tk9);
        tokens.add(tk10);
        tokens.add(tk11);
        tokens.add(tk12);
        tokens.add(tk13);
        tokens.add(tk14);
        tokens.add(tk15);
        tokens.add(tk16);
        tokens.add(tk17);
        tokens.add(tk18);
        tokens.add(tk19);
        tokens.add(tk20);
````

Ahora bien, si suponemos que los tokens anteriores fueron extraídos de algún código, se vería de la siguiente manera:

````
1	SENTENCIA;
2	SENTENCIA;
3	SENTENCIA;
4	{
5		SENTENCIA;
6		SENTENCIA;
7		{
8			SENTENCIA;
9		}
10		SENTENCIA;
11	}
12	SENTENCIA;
````

Podemos desplegar la estructura de nuestro código mediante un método de la clase Functions en varios bloques de código. El método en cuestión se llama splitCodeInCodeBlocks. Mandaremos como parámetro el arreglo de tokens, el bloque iniciador de código ('{'), el bloque terminador de código ('}') y el bloque terminador de sentencia (';'). El método nos generará un objeto de tipo CodeBlock, el cual imprimiremos en consola:

````java
        // Desplegamos el código en bloques de código
        CodeBlock code = Functions.splitCodeInCodeBlocks(tokens, "{", "}", ";");
        System.out.println(code);
````

La consola nos mostrará lo siguiente:

````
[12 líneas...]-->([3 líneas...]-->([3 líneas...]-->([1 líneas...]), [1 líneas...]), [1 líneas...])
````

Como puede observar, nos muestra la estructuración en bloques de nuestro código, divididos y agrupados mediante las sentencias y bloques iniciadores/terminadores. Lo anterior es meramente informativo. Para obtener el código agrupado en bloques en orden de ejecución, mandamos a llamar el método getBlocksOfCodeInOrderOfExec en el objeto de tipo CodeBlock:

````java
        System.out.println(code.getBlocksOfCodeInOrderOfExec());
````

Lo anterior nos mostrará lo siguiente en consola:

````
[~6da159e2-ce9f-483e-9aea-5c4a82f276f0~, SENTENCIA ;SENTENCIA ;SENTENCIA ;, ~e9ef04f0-2ccd-42fc-aa38-8af4031b63ed~, SENTENCIA ; SENTENCIA ;, ~54e8cf15-f1d8-4775-b7bd-346425a2efc4~, SENTENCIA ;, ~54e8cf15-f1d8-4775-b7bd-346425a2efc4~, SENTENCIA ;, ~e9ef04f0-2ccd-42fc-aa38-8af4031b63ed~, SENTENCIA ;, ~6da159e2-ce9f-483e-9aea-5c4a82f276f0~]
````
Podemos visualizar nuestro código dividido en varios segmentos. El inicio y final de un segmento está dividido por un marcador que inicia con el caracter ~, seguido de un UUID único, y termina con otro caracter ~.  Es decir, que tenemos dos marcadores por cada segmento: el inicial y final. Tanto el marcador inicial como final son exactamente el mismo. En el [videotutorial](https://youtu.be/AHGe8l_yG6s), vemos un ejemplo de ejecución con ciclos inventados para nuestro lenguaje de programación.

##### Nota
Muchos de los métodos están sobrecargados, pueden recibir distintas cantidades y combinaciones de parámetros, según lo que se desee que ejecute el método.

### ¿Cómo puedo ayudar?
El uso de la librería es totalmente gratuito, no necesita hacer nada en especial. Si usted lo desea, puede hacer una pequeña [donación](https://www.paypal.com/donate/?hosted_button_id=W8H3EFEBKQMKE) en PayPal, lo cual me motivaría a seguir haciendo herramientas que puedan ayudar a otros.

[![Donar](https://www.paypalobjects.com/es_XC/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donate/?hosted_button_id=W8H3EFEBKQMKE)

### Autor y Licencia
Copyright 2021-2022 by Yisus Efebei and M45t3r L3g10n
