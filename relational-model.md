# :cd: Modelo relacional

## Introducción

- ☑️ Creado por Edgar F. Codd (1969)
- ☑️ Basado en la Teoría de Conjuntos
- ☑️ Va más allá de la definición de un Modelo de Datos
- ☑️ Álgebra de conjuntos
- ☑️ Inclusión
- ☑️ disyunción
- ☑️ Lenguaje basado en la Lógica de Predicados
- ☑️ Tratamiento de la Derivabilidad, Redundancia y Consistencia de las
Relaciones
- ☑️ Evaluación de Limitaciones y Bondades de los Sistemas de Información

## ¿Qué es una <abbr title="Base de Datos">BBDD</abbr> en el modelo relacional?

En el **modelo relacional** una <abbr title="Base de Datos">BBDD</abbr> es un **conjunto de relaciones**. Una **relación** es un conjunto de **tuplas** y una **tupla** es un conjunto de **atributos**.

![Diagrama de un BBDD en el modelo relacional](https://github.com/webferrol/ddbb_sessions/assets/35032717/9b03e1c9-3e13-4e8f-8d72-2abb14f3f725)

Cuando vemos las relaciones en una <abbr title="Base de Datos">BBDD</abbr>, éstas nos las presentan como tablas o matrices lo que nos crea una falsa impresión de orden.

## Atributos

Existen dos tipos:

1. Atómicos
2. No atómicos

¿Cuando descomponer o dividir los atributos? Depende de las reglas del negocio.

  ⚠️ Atómico no quiere decir crear el atributo más pequeño que se pueda si no el más pequeño de acuerdo con las reglas que se requieran.

Y recuerda:

>Pensar en grande cuesta lo mismo que pensar en pequeño.

## Derivalidad, redundancia y consistencia de las relaciones

<dl>
  <dt>☑️ Dervivalidad</dt>
  <dd>Una relación es derivable SI PODEMOS
OBTENER SUS ATRIBUTOS DE OTRA PARTE.</dd>
  <dt>☑️ Redundancia</dt>
  <dd>Datos que se repiten. Puede haber una <strong>redundancia fuerte</strong> o una <strong>redundacia débil</strong>. Esta última es la necesaria.</dd>
  <dt>☑️ Consistencia</dt>
  <dd>Durabilidad, estabilidad y veracidad de los datos. Esto es la <strong>calidad de los datos</strong>.</dd>
</dl>

## Identificación inequívoca de los datos

El **atributo** o **atributos** que identifica o indentifican de manera inequívoca a otros datos se conoce como **llave**. También recibe nombres como **llave primaria**, **clave primaria**, **primary key** (PK).

Puenden ser de dos tipos:

- ☑️ Llave natural
  - Llave/clave relacionada con los demás atributos
  Ej: DNI
- ☑️ Llave suplente cuando la llave natural
  - ☑️ No existe
  - ☑️ No se conoce
  - ☑️ Puede cambiar
  - ☑️ Es muy grande
  - ☑️ Puede quedar invalidada