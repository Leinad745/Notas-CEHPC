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

#### Metodo Three-wayshandshake

1. Inicio de conexion TCP, el origen envia un paquete SYN
2. El destino responde con un paquete SYN/CK
3. El paquete ACK confirma la llegada del primer paquete SYN a la fuente
4. La fuente envia un paquete ACK para el paquete ACK/SYN transmitido por el destino
5. Desencadena una conexion "OPEN" permitiendo la comunicacion entre origen y destino, hasta que uno envia un paquete "FIN" o "RST" para cerrar la conexion.

### Introduccion a NMAP

Es una herramienta que permite el escaneo de redes para el descubrimiento de hosts y servicios en una red.

#### Categorias de Escaneo nmap

- **Descubrimiento de hosts**: Detecta hosts o dispositivos activos en la red, indetificando equipos vivos y como realizar trabajos sobre estos.
- **Escaneo de ping ARP**: Envia paquetes ARP para descubrir los dispositivos activos en el rango IPv4, aunque este oculta por un firewall.
- **Escaneo de ping ICMP ECHO**: Envia paquetes al sistema destino para recopilar la informacion necesarias.
- **Escaneo de ping UDP**: Envia paquetes UDP al host destino.

#### Tecnicas de escaneo

- **Escaneo TCP completo (-sS)**: tecnica predeterminada, escanea todos los puertos tcp del host para encontrar caules estan abiertos.
- **Escaneo TCP ACK (-sA)**: determina si un firewall esta filtrando el trafico. Envia un paquete ACK al host objetivo y espera una respuesta RST/ACK para determinar si el puerto fue filtrado.
- **Escaneo TCP Connect (-sT)**: Determina si un puerto esta abierto. Establece una conexion tcp con el host objetivo y espera una respuesta SYN/ACK, para detectar si el puerto esta abierto
- **Escaneo UDP (-sU)**: Escanea todos los puertos udp del host para encontrar cuales estan abiertos.
- **Escaneo TCP NULL (-sN)**: Determina si un puerto esta abierto, envia paquetes sin banderas, esperando una respuesta RST.
- **Escaneo TCP FIN (-sF)**: Envia un paquete fin al host objetivo, esperando una respuesta.
- **Escaneo TCP Xmas**: Envia un paquete con las banderas FIN, PSH, y URG, esperando respuesta RST para ver si esta abierto.
