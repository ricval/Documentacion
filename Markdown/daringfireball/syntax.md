Markdown: Sintaxis
==================

*   [Resumen](#resumen)
    *   [Filosofía](#filosofía)
    *   [HTML en línea](#html-en-línea)
    *   [Escape automático para Caracteres Especiales](#escape-automático-para-caracteres-especiales) 

*   [Elementos de Bloque](#elementos-de-bloque)
    *   [Párrafos y saltos de línea](#párrafos-y-saltos-de-línea)
    *   [Encabezados](#encabezados)
    *   [Blockquotes](#blockquotes)
    *   [Listas](#listas)
    *   [Bloques de Código](#bloques-de-código)
    *   [Barras Horizontales](#barras-horizontales)

*   [Elementos de segmento](#elementos-de-segmento)
    *   [Links](#links)
    *   [Énfasis](#Énfasis)
    *   [Código](#código)
    *   [Imágenes](#imágenes)

*   [Misceláneo](#misceláneo)
    *   [Links Automáticos](#links-automáticos)
    *   [Escape de Backslash](#escapes-con-diagonal-inversa) 

**Nota:** Este documento es una traducción del sitio oficial que está en Inglés
[daringfireball : syntax][src].

  [src]: http://daringfireball.net/projects/markdown/syntax


* * *

## Resumen ##

### Filosofía ###

Markdown tiene el propósito de hacer el fácil-de-leer y fácil-de-escribir
tanto como sea posible.

La legibilidad, es el énfasis sobre todo lo demás. Un documento con formato
Markdown debería publicarse así tal cual, en texto plano, sin vista como si
hubiera sido marcado con etiquetas o instrucciones de formateo. Mientras que
la sintaxis de Markdown a sido influenciado severamente por filtros
texto-a-HTML existentes -- incluyendo [Setext] [1], [atx] [2], [Textile] [3],
[reStructuredText] [4], [Grutatext] [5], y [EtText] [6] -- la gran
inspiración para la sintaxis de Markdown es el formato de texto plano de los
email (correos electrónicos).

[1]: http://docutils.sourceforge.net/mirror/setext.html
[2]: http://www.aaronsw.com/2002/atx/
[3]: http://textism.com/tools/textile/
[4]: http://docutils.sourceforge.net/rst.html
[5]: http://www.triptico.com/software/grutatxt.html
[6]: http://ettext.taint.org/doc/

Para ello, la sintaxis de Markdown está compuesta enteramente por caracteres
de puntuación, caracteres de puntuación que han sido cuidadosamente
seleccionados con el fin de que parezcan lo que significan. Por ejemplo, los
asteriscos al rededor de una palabra se ven como un \*enfatizado\*. Una lista
Markdown se ve, pues bien, como una lista. Incluso los _blockquotes_ se ven
como pasajes de texto citado, suponiendo que alguna vez has utilizado el
formato de email.



### HTML en línea ###

La sintaxis Markdown está inspirada por un propósito: ser utilizado como
formato de *escritura* para la web.

Markdown no es un remplazo del HTML, ni se acerca a eso. Su sintaxis es muy
pequeña, correspondiente solamente a un pequeño sub-conjunto de etiquetas
HTML. La idea *no* es crear una sintaxis que haga más fácil insertar
etiquetas HTML. En mi opinión, las etiquetas HTML ya son fáciles de insertar.
La idea de Markdown es hacer más fácil la lectura, escritura e edición. HTML
es un formato de *publicación*; Markdown es un formato de *escritura*. Así,
la sintaxis y formateo Markdown sólo se ocupa de cuestiones que puedan ser
transmitidas en texto plano.

Para cualquier marcado que no este cubierto por la sintaxis de Markdown,
simplemente utilice HTML. No hay necesidad de escribir un prólogo o una
delimitante para indicarle que puede alternar entre Markdown y HTML; sólo
utilice las etiquetas HTML donde le sea conveniente.

Las únicas restricciones son que los elementos HTML de nivel-de-bloque
-- Ejem. `<div>`, `<table>`, `<pre>`, `<p>`, etc. -- deberán estar separadas
del contenido subyacente por lineas en blanco, y las etiquetas de inicio y
final del bloque no deben estar identadas con tabuladores o espacios.
Markdown no es lo suficientemente listo para agregar una etiqueta `<p>` extra
(faltante) que cubra una etiqueta de nivel-de-bloque HTML.

Por ejemplo, para agregar una tabla HTML para un artículo Markdown:

    Este es un párrafo normal.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    Este es otro párrafo normal.

Nota que la sintaxis de formateo Markdown no está procesando el interior de
las etiquetas de nivel-de-bloque HTML. Ejem., no puedes utilizar `*énfasis*`
estilo-Markdown dentro del bloque HTML.

Las etiquetas nivel-de-segmento HTML -- ejem. `<span>`, `<cite>`, o `<del>`
-- pueden ser utilizadas en cualquier lugar dentro de un párrafo Markdown,
_items_ de listas o encabezados. Si quieres, puedes incluso utilizar
etiquetas HTML en lugar de un formato Markdown; ejem. si prefieres utilizar
etiquetas HTML `<a>` o `<img>` en lugar de la sintaxis de links o imágenes,
adelante.

A diferencia de las etiquetas HTML nivel-de-bloque, la sintaxis Markdown
*es* procesada dentro de las etiquetas nivel-de-segmento.


### Escape automático para Caracteres Especiales ###

En HTML, hay dos caracteres que requieren tratamiento especial: `<` y `&`.
El carácter de menor-que que es utilizado para comenzar una etiqueta; y los
ampersons que son utilizados para denotar entidades HTML. Si quieres utilizar
estos como caracteres literales, debes escaparlos como entidades, ejem.
`&lt;`, y `&amp;`.

Los ampersons son particular molestos para los escritores web. Si quieres
escribir acerca de 'AT&T', necesitas escribir '`AT&amp;T`'. Incluso necesitas
escapar ampersosns dentro de URLs. Así que, si quieres un link a:

    http://images.google.com/images?num=30&q=larry+bird

necesitas codificar la URL así:

    http://images.google.com/images?num=30&amp;q=larry+bird

en tu atributo `href` de la etiqueta de enlace. Sobra decir, que es fácil
olvidarlo, y es probablemente el error de validación HTML más común.

Markdown te permite utilizar estos caracteres de forma natural, tomando
cuidado de todo lo necesario para escaparlos por ti. Si utilizas un amperson
como parte de una entidad HTML, se mantendrá sin cambios; de lo contrario
será traducido a `&amp;`.

Veamos, si quieres incluir un símbolo de derechos de _copyright_, puedes
escribir:

    &copy;

y Markdown lo dejara pasar. Pero si escribes:

    AT&T

Markdown lo traducirá a:

    AT&amp;T

Similarmente, porque Markdown soporta [HTML en línea](#html), si utilizas
símbolos menor-que como delimitaros de etiquetas HTML, Markdown los tratará
como se espera. Pero si escribes:

    4 < 5

Markdown los traducirá a:

    4 &lt; 5

Sin embargo, dentro de bloques y códigos de segmento Markdown, el símbolo
menor-que y los ampersons *siempre* serán codificados automáticamente. Esto
hace más fácil el uso de Markdown para escribir sobre código HTML.
(Contrario al HTML directo, que es un terrible formato de escritura para
sintaxis HTML, porque cada `<` y cada `&` en tu código de ejemplo necesitará
ser escapado.)

* * *

## Elementos de Bloque ##


### Párrafos y saltos de línea ###

Un párrafo es una o más líneas de texto consecutivas, separadas por uno o más
líneas en blanco. (Una línea en blanco es cualquier línea que se vea como una
línea en blanco -- una línea que no contiene nada pero los espacios o 
tabulaciones son considerados espacios en blanco.) Un párrafo normal no
debería ser identando con espacios o tabulaciones.

La implicación de la regla "uno o más lineas consecutivas de texto" es que
Markdown soporta párrafos de texto con "ajuste-de-ancho-duro" (que significa
que al llegar al limite de ancho de caracteres, se agrega un retorno, una
nueva línea comienza a escribirse, pero siendo parte del mismo párrafo o
renglón. Este difiere significativamente de la mayoría de otros formatos
texto-a-HTML (incluyendo Tipo Movibles con la opción de "Convertir Saltos
de Línea" ) que traduce cada carácter de salto de línea de un párrafo en una
etiqueta `<br />`.

Cuando quieras insertar una etiqueta de corte `<br />` usando Markdown,
termina tu línea con dos o más espacios, después teclea un retorno.

Sí, esto toma un poco más de esfuerzo que crear un `<br />`, pero la regla de
que "cada salto de línea es un `<br />`" no funciona para Markdown. El
estilo-email de Markdown [blockquoting][bq] y multi-parrafo
[lista de items][1] trabaja mejor -- y se ve mejor -- cuando utilizas un
formato de salto de líneas duro.

  [bq]: #blockquote
  [l]:  #list



### Encabezados ###

Markdown soporta dos estilos de encabezados, [Setext][1] y [atx][2].

Los encabezados estilo-Setext son "subrayados" utilizando el signo de igual
(para el primer-nivel de encabezado) y guiones (para el segundo-nivel de
encabezados). Por ejemplo:

```markdown
Esto es un H1
=============

Esto es un H2
-------------
```

Cualquier cantidad de subrayado `=` o `-` funcionará.

Los encabezados estilo-atx utilizan de 1-6 caracteres de gato o _hash_ al
comienzo de la línea, que corresponden al nivel de encabezado. Por ejemplo:

```markdown
# Este es un H1

## Este en un H2

###### Este es un H6
```

Opcionalmente, puedes "cerrar" los encabezados estilo-atx. Esto es meramente
estético -- puedes utilizar esto si piensas que se ve mejor. Los _hashes_ de
cerrado no necesitan coincidir con los _hashes_ de apertura del encabezado.
(Ya que el número de _hashes_ de apertura determinan el nivel del
encabezado.):

```markdown
# Este es un H1 #

## Este es un H2 ##

### Este en un H3 ######
```



### Blockquotes ###

Markdown utiliza el carácter `>` del estilo-email para _blockquoting_. Si
estas familiarizado con texto citado en un mensaje de email, entonces sabes
como crear un _blockquote_ en Markdown. Se ve mejor si utilizas ajuste duro
de texto y colocas un `>` antes de cada línea:

    > Esto es un blockquote con dos parrafos. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    >
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown te permite ser flojo porque solo necesitas poner el `>` al inicio de
la primer línea de un párrafo con ajuste-duro:

    > Esto es un blockquote con dos parrafos. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Los _blockquotes_ pueden estar anidados (ejem. un blockquote-dentro-de-un-
blockquote) agregado un nivel adicional de `>`:

    > Este es el primer nivel de citado.
    >
    > > Este es un blockquote anidado.
    >
    > De regreso al primer nivel.

Los _Blockquotes_ pueden contener otros elementos Markdown, incluyendo
encabezados, listas, y bloques de código:

```markdown
> ## Este es un encabezado.
>
> 1.    Este es el primer _item_ de la lista.
> 2.    Este es el segundo _item_ de la lista.
>
> Aquí algo de código de ejemplo:
>
>       return shell_exec("echo $input | $markdown_script");

```

Renderizado se ve así:

* * *

> ## Este es un encabezado.
>
> 1.    Este es el primer _item_ de la lista.
> 2.    Este es el segundo _item_ de la lista.
>
> Aquí algo de código de ejemplo:
>
>       return shell_exec("echo $input | $markdown_script");

* * *

Cualquier editor decente debería poder hacer el citado de texto estilo-email
fácilmente. Por ejemplo, con BBEdit, puedes hacer una selección y elegir
Incrementar el Nivel de Citado desde el menú de Texto.



### Listas ###

Markdown soporta listas ordenadas (numeradas) y des-ordenadas (viñetas).

Las listas des-ordenadas utilizan asteriscos, pulsos o guiones
-- intercambiables -- como marcadores de lista:

    *   Rojo
    *   Verde
    *   Azul

es equivalente a:

    +   Rojo
    +   Verde
    +   Azul

y:

    -   Rojo
    -   Verde
    -   Azul

Las listas ordenadas utilizan números seguidos por un punto:

    1.  Pájaro
    2.  Zorro
    3.  Pez

Es importante notar que los números que utilizas para hacer el listado no
tienen efecto en el HTML de salida que produce Markdown. El HTML que produce
Markdown del ejemplo de listado anterior sería así:

```html
<ol>
<li>Pájaro</li>
<li>Zorro</li>
<li>Pez</li>
</ol>
```

Renderizado se vería así:

* * *

  1.  Pájaro
  2.  Zorro
  3.  Pez

* * *

Si escribes una lista en Markdown que se vea así:

    1.  Pájaro
    1.  Zorro
    1.  Pez

o incluso así:

    3.  Pájaro
    1.  Zorro
    8.  Pez

obtendrás la misma salida HTML. La idea es, que si quieres, puedes utilizar
números secuenciados en tus listas ordenas Markdown, para que los números en
tu fuente coincidan con los números en tu HTML publicado. Pero si quieres ser
flojo, no tienes que hacerlo.

Si utilizas una lista numerada floja, aún así deberías comenzar la lista con
el número 1. En algún punto en el futuro, Markdown puede soportar el comienzo
de listas ordenadas con cualquier número.

Los marcadores de listado normalmente comienzan en el margen izquierdo, pero
pueden estar identadas por uno o tres espacios. Los marcadores de espacios
deben ser seguidos por uno o más espacios o un tabulador.

Para hacer que las listas se vean bien, puedes ajustar los _items_ con la
misma identación:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

Pero si quieres ser flojo, no tienes que hacerlo:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

Si los _items_ de la lista están separados por líneas en blanco, Markdown
envolverá el _item_ en una etiqueta `<p>` en la salida HTML. Por ejemplo,
esta entrada:

    *   Pájaro
    *   Magia

se transformará en este código HTML:

```html
<ul>
<li>Pájaro</li>
<li>Magia</li>
</ul>
```

renderizado se verá así:

* * *

*   Pájaro
*   Magia

* * *

Pero este:

    *   Pájaro

    *   Magia

se transformará en:

```html
<ul>
<li><p>Pájaro</p></li>
<li><p>Magia</p></li>
</ul>
```

Los _items_ de las listas pueden consistir en múltiples párrafos. Cada párrafo
subsecuente en la lista de _items_ debería ser identado por cuatro espacios o
un tabulador:

    1.  Este es un item de la lista con dos párrafos. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

Se ve bien si identaste cada línea de los párrafos subsecuentes, pero aquí
también, Markdown te permite ser flojo:

    *   Este es un item de la lista con dos párrafos.

        Este es el segundo párrafo en la lista de _items_. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Otro item en la misma lista.

Para colocar un _blockquote_ dentro de un _item_ de una lista, el delimitador
`>` necesita ser identado:

    * Un item de las litas con un blockquote:

        > Este es un blockquote
        > dentro del item de una lista.

Para colocar un bloque de código dentro de un _item_ de una lista, el bloque
de código necesita ser identado *dos veces* -- 8 espacios o dos tabulaciones:

    *   Un item de la lista con un bloque de código:

            <el código va aquí>

Vale la pena señalar que es posible activar un lista ordenada por accidente,
escribiendo algo así:

    1986. Que gran temporada.

En otras palabras, una secuencia *número-punto-espacio* al comienzo de una
línea. Para evitar esto, puedes utilizar un escape con diagonal-invertida para
el punto:

    1986\. Que gran temporada.



### Bloques de Código ###

Los bloques de código pre-formateado son utilizados para escribir acerca de
programación o remarcar un código fuente. Mejor que los párrafos normales, las
líneas con un bloque de código son interpretadas literalmente. Markdown
envuelve un bloque de código con ambas etiquetas `<pre>` y `<code>`.

Para producir un bloque de código en Markdown, simplemente identa cada línea
del bloque con por lo menos 4 espacios o 1 tabulador. Por ejemplo, dando esta
entrada:

    Este es un párrafo normal:

        Este es un bloque de código.

Markdown generará:

```html
<p>Esto es un párrafo normal:</p>

<pre><code>Esto es un bloque de código.</code></pre>
```

Un nivel de identación -- 4 espacios o 1 tabulador -- es removido de cada
línea del bloque de código. Por ejemplo, esto:

    Este es un ejemplo de AppleScript:

        tell application "Foo"
            bee
        end tell

se convertirá en:

```html
<p>Este es un ejemplo de AppleScript:</p>

<pre><code>tell application "Foo"</code></pre>
    beep
end tell
</code></pre>
```

que se verá así:

* * *

Este es un ejemplo de AppleScript:

    tell application "Foo"
        bee
    end tell

* * *

Un bloque de código continua hasta encontrarse con una línea que no esté
identada (o el final del articulo).

Dentro de un bloque de código, el amperson (`&`) y los paréntesis triangulares
(`<` y `>`) son automáticamente convertidos a entidades HTML. Esto hace más
simple para incluir ejemplos de códigos fuente HTML utilizando Markdown --
solo pegue e idente, y Markdown se encargara de como codificar los ampersons y
los símbolos. Por ejemplo, esto:

        <div class="footer">
            &copy; 2004 Corporación Foo
        </div>

se convertirá en:

```html
<pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Corporación Foo
&lt;/div&gt;
</code></pre>
```

La sintaxis regular de Markdown no procesará el contenido de los bloques de
código. Ejem., los asteriscos son sólo asteriscos literales dentro de un
bloque de código. Esto significa que también es fácil utilizar Markdown para
escribir acerca de la propia sintaxis de Markdown.



### Barras Horizontales ###

Puedes crear una etiqueta de barra horizontal (`<hr>`) colocando tres o más
asteriscos, o guiones-medios en una línea. Si deseas, puedes colocar espacios
en blanco entre cada guión-medio o asterisco. Cada uno de los siguientes
ejemplos producirá una barra horizontal:

    * * *

    ***

    *****

    - - -

    ---------------------------------------


* * *



## Elementos de Segmento ##

### Links ###

Markdown soporta dos tipos de links: *en-línea* y *por-referencia*.

En ambos estilos, el texto del link está delimitado por [paréntesis
cuadrados].

Para crear un links en-línea, utiliza un par de paréntesis cuadrados con el
texto del link, seguido por un par de paréntesis normales que contiene la URL
a donde quieres que apunte tu link, *opcional* al lado puedes poner un titulo
del link, encerrado por comillas. Por ejemplo:

```markdown
Esto es [un ejemplo](http://ejemplo.com/ "Título") de un link en línea.

  [Este link](http://ejemplo.net/) no tiene el atributo de título.
```

producirá:

```html
<p>Este es <a href="http://ejemplo.com/" title="Título">de un link en línea.</a></p>

<p><a href="http://ejemplo.net/">Este link</a> no tiene el atributo de título.</p>
```

que se verá así:

* * *

Esto es [un ejemplo](http://ejemplo.com/ "Título") de un link en línea.

[Este link](http://ejemplo.net/) no tiene el atributo de título.

* * *

Si te estás refiriendo a un recurso local en el mismo servidor, puedes
utilizar rutas relativas:

```markdown
Vea mi pagina [Acerca de](/acerca/) para más detalles.
```

Los links estilo por-referencia utilizan un segundo par de paréntesis
cuadrados, dentro del cual debes colocar una etiqueta para seleccionar un
identificado del link:

```markdown
Esto es [un ejemplo][id] de un link por-referencia.
```

Opcionalmente puedes utilizar un espacio para separar el par de paréntesis:

```markdown
Esto es [un ejemplo] [id] de un link por-referencia.
```

Entonces, en cualquier lugar del documento, puedes definir la dirección de tu
etiqueta de link así, en una línea:

```markdown
    [id]: http://ejemplo.com/  "Título opcional aquí"
```

Esto es:

*   Los paréntesis cuadrados contienen el identificador del link
    (opcionalmente identados del margen izquierdo utilizando más de tres
    espacios);
*   seguido por signo de dos-puntos;
*   seguido por uno o mas espacios (o tabulaciones);
*   seguido por la URL del link;
*   opcionalemente seguido por el atributo de título del link, encomillado
    por comillas simples o dobles, o encerrado en paréntesis.

Las siguientes tres definiciones de links son equivalentes:

```markdown
    [foo]: http://ejemplo.com/  "Título opcional aquí"
    [foo]: http://ejemplo.com/  'Título opcional aquí'
    [foo]: http://ejemplo.com/  (Título opcional aquí)
```

**Nota: Hay un bug conocido en Markdown.pl 1.0.1 que impide encomillado simple
**para delimitar los títulos de los links.

La URL del link debería, opcionalmente, ser envuelta por paréntesis
triangulares:

```markdown
    [id]: <http://ejemplo.com/>  "Título opcional aquí"
```

Puedes colocar el atributo de título en la siguiente línea y utilizar espacios
extra o tabulaciones para dar espaciado, y así se vea mejor las URL muy
largas:

```markdown
    [id]: http://ejemplo.com/largisima/ruta/a/el/recurso/del/enlace
        "Título opcional aquí"
```

Las definiciones de los links son utilizados solamente para crear links
durante el procesado de Markdown, y son quitados de tu documento de salida
HTML.

Los nombres de las definiciones de links pueden consistir en letras, números,
espacios y signos de puntuación -- pero *no* son sensibles a mayúsculas o
minúsculas. Ejem. Estos dos links:

    [texto de link][a]
    [texto de link][A]

son equivalentes.

La forma corta para *nombres de enlaces implícitos* permiten omitir el nombre
del link, en ese caso se utiliza el propio nombre del link como nombre. Sólo
utiliza un conjunto de paréntesis cuadrados vacíos -- Ejem., para hacer un
link de la palabra "Google" al sitio web google.com, puedes simplemente
escribir:

    [Google][]

Y después define del link:

    [Google]: http://google.com/

Debido a que los nombres de los links pueden contener espacios, esta forma
corta puede incluso funcionar para múltiples palabras en el texto del link:

    Visita [Daring Fireball][] para más información.

Y después define el link:

    [Daring Fireball]: http://daringfireball.net/

Las definiciones de los Links pueden ser colocadas donde sea en tu documento
Markdown. Yo acostumbro a colocarlos inmediatamente después de cada párrafo en
el que los he utilizado, pero si quieres, puedes colocarlos todos al final de
tu documento, como si fueran notas de pie de página.

Aquí un ejemplo de links de referencia en acción:

```markdown
Tengo 10 veces más trafico de [Google] [1] que de [Yahoo] [2] o [MSN] [3].

    [1]: http://google.com/         "Google"
    [2]: http://search.yahoo.com/   "Yahoo Search"
    [3]: http://search.msn.com/     "MSN Search"
```

Utilizando la forma corta con el nombre implícito, podrías escribirlo:

```markdown
Tengo 10 veces más trafico de [Google][] que de
[Yahoo][] o [MSN][].

    [google]: http://google.com/        "Google"
    [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
    [msn]:    http://search.msn.com/    "MSN Search"
```

Ambos ejemplos anteriores producirán la siguiente salida HTML:

```html
<p>Tengo 10 veces más trafico de <a href="http://google.com/"
title="Google">Google</a> que de <a href="http://search.yahoo.com/"
title="Yahoo Search">Yahoo</a> o <a href="http://search.msn.com/"
title="MSN Search">MSN</a>.</p>
```

Para comparación, aquí está el mismo párrafo escrito utilizando estilo
en-línea Markdown:

```markdown
Tengo 10 veces más trafico de [Google](http://google.com/ "Google")
que de [Yahoo](http://search.yahoo.com/ "Yahoo Search")
o [MSN](http://search.msn.com/ "MSN Search").
```

El punto de los enlaces estilo por-referencia no es que sean más fáciles de
escribir. El punto es que con los enlaces estilo por-referencia, tu documento
fuente es mucho más legible. Compara los ejemplos de arriba: utilizando
enlaces estilo por-referencia, el párrafo por si sólo cuenta con solo 81
caracteres; con los enlaces estilo en-línea, éste es de 176 caracteres; y como
HTML es de 234 caracteres. En el HTML, hay más marcado que en el texto.

Con enlaces estilo por-referencia Markdown, el documento fuente se asemeja más
a la salida final, como es interpretado por el navegador. Haciendo que la
información relacionada a los enlaces estén fuera del párrafo, así puedes
agregar enlaces sin interrumpir el flujo de la lectura.


### Énfasis ###

Markdown trata los asteriscos (`*`) y guiones-bajos (`_`) como indicadores de
énfasis. El texto envuelto entre un `*` ó `_` será envuelto por una etiqueta
HTML `<em>`; doble `*` o `_` serán envueltos con etiquetas HTML `<strong>`.
Ejem., ésta estrada:

    *asteriscos simple*
    
    _guión-bajo simple_
    
    **asteriscos dobles**
    
    __guión-bajo dobles__

producirá:

```html
<em>asteriscos simple</em>

<em>guión-bajo simple</em>

<strong>asteriscos dobles</strong>

<strong>guión-bajo dobles</strong>
```

que se verá así:

* * *

*asteriscos simple*

_guión-bajo simple_

**asteriscos dobles**

__guión-bajo dobles__

* * *

Puedes utilizar cualquier estilo que prefieras; la única restricción es que el
mismo carácter debe ser utilizado para abrir y cerrar el texto a enfatizar.

El enfatizado puede ser utilizado en medio de una palabra:

```markdown
por*increíble*que parezca.
```

Pero si rodeas un `*` ó un `_` con espacios, será tratado como un asterisco o
guión-bajo normal.

Para producir un asterisco o guión-bajo normal en una lugar donde de otro modo
sería utilizado como delimitador de énfasis, puedes utilizar una diagonal
invertida para escaparlo:

    \*este texto está rodeado por asteriscos normales\*



### Código ###

Para indicar un segmento de código, envuélvalo con un apostrofe invertido
(`` ` ``). A diferencia de los bloques de código pre-formateado, un segmento
de código muestra código dentro de un párrafo normal. Por ejemplo:

    Utilice la función `printf()` para imprimir texto.

Esto producirá:

```html
<p>Utilice la función <code>prinf()</code> para imprimir texto.</p>
```

que se verá así:

* * *

Utilice la función `printf()` para imprimir texto.

* * *

Para incluir un carácter de apostrofe invertido literal dentro de un segmento
de código, puede utilizar múltiples apostrofes inversos como delimitadores de
apertura y cerrado:

    ``Aquí se muestra (`) un apostrofe invertido.``

lo que producirá esto:

```html
<p><code>Aquí se muestra (`) un apostrofe invertido.</code></p>
```

Los delimitadores apostrofes inversos que rodean un segmento de código pueden
incluir espacios -- uno después de la apertura, uno antes del cerrado. Esto le
permite colocar un apostrofe literal al comienzo y final de su segmento de
código:

    Un apostrofe invertido en un segmento de código: `` ` ``

    Un texto delimitador-apostrofe-invertido en un segmento de
    código: `` `foo` ``

producirá el HTML:

```html
<p>Un apostrofe invertido en un segmento de código: <code>`</code></p>

<p>Un texto delimitador-apostrofe-invertido en un segmento de código: <code>`foo`</code></p>
```

que se verá:

* * *

Un apostrofe invertido en un segmento de código: `` ` ``

Un texto delimitador-apostrofe-invertido en un segmento de
código: `` `foo` ``

* * *

Con un segmento de código, los apersons y los paréntesis triangulares son
codificados automáticamente en entidades HTML, lo que hace fácil el incluir
ejemplos de etiquetas HTML. Markdown convertirá esto:

    Por favor no utilice ninguna etiqueta `<blink>`.

en esto:

```html
<p>Por favor no utilice ninguna etiqueta <code>&lt;blink&gt;</code>.</p>
```

que se ve así:

* * *

Por favor no utilice ninguna etiqueta `<blink>`.

* * *

Puede escribir esto:

    `&#8212;` es la codificación-decimal equivalente de `&mdash;`.

para producir este resultado HTML:

```html
<p><code>&amp;#8212;</code>es la codificación-decimal equivalente de <code>&amp;mdash;</code>.</p>
```

que se verá así:

* * *

`&#8212;` es la codificación-decimal equivalente de `&mdash;`.

* * *



### Imágenes ###

La verdad es que es bastante difícil idear una sintaxis "natural" para colocar
imágenes dentro de un documento de texto plano.

Markdown utiliza una sintaxis para las imágenes parecida a la sintaxis
utilizada para los links, aplicable para los dos estilos: *en-línea* y
*por-referencia*.

La sintaxis para el estilo en-línea se ve así:

```markdown
![Texto Alt](/ruta/de/la/imagen.jpg)

![Texto Alt](/ruta/de/la/imagen.jpg "Título opcional")
```

Esto es:

*   Un signo de exclamación `!`;
*   seguido por un par de paréntesis cuadrados, que contienen el atributo
    `alt` del texto de la imagen;
*   seguido por un par de paréntesis, que contienen la URL de la ruta de la
    imagen, y el atributo `title` opcional, encerrado con comillas dobles o
    simples.

La sintaxis para el estilo por-referencia se ve así:

    ![Texto Alt][id]

Donde "id" es el nombre de la referencia definida de la imagen. Las
referencias de las imágenes utilizan la misma sintaxis que los links
por-referencia:

    [id]: ruta/de/la/imagen.jpg     "Atributo _title_ opcional"

Markdown no tiene sintaxis para especificar las dimensiones de una imagen; si
ésto es importante para usted, puede sencillamente utilizar la etiqueta HTML
`<img>`.


* * *


## Misceláneo ##

### Links Automáticos ###

Markdown soporta una forma corta para crear links en "automático" para URLs y
direcciones de correo electrónico: simplemente encierre las URL o direcciones
de correo con paréntesis triangulares. Lo que significa que quieres mostrar el
texto actual de la URL o email, y a la vez que sea un link a dicha dirección,
puedes hacer esto:

    <http://ejemplo.com/>

Markdown lo convertirá en esto:

```html
<a href="http://ejemplo.com/">http://ejemplo.com/</a>
```

Los links automáticos para direcciones de correo electrónico funcionan de
forma similar, excepto que Markdown los transformará un poco por decimales
aleatorios y codificará en entidades hexadecimales para ayudar a ofuscar tu
dirección de _spambots_ recolectores de direcciones. Por ejemplo, Markdown
transformará esto:

    <address@example.com>

en algo como esto:

```html
<a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
&#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>
```

Ésto será interpretado en el navegador como un link enlazado
a "address@example.com".

así:

* * *

<address@example.com>

* * *

(Este pequeño truco de codificación-en-entidades engañara a varios, si no es
(que a muchos, _bots_ recolectores de direcciones, pero en definitiva no
(engañara a todos. Esto es mejor que nada, pero una dirección publicada de
(esta forma problamente comenzará a recibir _spam_.)



### Escapes con Diagonal-Inversa ###

Markdown te permite utilizar escapes con diagonal-inversa para generar
caracteres literales que de otra forma tendrían un significado especial dentro
de la sintaxis de Markdown. Por ejemplo, si querías rodear una palabra con
asteriscos de forma literal (sin que el contenido quedara escapado dentro de
etiquetas HTML `<em>`), puedes utilizar una diagonal-inversa antes de cada
asterisco, así:

    \*asteriscos literales\*

render:

* * *

\*asteriscos literales\*

* * *

Markdown provee escapes con diagonal-inversa para los siguientes caracteres:

    \   diagonal inversa
    `   apostrofe inverso
    *   asterisco
    _   guión bajo
    {}  llaves
    []  paréntesis cuadrados
    ()  paréntesis
    #   _hash_
    +   signo de suma
    -   signo de resta (guión)
    .   punto
    !   signo de exclamación
