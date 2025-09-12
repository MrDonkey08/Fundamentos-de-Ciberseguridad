# Refuerzo de Seguridad de la Red

- **Filtrado de puertos**: Función de un firewall que bloquea o permite ciertos
  puertos para limitar comunicaciones no deseadas. Estas reglas se establecen en
  la configuración del firewall.

- Privilegio de acceso a la red
- Encriptación

Algunas tareas que regularmente realizamos son:

- Mantenimiento de las reglas del firewall

- **Análisis de los registros de red**: Proceso de examinar registros para
  identificar eventos de interés. Los equipos de seguridad utilizan una
  herramienta analizadora de registros, conocida como SIEM para realizar
  análisis de red.

- Actualizaciones de parches

- Respaldos de servidores

> [!NOTE]
>
> **SIEM (Security Information and Event Manager)**: Aplicación que recopila y
> analiza datos de registros para monitorizar actividades críticas en una
> organización para monitorizar actividades críticas en una organización.

## Herramientas de seguridad de red

### Firewall

La mayoría de los firewalls son similares en sus funciones básicas. Firewalls
permiten o bloquean tráfico conforme a un conjunto de reglas. Cuando los
paquetes de datos entran a una red, la cabecera del paquete es inspeccionada
para luego ser permitido o denegado en base a su número de puerto. NGFWs son
también capaces de inspeccionas _packet payloads_. Cada sistema debería contar
con su propio firewall, independientemente del firewall de la red.

### Instruction Detection System (IDS)

Un **Intrusion detection system** (IDS) es una aplicación que monitoriza la
actividad del sistema y alerta sobre posibles intrusiones. Un IDS alerta a los
administradores en base en la firma del tráfico malicioso.

El IDS es configurado ara detectar ataques conocidos. Sistemas IDS a menudo
_sniff_ paquetes de datos mientras navegan por la red y los analiza en busca de
características de ataques conocidos. Algunos sistemas IDS no solo revisan
firmas de ataques conocidos, sino también for anomalías que podrían ser una
señal de una actividad maliciosa. Cuando un IDS descubre una anomalía, envía una
alerta al administrador de la red el cual puede investigar más a fondo.

Las limitaciones de los sistemas IDS son que solo pueden escanear por fuentes
conocidas o anomalías obvias. Ataques nuevos o sofisticados pueden no ser
detectados. La otra limitación es que IDS no detienen el tráfico entrante si
detecta algo raro. Depende del administrador de la red de capturar la actividad
maliciosa antes de que llegue a dañar a la red.

Cunado es combinado con un firewall, un IDS agrega otra capa de defensa. El IDS
es colocado detrás del firewall y antes de entrar a la LAN, lo cual permite al
IDS analizar streams de datos después de que el tráfico de red haya sido
filtrado por el firewall. Esto es hecho para reducir sonido en las alertas IDS,
también referidas como falsos positivos.

### Intrusion Prevention System (IPS)

Un **Intrusion prevention system (IPS)** es una aplicación que monitoriza
actividad del sistema en búsqueda de actividad intrusiva para detenerla. Ofrece
incluso mayor protección que un IDS porque activamente detiene anomalías cuando
las detecta, a diferencia del IDS que solo las reporta al administrador de red.

Un IPS busca por firmas de un ataque conocido y anomalías de datos. Un IPS
reporta anomalías para asegurar analistas y bloquear a un emisor específico o
desecha paquetes que se ven sospechosos.

El IPS, al igual que un IDS, se posiciona detrás del firewall in la arquitectura
de red. Esto ofrece un alto nivel de seguridad debido a que _streams_ de datos
peligrosos son interrumpidos antes de que incluso puedan alcanzar partes
sensibles de la red. Sin embargo, una limitación potencial es que si se rompe,
se rompe la conexión entre la red privada y el internet. Otra limitación de un
IPS es la posibilidad de falsos positivos, el cual puede resultar en tráfico
legítimo siendo descartado.

### Full packet capture devices

**Full packet capture devices** pueden ser de gran utilidad para administradores
y profesionales de la seguridad. Estos dispositivos permiten registrar y
analizar todos los datos que son transmitidos a través de tu red. También
apuntan a investigar alertas creadas por un IDS.

## Security Information and Event Management (SIEM)

Un **Security information and event management (SIEM)** es una aplicación que
recopila y analiza datos de registros para monitorizar actividades críticas en
una organización. Herramientas SIEM trabajan en tiempo real para reportar
actividades sospechosas en un _dashboard_ centralizado. Herramientas SIEM
adicionalmente analizan datos de registros de red de fuentes como IDSs, IPSs,
firewalls, VPNs, proxies y registros de DNS. Herramientas SIEM son una manera de
agregar datos de eventos de seguridad para que todo aparezca en un solo lugar
para que los analistas de seguridad puedan analizarlo. Esto es referido como
_single pane of glass_.
