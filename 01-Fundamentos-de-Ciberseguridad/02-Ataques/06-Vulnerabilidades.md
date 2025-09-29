# Vulnerabilidades

Una **vulnerabilidad** es una debilidad que puede ser explotada por una amenaza.
Por lo tanto, las organizaciones deben inspeccionar regularmente las
vulnerabilidades de sus sistemas, clasificarlas y aplicar medidas de mitigación
adecuadas.

## Vulnerabilidades de hardware

### Vulnerabilidades de gestión de hardware y dispositivos físicos

- **Hardware desactualizado**: El hardware antiguo puede ser propenso a fallos
  de seguridad y dejar de recibir soporte de parches.

- **Equipos sin aseguramiento físico (e.g., candados, gabinetes, cableado de
  seguridad)**: Aumentan el riesgo de robo físico de dispositivos y la
  exposición de datos sensibles.

- **Equipos dejados encendidos**: Si el equipo se encuentra vulnerado, puede
  permitir a un atacante acceder al equipo remotamente o desplegar ataques.

- **Equipos dejados desbloqueados**: Permiten a un atacante acceder directamente
  a sistemas sin autenticación.

- **Equipos sin autenticación habilitada**: Dispositivos que no requieren PIN,
  contraseña, datos biométricos, etc. facilitan accesos no autorizados.

### Vulnerabilidades de arquitectura de hardware

- **Meltdown**: Permite a un atacante leer memoria privilegiada de procesos o
  del kernel en CPUs modernas.

- **Spectre**: Explotación de la ejecución especulativa en CPUs que permite
  filtrar datos de otros procesos.

## Vulnerabilidades de software

### Manejo de software

- **Contraseñas débiles**: Contraseñas comunes, cortas, con patrones simples o
  asociadas a datos personales tal como nombre de usuario, correo electrónico,
  nombre de la empresa, nombre del servicio (e.g., Netflix), datos propios del
  dispositivo (e.g., modelo, dirección MAC, marca).

- **Sistemas sin parchear**: Sistemas que todavía tienen soporte oficial, pero
  no se les aplican actualizaciones de seguridad.

- **Protocolos inseguros**: Protocolos que no garantizan la triada **CIA**
  (e.g., Telnet, HTTP, FTP).

- **Configuraciones débiles o por defecto**: Ajustes predefinidos fácilmente
  conocidos por documentación oficial o externa (e.g., contraseñas por defecto)
  y configuraciones débiles (e.g., contraseñas débiles, firewall desactivado,
  ausencia de filtrado de MAC, accesos no revocados).

- **Sistemas legacy**: Sistemas que ya no tienen soporte del fabricante, es
  decir, ya no reciben actualizaciones de seguridad.

- **Instalación de software no autorizado**: Aplicaciones no aprobadas que
  introducen riesgos de seguridad.

- **Problemas del control de accesos**: El **control de accesos** es el proceso
  de controlar a **qué puede** acceder un usuario, **cuándo puede hacerlo** y
  **qué puede hacer** con un recurso en base al rol que posee. Estos recursos
  pueden ser físicos (e.g., una computadora, un lugar) o lógicos (e.g., un
  archivo).

  Controles mal definidos permiten a usuarios realizar acciones fuera de su rol
  autorizado.

### Vulnerabilidades generales de software

- **Buffer overflow**: Los **buffers** son áreas de memorias asignadas a una
  aplicación. El **buffer overflow** sucede cuando los datos son escritos más
  allá de los límites de un buffer. Esto puede provocar que la aplicación pueda
  acceder a memoria asignada a otros procesos. Esto puede causar fallo del
  sistema, corrupción de datos, o proveer escalado de privilegios.

- **Input no validado**: Cuando un _input_ (entrada) no es validado, un atacante
  puede ingresar datos maliciosos, los cuales provocan que el programa tenga
  resultados o comportamiento inesperados.

  El _input no validado_ puede causar vulnerabilidades en sistemas y
  aplicaciones que resultan en _buffer overflow_ o _ataques inyección de
  código_.

