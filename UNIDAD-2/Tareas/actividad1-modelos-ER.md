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
|EJEMPLAR| Cuantos ejemplares pueden corresponder a una especie| (1,N) |
|ESPECIE| A cuantas especies puede corresponder un ejemplar| (1,1) |
|EJEMPLAR| Cuantos ejemplares pertenecen a un entrenador| (0,N) |
|ENTRENADOR| A cuantos entrenadores puede corresponder un ejemplar| (1,1) |

### Modelo completo E/R
<img width="601" height="341" alt="Pokemon drawio (3)" src="https://github.com/user-attachments/assets/798934ab-c53e-4fc4-8053-ddc6ec39d032" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|ENTRENADOR| Código, Nombre, Región_de_origen |
|EJEMPLAR| Código, Apodo_opcional, Nivel_opcional, Fecha_de_captura |
|ESPECIE| Tipo_principal, Número_de_Pokédex, Nombre |

## 3. Breaking Bad: personajes y episodios

### Posibles entidades y relaciones

 De cada **personaje** guarda un código, un nombre y una ocupación. También registra los **episodios** mediante un código único, junto con su título, temporada, número de episodio y duración en minutos. La guía anota, para cada _aparición_ concreta, el tiempo aproximado en pantalla y si el personaje tiene un papel principal o secundario en ese episodio.
 
**-Entidades:** PERSONAJE, EPISODIOS

**Relaciones:** aparece_en

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|aparece_en| Cuantos personajes aparecen en un episodio| En cuantos episodios aparece un personaje|

### Modelos de la frase
<img width="477" height="72" alt="Breaking Bad (2) drawio" src="https://github.com/user-attachments/assets/9764ed03-fdd7-41b4-ae90-bef78c731f47" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|PERSONAJE| Cuantos personajes aparecen en un episodio| (1,N)|
|EPISODIO| En cuantos episodios aparece un personaje| (1,N)|

### Modelo completo E/R
<img width="662" height="242" alt="Breaking Bad drawio" src="https://github.com/user-attachments/assets/25b7236c-5db7-4e83-b3ae-f0ab08d07062" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|PERSONAJE| Código, nombre, ocupación|
|EPISODIO| Código, título, temporada, número_de_episodio, duración_en_minutos|

### 4. Minecraft: mundos y construcciones

De cada **mundo** guarda un código, un nombre y su fecha de creación.  De cada **construcción** se guarda su número, nombre y fecha de inicio. El servidor registra además **jugadores** mediante un código y un nombre de usuario. De cada _colaboración_ se guarda la fecha en que comenzó.  

**-Entidades:** MUNDO, CONSTRUCCIÓN, JUGADORES

**Relaciones:** colaboran_en

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|colaboran_en| Los jugadores que colaboran en un mundo | En cuantos mundos colaboran los jugadores |
|colaboran_en| Los jugadores que colaboran en una construcción | En cuantas construcciones colaboran los jugadores |

### Modelos de la frase

<img width="477" height="72" alt="Breaking Bad (2) drawio" src="https://github.com/user-attachments/assets/9764ed03-fdd7-41b4-ae90-bef78c731f47" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|JUGADORES| Los jugadores que colaboran en un mundo | (1,N) |
|MUNDO| Los mundos en los que colaboran los jugadores | (1,N) |
|JUGADORES| Los jugadores que colaboran en una construcción | (0,N) |
|CONSTRUCCIÓN| Las construcciones en las que colaboran los jugadores | (0,N) |

### Modelo completo E/R
<img width="662" height="242" alt="Breaking Bad drawio" src="https://github.com/user-attachments/assets/25b7236c-5db7-4e83-b3ae-f0ab08d07062" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|JUGADORES| Nombre_de_usuario, código|
|MUNDO| Código, nombre, fecha_de_creación|
|CONSTRUCCIÓN| Número, nombre, fecha_de_inicio|

## 5. Fortnite: escuadrones y partidas

### Posbles entidades y relaciones

Una aplicación de Fortnite registra **jugadores** mediante un código, un nombre de usuario y su fecha de alta. Un **jugador** puede _pertenecer_ a un escuadrón como máximo, y un **escuadrón** puede tener varios jugadores. De cada **escuadrón** se guarda un código y un nombre. La aplicación registra **partidas** mediante un código, fecha, hora y modo de juego. De la _participación_ de cada jugador en cada partida se almacena su posición final y el número de eliminaciones.

**-Entidades:** JUGADOR, PARTIDA, ESCUADRÓN

**-Relaciones:** participa_en, pertenece_a

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|participa_en| Cuántos jugadores participan en una partida | En cuántas partidas participa un jugador |
|pertenece_a| Cuántos jugadores pertencen a un escuadrón | A cuántos escuadrones pertenece un jugador |

### Modelos de la frase
<img width="422" height="262" alt="Fortnite (2) drawio" src="https://github.com/user-attachments/assets/1dc518c9-6e1a-4cb8-8cf3-ca42abb51b8a" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|JUGADOR| Cuántos jugadores participan en una partida | (1,N) |
|PARTIDA| En cuantas partidas puede participar un jugador | (1,1) |
|JUGADOR|Cuántos jugadores pertenecen a un escuadrón | (1,N) |
|ESCUADRÓN| En cuántos escuadrones puede pertenecer un jugador| (1,1) |

### Modelo completo E/R
<img width="662" height="392" alt="Fortnite drawio" src="https://github.com/user-attachments/assets/e18256d8-32bc-4d19-b4ea-38e7894e8287" />
