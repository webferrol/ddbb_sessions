# Proceso de normalización

Recordemos

## Primera forma normal (1FN)

- ✔️ No debe haber tuplas repetidas.
- ✔️ No debe importar el orden de las tuplas.
- ✔️ Existencia de una Llave Primaria.
- ✔️ Atributos atómicos.

⚠️ Aunque estas características ya vimos que está impuestas por el propio modelo relacional

>**La Forma de Los Grupos Repetitivos**: Una Relación está en Primera Forma Normal (1NF) si, y sólo si, no tiene **Grupos Repetitivos**

## Segunda forma normal (2FN)

- ✔️ Cumple con las reglas de 1FN.
- ✔️ Todos los atributos que no forman parte de la **Clave Principal** tienen **dependencia funcional completa** de ella. Dicho de otra forma: No debe haber dependencias parciales de ninguna **clave candidata** en ninguna columna no clave.

>**Forma de la Dependencia Funcional completa**: Ningún atributo depende únicamente de una parte de la Llave Primaria.

## Ejercicios de normalización

### Ejercicio 1

| #id_estudiante | dni | nombre | curso | nacionalidad |
| ------------- | --- | ------ | ----- | ------------ |
| 1 | 20286841-K | Jorge | 	Matemáticas, Lenguaje |	Chile |
| 2 | 18075847-K | Brenda | Matemáticas| Colombia |
| 3 | 17016778-3 | Luis	 | Historia | Argentina |
| 4 | 21616330-3 | Flor	 | Historia, Ciencias |	Cuba |

### Ejercicio 2

| #id_estudiante | dni | tutor | clase1 | clase2 | clase3 |
| ------------- | --- | ----- | ---- | ------ | ------ |
| 1 | 20286841-K | Jorge | 111-02 |	111-02 | 111-03 |
| 2 | 18075847-K | Brenda | 211-02 |	211-02 | 211-03 |
| 3 | 17016778-3 | Luis	 | 311-02 |	311-02 | 311-03 |
| 4 | 21616330-3 | Flor	 | 411-02 |	411-02 | 411-03 |

### Ejercicio 3

| #id_pedido | titulo_libro | autor | editorial |
| ----------| ------------ | ----- | --------- |
| 1 | El Cid Campeador | Anómimo | Anaya |
| 2 | Don Quijote de la Mancha | Miguel de Cervantes | Anaya |
| 3 | La Odisea | Homero | Oxford Editorial |
| 4 | As Metamorfoses | Ovidio | Edicións Xerais |

### Ejercicio 4

| #DNI | Nombre | #Curso | FechaMatrícula | Tutor | LocalidadAlumno | ProvinciaAlumno |
| --- | ------ | ----- | -------------- | ----- | --------------- | --------------- |
| 11111111A | Eva | 1ESO-A | 01-Julio-2016 | Isabel | Écija | Sevilla |
| 22222222B | Ana | 1ESO-A | 09-Julio-2016 | Isabel | Écija | Sevilla |
| 33333333C | Susana | 1ESO-B | 11-Julio-2016 | Roberto | Écija | Sevilla |
| 44444444D | Juan | 2ESO-A | 05-Julio-2016 | Federico | El Villar | Córdoba |
| 55555555E | José | 2ESO-A | 02-Julio-2016 | Federico | El Villar | Córdoba |
