# Wi-Fi

## Métodos de autenticación Wi-Fi

- **Open system authentication**:
  - No requiere una contraseña
  - Cualquier dispositivo puede conectarse.
  - Usado comúnmente para proveer acceso a interne gratuito en áreas públicas
  - La responsabilidad de seguridad recae en el cliente

  > [!CAUTION]
  >
  > Utilizar redes con este tipo de autenticación es inseguro debido a que los
  > atacantes pueden conectarse a la red y pueden ser capaces de leer y
  > modificar los datos que pasan a través de la red

- **Shared-Key autenticación**: Provee mecanismos tales como WEP, WPA, WPA2 y
  WPA3 para la autenticación y la encriptación de los datos entre clientes
  inalámbricos y AP.

### Métodos de autenticación shared-key

- **Wired Equivalent Privacy (WEP)**: La especificación original diseñada para
  asegurar los datos usando el método de encriptación Rivest Cipher 4 (RC4) con
  una llave estática. Sin embargo, las llaves nunca cambian cuando se
  intercambian paquetes. Esto lo hase más fácil de hackear. WEP ya no es
  recomendados y no debería de usarse.

- **Wi-Fi Protected Access (WPA)**: Una estándar de la Wi-Fi Alliance que
  utiliza WEP, pero protege los datos con el algoritmo de encriptación Temporal
  Key Integrity Protocol (TKIP). TKIP cambia la llave para cada paquete,
  haciéndolo más difícil de hacker.

- **WPA2**: El estándar actual en la industria. Utiliza el Advanced Encryption
  Standard Protocol (AES) para la encriptación. AES es considerado el protocolo
  más fuerte de encriptación.

- **WPA3**: Esta es la siguente generación de seguridad de Wi-Fi. Todos los
  dispositivos habilitados con WPA3 usan los métodos de seguridad más recientes,
  deshabilitando protocolos legacy. Requiere el uso de Protected Management
  Frames (PFM). Sin embargo, dispositivos con WPA3 todavía no están disponibles.

## Wireless and mobile devices attacks

- Grayware
- SMiShing
- SIM swapping - Mozilla

- Rogue access point
- Radio frequency jamming
- Bluejacking
- Bluesnarfing
- Bluebugging

## Wireless threats

- **Intercepción de datos**: Los datos inalámbricos deberían ser encriptados
  para prevenir que sean leídos por interceptores

- **Intrusos inalámbricos**: Usuarios no autorizados intentando acceder a
  recursos que intentan acceder a recursos a los recursos de la red pueden ser
  prevenidos por medio de técnicas de autenticación

- **Ataques de Denegación de Servicios (DoS)**: El acceso a los servicios de
  WLAN pueden ser comprometidos ya sea accidental o maliciosamente. Varias
  soluciones dependen en función del origen del ataque DoS

- **Rogue APs**: Los APs instalados sin autorización por un usuario con buenas
  intenciones, o malas intenciones, puede ser detectado usando software de
  gestión de redes.

### Ataques DoS

Ataques DoS inalámbricos pueden ser resultado de:

- **Dispositivos configurados inapropiadamente**: Error de configuración pueden
  inhabilitar el WLAN. Por ejemplo, un administrador podría accidentalmente
  alterar una configuración y deshabilitar la red, o un intruso con privilegios
  de administrador podría deshabilitar una WLAN

- **Usuario malintencionado interfiere con la comunicación inalámbrica**: Su
  objetivo es deshabilitar la red la red inalámbrica completamente o al punto
  que ningún dispositivo legítimo pueda acceder al medio.

- **Interferencia accidental**: Las WLANs están propensos a interferencias por
  otros de otros dispositivos inalámbricos, incluyendo hornos de microondas,
  teléfonos inalámbricos, monitores para bebés, etc.

Para minimizar el riesgo de los ataques DoS debido a dispositivos configurados
inapropiadamente, asegura todos los dispositivos, mantén las contraseñas
seguras, crea respaldos, y asegúrate que todos los cambios son incorporados
fuera del horario laboral.

