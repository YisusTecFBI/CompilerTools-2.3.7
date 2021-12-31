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
 código a ejecutar.</div>
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
