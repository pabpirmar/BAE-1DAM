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


## 2. Pokémon: la colección de capturas

### Posbles entidades y relaciones

De cada **entrenador** guarda un código, un nombre y una región de origen. También mantiene un catálogo de especies Pokémon: cada especie tiene su número de Pokédex, su nombre y su tipo principal. Cada **ejemplar** tiene un código propio, un apodo opcional, su nivel actual y la fecha de captura. Cada ejemplar _pertenece a_ un único **entrenador** y _corresponde_ a una única **especie**.

**-Entidades:** ENTRENADOR, EJEMPLAR, ESPECIE

**-Relaciones:** pertenece_a, corresponde_a

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|corresponde_a| Cada ejemplar corresponde a una única especie | Cada especie puede corresponder a varios ejemplares |
|pertence_a| Cada ejemplar pertenece a un único entrenador | Cada entrenador puede corresponder a varios ejemplares |

### Modelos de la frase
<img width="282" height="252" alt="Pokemo (2) drawio" src="https://github.com/user-attachments/assets/584902e4-717e-4589-819d-d9dc57ebfc3b" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|EJEMPLAR| Cuantos ejemplares pueden corresponder a una especie| (0,N) |
|ESPECIE| A cuantas especies puede corresponder un ejemplar| (1,1) |
|EJEMPLAR| Cuantos ejemplares pertenecen a un entrenador| (0,N) |
|ENTRENADOR| A cuantos entrenadores puede corresponder un ejemplar| (1,1) |

### Modelo completo E/R
<img width="601" height="341" alt="Pokemon drawio (2)" src="https://github.com/user-attachments/assets/83ef2f17-3e4b-47c7-9908-1411db49e1fa" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|ENTRENADOR| Código, Nombre, Región_de_origen |
|EJEMPLAR| Código, Apodo_opcional, Nivel_opcional, Fecha_de_captura |
|ESPECIE| Tipo_principal, Número_de_Pokédex, Nombre |
