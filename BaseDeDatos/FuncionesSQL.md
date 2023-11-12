# Funciones SQL

### SELECT 
- **Función:** Obtener Datos
- **Ejemplo:** `SELECT column1`
### ORDER BY
- **Función:** Ordena los resultados de la consulta según una o más columnas, de forma ascendente o descendente.
- **Ejemplo:** `SELECT column1, column2 FROM table ORDER BY column1 ASC, column2 DESC;`

### DISTINCT
- **Función:** Devuelve valores únicos de una columna o conjunto de columnas.
- **Ejemplo:** `SELECT DISTINCT column FROM table;`

### WHERE
- **Función:** Filtra registros basados en una condición dada.
- **Ejemplo:** `SELECT * FROM table WHERE condition;`

### Operadores Lógicos (AND, OR, NOT, IN)
- **Función:** Combina condiciones lógicas en las cláusulas WHERE.
- **Ejemplo:** `SELECT * FROM table WHERE condition1 AND condition2;`

### LIMIT
- **Función:** Limita el número de filas devueltas en el resultado de la consulta.
- **Ejemplo:** `SELECT * FROM table LIMIT 10;`

### BETWEEN
- **Función:** Filtra resultados dentro de un rango especificado.
- **Ejemplo:** `SELECT * FROM table WHERE column BETWEEN value1 AND value2;`

### LIKE
- **Función:** Filtra resultados basados en patrones de texto.
- **Ejemplo:** `SELECT * FROM table WHERE column LIKE 'pattern%';`

### IS NULL / IS NOT NULL
- **Función:** Filtra registros que son (o no son) nulos.
- **Ejemplo:** `SELECT * FROM table WHERE column IS NULL;`

## Funciones de Agregación
Estas funciones permiten realizar cálculos sobre conjuntos de datos, proporcionando información resumida y estadísticas útiles.

### COUNT
- **Función:** Devuelve el número de filas en un conjunto de resultados.
- **Ejemplo:** `SELECT COUNT(column) FROM table;`

### SUM
- **Función:** Calcula la suma de los valores en una columna numérica.
- **Ejemplo:** `SELECT SUM(column) FROM table;`

### AVG
- **Función:** Calcula el promedio de los valores en una columna numérica.
- **Ejemplo:** `SELECT AVG(column) FROM table;`

### MIN
- **Función:** Devuelve el valor mínimo en una columna.
- **Ejemplo:** `SELECT MIN(column) FROM table;`

### MAX
- **Función:** Devuelve el valor máximo en una columna.
- **Ejemplo:** `SELECT MAX(column) FROM table;`


## Agrupación y Filtrado de Grupos

### GROUP BY
- **Función:** Agrupa filas que tienen los mismos valores en columnas específicas.
- **Ejemplo:** `SELECT column1, COUNT(column2) FROM table GROUP BY column1;`

### HAVING
- **Función:** Filtra resultados de la agrupación basándose en condiciones.
- **Ejemplo:** `SELECT column1, COUNT(column2) FROM table GROUP BY column1 HAVING COUNT(column2) > 1;`

## Joins - Unir Tablas

### INNER JOIN
- **Función:** Devuelve registros que tienen valores coincidentes en ambas tablas.
- **Ejemplo:** `SELECT * FROM table1 INNER JOIN table2 ON table1.column = table2.column;`

### CROSS JOIN
- **Función:** Devuelve el producto cartesiano de las tablas unidas.
- **Ejemplo:** `SELECT * FROM table1 CROSS JOIN table2;`

### LEFT JOIN
- **Función:** Devuelve todos los registros de la tabla izquierda y los registros coincidentes de la derecha.
- **Ejemplo:** `SELECT * FROM table1 LEFT JOIN table2 ON table1.column = table2.column;`

### RIGHT JOIN
- **Función:** Devuelve todos los registros de la tabla derecha y los registros coincidentes de la izquierda.
- **Ejemplo:** `SELECT * FROM table1 RIGHT JOIN table2 ON table1.column = table2.column;`

### OUTER JOIN
- **Función:** Devuelve registros cuando hay una coincidencia en una de las tablas.
- **Ejemplo:** `SELECT * FROM table1 FULL OUTER JOIN table2 ON table1.column = table2.column;`

## UNION
- **Función:** Combina los resultados de dos o más consultas.
- **Ejemplo:** `SELECT column FROM table1 UNION SELECT column FROM table2;`

## Subconsultas y Operadores
### ANY, ALL, SOME
- **Función General:** Utilizados con subconsultas para comparar valores.
  
### ANY
- **Función:** Compara un valor con cualquier valor devuelto por la subconsulta.
- **Ejemplo:** `SELECT column FROM table WHERE column > ANY (SELECT column FROM table2);`

### ALL
- **Función:** Compara un valor con todos los valores devueltos por la subconsulta.
- **Ejemplo:** `SELECT column FROM table WHERE column > ALL (SELECT column FROM table2);`

### SOME
- **Función:** Similar a ANY, compara un valor con algunos de los valores devueltos por la subconsulta.
- **Ejemplo:** `SELECT column FROM table WHERE column > SOME (SELECT column FROM table2);`

### EXISTS
- **Función:** Verifica si la subconsulta devuelve algún resultado.
- **Ejemplo:** `SELECT column FROM table WHERE EXISTS (SELECT * FROM table2 WHERE condition);`

Estas funciones y cláusulas proporcionan herramientas poderosas para manejar y filtrar datos en SQL.
