# Apuntes de Organizacion de Computadoras
## Redundant Array of Independent Disks
> RAID es una combinacion de varias unidades para trabajar con ellas com si fuesen una sola.
> La finalidad de un sistema ***RAID*** es la de proteger los datos en caso de que aluguno de los sicos falle , o en algunos casos es la de mejorar la velocidad de lectura de sobre los discos que conforman el sistema.
### Tipos de confiuraion
* Disk Mirroring
    * Esto permite la redundancia de datos ante un posible fallo.
* Disk Stripping
    * No busca la redundancia de datos, en cambio su objetivo es la velocidad de transferencia de los mismos.
### Redundancia
> La redundancia en el contexto de almacenamiento de datos y sistemas informáticos se refiere a la duplicación de componentes o información para aumentar la fiabilidad y disponibilidad del sistema. Esto significa que si un componente falla, otro puede asumir su función sin pérdida de datos o interrupción del servicio. La redundancia se utiliza para proteger contra fallos y asegurar la continuidad operativa
## ***RAID 0***
## ***RAID 1***
## ***RAID 2***
## ***RAID 3***
## ***RAID 4***
## ***RAID 5***
## ***RAID 6***
### ***OR Exclusivo o XOR *** ⊕
> Si la cantidad de 1 en la entrada es un numero impar, entonces la salida se activa => 1
#### Tabla ⊕
| A | B | S |
| -- | -- | -- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |