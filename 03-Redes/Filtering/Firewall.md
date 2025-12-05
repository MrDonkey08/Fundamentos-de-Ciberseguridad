# Firewall

Un **firewall** (o _cortafuegos_) es un sistema de seguridad —ya sea
**software** o **hardware**— que actúa como una **barrera** entre una red (o
dispositivo) y posibles amenazas externas. Su función principal es **filtrar el
tráfico de red** según reglas predefinidas, permitiendo o bloqueando
comunicaciones para proteger contra accesos no autorizados, ciberataques o
malware.

## Cómo Funciona

- **Filtra paquetes de datos**: Analiza el origen (IP), destino, puertos y tipo
  de tráfico (e.g.,, HTTP, FTP).

- **Bloquea conexiones peligrosas**: Puede denegar acceso a direcciones IP
  maliciosas, puertos abiertos innecesarios o protocolos inseguros.

- **Reglas personalizadas**: Permite definir qué servicios o aplicaciones pueden
  comunicarse (e.g., permitir solo Zoom, pero bloquear Torrent).

- **Filtrado de puertos**: Permite bloquear o permitir ciertos números de
  puertos para restringir comunicación no deseada.

## Tipos de Firewall

Existen 4 tipos de firewalls:

1. **Firewall de software**: Programa instalado en un dispositivo (e.g., Windows
   Defender Firewall, firewalls en antivirus).

   Protege **individualmente** ese equipo, filtrando tráfico entrante/saliente.
   - Ejemplo: Bloquear que un juego acceda a Internet si se sospecha que envía
     datos privados.

2. **Firewall de hardware**: Dispositivo físico (como un router avanzado) que
   protege **toda una red**.

   Se ubica entre el módem y los dispositivos locales, filtrando tráfico antes
   de que llegue a ellos.
   - Ejemplo: Impedir que hackers externos escaneen puertos de tu red doméstica.

3. **Cloud-based firewall**: Software firewalls que están hosteados por un
   provedor de servicios de nube.
   - **Stateful**: Una clase de firewall que mantiene seguimiento de la
     información que pasa a través de él y proactivamente filtra amenazas.

     Analiza características o comportamientos que parecen sospechosos y los
     bloquea de la red.

   - **Stateless**: Una clase de firewall que opera en base a las reglas
     predefinidas y no mantiene seguimiento de la información de los paquetes.

4. **NGFWs (Next Generation firewall)**:
   - Inspección stateful de tráfico entrante y saliente

   - **Inspección de paquetes profundo**: Un tipo de _packet sniffing_ que
     examina datos de paquetes y toma acciones si una amenaza existe.

   - **Protección de intrusos**: Detectan las amenazas de seguridad y notifica a
     los administradores de firewall

   - Inteligencia de amenazas

   - Algunos NGFWs tienen funciones adicionales tales como:
     - Malware Sandboxing
     - Network Anti-Virus
     - URL Filtering
     - DNS Filtering

## Por Qué Usar un Firewall

- **Seguridad básica**: Evita intrusiones desde Internet (e.g., ataques DDoS,
  ransomware).

- **Control de acceso**: Restringe qué servicios se conectan (útil en empresas o
  redes públicas).

- **Privacidad**: Limita el envío no autorizado de datos desde tus dispositivos.

- **Cumplimiento legal**: En entornos profesionales, suele ser un requisito
  (e.g., normativas de protección de datos).

## Referencias

- Google (s.f.). _Firewalls and network security measures_. Connect and Protect:
  Networks and Network Security.
  <https://www.coursera.org/learn/networks-and-network-security/lecture/TrOAQ/firewalls-and-network-security-measures>
