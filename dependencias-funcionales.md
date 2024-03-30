# [:back:](/) Dependencias funcionales

## Definición

<dl>
  <dt>Dependencia funcional</dt>
  <dd>El valor de un <strong>conjunto de atributos</strong> permite <mark>encontrar</mark> el valor de otro <strong>conjunto de atributos</strong</dd>
</dl>

![Diapositiva de dependencia funcional](https://github.com/webferrol/ddbb_sessions/assets/35032717/bfed60f7-20b3-4438-af59-301a9da039d2)

## Tipos de dependencias funcionales

α &#10132; β

1. Dependencias triviales
  - <code>β ⊆ α</code>. En este caso **beta** es un **subconjunto propio** de **alfa**. Ejemplos:
    - Polígonos &#10132; polígonos regulares (Polígonos regulares es un subconjunto propio de polígonos)
    - AC &#10132; A (A es un subconjunto propio de AC)
    - BCD &#10132; BC (BC es un subconjunto propio de BCD)
2. Dependencias no triviales
  - No se da el subconjunto A ⊊ B. Ejemplos:
    - BC &#10132; AC
    - D &#10132; BC
3. Dependencias completas
  - A ∩ B = 0. Ejemplos:
    - BC &#10132; AD
    - D &#10132; BC

## Características de las dependencias funcionales

### Dependencia funcional aumentada

Sean α, β, γ **permutaciones** de R

<pre>
Si α &#10132; β
Entonces γα &#10132; γβ
</pre>

A &#10132; CD

AB &#10132; CDB

### Dependecia funcional transitiva

Sean α, β, γ **permutaciones** de R

<pre>
Si α &#10132; β y β  &#10132; γ
      α &#10132; γ
</pre>

A &#10132; CD

CD &#10132; B

Entonces:

A &#10132; B

## Cierre de α

α es un conjunto de atributos de la R

F es un conjunto de **Dependencias funcionales** de esta misma relación

¿Cuál es el mayor conjunto de atributo de R que podemos **encontrar** conociendo el valor de α?

A este conjunto lo vamos a llamar **cierre de α bajo F** o, simplificando, **cierre de α**. Se denota como <code>α<sup>+</sup></code>

<pre>
R (A, B, C, D, E)

A &#10132; C
C &#10132; E
AE &#10132; D

A<sup>+</sup>=?
</pre>

## ¿Cuál es la importancia de las dependencias funcionales?

Son las bases del **modelo relacional**. Sobre todo del proceso de **normalización**.

Ya que son las dependencias funcionales las que vamos a usar para definir la forma en la que vamos a dividir nuestras relaciones, utilizando el concepto de **llaves**.

## LLaves

Las **llaves** son un *conjunto de atributos* que determina el valor de otro conjunto de atributos. **En una dependencia funcional todo determinante es una llave**:

<code>α &#10132; β</code>

### Super llave

<pre>
α &#10132; β
a<sup>+</sup>=R
</pre>

Dada una dependencia funcional cualquiera, si el cierre de su determinante contiene todos los elementos de la relación entonces este determinante se denomina **súper llave** ya que es una llave que determina todos los atributos de la relación.

<pre>
Dada la siguiente relación y el conjunto de dependencias funcionales de esa relación vamos a calcular el cierre de A.

R (A, B, C, D, E)

A &#10132; C,B
C &#10132; E
AE &#10132; D

A<sup>+</sup>=ACBED
</pre>

Como ya vimos el cierre de A incluye a todos los elementos de la relación, es decir A es una súper llave. En las mismas condiciones, si calculamos el cierre de AE, vemos que el cierre de AE también contiene a todos los elementos de la relación y por lo tanto AE también es una súper llave. Y esto es lógico porque A es un subconjunto propio de AE y por lo tanto sí A es una súper llave AE también lo es. Pero AE es más grande que A porque A es un subconjunto propio de AE.

### LLaves candidatas

Entonces vamos a decir que A es una llave candidata pero AE no lo es; no es lógico que utilicemos AE si podemos utilizar simplemente A que es una llave más pequeña. 

>Las llaves candidatas son todas aquellas super llaves que no tienen ningún **subconjunto propio** que también sea una super llave. 

Veamos una relación con varias llaves candidatas. 

foto

En esta **relación Persona** podemos identificar las súper llaves: 

- documento nacional de identidad
- número de pasaporte
- número de Seguro Social

Todas ellas son llaves candidatas ya que todas son **súper llaves** y **no hay ningún subconjunto propio** de cada una de ellas que también sea una súper llave.

### Llave primaria y llave alterna

En la anterior relación **relación Persona** pudimos identificar las súper llaves: 

- documento nacional de identidad
- número de pasaporte
- número de Seguro Social

La llave candidata que escogemos que identifique la relación (pues sólo puede haber una) la llamamos **llave primaria** o **primary key**. Las no escogidas reciben el nombre de **llave alterna**.