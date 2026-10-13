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

### Posibles entidades y relaciones

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

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|JUGADOR| Código, nombre de usuario, fecha de alta|
|PARTIDA| Código, fecha, hora, modo de juego|
|ESCUADRÓN| Código, nombre|

## 6. Arcane: personajes y vínculos familiares

### Posibles entidades y relaciones

De cada **personaje** guarda un código, su ciudad de procedencia y su nombre completo. El nombre completo se divide, cuando se conoce, en nombre y apellido; el apellido puede no constar. La enciclopedia quiere registrar qué personajes son _hermanos_ entre sí. Un **personaje** puede no tener _hermanos_ registrados o tener varios. De cada **lugar** se guarda un código y un nombre. De cada _visita_ registrada se conoce la fecha dentro de la cronología de la enciclopedia.

**-Entidades:** PERSONAJE, LUGAR

**Relaciones:** hermano_de, visita

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|hermano_de| Cuántos personajes son hermano de personajes| Cuántos personajes son hermanos de personajes |
|visita| Cuántos personajes visitan un lugar| Cuántos lugares visita un personaje|

### Modelos de la frase
<img width="322" height="172" alt="Arcane (2) drawio" src="https://github.com/user-attachments/assets/a75ec8ee-d186-4790-a9d1-fd6668e9cc71" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|PERSONAJE| Cuántos personajes son hermanos de personajes | (0,N) |
|PERSONAJE| Cuántos personajes son hermanos de personajes | (0,N) |
|PERSONAJE| Cuántos personajes visitan un lugar | (0,N) |
|LUGAR| Cuántos lugares puede visitar un personaje | (0,N) |

### Modelo completo E/R
<img width="791" height="271" alt="Arcane drawio" src="https://github.com/user-attachments/assets/64c89396-c408-47dc-91e5-b5ba7b20fe3c" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|PERSONAJE| Código, ciudad de procedencia, nombre completo|
|LUGAR| Código, nombre| 

## 7. Elden Ring: zonas, jefes y victorias

### Posibles entidades y relaciones

De cada **zona** guarda un código, su nombre y un nivel recomendado. Cada **jefe** tiene un código, un nombre y la cantidad de runas que concede al derrotarlo por primera vez. Cada jefe _aparece en_ una sola zona de esta guía. Los **jugadores** registrados tienen un código y un alias. La guía registra una única **victoria** por cada pareja jugador-jefe, junto con la fecha de esa primera victoria y el número de intentos necesarios.

**-Entidades:** ZONA, JEFE, JUGADOR

**-Relaciones:** aparece_en, derrota

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|derrota| Cuántos jefes puede derrotar cada jugador | Cuántos jugadores pueden derrotar a cada jefe |
|aparece_en| En cuántas zonas aparece cada jefe | Cuántos jefes puede tener cada zona |

### Modelos de la frase
<img width="588" height="60" alt="Elden Ring (2) drawio" src="https://github.com/user-attachments/assets/9eb62301-5832-4937-b408-0c9a2700fe46" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|JUGADOR| Cuantos jugadores pueden derrotar un jefe | (0,N) |
|JEFE| Cuantos jefes puede derrotar un jugador | (0,N) |
|JEFE| Cuantos jefes pueden aparecer en una zona | (1,1) |
|ZONA| En cuantas zonas puede aparecer un jefe | (0,N) |

### Modelo completo E/R
<img width="662" height="173" alt="Elden Ring  drawio" src="https://github.com/user-attachments/assets/3ba3b23e-01e1-4979-841a-3cb54a893acf" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|ZONA| Código, nombre, nivel recomendado|
|JEFE| Código, nombre, cantidad de runas|
|JUGADOR| Código, alias|

## 8. Valorant: jugador, agente y partida

### Posibles entidades y relaciones

Una aplicación de estadísticas de Valorant registra **jugadores** mediante un código y un nombre de usuario; **agentes** mediante un código, un nombre y un rol; y **partidas** mediante un código, una fecha y un mapa. Quiere almacenar qué agente _utilizó_ cada jugador en cada partida.

**-Entidades:** JUGADOR, AGENTE, PARTIDA

**-Relaciones:** utiliza

### Frases que describen el problema

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|utiliza| Con cuántos agentes participa un jugador en una partida | Con cuántos jugadores puede utilizarse un agente en una partida |

### Modelos de la frase
<img width="352" height="144" alt="Valorant (2) drawio" src="https://github.com/user-attachments/assets/fadf4893-6f03-4b5e-a873-9971ccbb2230" />

### Estudio de cardinalidad

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|JUGADOR| Cuantos jugadores pueden utlizar un agente| (0,N) |
|AGENTE| Cuantos agentesson utilizados por un jugador| (0,N)|
|JUGADOR| En cuántas partidas puede participar cada jugador| (1,N) |
|PARTIDA| Con cuántos jugadores puede contar cada partida| (0,N)|

### Modelo completo E/R
<img width="462" height="252" alt="Valorant drawio" src="https://github.com/user-attachments/assets/f11f176c-5d63-40fc-9eca-ec9a92b7cd09" />

### Los atributos y los identificadores
| Entidad | Atributos |
|---|---|
|JUGADOR| Código, nombre de usuario|
|AGENTE| Código, nombre, rol|
|PARTIDA| Código, fecha, mapa|

## 9. Nintendo: versiones de juegos

### Posibles entidades y relaciones


