# <img src="https://github.com/webferrol/ddbb_sessions/assets/35032717/ae35f1a1-9575-4107-aedb-4303aebcf82f" width="24" alt="Sesión sobre"> Base de datos

## <img src="https://github.com/webferrol/ddbb_sessions/assets/35032717/9167d33e-5c58-48a6-b2a2-2501fa456ff7" width="24" alt="Invitación a "> Classroom

☑️ Invitación a [classroom](https://classroom.google.com/c/NjA1NzIyNDc3MzUx?cjc=hugqvan)

## Conceptos

### Dato

**Representación simbólica** de un *atributo* o *variable* cuantitiva o cualificada.

Como representa una entidad, hecho o momento (sólo uno) aisladamente es irrelevante, incomprensible y no contiene información.

### Base de datos (<abbr title="Base de datos">BBDD</abbr>)

**Colección** de *datos informativos* **organizados** en un mismo contexto para su uso y vinculación.

### Modelo de datos o conceptual

**Lenguaje de modelado** para la definición de **esquemas**.

<dl>
  <dt>Esquema</dt>
  <dd>Representación Gráfica o Simbólica de cosas materiales o inmateriales.
</dl>

![Modelo base de datos relacional](https://github.com/webferrol/ddbb_sessions/assets/35032717/c0a86f4c-e4e9-43a1-82ee-b0bec8431647)

## Modelos de <abbr title="Base de Datos">BBDD</abbr>
1. **Modelo de archivos planos**
    - Difíciles de manejar
2. **Modelo jerárquico**
    - Tiene estructuras como *entidades*, *atributos* y *relaciones*
3. **Modelo de redes**
    - Grafos
4. **Modelo relacional**
    - Teoría de los conjuntos, álgebra relacional, relaciones, tuplas, lenguaje de alto nivel ...

## Modelo relacional (modelo conceptual)

- [Introducción](./relational-model.md)
- [Álgebra relacional](./algebra-relacional.md)
- [Dependencias funcionales](./dependencias-funcionales.md)
- [Base canónica](./base-canonica.md)

## Normalización

1. **Primera Forma normal**:
   La Forma de Los Grupos Repetitivos
3. **Segunda Forma normal**:
   Forma de la Dependencia Funcional completa
5. **Tercera Forma normal**:
   Un **atributo no primo** no depende transitivamente de una **clave candidata**.
  Consideremos los siguientes campos para una librería:
  - ID_PEDIDO
  - TITULO_LIBRO
  - AUTOR_LIBRO
  - EDITORIAL_LIBRO.
    
  El campo, ID_PEDIDO depende directamente de TITULO_LIBRO, dado que cada pedido está asociado a un título de libro específico. Sin embargo, tanto AUTOR_LIBRO como EDITORIAL_LIBRO dependen indirectamente de ID_Pedido a través de su dependencia con TITULO_LIBRO, puesto que cada libro (identificado por su título) está vinculado a un único autor y a una única editorial. Esta cadena de dependencias muestra que AUTOR_LIBRO y EDITORIAL_LIBRO tienen una dependencia transitiva respecto a ID_PEDIDO a través de TITULO_LIBRO.

## Entidad/Relación (modelo lógico)

### Entidad y tipo de entidad

Se puede definir una **entidad** como cualquier objeto (real o abstracto) que existe en lo realidad y acerca del cual queremos almacenar información en la base de datos.

>ℹ️ La estructura genérica que describe un **conjunto de ejemplares** aplicando la abstracción de lo clasificación se denomina **tipo de entidad** mientras que la **entidad** es **cada uno de los ejemplares**.

![entity-relationship](https://github.com/webferrol/ddbb_sessions/assets/35032717/1b92ede6-ec40-43bb-891b-623e0a36502e)

### Programas para diagramar

- ☑️ [Para diagramar](https://www.drawio.com/blog/move-diagrams-net)

## Nivel físico

### <abbr title="Structured Query Language">SQL</abbr>

Una de las características que *Edgar Frank Codd* destaca en el modelo **modelo conceptual** es que éste: 

>ℹ️ Provee las bases para un lenguaje de consulta de alto nivel. Por tanto se debe brindar independencia de la estructura de los datos en la máquina.

En este nivel ya hablamos de <abbr title="Structured Query Language">SQL</abbr>

### Comandos básicos

- ☑️ DDL (Data Definition Language)
  
    <abbr title="Data Definition Language">DDL</abbr> es un conjunto de comandos <abbr title="Structured Query Language">SQL</abbr> utilizados para **crear**, **modificar** y **eliminar** *estructuras de bases de datos*, pero no los datos propios.
  
- ☑️ DQL (Data Query Language)

    Las declaraciones <abbr title="Data Query Language">DQL</abbr> se utilizan para realizar consultas sobre los datos dentro de los objetos del esquema.

- ☑️ DML(Data Manipulation Language)

    <abbr title="Data Manipulation Language">DML</abbr> Los comandos <abbr title="Structured Query Language">SQL</abbr> que se ocupan de la manipulación de datos presentes en la base de datos pertenecen a **DML** o Data Manipulation Language y esto incluye la mayoría de las declaraciones <abbr title="Structured Query Language">SQL</abbr>.

- ☑️ DCL (Data Control Language)

     <abbr title="Data Control Language">DCL</abbr> incluye comandos como **GRANT** y **REVOKE** que se ocupan principalmente de los **derechos**, **permisos** y otros controles del sistema de base de datos. 

- ☑️ TCL (Transaction Control Language)

    Las transacciones (<abbr title="Transaction Control Language">TCL</abbr>) agrupan un conjunto de tareas en una sola unidad de ejecución. Cada transacción comienza con una tarea específica y termina cuando todas las tareas del grupo se completan con éxito.

[![Comandos básicos: DDL, DQL, DML, DCL, TCL](./assets/comandos-basicos.png)](https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/)

### Comandos para sacarnos de apuros

#### Para obtener información de las tablas entre otras cosas ver los nombres de las "constraints" o restricciones

```sql
SHOW CREATE TABLE nombre_tabla;
```

### Funciones

#### `IFNULL`

- **Sintaxis**: `IFNULL(expr1, expr2)`
- **Propósito**: Devuelve `expr2` si `expr1` es `NULL`; de lo contrario, devuelve `expr1`.
- **Compatibilidad**: Esta función es específica de MySQL.
- **Número de argumentos**: Acepta exactamente dos argumentos.

 ```sql
 SELECT IFNULL(nombre, 'Desconocido') FROM usuarios;
 ```
  
 En este ejemplo, si el valor de `nombre` es `NULL`, se devuelve 'Desconocido'; de lo contrario, se devuelve el valor de `nombre`.

#### `COALESCE`

- **Sintaxis**: `COALESCE(expr1, expr2, ..., exprN)`
- **Propósito**: Devuelve el primer valor no nulo en la lista de expresiones.
- **Compatibilidad**: Esta función es parte del estándar SQL y es compatible con la mayoría de las bases de datos (MySQL, PostgreSQL, SQL Server, Oracle, etc.).
- **Número de argumentos**: Puede aceptar dos o más argumentos.

```sql
SELECT COALESCE(nombre, apodo, 'Desconocido') FROM usuarios;
```
En este ejemplo, se devuelve el primer valor no nulo entre `nombre`, `apodo` y 'Desconocido'. Si `nombre` es `NULL`, se evalúa `apodo`; si ambos son `NULL`, se devuelve 'Desconocido'.

#### `YEAR`

se utiliza para extraer el año de una fecha dada.

**Obtener el año de una fecha específica**:

```sql
SELECT YEAR('2024-05-17') AS year;
```

#### `CURDATE`

Devuelve al fecha actual

#### `SUBDATE` 

En MySQL se utiliza para restar un intervalo de tiempo a una fecha. Esta función puede tomar dos formas principales: restar un número de días o restar un intervalo específico. A continuación, se muestran ejemplos de ambas formas:

1. Restar un número de días de una fecha

```sql
SELECT SUBDATE('2024-05-19', 10) AS fecha_menos_diez_dias;
```

En este ejemplo, se resta 10 días de la fecha '2024-05-19'. El resultado será '2024-05-09'.

2. Restar un intervalo específico de una fecha

Puedes restar un intervalo de tiempo específico utilizando la función `INTERVAL`. Los intervalos pueden ser días, meses, años, horas, minutos, segundos, etc.

2.1. Ejemplo de restar días:

```sql
SELECT SUBDATE('2024-05-19', INTERVAL 10 DAY) AS fecha_menos_diez_dias;
```

Este ejemplo también resta 10 días de la fecha '2024-05-19'. El resultado será '2024-05-09'.

2.2 Ejemplo de restar meses:

```sql
SELECT SUBDATE('2024-05-19', INTERVAL 2 MONTH) AS fecha_menos_dos_meses;
```

Este ejemplo resta 2 meses de la fecha '2024-05-19'. El resultado será '2024-03-19'.

2.3 Ejemplo de restar años:

```sql
SELECT SUBDATE('2024-05-19', INTERVAL 1 YEAR) AS fecha_menos_un_año;
```

Este ejemplo resta 1 año de la fecha '2024-05-19'. El resultado será '2023-05-19'.

2.4 Ejemplo práctico en una tabla

Supongamos que tienes una tabla `eventos` con una columna `fecha_evento` y quieres seleccionar todas las filas donde la fecha del evento sea al menos 30 días antes de hoy.

```sql
SELECT *
FROM eventos
WHERE fecha_evento <= SUBDATE(CURDATE(), INTERVAL 30 DAY);
```

En este ejemplo, `CURDATE()` devuelve la fecha actual, y `SUBDATE(CURDATE(), INTERVAL 30 DAY)` devuelve la fecha actual menos 30 días. La consulta selecciona todos los eventos que ocurrieron hace 30 días o más.

Estos ejemplos demuestran cómo se puede utilizar la función `SUBDATE` en MySQL para restar intervalos de tiempo de fechas.

#### `COUNT`

en SQL se utiliza para contar el número de filas en un conjunto de resultados que cumplen con una condición específica. Es una de las funciones de agregación más comunes y útiles en SQL.

##### Parámetros

- **expression**: Puede ser una columna específica o un asterisco (`*`). 
  - `COUNT(*)`: Cuenta todas las filas en el conjunto de resultados.
  - `COUNT(column_name)`: Cuenta las filas en las que `column_name` no es `NULL`.
  - `COUNT(DISTINCT column_name)`: Cuenta las filas únicas en las que `column_name` no es `NULL`.

**Contar todas las filas de una tabla**:
```sql
 SELECT COUNT(*) AS total_filas FROM empleados;
 ```
 
Este ejemplo cuenta todas las filas de la tabla `empleados`.

**Contar las filas que no tienen valores nulos en una columna específica**:

```sql
SELECT COUNT(email) AS total_emails FROM usuarios;
```
Este ejemplo cuenta las filas de la tabla `usuarios` donde la columna `email` no es `NULL`.

**Contar filas con valores distintos en una columna**:

```sql
SELECT COUNT(DISTINCT departamento) AS departamentos_unicos FROM empleados;
```
Este ejemplo cuenta el número de valores únicos en la columna `departamento` de la tabla `empleados`.

##### Consideraciones

- `COUNT(*)` es generalmente más rápido que `COUNT(column_name)` porque no necesita verificar si los valores son `NULL`.
- `COUNT(column_name)` es útil cuando necesitas contar solo las filas donde la columna específica no es `NULL`.
- `COUNT(DISTINCT column_name)` es útil para contar valores únicos en una columna, ignorando duplicados y `NULL`.

En resumen, la función `COUNT` es extremadamente versátil y esencial para realizar análisis de datos y generar reportes en SQL.

### Programas gestores de BBDD

- ☑️ [Línea de comandos](https://desarrolloweb.com/articulos/2408.php)
- ☑️ [Gestor de BBDD: DBeaver](https://dbeaver.io/)
- ☑️ [Gestor de BBDD: MySQL Workbench](https://www.mysql.com/products/workbench/)
- ☑️ [Gestor de BBDD: Navicat](https://www.navicat.com/es)

## Enlaces de intereses

- ☑️ [mysql +node + typescript +  crud](https://www.youtube.com/playlist?list=PLCKuOXG0bPi3nKe-CHNQ5jwJ5V4SR77yd)
