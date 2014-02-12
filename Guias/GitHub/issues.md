Maestría en _Issues_
====================
Traducción de [Mastering Issues][issues_EN]. `2014.02.07`.

[issues_EN]: http://guides.github.com/overviews/issues/

  - [Introducción](#introducción)
  - [Etapas, Etiquetas e Asignaciones](#etapas-etiquetas-e-asignaciones)
  - [Notificaciones, @menciones, y referencias](#notificaciones-menciones-y-referencias)
  - [Búsqueda](#búsqueda)
  - [Resúmenes y Reportes](#resúmenes-y-reportes)
  - [Otros usos para los Issues](#otros-usos-para-los-issues)


## Introducción ##

Los _Issues_ son una forma genial de administrar tus tareas, mejoras y _bugs_ de tus proyectos. Son como un tipo de email — excepto que pueden ser compartidos y debatidos con el resto de tu equipo. La mayoría de los proyectos de software tienen un software administrador de _bugs_ o algo parecido. El administrador de GitHub es llamado **Issues**, y tiene su propia sección en cada repositorio.

![sección de Issues](http://guides.github.com/overviews/issues/navigation-highlight.png)

Por ejemplo, demos un vistazo a la [sección de _Issues_ de Bootstrap][issue_bootstrap]:

[issue_bootstrap]: https://github.com/twbs/bootstrap/issues

![bootstrap issue screenshot](http://guides.github.com/overviews/issues/listing-screen.png)

El administrador de _issue_ de GitHub es especial debido a que se concentra en la colaboración, referencias y contiene un formateo de texto excelente. Un _issue_ típico en GitHub se ve más o menos así:

![issue de ejemplo](http://guides.github.com/overviews/issues/example-issue.png)

 - El **título y la descripción** describen de que se trata el _issue_.
 - Las **etiquetas (_Labels_)** coloreadamente-resaltadas ayudan a organizar y filtrar tus _issues_ (como las etiquetas en Gmail).
 - Las **etapas (_Milestone_)** actúan como contenedores de _issues_. Esto es útil para asociar ciertos _issues_ con características especificas o fases del proyecto (ejem. _Sprint Semanal 9/5-9/16_ o _Envío 1.0_)
 - Un **asignado (_Assignee_)** es responsable de trabajar en el _issue_ en un momento dado.
 - Los **comentarios** permiten a cualquiera con acceso al repositorio dar su opinión.



## Etapas, Etiquetas e Asignaciones

Una vez que tengas un montón de _issues_, podría serte difícil encontrar en el que quieres trabajar. Las **etapas**, **etiquetas**, y **asignaciones** son una genial característica para filtrar y organizar tus _issues_.

Puedes cambiar o agrear una etapa (_milestone_), una asignación (_assignee_), y etiquetas (_labels_) dando un clic en el icono de engrane correspondiente en la barra lateral derecha.

![labels](http://guides.github.com/overviews/issues/labels.png)

Si no ves los botones de edición, es porque no tienes permiso para modificar ese _issue_. Puedes pedirle al dueño del repositorio que te agregue como colaborador para tener acceso.

### Etapas (_Milestones_)

![milestones](http://guides.github.com/overviews/issues/milestones.png)

Las Etapas son grupos de _issues_ que corresponden a un proyecto, una característica, o un periodo de tiempo. Las personas utilizan esto de muchas maneras diferentes en el desarrollo de software. Algunos ejemplos:

  - **Lanzamiento Beta —** Archivos con _bugs_ que necesitas arreglar antes de poder lanzar la beta de tu proyecto. Es una idea genial para asegurarte que no estas olvidando nada.
  - **Sprint de Octubre —** Lista de _issues_ en los que quieres trabajar en Octubre. Una forma genial de enfocar tu esfuerzo cuando hay mucho que hacer.
  - **Re-diseño —** Lista de _issues_ relacionados al re-diseño de tu proyecto. Una forma genial de coleccionar ideas en las que podrías trabajar.

### Etiquetas (_Labels_)

Las etiquetas son una forma de organizar diferentes tipos de _issues_. Los _issues_ pueden tener tantas etiquetas como quieras, y puedes filtrarlas por una o por varias.

![listado de etiquetas](http://guides.github.com/overviews/issues/labels-listing.png)

### Asignaciones (_Assignees_)

Cada _issue_ tiene un asignado — una persona que es la responsable para llevar el _issue_ en buena dirección. Las asignaciones son seleccionadas de la misma manera que las etapas, a través de la barra gris en la parte superior de un _issue_.



## Notificaciones, @menciones, y Referencias

Utilizando @menciones y referencias dentro de un _issue_, puedes notificar a otros usuarios o equipos en GitHub, y puede hacer llamados desde o otros _issues_. Esto provee una forma flexible de llamar a las personas correctas para que se involucren en resolver un _issue_ efectivamente, y es fácil de aprender a utilizar. Funcionan en todos los campos de texto dentro de GitHub — son parte de nuestra sintaxis de formateo llamada [GitHub Flavored Markdown][GFM].

[GFM]: https://help.github.com/articles/github-flavored-markdown

![ejemplo markdown](http://guides.github.com/overviews/issues/markdown-example.png)

Si quieres conocer más, puedes dar un vistazo a la Guía de [Maestría en _Markdown_](mastering-markdown.md).

### Notificaciones

Las [notificaciones][] son la forma de mantenerte al día con tus _Issues_. Puedes utilizarlas para saber que hay de nuevo en _issues_ o en repositorios, o simplemente para saber cuando alguien necesita de tu ayuda.

Hay dos formas de recibir las notificaciones: vía email, y vía web. Puedes configurar cómo deseas recibir las notificaciones en [tus opciones][tus-opciones]. Si tu plan es recibir un motón de notificación, te recomendamos que las recibas vía web y email para **participar**, y notificaciones web para **Observar**.

![notificaciones img](http://guides.github.com/overviews/issues/notifications.png)

Con esta configuración, recibirás emails sólo cuando seas mencionado, así que visita la interfaz web para mantenerte al día con los repositorios en los que estás interesado.

Puedes tener acceso a tus notificaciones a través de la pantalla de [notificaciones][]. Esta pantalla es genial para escanear muchas notificaciones a la vez y marcar cuando las has leído o callar una conversación. Intenta utilizar los atajos del teclado para mayor rapidez — presiona `?` en la página para ver los atajos del teclado que están disponibles.

![notification-img](http://guides.github.com/overviews/issues/notification.png)

Callar conversaciones hará que no muestre más mensajes de no-leído hasta que seas @mencionado de nuevo. Esto hace que callar sea un estrategia genial para conversaciones en las que no estás tan interesado (preparativos de un sub-sistema en los que no estas muy familiarizado). Si marcas un _issue_ como leído, este se mantendrá así hasta que alguien comente en esa conversación nuevamente.

GitHub también sincroniza el estado de leído/no-leído de las notificaciones vía email — si ya leíste una notificación en tu cliente de correo, éste se marcara como leído en la interface web (asegúrate de que tu cliente de correo despliegue las imágenes si quieres que ésta función opere).

[notificaciones]: https://github.com/notifications
[tus-opciones]: https://github.com/settings/notifications

### @menciones

Las @menciones son la forma de referirse a otros usuarios en GitHub dentro de los _issues_ de GitHub. Dentro de la descripción o en cualquier comentario de un _issue_, incluye el @nombre-de-usuario de otro usuario de GitHub para enviarle una notificación. Esto funciona muy similar a como lo hace Twitter con sus @menciones.

Nos gusta utilizar la sintaxis `\cc` (una abreviación de copia al carbón) para incluir personas en un _issue_:

> Parece que el nuevo _widget_ no funciona en Safari. Cuando lo probé y cree el _widget_, Safari fallo. Este funciona en la versión 10.8, pero no en la versión 10.9. ¿Podría ser una _bug_ del navegador?
>
> /cc @kneath @jresig

Es una forma genial si sabes a que usuarios deseas incluir, pero muchas veces estamos trabajando con varios equipos y realmente no sabemos quien está disponible para ayudarnos. Las @menciones también funcionan para Equipos dentro de una organización en GitHub. Si creas un Equipo llamado _browser-bugs_ dentro de la organización @acmeinc, puedes referirte a ese equipo con la @mención:

> /cc @acmeinc/browser-bugs

Esto enviará una notificación a cada miembro del equipo _browser-bugs_.

### Referencias

Muchas veces los _issues_ dependen de otros _issues_, o al menos se relacionan entre sí y quieres que estén conectados. Puedes referirte a un _issue_ escribiendo un _hashtag_ seguido del número del _issue_.

> Hey @kneath, Creo que el problema comenzó en #42

Cuando haces esto, nosotros creamos un evento dentro del _issue_ #42 que se ve algo así:

![reference](http://guides.github.com/overviews/issues/reference.png)

¿Un _issue_ en otro repositorio? Solo incluye el repositorio antes del nombre, así: `kneath/proyecto-de-ejemplo#42`.

Una de las cosas más interesantes de utilizar _Issues_ en GitHub es la referencia a _issues_ directamente desde los _commits_. Incluye un número de _issue_ dentro de un mensaje de un _commit_.

![commit](http://guides.github.com/overviews/issues/commit.png)

Anteponiendo en tus _commits_ la palabra "Fixes", "Fixed", "Fix", "Closes", "Closed" o "Close" cuando el _commit_ se _merge_ (funcione) con el _master_, automáticamente ese _issue_ se cerrará.

Las referencias hacen posible conectar el trabajo que se está haciendo con el _bug_ que se esta tratando, y son una forma genial de añadir visibilidad dentro del historial de tu proyecto.



## Búsqueda 

Arriba de cada página se encuentra el campo de búsqueda que te permite hacer búsquedas entre los _issues_.

![search](http://guides.github.com/overviews/issues/search.png)

  - [Todos los _issues_ mensionados en la barra lateral][all_issues]
  - [...que estén abiertos][issues_open] (da un vistazo a los links de la barra lateral a mano izquierda para filtrar los abiertos o cerrados)
  - [Asignados a @mdo][issues_mdo]
  - [O buscar entre todos los _issues_ de GitHub dando clic en el link de la barra lateral][issues_GitHub]

Vista la página de [búsqueda avanzada][busqueda-avanzada] para aprender otras formas de buscar entre los _issues_: utilizando fechas de creación o actualización, etiquetas, autores, numero de comentarios, por dueño de repositorios, y más.

[all_issues]: https://github.com/twbs/bootstrap/search?q=sidebar&type=Issues
[issues_open]: https://github.com/twbs/bootstrap/search?q=sidebar&state=open&type=Issues
[issues_mdo]: https://github.com/twbs/bootstrap/search?q=assignee%3Amdo&ref=cmdform&type=Issues
[issues_GitHub]: https://github.com/search?q=sidebar&ref=reposearch&state=open&type=Issues
[busqueda-avanzada]: https://github.com/search/advanced?q=sidebar&ref=reposearch&state=open&type=Issues



## Resúmenes y Reportes

Fuera de las sección de _Issues_, hay otras dos páginas que te ayudarán a resumir que pasa con los _issues_ a través de un repositorio y a través de todos tus repositorios.

### El _Dashboard_ de _Issues_

Si estás buscando un listado de todos tus _issues_ a través de muchos proyectos, el [Dashboard de Issues][dashborar_issues_link] puede ser una gran herramienta. El _dashboard_ funciona muy similar a la sección de _issues_, pero agrupa los _issues_ de forma diferente:

  - Todos los _issues_ en repositorios que eres dueño o en los que colaboras.
  - _Issues_ asignados a ti.
  - _Issues_ que tu has creado.

Si utilizas organizaciones, cada organización tendrá su propio _dashboar de Issues_ que separa cada _Issue_ dentro de la organización.

[dashborar_issues_link]: https://github.com/dashboard/issues

### Pulso (_Pulse_)

Dentro de cada repositorio está una sección llamada **Pulse** (Pulso) **—** El Pulso es un _snapshot_ de todo lo que paso en el repositorio hace una semana ( día, ó 3 meses, etc).

![Pulso](http://guides.github.com/overviews/issues/pulse.png)

Es una forma genial de ponerse al día con los repositorios para cuando has esta fuera y no quieres recibir notificaciones regularmente como cuando estas observando un repositorio.



## Otros Usos para los _Issues_

Los _Issues_ son geniales para rastrear todo tipo de cosas — y GitHub es un lugar genial para compartir de manera fácil y de colaborar con tus _issues_. Aquí hay unos de nuestros favoritos:

  - [Rastrear _bugs_ desde tu casa](https://github.com/frabcus/house/issues?labels=building&state=open) incluyendo algunas gemas como [la puerta está colgada incorrectamente](https://github.com/frabcus/house/issues/58)
  - [Rastrear _bugs_ para proyectos _open source_](https://github.com/joyent/node/issues)
  - [Pedir recetas](https://github.com/newmerator/recipes/issues) (o talvés tengas una buena [receta de pizza sin gluten](https://github.com/newmerator/recipes/issues/3))



## Fin

**Ahora felicítate a ti mismo —** eso fue mucho que leer. La administración de _Issues_ es una de las herramientas más poderosas que está a disposición de cualquier desarrollador. Supongo que todo lo que queda es arreglar tus bugs.