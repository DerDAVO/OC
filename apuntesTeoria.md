# <center>Organización de Computadoras (apuntes)</center>

## Redundant Array of Independent Disks

> RAID es una combinación de varias unidades para trabajar con ellas como si fueran una sola. La finalidad de un sistema **RAID** es la de proteger los datos en caso de que alguno de los discos falle, o en algunos casos es la de mejorar la velocidad de lectura sobre los discos que conforman el sistema.

### Redundancia

> La redundancia en el contexto de almacenamiento de datos y sistemas informáticos se refiere a la duplicación de componentes o información para aumentar la fiabilidad y disponibilidad del sistema. Esto significa que si un componente falla, otro puede asumir su función sin pérdida de datos o interrupción del servicio. La redundancia se utiliza para proteger contra fallos y asegurar la continuidad operativa.

### Tipos de configuración

* Disk Mirroring

    > Esto permite la redundancia de datos, ante un posible fallo en uno de los discos la información aún está disponible en el disco restante.

* Disk Stripping

    > No busca la redundancia de datos, en cambio su objetivo es la velocidad de transferencia de los mismos.
<details>
   <summary><h2>RAIDS 0 a 6 </h2></summary>
   <details>
  <summary><h3>RAID 0</h3></summary>
      
  > **Funcionamiento**: RAID 0 utiliza la técnica de "striping" para dividir los datos en bloques más pequeños y distribuirlos entre múltiples discos duros. Esto mejora significativamente el rendimiento de lectura y escritura, ya que varios discos pueden trabajar simultáneamente.
  >
  > **Ventajas**:
  > - Mejora notable en la velocidad de lectura/escritura.
  > - Utilización eficiente de múltiples discos.
  >
  > **Desventajas**:
  > - Falta de redundancia: no ofrece tolerancia a fallos. Si uno de los discos falla, se pierden todos los datos.
  > - Mayor riesgo de pérdida de datos.
  >
  > **Objetivo**: Mejorar el rendimiento mediante la distribución de datos entre discos para operaciones más rápidas.
</details>

<details>
  <summary><h3>RAID 1</h3></summary>
      
  > **Funcionamiento**: RAID 1 utiliza "mirroring" para duplicar los datos en dos o más discos duros. Cada disco contiene la misma información, proporcionando redundancia.
  >
  > **Ventajas**:
  > - Alta disponibilidad y redundancia: si un disco falla, los datos siguen estando disponibles en el otro(s).
  > - Tolerancia a fallos mejorada.
  >
  > **Desventajas**:
  > - Costo más alto debido a la duplicación de almacenamiento.
  > - No mejora la velocidad de lectura/escritura significativamente.
  >
  > **Objetivo**: Mejorar la fiabilidad y la disponibilidad de datos mediante la duplicación.
</details>

<details>
  <summary><h3>RAID 2</h3></summary>
      
  > **Funcionamiento**: RAID 2 utiliza "bit-level striping" con bits de paridad distribuidos entre los discos. Cada bit de datos se divide y se almacena en discos separados, con bits de paridad para verificar errores.
  >
  > **Ventajas**:
  > - Alta velocidad de lectura debido al striping a nivel de bits.
  > - Capacidad de detectar y corregir errores con la paridad.
  >
  > **Desventajas**:
  > - Implementación compleja y costosa.
  > - Menor eficiencia en comparación con otros niveles de RAID más modernos.
  >
  > **Objetivo**: Proporcionar alta velocidad y fiabilidad en entornos que requieren tolerancia a fallos y detección/corrección de errores a nivel de bit.
</details>

<details>
  <summary><h3>RAID 3</h3></summary>
      
  > **Funcionamiento**: RAID 3 utiliza "byte-level striping" con un disco dedicado para la paridad. Los datos se dividen en bytes y se distribuyen entre los discos, mientras que un disco se utiliza exclusivamente para almacenar información de paridad.
  >
  > **Ventajas**:
  > - Alto rendimiento en operaciones de lectura secuencial.
  > - Tolerancia a fallos con la paridad dedicada.
  >
  > **Desventajas**:
  > - Rendimiento limitado en escritura debido a la dependencia del disco de paridad.
  > - Menor eficiencia en entornos con múltiples operaciones de escritura simultáneas.
  >
  > **Objetivo**: Mejorar el rendimiento en aplicaciones que realizan muchas operaciones de lectura secuencial y necesitan cierta redundancia.
</details>

<details>
  <summary><h3>RAID 4</h3></summary>
      
  > **Funcionamiento**: RAID 4 utiliza "block-level striping" con un disco dedicado para la paridad. Los datos se dividen en bloques más grandes y se distribuyen entre los discos, con un disco dedicado para almacenar la paridad de los bloques.
  >
  > **Ventajas**:
  > - Mejora el rendimiento en operaciones de lectura secuencial.
  > - Tolerancia a fallos con la paridad dedicada.
  >
  > **Desventajas**:
  > - Rendimiento limitado en escritura debido a la dependencia del disco de paridad.
  > - Problemas de rendimiento en entornos con muchas operaciones de escritura simultáneas.
  >
  > **Objetivo**: Proporcionar un equilibrio entre rendimiento y tolerancia a fallos en entornos que manejan grandes volúmenes de datos secuenciales y necesitan redundancia.
</details>

<details>
  <summary><h3>RAID 5</h3></summary>
      
  > **Funcionamiento**: RAID 5 utiliza "striping" con paridad distribuida. Los datos se dividen en bloques y se distribuyen entre varios discos, mientras que la paridad se distribuye entre todos los discos para proporcionar redundancia.
  >
  > **Ventajas**:
  > - Buena combinación de rendimiento y redundancia.
  > - Mejora la velocidad de lectura y tolera la pérdida de un disco sin pérdida de datos.
  >
  > **Desventajas**:
  > - Rendimiento reducido durante la reconstrucción después de un fallo.
  > - Complejidad adicional en la implementación y gestión.
  >
  > **Objetivo**: Mejorar la tolerancia a fallos y el rendimiento en entornos que requieren tanto capacidad como velocidad.
</details>

<details>
  <summary><h3>RAID 6</h3></summary>
      
  > **Funcionamiento**: Similar a RAID 5 pero con una segunda paridad distribuida. Permite la pérdida de hasta dos discos sin pérdida de datos, mejorando aún más la tolerancia a fallos.
  >
  > **Ventajas**:
  > - Alta tolerancia a fallos: puede resistir la pérdida de dos discos simultáneamente.
  > - Mejora la seguridad de los datos críticos.
  >
  > **Desventajas**:
  > - Menor rendimiento en comparación con configuraciones RAID más simples debido a la sobrecarga de paridad adicional.
  > - Costo más alto debido al uso de más discos para la paridad.
  >
  > **Objetivo**: Proporcionar una mayor protección de datos en aplicaciones críticas donde la tolerancia a fallos es fundamental.
</details>

</details>
### Operación XOR (Exclusivo OR)

> Si la cantidad de 1 en la entrada es un número impar, entonces la salida se activa => 1
>
> #### Tabla XOR
>
> | A | B | S |
> | -- | -- | -- |
> | 0 | 0 | 0 |
> | 0 | 1 | 1 |
> | 1 | 0 | 1 |
> | 1 | 1 | 0 |
