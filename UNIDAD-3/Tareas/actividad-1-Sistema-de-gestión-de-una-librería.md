# Ejercicio 1- Sistema de gestión de una librería

## Método paso a paso para transformar un modelo E/R

   1. Localiza las entidades del diagrama.
   2. Crea una tabla por cada entidad e incluye sus atributos.
   3. Marca la clave primaria (PK) de cada tabla.
   4. Busca las relaciones 1:N y coloca las FKs en el lado N.
   5. Busca las relaciones N:M y crea las tablas intermedias correspondientes.
   6. Revisa las relaciones 1:1 y decide dónde colocar una FK única.
   7. Comprueba los casos especiales: entidades débiles, reflexivas, jerarquías y ternarias.
   8. Revisa los resultados: ninguna FK debe hacer referencia a un registro inexistente; determina cuáles pueden admitir `NULL` y qué valores deben ser únicos.

## Entidades del modelo

- Provincia
- Localidad
- Cliente
- Autor
- Almacén
- Cesta
- Libro
- Editorial
- Papel
- Ebook
