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

### 6. Modelo completo E/R.

<img width="1212" height="692" alt="Stars Wars drawio" src="https://github.com/user-attachments/assets/6528d7c6-d7cb-4ecb-977c-51f2f538e9e6" />

### 7.
