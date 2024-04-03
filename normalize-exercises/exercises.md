# Proceso de normalización

Recordemos

## Primera forma normal

- ✔️ No debe haber tuplas repetidas
- ✔️ No debe importar el orden de las tuplas
- ✔️ Existencia de una Llave Primaria
- ✔️ Atributos atómicos

⚠️ Aunque estas características ya vimos que está impuestas por el propio modelo relacional

>**La Forma de Los Grupos Repetitivos**: Una Relación está en Primera Forma Normal (1NF) si, y sólo si, no tiene **Grupos Repetitivos**

## Ejercicios de normalización

### Ejercicio 1

| id_estudiante | dni | nombre | curso | nacionalidad |
| ------------- | --- | ------ | ----- | ------------ |
| 1 | 20286841-K | Jorge | 	Matemáticas, Lenguaje |	Chile |
| 2 | 18075847-K | Brenda | Matemáticas| Colombia |
| 3 | 17016778-3 | Luis	 | Historia | Argentina |
| 4 | 21616330-3 | Flor	 | Historia, Ciencias |	Cuba |

### Ejercicio 2

| id_estudiante | dni | tutor | clase1 | clase2 | clase3 |
| ------------- | --- | ----- | ---- | ------ | ------ |
| 1 | 20286841-K | Jorge | 111-02 |	111-02 | 111-03 |
| 2 | 18075847-K | Brenda | 211-02 |	211-02 | 211-03 |
| 3 | 17016778-3 | Luis	 | 311-02 |	311-02 | 311-03 |
| 4 | 21616330-3 | Flor	 | 411-02 |	411-02 | 411-03 |
