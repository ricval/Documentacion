Llevando tu proyecto a GitHub
=============================

Traducción de [Getting your project on GitHub][desktop_EN]. `2014.02.06`.

[desktop_EN]: http://guides.github.com/overviews/desktop/

  - [Introducción](#introducción)
  - [GitHub Desktop](#github-desktop)
  - [Configura tu proyecto en GitHub Desktop](#configura-tu-proyecto-en-github-desktop)
  - [Envía tu código a GitHub.com](#envía-tu-código-a-githubcom)
  - [Tomando código desde GitHub.com](#tomando-código-desde-githubcom)
  - [¡Hora de celebrar!](#hora-de-celebrar)


## Introducción ##

El software se encuentra en el corazón de GitHub — y el código es el ADN del software. Lo más probable es que si te estas uniendo, es porque tienes algo de código que quieres subir a GitHub. ¡Y esa es una fantástica idea!

Aquí listamos algunas grandes razones para que subas tus proyectos a GitHub:

  - **Control de Versiones —** Todo en GitHub es almacenado en [Git][], el mejor sistema de control de versiones. El control de versiones te permite experimentar y cometer errores en tu código sin que afecte a tu producto final.
  - **Mantén tu código en un solo lugar —** Si trabajar en varias computadoras o si solo quieres mantener tus viejos proyectos fuera de tu computadora, GitHub es el lugar perfecto para almacenar tus proyectos en línea.
  - **Colaboración —** Una vez que tu código está en GitHub, puedes invitar a otros a trabajar en tu código contigo. Envíales un mensaje para que te ayuden a solucionar un problema.

![Repositorio](http://guides.github.com/overviews/desktop/repository.png)

[Git]: http://git-scm.com/

Una vez que tu proyecto este en GitHub, te otorgaremos una URL para cada archivo de tu proyecto. Por ejemplo, este es el proyecto [d3][] bastante popular de Mike Bostock para crear documentos basados en datos con JavaScript.

[d3]: https://github.com/mbostock/d3

Vamos a utilizar las palabras Git y GitHub en todo este articulo, así que déjame aclarar que significan.

  - **Git —** La herramienta para el control de versiones sobre la que GitHub está construida.
  - **GitHub —** Nuestra compañía y el nombre de nuestro software. Hacemos software y sitos web para ayudar a interactuar con los repositorios Git de una manera más agradable.
  - **GitHub.com —** El sitio web con el que te conectas a tus repositorios en línea.
  - **GitHub Desktop —** Una aplicación que puedes instalar en tu computadora para ayudarte a sincronizar tu código local con GitHub.com


## GitHub Desktop ##

GitHub Desktop es la forma más sencilla para tomar código de GitHub.com. No necesitas aprender ninguna instrucción de linea-de-comandos, llaves SSH, o terminología complicada de Git. Todo lo que necesitas es tu computadora Mac o Windows y una [cuenta en GitHub.com][cuenta_GitHub].

[cuenta_GitHub]: https://github.com/join

Puedes descargar GitHub Desktop para [Mac][GitHub_Mac] o para [Windows][GitHub_Windows]. Una vez instalado GitHub Desktop, necesitaras una pequeña configuración que será guiada paso a paso para algunas configuraciones que te ayudaran a conectar tu GitHub Desktop con tu cuenta de GitHub.com.

[GitHub_Mac]:     http://mac.github.com/
[GitHub_Windows]: http://windows.github.com/

## Configura tu proyecto en GitHub Desktop ##

La forma más sencilla para llevar tu proyecto a GitHub Desktop es arrastrar el directorio que contiene tu código dentro de la pantalla principal de la aplicación.

_Nota: Este ejemplo muestra la aplicación para Mac, pero es lo mismo para la aplicación para Windows._

![GitHub Desktop Mac](http://guides.github.com/overviews/desktop/mac-dragndrop.jpg)

Si estas arrastrando un repositorio Git existente, puedes saltarte este paso e ir a [enviar tu código a GitHub.com](#envía-tu-código-a-githubcom).

Si el directorio aún no es un repositorio Git, GitHub Desktop te preguntará si quieres convertirlo en un repositorio. Convertir tu proyecto en un repositorio Git no borra o arruina los archivos de tu directorio — éste simplemente crea algunos archivos ocultos que le permitirán a Git hacer su magia.

![GitHub Desktop Mac Git Init](http://guides.github.com/overviews/desktop/mac-gitinit.jpg)

### Tu primer _commit_ ###

Todos los repositorios Git están basados en _commits_ — _snapshots_ de tu código en un punto del tiempo. Necesitas hacer un último _commit_ antes de poder hacer un envío de tu código a GitHub.com

![GitHub Desktop Mac Commit](http://guides.github.com/overviews/desktop/mac-commit.jpg)

Ve a la pestaña de **Cambios** y da clic en **Commit** para crear tu primer _commit_. Necesitarás crear un nuevo _commit_ cada vez que hagas cambios en tus archivos. Crear un _commit_ es como hacer un guardado de tus archivos — le estas diciendo a Git que quieres que recuerde este momento en la historia.

Haz tantos _commits_ localmente como quieras. Nadie aparte de ti puede ver estos _commits_ hasta que los envíes (_push_) a GitHub.com.


## Envía tu código a GitHub.com ##

![GitHub Desktop Mac Push](http://guides.github.com/overviews/desktop/mac-push.jpg)

Da clic en el botón "Push to GitHub" que está en la esquina superior derecha, y GitHub Desktop te preguntará que tipo de repositorio crear:

  - **Repositorio Público —** Cualquiera puede ver un repositorio público, pero puedes elegir quien puede hacer un _commit_ (hacer cambios) en él. Puedes crear tantos repositorios públicos como quieras de forma gratuita en GitHub.com.
  - **Repositorios Privados —** Por defecto, solo tú puedes ver los repositorios privados. Puedes elegir quien puede ver y hacer _commit_ a ese repositorio agregando colaboradores. Los repositorios privados requieren una [suscripción de pago][cuenta_de_pago_GitHub] en GitHub.com.

[cuenta_de_pago_GitHub]: https://github.com/settings/billing

Ahora que has publicado tu repositorio, tu proyecto está en dos lugares:

  - **Repositorio local en tu computadora —** Puedes trabajar en este repositorio sin tener una conexión a Internet usando GitHub Desktop. Aquí es donde puedes editar los archivos y hacer cambios a tu proyecto.
  - **Reposiotorio remoto en GitHub.com —** Puedes enviar un link de tu repositorio alojado en GitHub.com a amigos, para que ellos puedan ver tu código y utilicen todas las demás características que GitHub ofrece (como manejo de _Issues_ y _Pull Requests_).

Cada vez que hagas cambios en tu repositorio local, necesitarás hacer una sincronización de tus cambios (dando clic en el botón localizado en la esquina superior derecha de GitHub Desktop) para asegurarte que se muestren en línea.


## Tomando código desde GitHub.com ##

Si quieres copiar algo de código desde GitHub.com a tu computadora o sincronizar cambios entre varias computadoras, necesitas hacer un _pull change_ o clonar un repositorio:

  - **Pull Changes —** Da clic en el botón de "Sync" que está en al esquina superior derecha de GitHub Desktop para traer el código de tu repositorio en línea (por ejemplo, cambios que tu colaboradores hayan subido) a tu computadora. _Nota: Esto enviará los cambios que aún no habías enviado_.
  - **Clonar un repositorio —** Da clic en el botón de "Clone in Desktop" en GitHub.com para crear una nueva copia de un repositorio en tu computadora.


## ¡Hora de celebrar! ##

Ya conoces las bases para manejar un proyector en GitHub.

  - Descarga y utiliza GitHub Desktop.
  - Haz _commits_ cada vez que cumplas un objetivo o quieras salvar tu progreso.
  - Sincroniza los cambios con GitHub.com para subir tus nuevos _commits_ y descargar los _commits_ de otros.

¡Y listo! Aquí un montón de [cosas increíbles que puedes hacer con los repositorios][GitHub_features].

[GitHub_features]: https://github.com/features