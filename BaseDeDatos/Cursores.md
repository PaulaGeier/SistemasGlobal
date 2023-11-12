# Cursores en SQL

## Definición
Los cursores en SQL son estructuras que permiten recorrer los resultados de una consulta de manera secuencial. Proporcionan un mecanismo para procesar filas una a una, facilitando el acceso y manipulación de datos en el contexto de un procedimiento almacenado o un bloque de código.

## Tipos de Cursores
Existen dos tipos principales de cursores:

### Cursor Implícito
- Se utiliza automáticamente para procesar el resultado de una consulta.
- Apto para recorrer filas generadas por una consulta SELECT.

### Cursor Explícito
- Se crea y maneja explícitamente en el código del usuario.
- Brinda mayor control y flexibilidad, pero requiere más código.

## Ciclo de Vida Básico
1. **Declaración del Cursor:**
   ```sql
   DECLARE nombre_cursor CURSOR FOR SELECT columna FROM tabla;
    ```
2. **Apertura del Cursor:**
   ```sql
   OPEN nombre_cursor;
    ```
3. **Declaración del Cursor:**
   ```sql
   FETCH nombre_cursor INTO variable;
-- Procesar la fila actual
    ```
4. **Declaración del Cursor:**
   ```sql
   CLOSE nombre_cursor;
   ```
## Ejemplo Basico

```sql
-- Declaración del Cursor
DECLARE ejemplo_cursor CURSOR FOR SELECT nombre FROM empleados;

-- Apertura del Cursor
OPEN ejemplo_cursor;

-- Recorrido y Procesamiento de Filas
FETCH ejemplo_cursor INTO @nombre_empleado;
WHILE @@FETCH_STATUS = 0 DO
    -- Procesar la fila actual
    PRINT @nombre_empleado;

    -- Obtener siguiente fila
    FETCH ejemplo_cursor INTO @nombre_empleado;
END WHILE;

-- Cierre del Cursor
CLOSE ejemplo_cursor;

```
## Consideraciones
- Es importante cerrar el cursor después de su uso para liberar recursos.
- El uso adecuado de cursores puede mejorar la eficiencia y flexibilidad en ciertos escenarios, pero en general, se recomienda evitarlos cuando sea posible debido a su impacto en el rendimiento.
   
