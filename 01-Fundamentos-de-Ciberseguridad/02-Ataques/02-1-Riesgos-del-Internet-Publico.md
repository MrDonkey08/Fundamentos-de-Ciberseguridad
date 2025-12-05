# Riesgos del Internet Público

En lugares públicos como universidades, cafeterías y centros comerciales nos
encontramos con **redes públicas**, redes en las cuales podemos acceder a
Internet (coloquialmente conocido como Wi-Fi) gratuitamente. Sin embargo, estas
redes son peligrosas debido a que cualquier usuario dentro de la red y con los
suficientes conocimientos puede realizar un ataque **Man-in-the-Middle** (o, en
su defecto **Man-in-the-Mobile**) e interceptar los datos en tránsito.

## Man in the Middle (MitM) y Man in the Mobile (MitMo)

Un ataque **Man-in-the-Middle (MitM)**, o ataque **on-path**, es un ataque en el
cual un host atacante intercepta una comunicación entre dos puntos (i.e., un
host y un switch/router). Si la comunicación no está cifrada, el atacante puede
leer e inclusive alterar los datos en tránsito.

Por otra parte, un ataque **Man-in-the-Mobile (MitMo)** es una variación de un
ataque MitM. MitMo es usado para tomar control del dispositivo móvil de un
usuario. Cuando un dispositivo es infectado, se le indica al dispositivo filtrar
datos sensibles del usuario y enviarlos al atacante. Este tipo de ataque
comúnmente involucra malware instalado en el dispositivo que puede interceptar
SMS, credenciales y otra información personal.

### Packet Sniffing

A la práctica de usar herramientas de software para observar datos que viajan a
través de una red se le llama **packet sniffing** o **análisis de paquetes**.

Existen dos tipos de packet sniffing malicioso:

- **Passive packet sniffing:** Tipo de ataque donde los paquetes de datos son
  leídos en tránsito, es decir, el atacante lee el contenido del paquete sin
  modificarlo. El atacante permanece invisible en la red monitorizando el
  tráfico.

- **Active packet sniffing:** Tipo de ataque donde los paquetes de datos son
  manipulados en tránsito, es decir, el atacante modifica la información del
  paquete. Esto puede incluir inyección de protocolos de red para redirigir los
  paquetes a puertos no intencionados, o modificación de la información que el
  paquete contiene.

### Spoofing

El **spoofing** o **poisoning** es un tipo de ataque de suplantación de
identidad que toma ventaja de la relación de confianza entre dos sistemas.

Para llevar a cabo un ataque MitM, se utilizan ataques de spoofing tales como:

- **ARP spoofing:** Ocurre cuando un atacante envía un mensaje ARP spoofed a
  través de una LAN. Esto enlaza la dirección MAC del atacante con la dirección
  IP de un dispositivo autorizado. Este ataque se puede aprovechar para
  redirigir los paquetes del host víctima (host envenenado) que van hacia el
  default gateway (router) hacia el host atacante, haciendo posible la lectura y
  alteración de los datos del paquete. Adicionalmente, estos paquetes pueden ser
  redirigidos del host atacante al destino real, en este caso al default
  gateway, manteniendo la comunicación aparentemente normal.

- **IP spoofing:** Es cuando se envían paquetes IP desde una dirección falsa
  para ocultar el verdadero origen del paquete. Esto permite al atacante hacerse
  pasar por un host confiable.

- **DNS spoofing:** El DNS spoofing o **DNS cache poisoning** es un ataque en el
  cual datos falsos son introducidos en la caché de un DNS resolver, la base de
  datos que un sistema operativo mantiene para registrar consultas recientes de
  sitios web visitados y otros tipos de dominios de Internet. Estos ataques
  pueden explotar una debilidad en el software de cache DNS que causa que los
  servidores DNS redirijan el tráfico de un dominio legítimo hacia la dirección
  IP de un servicio malicioso. Este tipo de ataque puede ser combinado con un
  ataque ARP spoofing, para que cuando el usuario ingrese a un sitio web (e.g.,
  <https://facebook.com>) sea redirigido a una página ilegítima (i.e., un clon
  de Facebook), ingrese sus credenciales de inicio de sesión y estas sean
  enviadas al host del atacante.

## Medidas preventivas ante ataques MitM

### VPN

