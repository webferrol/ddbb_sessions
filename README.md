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

## Nivel físico

### <abbr title="Structured Query Language">SQL</abbr>

Una de las características que *Edgar Frank Codd* destaca en el modelo **modelo conceptual** es que éste: 

>ℹ️ Provee las bases para un lenguaje de consulta de alto nivel. Por tanto se debe brindar independencia de la estructura de los datos en la máquina.

En este nivel ya hablamos de <abbr title="Structured Query Language">SQL</abbr>

### Comandos básicos

- ☑️ DDL (Data Definition Language)
  
  DDL es un conjunto de comandos SQL utilizados para **crear**, **modificar** y **eliminar** *estructuras de bases de datos*, pero no los datos propios.
  
- ☑️ DQL (Data Query Language)
- ☑️ DML(Data Manipulation Language)
- ☑️ DCL (Data Control Language)
- ☑️ TCL (Transaction Control Language)

[![Comandos básicos: DDL, DQL, DML](./assets/comandos-basicos.png)](https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/)


## Enlaces de intereses

- ☑️ [Para diagramar](https://www.drawio.com/blog/move-diagrams-net)
- ☑️ [mysql +node + typescript +  crud](https://www.youtube.com/playlist?list=PLCKuOXG0bPi3nKe-CHNQ5jwJ5V4SR77yd)
- ☑️ [Línea de comandos](https://desarrolloweb.com/articulos/2408.php)
- ☑️ [Gestor de BBDD: DBeaver](https://dbeaver.io/)
- ☑️ [Gestor de BBDD: MySQL Workbench](https://www.mysql.com/products/workbench/)
- ☑️ [Gestor de BBDD: Navicat](https://www.navicat.com/es)

