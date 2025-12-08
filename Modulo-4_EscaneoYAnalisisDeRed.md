# Modulo 4: Escaneo y Analisis de Red

## 4.1 Introduccion al analisis de red

- **Ping**: Herramienta de diagnostico de red que comprueba la conectividad entre 2 dispositivos.
- **Traceroute**: Diagnostico de red que determina la ruta que sigue un paquete de datos desde su origen hasta su destino final a traves de internet.
- **Barrido de ping**: tecnica usada para identificar los dispositivos activos en la red. Envia paquetes ICMP de tipo "echorequests" a cada direccion en un rango especifico, para ver cuales estan activos.

### Tipos de puertos

1. **TCP (Protocolo de transmision)**: Enfoca en tener una establecida correctamente.
2. **UDP (Protocolo de Datagrama de Usuario)**: Envia paquetes rapido sin orden o prioridad.
3. **SYN**: Sincroniza los numeros de secuencia en 3 segmentos.
   1. Peticion de conexion.
   2. Confirmacion de conexion
   3. Recepcion de confirmacion

### Protocolo de control de mensajes de internet (ICMP)

Protocolo de capa de red que usan los dispositivos de red para diagnosticar problemas de comunicacion en la red. El ICMP se utiliza principalemente para determinal la llegada de los datos.

### SYN/ACK

Bit de control dentro del segmento TCP, que se utiliza para sincronizar numeros de secuencia iniciales de una conexion en el procedimiento de establecimiento de 3 fases.

### Indicadores de comunicacion TCP

Contiene varios indicadores que controlan la transmision de datos a traves de una conexion TCP. Seis flags de control TCP administran la conexion entre hosts y dan instrucciones al sistema.

Cuatro de estas banderas (SYN, ACK, FIN y RST) controlan el establecimiento de conexion, mantenimineto y terminacion de una conexion.

Las otras dos (PSH y URG) precisan instrucciones al sistema.

#### Banderas de comunicacion TCP

- **SYN**: Notifica la transmision de un nuevo numero de secuencia
- **ACK**: Confirma la recepcion de la transmision e identifica el siguiente numero de secuencia esperado.
- **PSH**: Indica que el emisor ha elevado la operacion al receptor. Implicando que el sistema remoto debe informar a la aplicacion receptora sobre los datos almacenados en el bufer remitente.
