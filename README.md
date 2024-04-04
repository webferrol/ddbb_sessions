# <img src="https://github.com/webferrol/ddbb_sessions/assets/35032717/074eaa75-7314-4fb9-b3f4-62269f839235" width="24" alt="Sesión sobre"> Base de datos

## Classroom

☑️ [BBDD]([https://classroom.google.com/c/NjA1NzIyNDc3MzUx?cjc=hugqvan](https://github.com/webferrol/ddbb_sessions/assets/35032717/26a0155a-db5d-43d3-bb76-b22d5d391842))

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

## Modelo relacional

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
   La **dependencia transitiva** ocurre cuando **una columna depende de otra que a su vez no es una clave principal**.
  Consideremos los siguientes campos para una librería:
  - ID_PEDIDO
  - TITULO_LIBRO
  - AUTOR_LIBRO
  - EDITORIAL_LIBRO.
    
  El campo, ID_PEDIDO depende directamente de TITULO_LIBRO, dado que cada pedido está asociado a un título de libro específico. Sin embargo, tanto AUTOR_LIBRO como EDITORIAL_LIBRO dependen indirectamente de ID_Pedido a través de su dependencia con TITULO_LIBRO, puesto que cada libro (identificado por su título) está vinculado a un único autor y a una única editorial. Esta cadena de dependencias muestra que AUTOR_LIBRO y EDITORIAL_LIBRO tienen una dependencia transitiva respecto a ID_PEDIDO a través de TITULO_LIBRO.

## Enlaces de intereses

☑️ [Para diagramar](https://www.drawio.com/blog/move-diagrams-net)

![entity-relationship](https://github.com/webferrol/ddbb_sessions/assets/35032717/1b92ede6-ec40-43bb-891b-623e0a36502e)

☑️ [mysql +node + typescript +  crud](https://www.youtube.com/playlist?list=PLCKuOXG0bPi3nKe-CHNQ5jwJ5V4SR77yd)