Monitoriza la WLAN en búsqueda de cualquier problema de interferencia accidental
y soluciónalos en cuanto aparezcan. Debido a que la banda 2.4 GHz es utilizado
por otro tipo de dispositivos, la banda de 5 GHz debería ser usado en áreas
susceptibles a interferencias

### Rogue Access Points

Un **rogue AP** es un AP o router inalámbrico que ha sido conectado a una red
inalámbrica corporativa sin la autorización explicita y en contra de la
política. Cualquier persona con acceso a las premisas puede instalar (maliciosa
o no maliciosamente) un router barato que pueden potencialmente permitir acceso
a un recurso de red seguro.

Una vez conectado, el rogue AP puede ser utilizado por un atacante para capturar
direcciones MAC, capturar paquetes de datos, ganar acceso a los recursos de red
o lanzar ataques Man-in-the-Middle.

Un red hotspot personal también podría ser usado como un rogue AP. Por ejemplo,
un usuario con acceso a una conexión segura habilita se equipo como un Wi-Fi AP.
Al hacerlo, se evitan las medidas de seguridad y otros dispositivos no
autorizados pueden acceder a los recursos de la red como un dispositivo
compartido.

Para prevenir la instalación de rogue APs, organizaciones deben configurar
controles de WLAN (WLCs) con políticas de rogue AP, y utilizar un software de
monitoreo para activamente monitorizar el espectro de frecuencia de radio en
búsqueda de APs no autorizadas.

### Ataque Man-in-the-Middle

En un ataque man-in-the-middle (MITM), el hacker es posicionado entre dos
entidades legítimas para leer o modificar los datos que pasan entre ambas
partes. Existen varias maneras de crear ataques MITM.

Un ataque MITM inalámbrico popular es llamado el "ataque del gemelo AP", donde
un ataque introduce un rogue AP y lo configura con el mismo SSID como un AP
legítimo. Ubicaciones ofreciendo Wi-Fi gratuito, tal como aeropuertos,
cafeterías, restaurantes, son particularmente lugares populares por este tipo de
ataque debido a la autenticación abierta.

Ataques MITM y sus variaciones son comúnmente referidas como ataques on-path.

Los clientes inalámbricos conectados a un rogue AP envían su tráfico a través
del rogue, el cual captura los datos y los comparte al AP legítimo. Asimismo, el
trafico retornado proveniente del AP legítimo es enviado al Rogue AP, capturado
y después compartido al usuario. El atacante puede robar las contraseñas del
usuario, información personal, ganar acceso al dispositivo, y comprometer el
sistema., capturado y después compartido al usuario. El atacante puede robar las
contraseñas del usuario, información personal, ganar acceso al dispositivo, y
comprometer el sistema.

Derrotar un ataque tal MITM depende en la sofisticación de la infraestructura
WLAN y la vigilancia en el monitoreo de la actividad de la red. El proceso
comienza con identificar dispositivos legítimos en el WLAN. Para esto, los
usuarios deben estar autenticados. Después de que todos los dispositivos
legítimos hayan sido identificados, la red puede ser monitorizada en búsqueda de
dispositivos o tráfico anormal.

## Wi-Fi and mobile devices defense

## Referencias

- Google (s.f.). _Wireless protocols_. Connect and Protect: Networks and Network
  Security.
  <https://www.coursera.org/learn/networks-and-network-security/lecture/bK86y/wireless-protocols>

- Google (s.f.). _The evolution of wireless security protocols_. Connect and
  Protect: Networks and Network Security.
  <https://www.coursera.org/learn/networks-and-network-security/supplement/x73QK/the-evolution-of-wireless-security-protocols>

- Zenarmor (mayo 28, 2023). _Bluetooth in Cyber Security: Understanding
  Bluetooth Attacks_.
  <https://www.zenarmor.com/docs/network-basics/what-is-bluetooth>

- NetAcad (s.f.). _3.6. Secure Wireless Access_. Network Support and Security.
  <https://www.netacad.com/launch?id=fa6ac75d-3afd-4bde-93f5-f164d8253ab6&tab=curriculum&view=a0acbd67-8f34-5df5-95a8-41de75301701>
