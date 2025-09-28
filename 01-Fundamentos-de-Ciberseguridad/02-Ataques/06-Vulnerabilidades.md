# Vulnerabilidades

Una **vulnerabilidad** es una debilidad que puede ser explotada por una amenaza.
Por lo tanto, las organizaciones deben inspeccionar regularmente las
vulnerabilidades de sus sistemas.

## Vulnerabilidades de hardware

- Left-powered
- Outdated-hardware
- Meltdown
- Spectre

## Vulnerabilidades de software

- **Buffer overflow**: Los buffers son áreas de memorias asignadas a una
  aplicación. El **buffer overflow** sucede cuando los datos son escritos más
  allá de los límites de un buffer. Esto puede provocar que la aplicación pueda
  acceder y a la memoria de asignada a otros procesos. Esto puede causar crasheo
  de sistemas, compromiso de datos, o proveer escalado de privilegios.

- **Input no validado**: Cuando una entrada de datos no es validada, un atacante
  puede ingresar datos maliciosos, los cuales provocan que el programa tenga
  resultados impredecibles o que se comporte diferente a lo intencionado

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

- **Debilidades en prácticas de seguridad**: Los sistemas y los datos sensibles
  pueden ser protegidos mediante técnicas tales como la autenticación, la
  autorización y el cifrado. Los desarrolladores deberían adherirse al uso de
  estas técnicas y librerías que ya han sido creadas, testeadas y verificadas, y
  no deberían intentar crear sus propios algoritmos de seguridad.

- **Problemas del control de accesos**: El **control de accesos** es el proceso
  de controlar a qué puede acceder un usuario, cuándo puede hacerlo y qué puede
  hacer con el recurso accedido en base al usuario o al rol que posee. Estos
  recursos pueden ser físicos (e.g., una computadora, un lugar) o lógicos (e.g.,
  un archivo).

---

- Software updates
- Outdated software
- Installing unauthorized software

---

- "Fake/legitimate address (e.g., email or website)"

## Application attacks

- **Cross-Site Scripting (XSS)**: Vulnerabilidad de aplicaciones web en donde
  los atacante inyecta scripts maliciosos dentro del contenido de sitios web
  legítimos. Estos scripts se ejecutan en los navegadores de las víctimas para
  robas datos sensibles, secuestrar sesiones de usuarios, o desfigurar sitios
  webs. Existen 3 tipos de ataques XSS:
  - **Almacenado (persistente)**: Introduce código malicioso en un servidor
  - **Reflejado (no persistente)**: Ocurre cuando la entrada del usuario es
    devuelta inmediatamente por una aplicación web.
  - **Basado en DOM**: Manipula el Document Object Model (DOM) en el navegador.

  Algunas estrategias de prevención son: validación de inputs, codificación de
  output, e implementación de cabeceras de Content Security Policy para mitigar
  el riesgo de vulnerabilidades XSS.

- **Code Injection**:
  - **XML Injection**: Este tipo de ataque puede corromper los datos de una base
    de datos XML y amenazar a la seguridad del sitio web.

    Funciona al interferir con el procesamiento, por parte de una aplicación, de
    los datos o consultas ingresadas por un usuario.

    Los cibercriminales pueden manipular la consulta al programarla para servir
    sus necesidades. Esto les proporcionará acceso a toda la información
    sencible almacenada en la base de datos y les permite hacer cualquier número
    de cambios al sitio web.

  - **SQL Injection**: Ataque que explota vulnerabilidades de Seguridad de SQL.
    Permite a los atacantes inyectar código SQL malicioso dentro de la base de
    datos de una aplicación, potencialmente provocando acceso, modificación o
    eliminación de datos no autorizada.

  - **DLL Injection**: Un archivo DLL es una librería que contiene un conjunto
    de código y datos para llevar a cabo una actividad en Windows. Las
    aplicaciones usan este tipo de archivo para agregar funcionalidad que no
    viene integrada, cuando ocupan llevar acabo dicha actividad.

    La **inyección DLL** permite a los cibercriminales engañar a una aplicación
    para que llame a un archivo DLL malicioso, el cual se ejecuta como parte del
    proceso del objetivo.

  - **LDAP Injection**: El **Lightweight Directory Access Protocol (LDAP)** es
    un protocolo abierto para la autenticación de accesos de usuarios a los
    servicios de directorio.

    Una **inyección LDAP** explota vulnerabilidades de input al inyectar y
    ejecutar consultas de servidores LDAP, dándole a los cibercriminales una
    oportunidad de extraer informacion sensible de un directorio LDAP de una
    organización.

