Maestría en _Issues_
====================
Traducción de [Mastering Issues][issues_EN]. `2014.02.07`.

[issues_EN]: http://guides.github.com/overviews/issues/

  - [Introducción](#introducción)
  - [Etapas, Etiquetas e Asignaciones](#crear-una-rama)
  - [Notificaciones, @menciones, y referencias](#agregar-commits)
  - [Búsqueda](#abrir-un-pull-request)
  - [Resumenes y Reportes](#discutir-y-revisar-tu-código)
  - [Otros usuarios para Issues](#fusionar-e-implementar)


## Introducción ##

Los _Issues_ son una forma genial de administrar tus tareas, mejoras y _bugs_ de tus proyectos. Son como tipo o como un email — excepto que pueden ser compartidos y debatidos con el resto de tu equipo. La mayoría de los proyectos de software tienen un administrador de _bugs_ o algo parecido. El administrador de GitHub es llamado **Issues**, y tiene su propia sección en cada repositorio.

![sección de Issues](http://guides.github.com/overviews/issues/navigation-highlight.png)

Por ejemplo, demos un vistazo a la [sección de _Issues_ de Bootstrap][issue_bootstrap]:

[issue_bootstrap]: https://github.com/twbs/bootstrap/issues

![bootstrap issue screenshot](http://guides.github.com/overviews/issues/listing-screen.png)

El administrador de _issue_ de GitHub es especial debido a que se concentra en la colaboración, referencias y contiene un formateo de texto excelente. Un _issue_ típico en GitHub se ve más o menos así:

![issue de ejemplo](http://guides.github.com/overviews/issues/example-issue.png)

 - El **título y la descripción** describen de que se trata el _issue_.
 - Las **etiquetas** coloreadamente-resaltadas ayudan a organizar y filtrar tus _issues_ (como las etiquetas en Gmail).
 - Las **etapas** actúan como contenedores de _issues_. Esto es útil para asociar ciertos _issues_ con características especificas o fases del proyecto (ejem. _Sprint Semanal 9/5-9/16_ o _Envío 1.0_)
 - Un **asignado** es responsable de trabajar en el _issue_ en un momento dado.
 - Los **comentarios** permiten a cualquiera con acceso al repositorio proveer de una opinión.



## Etapas, Etiquetas e Asignaciones

Una vez que tengas un montón de _issues_, podría serte difícil encontrar en el que quieres trabajar. Las **etapas**, **etiquetas**, y **asignaciones** son una genial característica para filtrar y organizar tus _issues_.

Puedes cambiar o agrear una etapa (_milestone_), una asignación (_assignee_), y etiquetas (_labels_) dando un clic en el icono de engrane correspondiente en la barra lateral derecha.

![labels](http://guides.github.com/overviews/issues/labels.png)

Si no ves los botones de edición, es porque no tienes permiso para para modificar ese _issue_. Puedes pedirle al dueño del repositorio que te agregue como colaborador para tener acceso.

### Etapas (_Milestones_)

![milestones](http://guides.github.com/overviews/issues/milestones.png)

Las Etapas son grupos de _issues_ que corresponden a un proyecto, una característica, o un periodo de tiempo. Las personas utilizan esto de muchas maneras diferentes en el desarrollo de software. Algunos ejemplos:

  - **Lanzamiento Beta —** Archivos con _bugs_ que necesitas arreglar antes de poder lanzar la beta de tu proyecto. Es una idea genial para asegurarte que no estas olvidando nada.
  - **Sprint de Octubre —** Lista de _issues_ en los que quieres trabar en Octubre. Una forma genial de enfocar tu esfuerzo cuando hay mucho que hacer.
  - **Re-diseño —** Lista de _issues_ relacionados al re-diseño de tu proyecto. Una forma genial de coleccionar ideas en las que podrías trabajar.

### Etiquetas (_Labels_)

Las etiquetas con una forma de organizar deferentes tipos de _issues_. Los _issues_ pueden tener tantas etiquetas como quieras, y puedes filtrarlas por una o varias etiquetas.

![listado de etiquetas](http://guides.github.com/overviews/issues/labels-listing.png)

### Asignaciones (_Assignees_)

Cada _issue_ tiene un asignado — una persona que es el responsable para llevar el _issue_ en buena dirección. Las asignaciones son seleccionadas de la misma manera que las etapas, a través de la barra gris en la parte superior de un _issue_.



## Notificaciones, @menciones, y Referencias

Utilizando @menciones y referencias dentro de un _issue_, puedes notificar a otros usuarios o equipos en GitHub, y puede hacer llamados desde o otros _issues_. Esto provee una forma flexible de llamar a las personas correctas para que se involucren en resolver un _issue_ efectivamente, y es fácil de aprender a utilizar. Funcionan en todos los campos de texto dentro de GitHub — son parte de nuestra sintaxis de formateo llamada [GitHub Flavored Markdown][GFM].

[GFM]: https://help.github.com/articles/github-flavored-markdown

![ejemplo markdown](http://guides.github.com/overviews/issues/markdown-example.png)

Si quieres conocer más, puedes dar un vistazo a la Guía de [Maestría en _Markdown_](mastering-markdown.md).

### Notificaciones

Las [notificaciones][] son la forma de mantenerte al día con tus _Issues_. Puedes utilizarlas para saber que hay de nuevo en _issues_ o en repositorios, o simplemente para saber cuando alguien necesita de tu ayuda.

Hay dos formas de recibir las notificaciones: vía email, y vía web. Puedes configurar como deseas recibir las notificaciones en [tus opciones][tus-opciones]. Si tu plan es recibir un motón de notificación, te recomendamos que las recibas vía web y email, para **participar** y notificaciones web para **Observar**.

![notificaciones img](http://guides.github.com/overviews/issues/notifications.png)

Con esta configuración, recibirás emails sólo cuando seas mencionado, así que visita la interfaz web para mantenerte al día con los repositorios en los que estás interesado.

Puedes tener acceso a tus notificaciones a través de la pantalla de [notificaciones][]. Esta pantalla es genial para escanear muchas notificaciones a la vez y marcar cuando las has leído o callar una conversación. Intenta utilizar los atajos del teclado para mayor rapidez — presiona `?` en la página para ver los atajos del teclado que están disponibles.

![notification-img](http://guides.github.com/overviews/issues/notification.png)

Callar conversaciones hará que no muestre más mensajes de no-leído hasta que seas @mencionado de nuevo. Esto hace que callar sea un estrategia genial para conversaciones en las que no estás tan interesado (preparativos de un sub-sistema en los que no estas muy familiarizado). Si marcas un _issue_ como leído, este se mantendrá así hasta que alguien comente en esa conversación nuevamente.

GitHub también sincroniza el estado de leído/no-leído de las notificaciones vía email — si ya leíste una notificación en tu cliente de correo, éste se marcara como leído en la interface web (asegúrate de que tu cliente de correo despliegue las imágenes si quieres que ésta función opere).

[notificaciones]: https://github.com/notifications
[tus-opciones]: https://github.com/settings/notifications

### @menciones


