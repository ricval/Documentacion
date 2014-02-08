Entendiendo la forma de trabajo de GitHub
=========================================

Traducción de [Understanding the GitHub Workflow][flow_EN]. `2014.02.07`.

[flow_EN]: http://guides.github.com/overviews/flow/

  - [Introducción](#introducción)
  - [Crear una rama](#crear-una-rama)
  - [Agregar commits](#agregar-commits)
  - [Abrir un Pull Request](#abrir-un-pull-request)
  - [Discutir y revisar tu código](#discutir-y-revisar-tu-código)
  - [Fusionar e implementar](#fusionar-e-implementar)


## Introducción ##

La forma de trabajo de GitHub es ligera, su forma de trabajo basado-en-ramas soporta equipos y proyectos donde las asignaciones se realizan regularmente. Esta guía explica como funciona la forma de trabajo de GitHub.



## Crear una rama ##

Cuando trabajas en un proyecto, vas a tener en cualquier momento un montón de características o ideas diferentes en el proceso – algunas de ellas en las que ya estás listo para hacer o implementar, y otros en los que no. Hacer ramificaciones existe para ayudarte a manejar este flujo de trabajo.

#### Consejo Pro ####

Ramificaciones en un concepto del núcleo de Git, y el Flujo de GitHub está basado siguiendo esto. Sólo hay una regla: cualquier cambio en la rama de `master` siempre es implementado.

Debido a ésto, es extremadamente importante que tu nueva rama sea creada fuera de _master_ cuando trabajas en una función o en hacer una corrección. El nombre de tu rama debe ser descriptiva (ejem., `refactorizar-autorización`, `cache-contenido-usuario`, `hacer-retina-avatars`), así otros pueden ver en lo que estás trabajando.



## Agregar _commits_ ##

Una vez que tu rama ha sido creada, es tiempo de comenzar a hacer cambios. Cuando agregas, editas o borras un archivo, estás haciendo un _commit_, y agregando eso a tu rama. Este proceso de agregar _commits_ mantiene un registro de tu progreso mientras trabajas en una función de la rama.

Los _commits_ también crean un historial de manera transparente de tu trabajo que otros pueden seguir para entender que has terminado y por qué. Cada _commit_ tiene asociado un mensaje, que es una descripción explicando por qué un cambio en particular fue hecho. Además, cada _commit_ es considerado una unidad separada de cambio. Esto te permite deshacer cambios, si un _bug_ (error) fue encontrado, o si decides ir en una dirección diferente.

#### Consejo Pro ####

Los mensajes de _commit_ son importantes, especialmente desde los seguimientos de Git de los cambios, ya que después los despliega dentro de los _commits_ una vez que ellos son enviados al servidor. Escribiendo mensajes de _commit_ claros, puedes hacer fácil para otras personas seguirte a lo largo y proveer retroalimentación.



## Abrir un _Pull Request_ ##

Un _Pull Request_ inicia una discusión acera de tus _commits_. Debido que ellos están estrechamente integrados con el repositorio Git, cualquiera puede ver exactamente que cambios se funcionarían si ellos aceptan tu petición.

Puedes abrir un _Pull Request_ en cualquier punto durante el proceso de desarrollo: cuando tienes un poco o no tanto de código para compartir o alguna idea en general, cuando estás atascado y necesitas ayuda o un consejo, o cuando estás listo para que alguien revise tu trabajo. Utilizando el sistema de @menciones de GitHub en tus mensajes de _Pull Request_, puedes pedir la atención de personas o equipos específicos, ya sea que estén en la oficina de a lado o a diez husos horarios de distancia.

#### Consejo Pro ####

Los _Pull Request_ son útiles para contribuir a proyectos de código abierto y para administrar cambios en los repositorios compartidos. Si estás utilizando un Modelo _Fork & Pull_, los _Pull Requests_ te darán una forma de notificar a los encargados del proyecto acerca de los cambios que desean que se consideren. Si estás utilizando el Modelo Repositorio Compartido, los _Pull Requests_ te ayudan a comenzar revisiones de código y conversaciones acerca de proporciones de cambios antes que ellos lo funcionen dentro de la rama _master_.



## Discutir y revisar tu código ##

Una vez que un _Pull Request_ ha sido abierto, la persona o el equipo que reviso tus cambios quizás tengan preguntas o comentarios. Tal vez el estilo de programación no coincide con las directrices del proyecto, el cambio no acepta los _unit testes_, o quizá todo se ve genial y está en orden. Los _Pull Requests_ están diseñados para alentar y capturar este tipo de conversaciones.

Puedes seguir enviando tus cambios a la rama en plena discusión o mientras comentan acerca de tus _commits_. Si alguien comenta que olvidaste hacer algo o que hay un _bug_ en tu código, puedes arreglarlo en tu rama y enviar el cambio. GitHub mostrará tus nuevos _commits_ y cualquier comentario adicional que quizás recibas en la vista unificada de _Pull Request_.

#### Consejo Pro ####

Los comentarios _Pull Request_ están escritos en Markdown, así que puedes incluir imágenes y _emoji_, utilizar bloques de texto con formato, y formateo ligero.



## Fusionar e implementar ##

Una vez que tu _Pull Request_ ha sido revisado y la rama paso tus pruebas, es tiempo de funcionar tu código con la rama _master_ para su implementación. Si quieres probar cosas antes de fusionarlo en el repositorio de GitHub, puedes realizar la fusión locamente primero. Esto es algo útil si no tienes acceso para enviar los cambios al repositorio.

Una vez funcionado, los _Pull Requests_ mantiene un registro del historial de cambios de tu código. Debido a esto puedes buscar, regresar a cualquier punto atrás en el tiempo para entender por qué y cómo una decisión fue tomada.

#### Consejo Pro ####

Incorporando ciertas claves dentro de tu texto en tus _Pull Request_, puedes asociar _issues_ con tu código. Cuando tu _Pull Request_ es fucionado, el _issue_ relacionado es cerrado. Por ejemplo, ingresando la frase `Closes #32` debería cerrar el _issue_ número 32 en el repositorio. Para más información, da un vistazo a nuestro [articulo de ayuda][ayuda].

[ayuda]: https://help.github.com/articles/closing-issues-via-commit-messages