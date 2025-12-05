# Tácticas de Ataque y Defensa

## Malicious packet sniffing

**Packet Sniffing** es la práctica de usar herramientas de software para
observar datos que viajan a través de una red.

Existen dos tipos de _malicious packet sniffing_:

- **Passive packet sniffing**: Tipo de ataque donde los paquetes de datos son
  leídos en tránsito, es decir, el atacante lee el contenido del paquete.

- **Active packet sniffing**: Tipo de ataque donde los paquetes de datos son
  manipulados en tránsito, es decir, el atacante modifica la información del
  paquete. Esto puedo incluir inyectado de protocolos de internet para
  redireccionar los paquetes a puertos no intencionados o cambiando la
  información que el paquete contiene.

## IP spoofing

**IP spoofing** es un ataque de red realizado cuando un atacante cambia la
dirección IP fuente de un paquete de datos para hacerse pasar por un sistema
autorizado y ganar acceso a una red.

Alguno ataques comunes de _IP spoofing_ son:

- **On-path attack**: Ataque donde un actor malicioso se posiciona en la mitad
  de una conexión autorizada e intercepta o altera los datos en tránsito.

- **Replay attack**: Ataque de red realizado cuando un actor malicioso
  intercepta un paquete de datos en tránsito y lo retrasa o lo repite en otro
  momento.

- **Smurf attack**: Ataque de red realizado cuando un atacante _sniffs_ una
  dirección IP de un usuario autorizado y lo inunda con paquetes.

### Cómo proteger una red de IP spoofing

- Implementar encriptación durante las comunicaciones, (e.g., TLS/SSL)

- Configurar firewalls en contra de _IP spoofing_.

  Si un firewall recibe un paquete de datos proveniente del internet dónde el
  dirección IP del emisor es la misma que la de la red privada, entonces el
  firewall deniega la transmisión, debido a que los dispositivos deberían estar
  ya en la red local.

## Referencias

- Google (s.f.). _Malicious packet sniffing_. Connect and Protect: Networks and
  Network Security.
  <https://www.coursera.org/learn/networks-and-network-security/lecture/At91i/malicious-packet-sniffing>

- Google (s.f.). _IP Spoofing_. Connect and Protect: Networks and Network
  Security.
  <https://www.coursera.org/learn/networks-and-network-security/lecture/9hspL/ip-spoofing>
