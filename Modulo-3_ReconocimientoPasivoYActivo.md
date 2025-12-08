# Modulo 3 - Reconocimiento Pasivo y Activo

## 3.1 Reconocimiento pasivo

Recoleccion pasiva: implica la recopilacion de informacion sin interaccion directa con sistemas o aplicaciones. Se puede usar:

- Google hacking
- Shodan
- DNS Recon
- Motores de Busqueda
- OSINT

### Open Source Intelligence (OSINT)

metodologia de recoleccion y analisis de informacion que se basa en el uso de fuentes de informacion publicas y abiertas. Esta técnica permite obtener datos valiosos de la victima sin acceder a informacion confidencial.

- **[OSINT FRAMEWORK](https://map.malfrats.industries/)**: plataforma en linea que recopila herraminetas y recursos para la realizacion de OSINT

### Google Hacking

Tecnica que usa busquedas avanzadas en google para la busqueda de informacion sensible o confidencial en la web.

#### Operadores Básicos

| Operador | Descripción |
|----------|-------------|
| **Intext** | Muestra resultados que contengan el texto/término. |
| **Intitle / Allintitle** | Muestra resultados que contengan término en el título. |
| **Inurl / Allinurl** | Muestra resultados que contengan la palabra o término en la URL. |
| **Author** | Sirve para buscar contenido usando el nombre del autor. |
| **Cache** | Muestra resultados de la Caché de un sitio en Google. |
| **Filetype** | Es empleada para buscar archivos mediante su extensión. |
| **Site** | Muestra resultados de un tipo en específico. |

#### Operadores Especiales

| Operador | Descripción |
|----------|-------------|
| **+** | Incluye alguna palabra o término de búsqueda. |
| **-** | Excluye alguna palabra o término de búsqueda. |
| **OR** | Operador booleano. |
| **\|** | Tiene la misma función que el operador booleano. |
| **..** | Permite buscar entre un rango de números. |
| **\*** | Funciona como un comodín. |
| **""** | Muestra resultados que contengan el término exacto dentro de las comillas. |

### Registros DNS

Registros de traduccion de nombres de dominio legibles para los humanos en direcciones IP numericas que las computadoras identifican y ubican unos a otros en la red. Tienen informacion como registros A, AAAA, MX, CNAME, permitiendo asi la comunicacion eficiente en la web.

### WhoIs

Protocolo TCP basado en peticion/Respuesta para efectuar consultas en una base de datos para determinar el propietario de un dominio o IP. Se realiza sobre un dominio ya registrado para ver la informacion publica del dominio.

### Shodan

Motor de busqueda enfocado en la busqueda de sistemas, dispositivos y servicios conectados a internet.

## 3.2 Reconocimiento Activo

### Escaneo y enumeracion de red

Recopila informacion mediante la interaccion directa con los sistemas o aplicaciones. Incluyendo el uso de herramientas automatizadas de escaneo de puertos y servicios, el escaneo de la red en busca de hosts y servicios, y el uso de tecnicas de ingenieria social para recopilar informacion.

### Puertos y Servicios

Puertos logicos, estos se ubican dentro del equipo informatico y permiten establecer comunicaciones con diferentes programas, asi como, realizar la distribucion de servicios y flujo de estos. En total son 65536.

#### Clasificacion de tipo de respuesta de escaneo de puertos

- Abierto: Indica que el puerto esta activo y en uso.
- Cerrado: No hay servicios activos en el puerto
- Filtrado: El firewall filtro y elimino el paquete de solicitud.
