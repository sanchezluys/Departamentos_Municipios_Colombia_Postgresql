# Base de Datos de Departamentos y Municipios de Colombia
# Para Postgresql

<hr>
    <img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Flag_of_Colombia.svg" alt="Bandera Colombia" width="150px">
<hr>

## Descripción

Este repositorio contiene una base de datos estructurada de los departamentos y municipios de Colombia. La base de datos está diseñada para ser utilizada en proyectos que requieran información geográfica y administrativa detallada del país. El SQL esta diseñado y verificado para PostgreSQL Version 16

## Contenido

La base de datos incluye:

- **Departamentos**: Lista completa de los departamentos de Colombia.
- **Municipios**: Lista completa de los municipios, asociados a sus respectivos departamentos.


## Diagrama Entidad Relación

![alt DER](/imagenes/diagramaEntidadRelacion.png)

## Estructura de la Base de Datos

La base de datos está organizada en las siguientes tablas:

### Tabla: `departamentos`

| Campo  | Tipo         | Descripción                          |
| ------ | ------------ | ------------------------------------ |
| id_departamento     | INT          | Identificador único del departamento |
| departamento | VARCHAR(255) | Nombre del departamento              |

### Tabla: `municipios`

| Campo           | Tipo         | Descripción                       |
| --------------- | ------------ | --------------------------------- |
| id_municipio              | INT          | Identificador único del municipio |
| municipio          | VARCHAR(255) | Nombre del municipio              |
| departamento_id | INT          | Identificador del departamento, llave Foranea  |

## Ejemplos de Consultas

### Obtener todos los departamentos

```sql
SELECT * FROM departamentos;
```

### Resultado:

![alt Query_departamentos](/imagenes/query_departamentos.png)


### Obtener todos los municipios

```sql
SELECT * FROM departamentos;
```

### Resultado:

![alt Query_municipios](/imagenes/query_municipios.png)


### Obtener todos los municipios con su departamento con un JOIN

```sql
SELECT 
        municipio,
        departamento
FROM 	municipios
JOIN 	departamentos 
        ON municipios.departamento_id = departamentos.id_departamento
```

![alt ListadoConJoin](/imagenes/query_join.png)

