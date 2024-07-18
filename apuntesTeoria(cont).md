# Apunte de teoria para el final de OC
## RAID
### ¿Como se llego al uso de sistemas RAID?
El desarrollo del Sistema RAID se dio al ver que los la velocidad de discos de memoria secundaria era significativamente menor a la de los procesadores se llevo a cavo tal sistema que proponia usar multiples 
discos que trabajaban independientemente de cada uno y en paralelo para ciertas tares , de tal forma era 
mas facil trabajar con tareas que solicitaran accesos a informacion que estaba distrbuida en los discos .
Ejemplo : 
Si en el sistema RAID conformado por los discos X1,X2 y X3 y se esta realizando un tarea E/S en la cual se
trabaja con informacion que esta en X1 y X3 la tarea se llevara a cabo manejando cada disco de forma independiente
la informacion que almacena y trabajando en paralelo para la tarea a realizar 
## Niveles RAID
### Los niveles RAID tienen 3 caracteristicas comunes : 
1. RAID Es un conjunto de unidades fisicas vistas por el sistema operativo como una unica unidad logica 
2. Los datos se distribuyen a atraves de las unidades fisicas del conjunto de unidades 
3. La capacidad de los discos redundantes se usa para almacenar informacion de paridad que garantice la recuperacion de los datos en caso de fallo de disco.
> [!NOTE]
> Las caracterisiticas 2 y 3 varian segun el nivel .RAID 0 no soporta la caracteristica 3.