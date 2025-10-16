# TCPdump logs

Un **analizador de protocolos de red**, algunas veces llamado _packet sniffer_,
es una herramienta diseñada para capturar y analizar datos de tráfico dentro de
una red. Son usados comúnmente como herramientas de investigación para
monitorizar redes e identificar actividades sospechosas. Hay una inmensa
variedad de _analizadores de protocolos de red_ disponible; alguno de los más
comunes son los siguientes:

- SolarWinds NetFlow Traffic Analyzer

- ManageEngine OpManager

- Azure Network Watcher

- Wireshark

- tcpdump

## TCPdump

**tcpdump** es una _analizador de protocolos de red_ CLI. Es popular, liviano,
es decir, poco uso de memoria y de CPU y utiliza la librería open-source
libpcap.

tcpdump provee un breve análisis de paquetes y convierte la información clave
acerca tráfico de redes en formatos fácilmente leídos por humanos. Imprime
información acerca del paquete en tu terminal. Adicionalmente, tcpdump también
muestra la dirección IP fuente y destino, y los números de puertos que están
siendo usados en las comunicaciones.

Alguna información que recibes de una captura de un paquete es:

- Timestamp
- IP fuente
- Puerto fuente
- IP destino
- Puerto destino

### Usos comunes

- Establecer una línea de base para patrones de tráfico de red y métricas de uso
  de la red.

- Detectar e identificar tráfico malicioso

- Crear alertas personalizadas para enviar notificaciones correctas cuando se
  encuentran problemas de red o amenazas de seguridad.

- Localizar puntos de mensajería instantánea, tráfico o puntos de acceso
  inalámbrico no autorizados.

Cabe destacar que los _analizadores de protocolos de red_ pueden ser utilizados
maliciosamente para ganar información de una red específica. Por ejemplo,
atacantes pueden capturar paquetes de datos que contienen información sensible,
tal como nombres de usuario y contraseñas e

## Referencias

- Google (s.f.). _Read tcpdump logs_. Connect and Protect: Networks and Network
  Security.
  <https://www.coursera.org/learn/networks-and-network-security/supplement/vqo1C/read-tcpdump-logs>
