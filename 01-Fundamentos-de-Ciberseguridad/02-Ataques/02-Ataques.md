# Ataques

Un **ataque** es un intento intencionado de aprovechar alguna vulnerabilidad de
un sistema con el fin de conseguir un bien o servicio o dañar de alguna manera
al negocio o empresa detrás del sistema.

## Tipos de ataques

### Ataques de red

- **DoS**: Los ataques de **denegación de servicios** o **denial of service
  (DoS)** son un tipo de ataque de red que son relativamente simples de llevar a
  cabo, incluso para un atacante inexperto. Estos ataques son un gran riesgo ya
  que usualmente resultan en algún tipo de retraso o interrupción de servicios,
  causando daño significativo en pérdida de tiempo y dinero.

  Incluso tecnologías operacionales, los cuales consisten en hardware o software
  que controlan los dispositivos físicos o procesos en edificios, fábricas, o
  proveedores de utilidades, son vulnerables a los ataques DoS, que pueden
  causar que los sistemas se apaguen en extremas circunstancias.
  - **Cantidad abrumadora de tráfico**: Cuando en red, host o aplicación le es
    enviado una enorme cantidad de tráfico de datos a un ritmo que no puede
    manejar. Este puede causar ralentización en la transmisión o respuesta, o
    causa que el dispositivo o servicio crashee.

  - **Paquetes maliciosos malformados**: Un paquete es una colección de datos
    que fluyen desde un host fuente hacia un destino a través de una red. Cuando
    un paquete formateado maliciosamente es enviado, el receptor no será capaz
    de manejarlo. Esto puede causar que el host destino se ralentice o crashee.

- **DDoS**: Un ataque **Distributed DoS (DDoS)** o **DoS Distribuido** es un
  ataque que se origina por múltiples fuentes coordinadas. Por ejemplo:
  - Un atacante crea una red (botnet) de hosts infectados llamados zombies, los
    cuales son controlados por sistemas gestor.

  - Las computadoras zombies constantemente escanearán e infectarán más host,
    creando más y más zombies.

  - Cuando el hacker esté listo, le indicará al sistema gestor que haga que el
    botnet de zombies lleve a acabo un ataque DDoS.

- **Botnet**: Una computadora bot es típicamente infectado por visitar un sitio
  web inseguro o abrir archivos adjuntos de correo o archivos de media
  infectados. Un **botnet** es un grupo de bots conectadas a través de Internet
  que pueden ser controlados por un individuo o grupo malicioso, típicamente a
  través de un servidor de comandos y control.

  Estos bots pueden ser activados para distribuir malware, lanzar ataques DDoS,
  distribuir correos de spam, o ejecutar ataques de fuerza bruta.

- DNS
  - **DNS reputation**:

  - **DNS spoofing**: El **DNS spoofing** o **DNS cache poisoning** es un ataque
    en el cual datos falsos son introducidos en la caché de un DNS resolver, la
    base de datos que un SO que graba registros recientes de sitios webs
    visitados y otros tipos de dominios de internet.

    Estos ataques pueden explotar una debilidad en el software de cacheado DNS
    que causa que los servidores DNS redirijan el tráfico de un dominio legítimo
    a la dirección IP de un servicio ilícito.

  - **Domain hijacking**: El **domain hijacking** o **secuestro de dominio** es
    cuando un atacante gana indebidamente el control de la información DNS del
    objetivo y hace cambios no autorizados.

    El tipo de domain hijacking más común es cambiar el correo de contacto del
    administrador a través de ingeniería social o al hackear la cuenta de email
    del administrador. El correo del administrador puede ser fácilmente
    encontrado a través del registro WHOIS del dominio, el cuál es un registro
    público

  - **Uniform resource locator (URL) redirection**: Una **URL redirection** o
    **redirección URL** es cuando una URL te redirige a otra. Esto comúnmente
    paso por propósitos legítimos. Sin embargo, esto puede ser explotado por
    atacantes, redirigiéndote a sitios web maliciosos.