- **Condiciones de carrera**: En el paralelismo o la concurrencia, una
  **condición de carrera** ocurre cuando dos o más procesos o hilos, que tienen
  una relación de dependencia, no están sincronizados correctamente o no se
  comunican adecuadamente (es decir, no existe un mecanismo de interacción
  adecuado). Esto puede generar resultados incorrectos o comportamientos
  inesperados. Algunos ejemplos típicos son:
  - **Acceso concurrente a recursos compartidos**: Dos procesos acceden
    simultáneamente a un mismo recurso (e.g., una variable en memoria) sin
    control adecuado, y al menos uno de ellos realiza una escritura. Esto puede
    provocar corrupción de datos.

  - **Dependencias de orden no controladas**: Dos o más tareas con una
    dependencia lógica (e.g., que una deba completarse antes que otra) no están
    coordinadas correctamente, lo que puede causar que se ejecuten fuera de
    orden.

- **Input no validado**: Cuando una _input_ no es validado, un atacante puede
  ingresar datos maliciosos que pueden provocar que el programa tenga resultados
  impredecibles o que se comporte diferente a lo intencionado (puede derivar en
  inyecciones SQL, XSS).

- **Manejo inadecuado de errores**: Mensajes de error detallados pueden filtrar
  información sensible como rutas de archivos, datos de base de datos (e.g.,
  nombre o campos de tablas), credenciales, etc.

- **Debilidades en prácticas de seguridad**: Los sistemas y los datos sensibles
  pueden ser protegidos mediante técnicas tales como la autenticación, la
  autorización y el cifrado. Los desarrolladores deberían adherirse al uso de
  estas técnicas y librerías que ya han sido creadas, testeadas y verificadas, y
  no deberían intentar crear sus propios algoritmos de seguridad.

<!-- - "Fake/legitimate address (e.g., email or website)" -->

### Explotación de vulnerabilidades de software (ataques)

- **Directory Traversal**: Consiste en la explotación de vulnerabilidades que
  permiten acceder a recursos de un servidor fuera del directorio previsto
  (e.g., a través de una aplicación o sitio web).

  Un atacante puede obtener acceso no autorizado a archivos de configuración
  (e.g., `/etc/passwd`), activos críticos y datos sensibles.

- **Remote Code Execution (RCE)**: Permite a un cibercriminal aprovechar las
  vulnerabilidades de una aplicación para ejecutar cualquier comando con los
  privilegios del usuario que ejecuta la aplicación en el dispositivo objetivo.

  El **escalado de privilegios** explota un bug, error de diseño, o una
  configuración incorrecta en un SO o aplicación para ganar acceso a los
  recursos que normalmente están restringidos.

- **API insegura**: Una **API (Application Programming Interface)** entrega una
  respuesta usuario a un sistema y el sistema envía una respuesta devuelta al
  usuario. Un **API attack** sucede cuando un cibercriminal abusa de un API
  endpoint inseguro (e.g., falta de rate limiting, autorización deficiente).

