# [:back:](/)  Base canónica

>Vamos a hablar de las **dependencias funcionales** como un **conjunto de elementos** y mediante ciertas operaciones **vamos a transformar** este conjunto en otro **conjunto más pequeño** que vamos a llamar **cierre canónico**.

## Cierre canónico sobre dependientes

<pre>
R(A, B, C, D)

B  &#10132; A
AD &#10132; BC
C  &#10132; ABD
</pre>

Si decomponemos las dependecial funcionales anteriores nos queda:

<pre>
R(A, B, C, D)

B  &#10132; A

AD &#10132; B
AD &#10132; C

C &#10132; A
C &#10132; B
C &#10132; D
</pre>

1. Cierre de B

<pre>
B  &#10132; A 

B<sup>+</sup>  = B,A

Ahora calcularemos de nuevo el cierre como si no existiera la dependencia funcional  B  &#10132; A 
B<sup>+</sup>  = B
</pre>

Observamos que hay pédida de información puesto que son diferentes. Por lo tanto no lo podemos eliminar. **Es esencial**.

2. Primer cierre de AD

<pre>
AD  &#10132; B

AD<sup>+</sup>  = A,D,B,C

Ahora calcularemos de nuevo el cierre como si no existiera la dependencia funcional  AD  &#10132; B 
AD<sup>+</sup>  = A,D,C,B
</pre>

Observamos que no hay pédida de información. Por lo tanto lo podemos eliminar. **NO es esencial**.

3. Segundo cierre de AD

<pre>
AD  &#10132; C

AD<sup>+</sup>  = A,D,C,B

Ahora calcularemos de nuevo el cierre como si no existiera la dependencia funcional  AD  &#10132; C 
AD<sup>+</sup>  = A,D
</pre>

Observamos que hay pédida de información puesto que son diferentes. Por lo tanto no lo podemos eliminar. **Es esencial**.

Recapitulemos. Nos queda por ahora:

<pre>
R(A, B, C, D)

B  &#10132; A

AD &#10132; C

C &#10132; A
C &#10132; B
C &#10132; D
</pre>

Sigamos:

<pre>
C  &#10132; A

C<sup>+</sup>  = C,A,B,D

Ahora calcularemos de nuevo el cierre como si no existiera la dependencia funcional  C  &#10132; A 
C<sup>+</sup>  = C,B,A,D
</pre>

No hay pérdida de información podemos prescindir de ella.

<pre>
C  &#10132; B

C<sup>+</sup>  = C,B,D,A

Ahora calcularemos de nuevo el cierre como si no existiera la dependencia funcional  C  &#10132; B 
C<sup>+</sup>  = C,D
</pre>

Es esencial

<pre>
C  &#10132; D

C<sup>+</sup>  = C,D,B,A

Ahora calcularemos de nuevo el cierre como si no existiera la dependencia funcional  C  &#10132; D 
C<sup>+</sup>  = C,B,A
</pre>

Es esencial

El cierre canónico nos quedaría

<pre>
R(A, B, C, D)

B  &#10132; A

AD &#10132; C

C &#10132; B,D
</pre>

## Cierre canónico sobre determinantes

<pre>
R(A, B, C, D)

B  &#10132; A

AD &#10132; C

C &#10132; B,D
</pre>

Trabajaremos sobre el **detreminante AD**:

<code>α - A = D</code>

<pre>D<sup>+</sup> = D</pre>

<code>α - D = A</code>

<pre>A<sup>+</sup> = A</pre>

No es posible simplificar los valores.