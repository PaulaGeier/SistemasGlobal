# Estructuras Condicionales y Repetitivas en SQL

## Estructuras Condicionales

### CASE
- **Función General:** Realiza evaluaciones condicionales en una consulta.
- **Ejemplo:**
  ```sql
  SELECT column1,
         CASE
            WHEN condition1 THEN result1
            WHEN condition2 THEN result2
            ELSE result3
         END AS new_column
  FROM table;

### IF
- **Función General:** Se utiliza en procedimientos almacenados para ejecutar acciones condicionales.
- **Ejemplo:**
  ```sql
  IF condition THEN
    -- statements
  ELSE
    -- statements
  END IF;

## Estructuras Repetitivas

### WHILE
- **Función General:** Se utiliza en procedimientos almacenados para implementar bucles mientras se cumple una condición.
- **Ejemplo:**
  ```sql
  WHILE condition DO
    -- statements
  END WHILE;

### LOOP
- **Función General:** Implementa un bucle sin una condición de salida explícita.
- **Ejemplo:**
  ```sql
  LOOP
    -- statements
    EXIT WHEN condition;
  END LOOP;
