UML : Básico
============


## Estructura de una Clase ##

 | __NombreDeLaClase__ |
 | ------------------- |
 | atributos           |
 | ------------------- |
 | métodos             |

 - __NombreDeLaClase__: Nombre de la clase, debe de ir en notación _StudlyCaps_, centrado y en negritas.
 - __atributos__: Lista de atributos, en notación _camelCase_.
 - __métodos__: Lista de Métodos, en notación _camelCase_.

### Visibilidad ###

  - Pública: `+`.
  - Protegida: `#`.
  - Privada: `-`.

### Estructura de Atributos ###

    + nombre: String

  - `+`: Visibilidad.
  - `nombre`: Nombre del atributo.
  - `String`: Tipo de variable.

### Estructura de Métodos ###

    + agregarEntrada(nuevaEntrada : BlogEntrada, autor : Autor): void

  - `+`: Visibilidad.
  - `agregarEntrada`: Nombre del método.
  - `()`: Paréntesis para parámetros.
    - `nuevaEntrada`: Nombre del primer parámetro.
    - `BlogEntrada`: Tipo de valor del parámetro.
  - `void`: Valor de retorno.

### Métodos o Atributos ###

Los Métodos o Atributos __estáticos__ deben estar subrayados.
Los Métodos o Atributos __abstractos__ deben estar en _itálica_. Incluso el nombre de la Clase debe estar en itálica de ser una clase abstracta.

### Relacciones entre clases ###

Hay cinco tipos de relaciones:

  1. [__Dependencia__](#dependencia): `<---` Flecha con línea punteada.
  2. [__Asociación__](#asociación): `<———`  Línea solida normal.
  3. [__Agregación__](#agregación): `<>———` Flecha con punta de diamante vacía.
  4. [__Composición__](#composición): `<>---` Flecha con punta de diamante rellena.
  5. [__Herencia__](#herencia): `<|———` Flecha con punta de triangulo vacía.

#### Dependencia

Una _dependencia_ es una relación de uso entre dos entidades, una usa a la otra. Es el tipo de relación más débil y básica entre clases. Se representa con una línea punteada y una flecha `<---`, que indica que clase depende de cual.

    A ----> B

  - Aquí, la clase A depende de la clase B.
  - La clase A usa la clase B.
  - La clase A conoce la existencia de la clase B, pero la clase B no conoce la existencia de la clase A, (uso de la flecha).
  - Todo cambio que se haga en la clase B, por la relación que hay con la clase A, podrá afectar a la clase A.

También se le conoce como __relación de uso__, porque la clase A _usa_ a la clase B.

```php
class A
{
    public function ejecutar()
    {
        $b = new B();
    }
}
```

#### Asociación

Significa que una clase contendrá una referencia a un objeto, u objetos de la otra clase en forma de un atributo. Si te encuentras diciéndote que una clase _trabaja con_ un objeto de otra clase, entonces la relación entre ellas será altamente candidata para un relación de asociación en lugar de una de una de [dependencia](#dependencia).

Se representa con una línea solida `<———`y la flecha indica la _Navegación_ que es aplicada para describir que clase contiene el atributo que soporta dicha relación.

    A ———> B

```php
class A
{
    private $_b;

    public function __construct()
    {
        $this->_b = new B();
    }
}
```

#### Agregación

La relación tipo _agregación_ es una versión más fuerte de la de [asociación](#asociación), y es utilizada para indicar que clase _posee pero puede compartir_ objetos de otra clase.

Es una relacción que en lugar de ser de '1 a 1' ahora es de '1 a muchos', la clase A agrega muchos elementos de la clase B.

    A <>——— B

Su representación es una linea continua con un rombo vacío. 

#### Composición

Similar a la de [agregación](#agregación), solo que además de agregar, ahora existe una relación de vida, donde elementos de B no pueden existir sin la relación de A.

    A <>——— B

Su representación es una linea continua con un rombo relleno.

#### Herencia

    A
    ^
    |
    B

```php

class A
{

}

class B extends A
{

}
```

