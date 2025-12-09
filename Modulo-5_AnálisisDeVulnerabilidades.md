# Modulo 5: Analisis de Vulnerabilidades

## Vulnerabilidades

Las vulnerabilidades son brechas de seguridad presentes en cualquier software. Al explotarse, pueden permitir a los atacantes obtener acceso no autorizado a informacion confidencial o causar problemas a toda la organizacion.

Las vulnerabilidades descubiertas se registran con una ID de CVE y un puntaje del CVSS en funcion del daño que podria costar su explotacion.

El analisis de vulnerabilidades es el proceso de identificar los sitemas en la red que tiene vulnerabilidades conocidas o indentificadas como exploits, fallas, brechas de seguridad, puntos de entrada y errores de configuracion.

### Common Vulnerability Score System (CVSS)

Medida que calcula la severidad de una vulnerabilidad en los sistemas informaticos.

CVSS v2 Vector (AV:N/AC:L/Au:N/C:C/I:C/A:C)

- **AV**:Vector de acceso.
- **AC**:Complejidad de Acceso.
- **Au**: Autenticacion.
- **C**: Impacto de confidencialidad.
- **I**: Impacto de integridad.
- **A**: Impacto a la disponibilidad.

### CVE

Los puntos vulnerables y exposiciones comunes son una lista de fallas de seguridad informatica que esta disponible publicamente.

### Nessus

Es un programa de escaneo de vulnerabilidades, que escanea los puertos y intenta usar exploits en aquellos abiertos con el fin de encontrar vulnerabilidades.

### OWASP ZAP

Herramienta que ofrece una amplia gama de funcionalidades, incluyendo escaneos automáticos, pruebas manuales, intercepcion y modificacion de trafico.

## Analisis de vulnerabilidades manual

- **Script vuln**: Comando nmap que permite identificar vulnerabilidades conocidas en el sistema

```bash
sudo nmap -f -sS -SV -Pn -script vuln
```

- **Script Auth**: Comando nmap que detecta usuarios anonimos al igual muestra el listado usuarios con permisos de super usuarios.

```bash
sudo nmap -f -sS -SV -Pn -script auth
```

- **Script Default**: Realiza escaneos con scripts predeterminados.

```bash
sudo nmap -f -sS -SV -Pn -script default
```

- **Script Safe**: Ejecuta secuencias de comandos poco intrusivas para la victima, minimazando el riesgo de interrupcion de aplicaciones.

```bash
sudo nmap -f -sS -SV -Pn -script safe
```