- **MitM**: Un ataque **man-in-the-middle (MitM)** o ataque **on-path** sucede
  cuando un cibercriminal toma control de un dispositivo intermediario sin el
  conocimiento del usuario. Con este tipo de acceso, un atacante puede
  interceptar, manipular, y transmitir información falsa entre la fuente y el
  destino.
  - **MitMo**: Un ataque **man-in-the-mobile (MitMo)** es una variación de un
    ataque MitM. MitMo es usado para tomar control del dispositivo móvil de un
    usuario. Cuando un dispositivo es infectado, se le indica al dispositivo
    exfiltrar datos sensibles del usuario y enviarlos al atacante.

## Ataques de la capa 2

La **capa 2** se refiere a la **capa de enlace de datos** del **modelo OSI**.

Esta capa es usada para mover datos a través de dispositivos enlazados en la
red. Las direcciones IP son mapeadas a una dirección física del dispositivo
(MAC), usando un proceso llamado address resolution protocol (ARP) o protocolo
de resolución de direcciones.

### Spoofing

El **spoofing** o **poisoning**, es un tipo de ataque de suplantación de
identidad que toma ventaja de la relación de confianza entre dos sistemas.

- **MAC address spoofing**: Sucede cuando un atacante disfraza su dispositivo
  como uno válido en una red, esto para pasar el proceso de autenticación. Esto
  se logra al cambiar la dirección MAC del host del atacante por uno autorizado.

- **ARP spoofing**: Ocurre cuando un atacante envía un mensaje ARP spoofed a
  través de una LAN. Esto enlaza la dirección MAC del atacante con la dirección
  IP de un dispositivo autorizado.

- **IP spoofing**: Es cuando se envía paquetes IP de una dirección falsa para
  ocultar el origen del paquete.

### MAC flooding

Los dispositivos de una red son conectados a través de un switch de red al usar
packet switching para recibir y compartir datos hacia el dispositivo destino. El
**MAC flooding** es cuando un atacante inunda la red con direcciones MAC falsas,
comprometiendo la seguridad de la red switch.

### Ataques de contraseñas

Los **ataques de contraseñas** consisten en intentar conseguir acceso a
dispositivos, sistemas, redes o datos protegidos con contraseñas. Algunos tipos
de ataques de contraseñas son:

- **Password spraying**: Consiste en adivinar la contraseña al introducir
  contraseñas comunes o posibles haciendo uso de la información personal. Esta
  técnica permite al atacante permanecer sin ser detectado siempre y cuando
  evite bloqueos de cuentas frecuentes.

- **Ataque de diccionario**: Se utiliza un diccionario de contraseñas para
  intentar con cada una de estas contraseñas.

- **Ataque de arcoiris**: Las contraseñas de un sistema no se suelen guardar en
  texto plano, sino se guardan como hash. Al diferencia del diccionario, este no
  utiliza un diccionario de contraseñas, sino uno de hash de contraseñas
  precalculados. Cuando se obtiene el hash correcto, el atacante identifica la
  contraseña usada para crear dicho hash.

- **Fuerza bruta**: Se va probando con cada una de las combinaciones posibles de
  contraseñas dentro de un conjunto de caracteres (e.g., dígitos, caracteres,
  símbolos) hasta que se obtiene la correcta.

- **Interception de tráfico**: Mediante ataques MitM se intercepta el tráfico de
  red, mientras el contenido del paquete se encuentre en texto plano (e.g.
  HTTP), es decir, sin cifrar (como lo haría HTTPS), se pueden leer las
  credenciales del usuario.

### Ataques físicos

- **Cables maliciosos:** Cables que han sido modificados internamente para
  incluir componentes electrónicos maliciosos (e.g., chips, transmisores) que
  pueden interceptar datos, inyectar malware o comprometer dispositivos al ser
  conectados.

- **Memoria USB maliciosa:** Dispositivos de almacenamiento USB que contienen
  malware o están programados para ejecutar automáticamente scripts maliciosos
  al ser conectados a una computadora. Pueden utilizarse para infectar sistemas,
  robar información sensible o establecer acceso remoto no autorizado.

