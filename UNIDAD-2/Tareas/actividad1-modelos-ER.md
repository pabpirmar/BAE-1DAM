# Actividad 1. Modelos E/R

## 1. Juego de Tronos: las casas de Poniente

### Posbles entidades y relaciones

De cada **casa** conserva un código, su nombre, su lema y el nombre de su asentamiento principal. Cada **personaje** tiene un código, un nombre y una fecha de nacimiento. Cada personaje _pertenece a_ una y solo una casa.

**-Entidades:** Casa y personaje

**-Relación:** pertenece_a

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
| pertenece_a | Cada personaje pertenece a una y solo una casa | Cada casa es pertenecida a un personaje |

### Modelos de la frase

| Modelo parcial | Primera entidad | Relación | Segunda entidad |
|---|---|---|---|
|Frase 1 | Casa | pertenece_a | Personaje |

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
| PERSONAJE | Los personajes que pertencen a una casa | (0,N) |
| CASA | A cuantas casas puede pertenecer un personaje | (1,1) |

### Modelo completo E/R



### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|Personaje| Código, nombre, fecha de nacimiento |
|Casa| Código, nombre, lema, nombre de asentamiento |
