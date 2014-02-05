GitHub Flavores Markdown
========================

GitHub.com utiliza su propia versión de sintaxis Markdown que provee un
conjunto de características adicionales, muchas de ellas para hacer más fácil
trabajar con el contenido en GitHub.com

Note que algunas de las características de [GitHub Flavored Markdown][GFM]
sólo están disponibles para las descripciones y comentarios de _issues_ y
_Pull Requests_. Estos incluyen @menciones así como referencias a _hashes_
SHA-1, _Issues_, y _Pull Requests_. Las listas de tareas también están
disponibles en comentarios de Gits y en archivos Gits Markdown.

Puedes utilizar Markdown en la mayoría de los lugares de GitHub:

  - [Gits](https://gist.github.com/)
  - Comentarios y _Issues_ y _Pull Requets_
  - En archivos con extensión `.md` o `.markdown`


## Bloques de Código _Fenced_ ##

El estándar Markdown convierte el texto que comienza con cuatros espacios en
cada línea en un bloque de código; GFM también soporta bloques de código. Sólo
encierra tu código en ```` ``` ```` (como se muestra enseguida) y no necesitarás
identar con cuatro espacios tu código. Note que los bloques de código
_Fenced_ no tienen que estar precedidos por una línea en blanco -- a
diferencia de los bloques de código identados -- aun así recomendamos colocar
una línea en blanco antes del bloque para hacer que el archivo fuente Markdown
sea más fácil de leer.

    Aquí un ejemplo:

    ```
    function test() {
      console.log("note que hay una línea en blanco antes del bloque");
    }
    ```

Tome en cuenta que, dentro de listas, deberá identar los bloques
_no-Fenced_ de código con _ocho_ espacios para que se interprete
correctamente.


## Resaltado de sintaxis ##

Los bloques de código pueden ir más haya agregando resaltado de sintaxis. En
su bloque _Fenced_, agregue de forma opcional el identificador de lenguaje y
nosotros haremos un resaltado de sintaxis apropiado. Por ejemplo, un resaltado
de código Ruby con [GitHub Flavored Markdown][GFM] sería así:

 [GFM]: https://help.github.com/articles/github-flavored-markdown

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("¡Hola Mundo!")
    puts markdown.to_html
    ```

y mostraría esto:

```ruby
require 'redcarpet'
markdown = Redcarpet.new("¡Hola Mundo!")
puts markdown.to_html
```

Nosotros utilizamos [Linguist][] para la detección del lenguaje y resaltado de
la sintaxis. Puedes encontrar los diferentes nombres de lenguajes aceptados en
este [archivo YAML][].

  [Linguist]: https://github.com/github/linguist
  [archivo YAML]: https://github.com/github/linguist/blob/master/lib/linguist/languages.yml

También puedes simplemente identar tu código con cuatro espacios:

        function fancyAlert(arg) {
            if(arg) {
                $.facebox({div:'#foo'})
            }
        }


## Links automáticos para URLs ##

Cualquier URL (como `http://www.github.com/`) será automáticamente convertido
en un link navegable.

como este de aquí http://www.github.com/ que fue solamente escrito entre el
texto del párrafo.


## Tachado ##

Cualquier palabra encerrada entre dos tildes (como `~~esto~~`) aparecerá
tachado; así:

Quiero ~~mandar un mensaje~~ a todos.


## Citas ##

Esto funciona igual que el estándar Markdown, pero para comprobar como
se ve, aquí un ejemplo:

```
> Así es como se ve un texto citado dentro de GitHub.
```

Resultado:

> Así es como se ve un texto citado dentro de GitHub.


## Tablas ##

Puedes crear tablas de una lista de palabras dividiéndolas por guiones `-`
(para la primera fila), y separar cada columna con un _pipe_ `|`:

```
    Primer Encabezado     | Segundo Encabezado
    --------------------- | ---------------------
    Contenido de la celda | Contenido de la celda
    Contenido de la celda | Contenido de la celda
```

Resulta en esto:

    Primer Encabezado     | Segundo Encabezado
    --------------------- | ---------------------
    Contenido de la celda | Contenido de la celda
    Contenido de la celda | Contenido de la celda

Para propósitos estéticos, puedes agregar _pipes_ extras a los lados:

    | Primer Encabezado     | Segundo Encabezado    |
    | --------------------- | --------------------- |
    | Contenido de la celda | Contenido de la celda |
    | Contenido de la celda | Contenido de la celda |

Note que cada guión del encabezado no necesita coincidir exactamente con la
longitud del texto del encabezado:

    | Nombre | Descripción          |
    | --------------- | ----------- |
    | Ayuda     | Muestra la ventana de ayuda. |
    | Cerrar    | Cierra la ventana     |

Incluso puedes incluir sintaxis Markdown en-línea como links, énfasis,
resaltado o tachado;

    | Nombre | Descripción          |
    | --------------- | ----------- |
    | Ayuda     | ~~Muestra la~~ ventana de ayuda. |
    | Cerrar    | _Cierra_ la ventana     |

Finalmente, incluyendo dos-puntos `:` dentro de la fila de encabezado, puedes
definir que el texto sea alineado a la izquierda, derecha o centrado:

    | Izquierda | Centrado | Derecha |
    | :-------- | :------: | ------: |
    | col 3 es  | algo de  |  $ 1600 |
    | col 2 es  | centrada |    $ 12 |
    | Zebra     | esta     |     $ 1 |

El signo de dos-puntos colocado del __lado-izquierdo__ indica alineación
hacia la izquierda para esa columna, el mismo signo colocado del
__lado-derecho__ para la alineación derecha y el mismo signo en __ambos__
lados indica alineación centrada.


## Emoji ##

GitHub soporta emoji :sparkles: :camel: :boom: Para ver la lista de
imágenes que soporta, da un vistazo a la [Hoja de Datos Emoji][Emoji].

[Emoji]: http://www.emoji-cheat-sheet.com/


* * *


## Sintaxis extra ##

La siguiente sintaxis de [GitHub Flavored Markdown][GFM]
sólo está disponibles para las descripciones y comentarios de _issues_ y
_Pull Requests_.


### Listas de Tareas ###

    - [x] Soporte de @menciones, #referencias, [links](), **formateo**, y de <del>etiquetas</del>
    - [x] lista de sintaxis requerida (cualquier lista des-ordenada y ordenada es soportada)
    - [x] esta es una tarea completa
    - [ ] esta es una tarea incompleta


### Referencias SHA ###

Cualquier referencia a un hash SHA-1 _commit_ será automáticamente convertido
en un link a ese _commit_ en GitHub.

```
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```


### Referencias _Issue_ dentro de un repositorio ###

Cualquier número que refiera a un _Issue_ o _Pull Request_ será
automáticamente convertido en un link.

    #1
    mojombo#1
    mojombo/github-flavored-markdown#1


### @menciones a usuario ###

Escribiendo un símbolo de `@`, seguido del nombre-de-usuario, notificará a
esa persona para que venga y vea el comentario. Esto es conocido como
"@mención", porque tu estas mencionando a la persona. También puedes
@mencionar equipos dentro de una organización.


* * *

__Referencias__

 - [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown)
 - [Mastering Markdown](http://guides.github.com/overviews/mastering-markdown/)