- **Buffer overflow**: Los **buffers** son areas de memorias asignadas a una
  aplicación. Un **buffer overflow** sucede cuando los datos están siendo
  escritos más allá de los límites del buffer. Al modificar datos más allá del
  buffer, la aplicación puede acceder a memoria asignada a otros procesos. Esto
  puede provocar que el sistema se crasheé, que los datos sean comprometidos, o
  inclusive escalado de privilegios.

- **Remote Code Executions**: Permite a un cibercriminal aprovechar las
  vulnerabilidades de una aplicación para ejecutar cualquier comando con los
  privilegios del usuario que ejecuta la aplicación en el dispositivo objetivo.

  El **escalado de privilegios** explota un bug, bandera de diseño, o una
  configuración incorrecta en un SO o aplicación para ganar acceso a los
  recursos que normalmente están restringidos.

- **Cross-site request forgery (CSRF)**: Describe el exploit malicioso de un
  sitio web donde comandos sin autorización son subidos al navegador del usuario
  a un aplicación web de confianza.

  Un sitio web malicioso puede transmitir dichos comandos a través de etiquetas
  de imágenes creadas, formularios ocultos o peticiones de JS, los cuales pueden
  funcionar sin el conocimiento del usuario.

- **Improper input handling attack**: Los datos ingresados por un usuario que no
  son validados apropiadamente puede afectar al flujo de datos de un programa y
  causar vulnerabilidades en sistemas y aplicaciones que resultan en _buffer
  overflow_ o _ataques de SQL injection_.

- **Error handling attack**: Los atacantes pueden usar mensajes de errores para
  extraer información específica tal como los _hostnames_ de sistemas internos y
  directorios o archivos que existen en un servidor web; en una base de datos,
  datos extraídos como nombres de campos pueden ser usados para construir
  _ataques de SQL injection_.

- **Application programming interface (API) attack**: Una API entrega una
  respuesta usuario a un sistema y el sistema envía una respuesta devuelta al
  usuario. Un **API attack** sucede cuando un cibercriminal abusa de un API
  endpoint.

- **Replay attack**: Situación en la que una transmisión de datos válida es
  repetida o retrasada de forma maliciosa o fraudulenta por un atacante, el cual
  intercepta, modifica y vuelve a enviar los datos para que el destinatario haga
  lo que él quiere.

- **Directory traversal attack**: Sucede cuando un atacante es capaz de leer
  archivos de un servidor web fuera del directorio de un sitio web. Un atacante
  puede usar esta información para descargar archivos de configuración del
  servidor que contienen información sensible, potencialmente exponer más
  vulnerabilidades del servidor o inclusive tomar control del servidor.

- **Resource exhaustion attacks**: Estos ataques son exploits de seguridad de
  computadoras que crashean, congelan, o interfieren con un programa o sistema
  específico. En lugar de saturar el ancho de banda tal como un ataque DoS, los
  _resource exhaustion attacks_ saturan los recursos de hardware disponibles en
  el servidor del objetivo.

## Referencias

- NetAcad (s.f.). _2.5 Application Attacks_.
  <https://www.netacad.com/launch?id=fa6ac75d-3afd-4bde-93f5-f164d8253ab6&tab=curriculum&view=2051f234-b3da-559c-8f85-051a18461925>

- Roadmap (s.f.). _Cyber Security Expert_. <https://roadmap.sh/cyber-security>
