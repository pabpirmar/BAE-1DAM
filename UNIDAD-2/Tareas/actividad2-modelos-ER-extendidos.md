# Actividad 2. Modelos E/R extendidos

## Ejercicio 1. Star Wars: flota de la Alianza Rebelde

### 1.Posibles entidades y las relaciones.

La Alianza Rebelde necesita organizar la información de los vehículos de su flota, las bases donde _se encuentran_ y las misiones para las que están _asignados_. De cada **vehículo** se guarda un código único, un nombre de identificación, el año de fabricación y su estado operativo. De cada **base** se guarda un código único, un nombre y el planeta donde está situada. De cada **misión** se registra un código único, un nombre, un objetivo y una fecha de inicio.

**-ENTIDADES:** VEHÍCULO, BASE, MISIÓN

**-RELACIONES:** se_encuentra_en, asignado_a

### 2.Frases que describan el problema.

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|se_encuentra_en| Un vehículo se encuentra en una y solo una base | En la base se encuentran ninguno, uno, o varios vehículos |
|asignado_a| Un vehículo está asignado a ninguna o una misión | Una misión puede tener asignados uno o varios vehículos |

### 3.Los modelos de cada frase.

#### -Modelo individual 1
<img width="452" height="152" alt="Modelo-individual(1) drawio" src="https://github.com/user-attachments/assets/0c5a84c0-968a-4c8e-bbf2-d8e7889455ba" />

#### -Modelo individual 2
<img width="422" height="132" alt="Modelo-individual(2) drawio" src="https://github.com/user-attachments/assets/73707a17-a033-4c88-971a-63685c27c73d" />

#### -Modelo individual 3
<img width="442" height="442" alt="Modelo-individual(3) drawio" src="https://github.com/user-attachments/assets/6b79c290-4a1f-4fd2-840b-1a6312012f75" />

### 4.Identificación de entidades y análisis su fortaleza.


### 5.Estudio de cardinalidad.

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
|VEHÍCULO| En cuántas bases se encuentra un vehículo | (1,1) |
|BASE| Cuántos vehículos se encuentran en una base | (0,N) |
|VEHÍCULO| En cuántas misiones está asignado un vehículo | (0,1) |
|MISIÓN| Cuántos vehículos se encuentran en una misión | (1,N) |

### 6 y 7. Modelo completo E/R y colocar los atributos a cada entidad e interrelación.

<img width="1212" height="692" alt="Stars Wars drawio" src="https://github.com/user-attachments/assets/6528d7c6-d7cb-4ecb-977c-51f2f538e9e6" />

## Ejercicio 3. Jujutsu Kaisen: academia de hechicería

### 1.Posibles entidades y las relaciones.

De cada **integrante** se guarda un único código, su nombre y su fecha de incorporación. Un integrante puede ser estudiante , docente o no desempeñar todavía ninguno de esos dos papeles. También es posible que una misma persona sea estudiante y docente a la vez. De los estudiantes se registra su curso actual y su nivel de energía maldita. De los **docentes** se guarda su especialidad y sus años de experiencia. Los estudiantes y los docentes conservan el código que tienen como integrantes de la academia. La academia organiza **misiones** , de las que almacena un código único, una descripción, una fecha y un nivel de peligro. De la _participación_ de cada estudiante en cada misión se registra el papel asignado y una evaluación, que puede estar pendiente.

### 2.Frases que describan el problema.

| Relación | Lectura directa | Lectura inversa |
|---|---|---|
|participa_en| Un estudiante participa en ninguna, una o muchas misiones | En una misión participa al menos un estudiante |
|dirige| Un docente dirige ninguna, una o muchas misiones | Una misión es dirigida por exactamente un docente |

### 3.Los modelos de cada frase.

#### -Modelo individual 1
<img width="207" height="202" alt="modelo (1) drawio (1)" src="https://github.com/user-attachments/assets/5990f6f5-b055-448e-a4f8-c6c24a782e1f" />

#### -Modelo individual 2
<img width="431" height="62" alt="modelo(2) drawio" src="https://github.com/user-attachments/assets/aed27830-a952-4f75-9964-eeab57770356" />

#### -Modelo individual 3
<img width="556" height="217" alt="modelo(3) drawio" src="https://github.com/user-attachments/assets/3692c61d-f029-44df-a03b-81ea8369ce26" />

### 5.Estudio de cardinalidad.

| Partimos de... | Contamos... | Mínimo y máximo |
|---|---|---|
| DOCENTE | En cuántas misiones está asignado un docente | (0,N) |
| MISIÓN | Cuántos docentes responsables tiene una misión | (1,1) |
| ESTUDIANTE | En cuántas misiones participa un estudiante | (0,N) |
| MISIÓN | Cuántos estudiantes participan en una misión | (1,N) |

### 6 y 7. Modelo completo E/R y colocar los atributos a cada entidad e interrelación.

<img width="914" height="412" alt="Jujutsu Kaisen drawio" src="https://github.com/user-attachments/assets/14997784-1709-4b39-9d75-22128d676f1f" />