El **VPN (Virtual Private Network)** es un servicio que proporciona una conexión
segura y cifrada entre dos redes, o entre un host determinado y una red.

Cuando estamos conectados a una VPN, los paquetes viajan cifrados desde el
cliente hasta el servidor VPN, por lo que la VPN evita que un atacante MitM
pueda leer o alterar los datos fácilmente. El túnel cifrado actúa como una capa
de protección adicional sobre la red pública.

En redes públicas o en páginas con HTTP, siempre utiliza una VPN para garantizar
una comunicación cifrada de los paquetes.

#### Ventajas de una VPN

- Transmisiones de contenido desde cualquier dispositivo.
- Acceder a páginas bloqueadas.
- Evitar la censura.
- Evitar la discriminación de precios.
- Evitar ser rastreado.

#### Desventajas de una VPN

- Velocidad potencialmente inferior.
- No son posibles las mediciones de QoS.
- Bloqueos de VPN por parte de la empresa.
- La privacidad no siempre es total.

### HTTPS y Certificados SSL/TLS

El protocolo **HTTPS**, a diferencia del **HTTP** provee una comunicación
cifrada entre el cliente y el servidor mediante el uso de certificados SSL/TLS,
dificultando que un atacante _MitM_ pueda leer o alterar los paquetes
interceptados.

Siempre, de ser posible, asegúrate de acceder solo a páginas **HTTPS** en lugar
**HTTP**, especialmente si estás enviando o recibiendo información sensible
(e.g., credenciales, documentos confidenciales). Si la página a la que necesitas
acceder utiliza _HTTP_, entonces utiliza una _VPN_ para asegurar una
comunicación cifrada de los datos.

### 2FA/MFA

El **Two Factor Authentication (2FA)** y el **Multi Factor Authentication
(MFA)** son una capa adicional de autenticación para evitar que personas no
autorizadas (e.g., atacantes) puedan acceder a una cuenta. Esta funciona de tal
manera que te solicita algún código o llave adicional, la cual ha sido enviada
mediante SMS, o correo o, en su defecto, puede ser consultada en tu app de
autenticación (e.g., Google Authenticator).

De ser posible configura todas tus cuentas con _2FA_ o _MFA_, especialmente
cuentas importantes, cuentas que contienen acceso a información confidencial,
posibilidad de realizar transacciones bancarias (e.g., transferencias, compras),
y, en general, cualquier actividad que te pueda perjudicar de alguna manera.

> [!IMPORTANT]
>
> Dentro de lo posible evita utilizar 2FA con SMS, ya que estos son susceptibles
> a ataques. En su lugar utiliza correos o, inclusive mejor, TOTP mediante apps
> de autenticación, o llaves de seguridad.

### Medidas Preventivas Adicionales

**Evitar redes públicas para actividades sensibles:** Limitar el uso de redes
públicas para navegación general, evitando transacciones bancarias o acceso a
información confidencial.

**Mantener software actualizado:** Mantener actualizados el sistema operativo,
navegadores y aplicaciones para protegerse contra vulnerabilidades conocidas.

**Verificación de redes:** Confirmar el nombre correcto de la red Wi-Fi con el
establecimiento antes de conectarse, ya que los atacantes pueden crear redes con
nombres similares (evil twin attacks).

---

**HIDRA**: Plataforma de ciberseguridad (o más bien hackeo) que se creó en los
EE.UU para hackear. Los hackers expusieron _hydra_ y cualquiera puede hacer uso
de él.

## Referencias

- NetAcad (s.f.). _3.1 Protecting Your Devices and Network_. Introduction to
  Cybersecurity.
  <https://www.netacad.com/launch?id=dc0847b7-d6fc-4597-bc31-38ddd6b07a2f&tab=curriculum&view=200e9011-e513-5d25-8d3b-e3d870bd3f5d>

- Google (s.f.). _Determine the type of attack_. Foundations of Cybersecurity.
  <https://www.coursera.org/learn/foundations-of-cybersecurity/supplement/I1z8u/determine-the-type-of-attack>

- Soto J., (s.f.). _Conceptos Generales de Seguridad de la Información_.
  Seguridad en la Información.
  <https://drive.google.com/file/d/15W5bOQ0wCuDyI1i6VgHb9I4BjgUFxp8A/view>
