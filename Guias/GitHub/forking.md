Forking de Proyectos
====================

Traducción de [Forking Projects][forking_EN]. `2014.02.06`.

[forking_EN]: http://guides.github.com/overviews/forking/

  - [Contribuyendo a un proyecto](#contribuyendo-a-un-proyecto)
  - [Haciendo un Fork del repositorio](#haciendo-un-fork-del-repositorio)
  - [Clona tu Fork](#clona-tu-fork)
  - [Haciendo un Pull Request](#haciendo-un-pull-request)
  - [¡Fuuaa!](#fuuaa)


## Contribuyendo a un proyecto ##

Después de utilizar GitHub tu solo por un tiempo, tal vez estés esperando contribuir en el proyecto de alguien más. O quizás quieras utilizar el proyecto de alguien más como punto de partida para tu propio proyecto. Éste proceso se conoce como _forking_.

Crear un "fork" es producir un copia personal del proyecto de alguien más. 
La acción de _Fork_ es un puente entre el repositorio original y tu copia personal. Puedes enviar un _Pull Request_ para ayudar o contribuir al proyecto de otras personas ofreciendo tus cambios al proyecto original. Hacer _Forking_ es el núcleo de la programación social en GitHub.

Para este tutorial, utilizaremos el proyecto [Spoon-Knife][], un repositorio de prueba que esta alojado en GitHub.com y que permite hacer pruebas para _Pull Request_.

  [Spoon-Knife]: https://github.com/octocat/Spoon-Knife

## Haciendo un _Fork_ del repositorio ##

Para hacer un _fork_ del repositorio del proyecto Spoon-Knife, da clic en el botón de __Fork__ que está en la parte superior del repositorio.

 ![Botón Fork](https://github-images.s3.amazonaws.com/help/bootcamp/Bootcamp-Fork.png)

Siéntate cómodo y observa la magia del proceso de _forking_. Cuando termine, tendrás tu propia copia del repositorio del proyecto Spoon-Knife.


## Clona tu _fork_ ##

Ya lograste un _fork_ exitoso del repositorio Spoon-Knife, pero hasta ahora, solo existe en GitHub. Para poder trabajar en el proyecto, necesitas clonarlo a tu computadora.

Si estás utilizando la aplicación de [GitHub para Escritorio][GitHub_Desktop], este proceso es cosa fácil. Debajo del titulo __GitHub.com__ en la barra lateral, da clic en tu avatar o nombre de cuenta, y comienza a teclear el nombre de "Spoon-Knife". Verás un botón que dice __Clonar a tu Computadora__. Dando clic en éste, clonas el repositorio en tu computadora.

 ![GitHub Desktop Mac - Clonar](https://github-images.s3.amazonaws.com/mac/sync/ghfm_clone_repo_locally.png)

 [GitHub_Desktop]: http://guides.github.com/overviews/desktop


## Haciendo y subiendo cambios ##

Adelante, haz algunos cambios al proyecto utilizando tu editor de texto favorito, como [Notepad++][] o [Sublime Text][]. Podrías, por ejemplo, cambiar el texto en _index.html_ y agregar tu nombre de usuario de GitHub.

  [Notepad++]: http://www.notepad-plus-plus.org/
  [Sublime Text]: http://www.sublimetext.com/

Cuando estés listo para enviar los cambios, escribe un _resumen commit_ en la aplicación de GitHub para Escritorio, y da clic en __Commit__.

 ![GitHub Desktop Mac - Commit](https://github-images.s3.amazonaws.com/mac/changes/changes-view-20130108-143933.jpg)

En este momento le haz dicho a Git, "Bien, toma un _snapshot_ de mis cambios" Puedes continuar haciendo más cambios, y tomar más _snapshots_ de _commit_. Cuando estés listos para enviar tus cambios a GitHub.com, da clic en el botón de __Sync__, que esta arriba a la derecha de tu lista de cambios.


## Haciendo un _Pull Request_ ##

Al final, estás listo para proponer cambios en el proyecto principal. Éste es el paso final en la producción de un _fork_ del proyecto de alguien más, y podría decirse que el más importante. Si hiciste un cambio que sientes que podría beneficiar a la comunidad, definitivamente deberías considerar envíar tu contribución.

Para hacerlo, ve al repositorio en GitHub.com donde esta tu copia del proyecto. Por ejemplo, algo así:
`https://www.github.com/<tu_nombre_de_usuario>/Spoon-Knife`. Verás un banner indicando que recientemente haz enviado una nueva rama (_branch_), y que puedes enviar está rama "un-nivel-arriba", al repositorio original.

 ![GitHub.com - Pull Request](https://github-images.s3.amazonaws.com/help/pull_requests/recently_pushed_branch.png)

Dando clic en botón de __Compare and Pull Request__ te envía a la página de discusiones, donde puedes ingresar un titulo y una descripción opcional. Es importante proveer la mayor información posible de _por qué_ estás haciendo este _Pull Request_ en primer lugar. El dueño del proyecto lo necesita para poder determinar si tus cambios son tan útiles para todos como tu lo crees.

Cuando hayas terminado de escribir todo tu argumento cordialmente escrito, da clic en __Send pull request__, y ¡Listo!

 ![pull request button](https://github-images.s3.amazonaws.com/help/pull_requests/pullrequest-send.png)

Tú _Pull Request_ está ahora en área de discusión. En este caso, el _Octocat_ esta muy ocupado, y probablemente no _merge_ tus cambios. Para otros proyectos, no te sientas ofendido si el dueño del proyecto rechaza tu _Pull Request_, o te pide más información de por qué hiciste tales cambios. Puede incluso que le dueño del proyecto decida no _merge_ tu _pull request_, y eso es totalmente válido. Tu copia seguirá existiendo en Internet. Y quien sabe – tal ves alguien que no conozcas encuentre tus cambios mucho más valiosos que el proyecto original.


## ¡Fuuaa! ##

Haz hecho un _fork_ exitoso y haz contribuido de vuelta a un repositorio. Sigue adelante, y contribuye algo más.