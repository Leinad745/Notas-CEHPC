# Modulo 6 - Explotacion

## Metasploit

Marcio de codigo abierto basado en ruby para hallazgos, explotacion y validacion de vulnerabilidades informaticas. Sus componentes:

- **Exploits**: Son modulos que toman ventaja de las vulnerabilidades en los sistemas para explotarlas.

- **Payloads**: Comandos o programas que se ejecutan en los sitemas luego de haberse explotado la vulnerabilidad. Estos pueden ser personalizados para satisfacer objetivos especificos.

- **Encoders**: Modulos utilizados para ofuscar o cifrar payloads y evitar deteccion por parte de las soluciones de seguridad.
- **Auxiliary**: Son modulos adicionales que proporcionan herramientas para tareas especificas de hacking, como la recopilacion de informacion del sistema o la enumeracion de contraseñas

### Comandos Basicos

- **search**: Busca informacion almacenada en los modulos anteriormente mencionados. Buscan por CVE, nombre de servicio, tipo de exploit.

- **use**: Carga un modulo especifico.

- **show options**: Muestra una lista de todas las opciones requeridad y configurables para el modulo en uso, junto con una breve descripcion de cada opcion.
- **set**: establece opciones requeridas para el modulo.
  - **set TARGET**: selecciona el OS/App de la victima
  - **set RHOST**: selecciona la IP de destino.
  - **set LHOST**: seleccion la IP del host local.
  - **set PAYLOAD**: configura la carga util
