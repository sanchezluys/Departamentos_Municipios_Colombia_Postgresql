# Base de Datos de Departamentos y Municipios de Colombia

![Colombia Flag](https://upload.wikimedia.org/wikipedia/commons/2/21/Flag_of_Colombia.svg)

## Descripción

Este repositorio contiene una base de datos estructurada de los departamentos y municipios de Colombia. La base de datos está diseñada para ser utilizada en proyectos que requieran información geográfica y administrativa detallada del país.

## Contenido

La base de datos incluye:

- **Departamentos**: Lista completa de los departamentos de Colombia.
- **Municipios**: Lista completa de los municipios, asociados a sus respectivos departamentos.

## Estructura de la Base de Datos

La base de datos está organizada en las siguientes tablas:

### Tabla: `departamentos`

| Campo  | Tipo         | Descripción                          |
| ------ | ------------ | ------------------------------------ |
| id     | INT          | Identificador único del departamento |
| nombre | VARCHAR(100) | Nombre del departamento              |

### Tabla: `municipios`

| Campo           | Tipo         | Descripción                       |
| --------------- | ------------ | --------------------------------- |
| id              | INT          | Identificador único del municipio |
| nombre          | VARCHAR(100) | Nombre del municipio              |
| departamento_id | INT          | Identificador del departamento    |

## Ejemplos de Consultas

### Obtener todos los departamentos

```sql
SELECT * FROM departamentos;