- **API attack**: **API (Application Programming Interface** expone endpoints
  que reciben peticiones y devuelven respuestas; un **API attack** consiste en
  abusar de endpoints inseguros (e.g., broken auth, lack of rate limiting,
  excessive data exposure).

- **Replay attack**: Situación en la que una transmisión de datos válida es
  repetida o retrasada de forma maliciosa o fraudulenta por un atacante, el cual
  intercepta, modifica y vuelve a enviar los datos para que el destinatario haga
  lo que él quiere.

- **Resource exhaustion attacks**: Consisten en agotar los recursos de hardware
  (e.g., CPU, RAM) de una máquina objetivo (e.g., un servidor), provocando que
  el sistema falle o se congele.

#### Inyección de código

- **Cross-Site Scripting (XSS)**: Inyección de scripts maliciosos en
  aplicaciones web. Puede robar sesiones, modificar contenido o robar datos.
  - _Almacenado (persistente)_: Se guarda en el servidor y afecta a múltiples
    usuarios.
  - _Reflejado (no persistente)_: Devuelto inmediatamente en la respuesta de la
    aplicación.
  - _Basado en DOM_: Manipula directamente el DOM del navegador.

  Algunas estrategias de prevención son: validación de inputs, codificación de
  output, e implementación de cabeceras de Content Security Policy para mitigar
  el riesgo de vulnerabilidades XSS.

- **Cross-site request forgery (CSRF)**: Describe el exploit malicioso de un
  sitio web donde comandos sin autorización son subidos al navegador del usuario
  a un aplicación web de confianza.

  Un sitio web malicioso puede transmitir dichos comandos a través de etiquetas
  de imágenes creadas, formularios ocultos o peticiones de JS, los cuales pueden
  funcionar sin el conocimiento del usuario.

- **XML Injection**: Este tipo de ataque puede corromper los datos de una base
  de datos XML y amenazar a la seguridad del sitio web.

  Funciona al interferir con el procesamiento, por parte de una aplicación, de
  los datos o consultas ingresadas por un usuario.

  Los cibercriminales pueden manipular la consulta al programarla para servir
  sus necesidades. Esto les proporcionará acceso a toda la información sensible
  almacenada en la base de datos y les permite hacer cualquier número de cambios
  al sitio web.

- **SQL Injection**: Consiste en la inyección de código SQL en consultas mal
  construidas o sin parametrizar. Un atacante puede código SQL malicioso dentro
  de la base de datos de una aplicación, potencialmente obteniendo acceso a la
  información o alterándolo los datos (i.e., CRUD).

- **DLL Injection**: Un archivo DLL es una librería que contiene un conjunto de
  código y datos para llevar a cabo una actividad en Windows. Las aplicaciones
  usan este tipo de archivo para agregar funcionalidad que no viene integrada,
  cuando requieren llevar acabo dicha actividad.

  La **inyección DLL** permite a los cibercriminales engañar a una aplicación
  para que llame a un archivo DLL malicioso, el cual se ejecuta como parte del
  proceso del objetivo.

- **LDAP Injection**: El **Lightweight Directory Access Protocol (LDAP)** es un
  protocolo abierto para la autenticación de accesos de usuarios a los servicios
  de directorio.

  Una **inyección LDAP** explota vulnerabilidades de input al inyectar y
  ejecutar consultas de servidores LDAP, dándole a los cibercriminales una
  oportunidad de extraer información sensible de un directorio LDAP de una
  organización.

### Vulnerabilidades críticas en software

- **ProxyLogon**: Una vulnerabilidad pre-autenticada que afecta al servidor
  Microsoft Exchange. Permite a un actor de amenazas autenticarse sin
  credenciales válidas para desplegar código malicioso desde una ubicación
  remota.

- **Zerologon**: Una vulnerabilidad crítica en el protocolo de autenticación
  Netlogon de Microsoft que permite a atacantes remotos obtener privilegios de
  administrador de dominio sin credenciales válidas.

- **Log4Shell**: Vulnerabilidad de ejecución remota de código en la librería
  Apache Log4j que permite a atacantes ejecutar código Java arbitrario en
  sistemas remotos.

- **PetitPotam**: Vulnerabilidad que explota el protocolo MS-EFSRPC para forzar
  autenticación NTLM desde controladores de dominio Windows, permitiendo ataques
  de relay NTLM.

- **Server-Side Request Forgery (SSRF)**: Permite a los atacantes manipular una
  aplicación del lado del servidor para realizar peticiones HTTP a recursos
  internos no autorizados.

## Referencias

- NetAcad (s.f.). _2.3. Security Vulnerability and Exploits_. Introduction to
  Cybersecurity.
  <https://www.netacad.com/launch?id=dc0847b7-d6fc-4597-bc31-38ddd6b07a2f&tab=curriculum&view=4e4a6ba2-9262-5cb3-b6b0-d0c70814ace9>

- NetAcad (s.f.). _2.5 Application Attacks_. Network Support and Security.
  <https://www.netacad.com/launch?id=fa6ac75d-3afd-4bde-93f5-f164d8253ab6&tab=curriculum&view=2051f234-b3da-559c-8f85-051a18461925>

- ACI Learning, Wes B., & Deal L. (febrero, 2024). _Threats, Vulnerabilities and
  Exploits_. Security Fundamentals.
  <https://subscription.packtpub.com/video/security/9781835463376/p1/video1_3/threats-vulnerabilities-and-exploits>

- Roadmap (s.f.). _Cyber Security Expert_. <https://roadmap.sh/cyber-security>

- Google (s.f.). _Manage common threats, risks, and vulnerabilities_. Play It
  Safe: Manage Security Risks.
  <https://www.coursera.org/learn/manage-security-risks/supplement/xBXUk/manage-common-threats-risks-and-vulnerabilities>
