# Resumen: Normalización de Bases de Datos

La normalización en bases de datos busca establecer esquemas relacionales que cumplan con ciertas condiciones, a través de las formas normales. A continuación, se resume la normalización hasta la Tercera Forma Normal (3FN) y la Forma Normal de Boyce y Codd (FNBC):

## Primera Forma Normal (1FN):
- **Definición:** Prohibición de grupos repetitivos en una relación, donde un atributo no puede tener más de un valor del dominio subyacente.
- **Obligatoriedad:** Restricción inherente al modelo relacional.

## Segunda Forma Normal (2FN):
- **Definición:** Una relación está en 2FN si, además de cumplir con 1FN, los atributos no clave suministran información acerca de la clave completa.
- **Ejemplo:** Descomposición de la relación PRESTAMO en PRESTAMO1 y LIBRO.

## Tercera Forma Normal (3FN):
- **Definición:** Una relación está en 3FN si, además de estar en 2FN, los atributos no clave facilitan información solo acerca de la(s) clave(s) y no acerca de otros atributos.
- **Ejemplo:** Descomposición de la relación LIBRO en LIBRO1 y EDITORIAL.

## Forma Normal de Boyce y Codd (FNBC):
- **Definición:** Una relación está en FNBC si el conocimiento de las claves candidatas permite averiguar todas las interrelaciones existentes entre los datos.
- **Ejemplo:** Descomposición de la relación PRESTAMO1 en SOCIO y PRESTAMO2.

## Ejemplo de Descomposición:
- **Relaciones Descompuestas:**
  - LIBRO1( cod_libro, editorial )
  - EDITORIAL( editorial, país )
  - SOCIO( num_socio, nombre_socio )
  - PRESTAMO2( num_socio, cod_libro, fec_prest )

## Dependencias en la Teoría de Normalización:
- **Funcionales:** Relacionadas con 2FN, 3FN y FNBC.
- **Multivaluadas:** Relacionadas con la 4FN.
- **De Proyección o Combinación:** Relacionadas con la 5FN.

La normalización mejora la eficiencia, consistencia y reduce redundancias en las bases de datos al seguir estas formas normales.
