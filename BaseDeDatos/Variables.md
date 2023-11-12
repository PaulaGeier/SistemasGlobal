# Variables en SQL

## Declaración de Variables
En SQL, puedes declarar variables utilizando la palabra clave `DECLARE`. Las variables pueden ser de diferentes tipos de datos, como INT, VARCHAR, etc.

```sql
DECLARE @mi_variable INT;
DECLARE @nombre VARCHAR(50);
```
## Asignación de Valores
Para asignar valores a variables, se utiliza la palabra clave SET.

```sql
SET @mi_variable = 10;
SET @nombre = 'Juan';
```
## Uso de Variables en Consultas
Puedes utilizar variables en consultas para realizar operaciones o filtrar resultados.
```sql
SELECT * FROM empleados WHERE salario > @mi_variable;
```
## Variables en Procedimientos Almacenados
Las variables son comúnmente utilizadas en procedimientos almacenados para almacenar y manipular datos.
```sql
CREATE PROCEDURE obtener_empleados_con_salario_superior
    @salario_limite INT
AS
BEGIN
    SELECT * FROM empleados WHERE salario > @salario_limite;
END;
```
