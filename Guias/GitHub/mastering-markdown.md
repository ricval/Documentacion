Maestría en _Markdown_
======================

Traducción de [Mastering Markdown][mastering-markdown_EN]. `2014.02.07`.

[mastering-markdown_EN]: http://guides.github.com/overviews/mastering-markdown/

  - [Introducción](#introducción)
  - [¿Qué es Markdown?](#qué-es-markdown)
  - [Ejemplos](#ejemplos)
  - [Sintaxis básica](#sintaxis-básica)
  - [GFM](#gfm)


## Introducción ##

Markdown es un lenguaje de formateo ligero, con una sintaxis fácil-de-usar para dar formato a todos los formularios o escribir en la plataforma GitHub.

**Qué vas a aprender:**

  - Como el formato Markdown hace la edición más fácil.
  - Como Markdown se diferencia del formateo tradicional.
  - Como utilizar Markdown para dar formato a tu texto.
  - Como GitHub hace una interpretación automática de Markdown.
  - Como aplicar las características Markdown únicas de GitHub.



## ¿Qué es Markdown? ##

Markdown es la forma de dar estilo al texto en la web. Controlas la forma en como se ve un documento; dando formato a las palabras como hacerlas negritas o itálicas, agregar imágenes, y creando listas, estás son solo algunas de las cosas que puedes hacer con Markdown. En general, Markdown es sólo un texto normal con un poco de caracteres no-alfabeticos en él, como `#` o `*`.

Puedes utilizar Markdown en la mayoría de los lugares de GitHub:

  - [Gits][]
  - Comentarios en _Issues_ y _Pull Request_
  - Archivos con extención `.md`o `.markdown`

[Gits]: https://gist.github.com/


## Ejemplos ##

#### Texto


  | Es bastante sencillo convertir algunas palabras en \*\*negritas\*\* y otras en \*italicas\* con Markdown. Incluso puedes hacer un \[link a Google\]\(http://google.com\). |
  |:-------|
  | Es bastante sencillo convertir algunas palabras en **negritas** y otras en *italicas* con Markdown. Incluso puedes hacer un [link a Google](http://google.com). |



## Sintaxis básica ##

Aquí un resumen de la sintaxis de Markdown que puedes utilizar en cualquier lugar de GitHub.com o en tus archivos de texto.

### Encabezados

    # Este es una etiqueta <h1>
    ## Este es una etiqueta <h2>
    ###### Este es una etiqueta <h6>

### Énfasis

    *Este texto estará en itálica*
    _Este texto también estará en itálica_

    **Este texto estará en negritas**
    __Este texto también estará en negritas__

    *Incluso **puedes** combinarlos*

### Listas

#### Desordenadas

    * Item 1
    * Item 2
        * Item 2a
        * Item 2b

#### Ordenadas

    1. Item 1
    2. Item 2
    3. Item 3
        * Item 3a
        * Item 3b

#### Imágenes

    ![GitHub Logo](/images/logo.png)

Formato:

    ![Atributo Alt](url "Atributo title Opcional")

#### Links

    1. http://github.com - ¡link automático!

    2. [GitHub](http://github.com)

    3. [GitHub][id]

    4. [GitHub][]

  1. **Link automático -** Cualquier dirección explicita será convertida en un link.
  2. **Link _en-línea_ -** `[Texto del Link](url)`.
  3. **Link _por-referencia_ -** `[Texto del Link][id]`. el id necesitará ser declarado en otra parte del documento así: `[id]: url`.
  4. **Link _por-referencia_ automática -** El id es el "Texto del Link", y también necesita ser declarado en otra parte del documento de igual manera que el "link por-referencia".

#### Citas

    Esto es un párrafo normal:

    > Y aquí está la cita que puede
    > seguir en varios renglones, y tener anidado más
    > > citas así, con un doble signo mayor-que.

#### Código en-línea

    Creo que debería utilizar una etiqueta `<addr>` aquí.



## GFM

GitHub Flavored Markdown (GFM). GitHub.com utiliza su propia versión de sintaxis Markdown que provee un conjunto de características adicionales, muchas de las cuales hacen más fácil trabajar con el contenido de GitHub.com

Note que algunas de las características de GitHub Flavored Markdown sólo están disponibles para las descripciones y comentarios de _issues_ y _Pull Requests_. Estos incluyen @menciones así como referencias a _hashes_ SHA-1, _Issues_, y _Pull Requests_. Las listas de tareas también están disponibles en comentarios de Gits y en archivos Gits Markdown.

### Resaltado de sintaxis

Aquí un ejemplo de como puede utilizar el resaltado de sintaxis [GitHub Flavored Markdown][GFM]:

    ```javascript
    function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
    ```

También puedes simplemente identar tu código con cuatro espacios:

        function fancyAlert(arg) {
          if(arg) {
            $.facebox({div:'#foo'})
          }
        }

Aquí un ejemplo de código en Python sin utilizar resaltado de sintaxis:

```
def foo:
  if not bar:
    return true
```

Para conocer más acera de los lenguar aceptados de un vistazo a este documento de [lenguajes aceptados][lenguajes].

[GFM]: https://help.github.com/articles/github-flavored-markdown
[lenguajes]: https://github.com/github/linguist/blob/master/lib/linguist/languages.yml

### Lista de Tareas

    - [x] Soporte de @menciones, #referencias, [links](), **formateo**, y de <del>etiquetas</del>
    - [x] lista de sintaxis requerida (cualquier lista des-ordenada y ordenada es soportada)
    - [x] esta es una tarea completa
    - [ ] esta es una tarea incompleta

### Referencias SHA ###

Cualquier referencia a un [hash SHA-1][sha1] _commit_ será automáticamente convertido en un link a ese _commit_ en GitHub.

```
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```

[sha1]: http://en.wikipedia.org/wiki/SHA-1

### Referencias _Issue_ dentro de un repositorio ###

Cualquier número que refiera a un _Issue_ o _Pull Request_ será automáticamente convertido en un link.

    #1
    mojombo#1
    mojombo/github-flavored-markdown#1


### @menciones a nombre-de-usuario ###

Escribiendo un símbolo de `@`, seguido del nombre-de-usuario, notificará a esa persona para que venga y vea el comentario. Esto es conocido como "@mención", porque tu estas mencionando a la persona. También puedes @mencionar equipos dentro de una organización.

### Links automáticos para URLs

Cualquier URL (como `http://www.github.com/`) será automática convertido en un link navegable.

### Tachado

Cualquier texto que este encerrado entre dos tildes (así `~~esto~~`) aparecerá tachado, así: ~~texto tachado~~.

### Emoji

GitHub soporta emoji :sparkles: :camel: :boom: Para ver la lista de imágenes que soporta, da un vistazo a la [Hoja de Datos Emoji][Emoji].

[Emoji]: http://www.emoji-cheat-sheet.com/

* * *

Para profundizar más, aquí algunas guías Markdown también en español:

  - [Markdown en español](https://github.com/ricval/Documentacion/tree/master/Markdown)