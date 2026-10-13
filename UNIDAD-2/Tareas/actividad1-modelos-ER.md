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

<img width="482" height="77" alt="Juego de Tronos (2) drawio" src="https://github.com/user-attachments/assets/d953e584-e4f0-4cc7-ab74-ec4cbc932171" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
| PERSONAJE | Los personajes que pertencen a una casa | (0,N) |
| CASA | A cuantas casas puede pertenecer un personaje | (1,1) |

### Modelo completo E/R

<img width="592" height="236" alt="Juego de Tronos drawio (2)" src="https://github.com/user-attachments/assets/4e9912f4-03bd-4183-9ba5-58eab21d5f79" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|Personaje| Código, nombre, fecha de nacimiento |
|Casa| Código, nombre, lema, nombre de asentamiento |
