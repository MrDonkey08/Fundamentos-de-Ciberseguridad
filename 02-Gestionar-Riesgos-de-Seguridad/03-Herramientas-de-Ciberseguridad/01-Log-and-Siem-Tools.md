# Logs y Herramientas SIEM

## Logs

Un **log** o **registro** es un registro de eventos que suceden dentro de los
sistemas y redes de una organización.

Los logs comúnmente se guardan en archivos logs. Un **archivo log** guarda un
conjunto de logs que pertenecen a un mismo grupo o categoría (e.g., logs de
inicio de sesión).

### Fuentes comunes de logs

- **Logs de firewall**: Registros de intentos de conexión o conexiones
  establecidas de tráfico proveniente del internet. También incluye solicitudes
  salientes a internet desde dentro de la red.

- **Logs de red**: Registro de todas las computadoras y dispositivos que entran
  y salen de la red. También registra conexiones entre dispositivos o servicios
  dentro la red.

- **Logs de servidor**: Registro de eventos relacionados a servicios, tales como
  sitios web, correos electrónicos, o archivos compartidos. También incluye
  acciones tales como inicio de sesión, contraseña, y solicitud de usuarios.

## Security Information and Event Management (SIEM)

Un **SIEM** es una aplicación que recopila y analiza datos de logs para
monitorizar actividades críticas en una organización. Provee visibilidad en
tiempo-real, monitoreo y análisis de eventos, y alertas automatizadas. También
guarda todos los datos de logs en una ubicación centralizada.

Una herramienta **SIEM** es una aplicación que recopila y analiza datos de logs
para supervisar actividades críticas en una organización. Las herramientas SIEM
ofrecen supervisión y seguimiento en tiempo real de los logs de eventos de
seguridad. A continuación, los datos se utilizan para realizar un análisis
exhaustivo de cualquier amenaza, riesgo o vulnerabilidad de seguridad potencial
que se identifique. Las herramientas SIEM tienen muchas opciones de panel de
control. Cada una de ellas ayuda a los miembros del equipo de ciberseguridad a
gestionar y supervisar los datos de la organización.

### Tipos de herramientas SIEM

- **Auto-alojadas**: Requiere que las organizaciones instalen, operen, y
  mantengan la herramienta haciendo uso de su propia infraestructura física.
  Estas aplicaciones son gestionadas y mantenidas por el departamento TI de la
  organización, en lugar de un proveedor externo. Son ideales cuando una
  organización debe mantener controles físicos de los datos confidenciales.

- **Alojadas en la nube**: Son mantenidos y gestionados por los proveedores de
  SIEM, haciéndolo accesible por medio del Internet. Son ideales para
  organizaciones que no quieren invertir en crear y mantener su propia
  infraestructura.

- **Híbridas**: Una solución híbrida consiste en usar una combinación de ambos,
  herramientas SIEM auto-alojadas y alojadas en la nube. Las organizaciones
  pueden escoger una solución híbrida para aprovechar los beneficios de la nube
  manteniendo el control físico de los datos confidenciales.

### Herramientas SIEM comunes

- **Splunk Enterprise**: Una herramienta self-hosted usada para retener,
  analizar, y buscar datos de los de una organización para proveer información
  de seguridad y alertas en tiempo real.

- **Splunk Cloud**: Una herramienta cloud-hosted usada para recopilar, buscar y
  monitorizar datos de log.

- **Chronicle**: Una herramienta cloud-native diseñada para retener, analizar y
  buscar datos.

<!-- suricata -->

## Referencias

- <https://www.coursera.org/learn/manage-security-risks/lecture/ve2c9/logs-and-siem-tools>

- <https://www.coursera.org/learn/manage-security-risks/supplement/aZDtF/the-future-of-siem-tools>

- <https://www.coursera.org/learn/manage-security-risks/lecture/7TmUB/explore-common-siem-tools>

- <https://www.coursera.org/learn/manage-security-risks/supplement/lCYDs/use-siem-tools-to-protect-organizations>