- **Clonación de tarjetas:** Conjunto de técnicas y ataques que emplean
  dispositivos especializados para copiar la información almacenada en tarjetas
  magnéticas o con chip (e.g., tarjetas de crédito, tarjetas de acceso,
  identificaciones corporativas). El objetivo es crear duplicados funcionales
  para acceso no autorizado.
  - **Skimmer:** Dispositivo físico o electrónico diseñado para capturar
    fraudulentamente la información de tarjetas de crédito o débito. Se instalan
    de manera encubierta en lectores legítimos como cajeros automáticos,
    terminales punto de venta (POS) o lectores de tarjetas de acceso,
    permitiendo el robo de datos de la banda magnética o chip.

- **Clonación de llaves:** Técnicas utilizadas para duplicar llaves físicas sin
  autorización, incluyendo métodos como el robo temporal para crear copias,
  fotografía de llaves para reproducción posterior, o uso de herramientas de
  impresión para generar duplicados basándose en patrones visuales.

### Ataques criptográficos

Un **ataque criptográfico** afecta a las formas comunicación seguras entre un
emisor y un receptor. Algunos tipos de ataques criptográficos son:

- Birthday
- Collision
- Downgrade

### Más tipos de ataques

- **SEO poisoning**: El **search engine optimización (SEO)** o optimización del
  motor de búsqueda es, en simples términos, la aplicación de técnicas y
  estrategias para para mejorar el sitio web de la organización con el objetivo
  de que gane mayor visibilidad en los resultados del motor de búsqueda.

  El **SEO poisoning** es cuando un atacante toman ventaja de términos de
  búsqueda populares para implementar SEO y empujar sus sitios web maliciosos
  para mejorar su ranking en la búsqueda de resultados.

- **Zero-day**: Un **zero-day** es cuando existe vulnerabilidad de un software
  desconocido por el proveedor de software.

  Un **zero-day-exploit** es el método o código que permite aprovecharse de
  dicha vulnerabilidad.

  Un **ataque zero-day** sucede cuando un atacante explota la vulnerabilidad
  antes de que sean conocidas y parcheadas por el distribuidor del software.

- **Inteligencia artificial adversaria**: Técnica que manipula la inteligencia
  artificial y la tecnología de aprendizaje automático para realizar ataques de
  forma más eficaz.

- **Ataque a la cadena de suministros**: Usa herramientas o servicios de
  terceros, referidos como cadenas de suministros, para infiltrarse en el
  sistema o red del objetivo.

## Complejidad de ataques

- **Ataques de algoritmo**: Toman ventaja de algoritmos de una pieza de una
  pieza de software legítimo para generar comportamientos no intencionados.

- **APT**: Un **advanced persistent threat** es un ataque continuo que utiliza
  tácticas de espionaje elaboradas, involucrando a multiples actores y/o
  software malicioso para ganar acceso a la red del objetivo.

  Los ataques permanecen indetectables por largos períodos de tiempo, con
  consecuencias potencialmente devastadoras.

## Referencias

- Google (s.f.). _Common attacks and their effectiveness_.
  <https://www.coursera.org/learn/foundations-of-cybersecurity/supplement/2ys9Q/common-attacks-and-their-effectiveness>

- Cloudflare (s.f.). _What is a supply chain attack?_.
  <https://www.cloudflare.com/learning/security/what-is-a-supply-chain-attack/>

- Google (s.f.). _Determine the type of attack_.
  <https://www.coursera.org/learn/foundations-of-cybersecurity/supplement/I1z8u/determine-the-type-of-attack>

- NetAcad (s.f.). _2.3 Cyber Attacks_.
  <https://www.netacad.com/launch?id=fa6ac75d-3afd-4bde-93f5-f164d8253ab6&tab=curriculum&view=4eca255b-a49b-5fd5-8fef-314f9ae1baf8>
