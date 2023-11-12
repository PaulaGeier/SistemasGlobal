# Procedimientos Almacenados en MySQL

## Qué es un procedimiento almacenado

Un procedimiento almacenado es un conjunto de instrucciones guardadas en el servidor para un uso posterior. Se nombran con la cláusula `PROCEDURE` y, a diferencia de las funciones, no retornan ningún valor. Pueden ser ejecutados desde el cliente mediante un comando y contienen instrucciones que se ejecutarán con frecuencia.

## Ventajas de usar procedimientos en MySQL

- **Seguridad:** Ocultan el nombre de las tablas a usuarios sin privilegios, proporcionando una capa de seguridad.
- **Estándares de código:** Facilitan la creación de sinergia en equipos de desarrollo al usar los mismos procedimientos.
- **Velocidad:** Es más eficiente ejecutar un programa ya definido mediante ciertos parámetros que reescribir las instrucciones.

## Crear un procedimiento en MySQL

La creación de un procedimiento comienza con la cláusula `CREATE PROCEDURE`. Se define un nombre y los parámetros necesarios para su funcionamiento, seguido por el cuerpo del procedimiento dentro de un bloque `BEGIN` y `END`.

```sql
DELIMITER //
CREATE PROCEDURE nombre_procedimiento ([parámetro1, parámetro2, ...])
[Atributos de la rutina]
BEGIN
  -- Instrucciones
END //
DELIMITER ;


