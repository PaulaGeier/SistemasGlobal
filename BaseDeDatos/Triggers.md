# Triggers en MySQL

Un Trigger en MySQL es un programa almacenado creado para ejecutarse automáticamente cuando ocurre un evento en la base de datos, como INSERT, UPDATE o DELETE.

## Crear un Trigger en MySQL

La sintaxis para crear un Trigger en MySQL es similar a la creación de Procedimientos y Funciones:

```sql
CREATE [DEFINER={usuario|CURRENT_USER}] TRIGGER nombre_del_trigger
{BEFORE|AFTER} {UPDATE|INSERT|DELETE} ON nombre_de_la_tabla
FOR EACH ROW
<bloque_de_instrucciones>
```
- DEFINER={usuario|CURRENT_USER}: Indica el usuario con privilegios para la invocación del Trigger. Por defecto, es CURRENT_USER.
- nombre_del_trigger: Nombre del trigger, siguiendo una nomenclatura práctica.
- BEFORE|AFTER: Especifica si el Trigger se ejecuta antes o después del evento DML.
- UPDATE|INSERT|DELETE: Elige la sentencia que activará el Trigger.
- ON nombre_de_la_tabla: Establece el nombre de la tabla asociada.
- FOR EACH ROW: Indica que el Trigger se ejecuta por cada fila en la tabla asociada.
- <bloque_de_instrucciones>: Define el bloque de sentencias que el Trigger ejecutará al ser invocado.

## Ejemplo Práctico
Supongamos que queremos crear un Trigger que registre cambios en la tabla "clientes" cada vez que se realiza una actualización:

```sql
CREATE TRIGGER registro_cambios_clientes
BEFORE UPDATE ON clientes
FOR EACH ROW
BEGIN
    INSERT INTO historial_cambios_clientes (id_cliente, fecha_cambio)
    VALUES (OLD.id, NOW());
END;
```
En este ejemplo, el Trigger se ejecutará antes de una actualización en la tabla "clientes", registrando el cambio en una tabla de historial.
