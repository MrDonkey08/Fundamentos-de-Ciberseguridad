# Credenciales

Las **credenciales** son los datos que un usuario proporciona para autenticarse
ante un sistema y, respectivamente, iniciar sesión. Por lo general, los sistemas
utilizan contraseñas como método de autenticación; además, comúnmente solicitan
un dato adicional para identificar al usuario dentro del sistema (e.g., correo,
nombre de usuario, teléfono).

Aunque las credenciales proporcionan confidencialidad dentro de un sistema, si
estas llegan a ser vulneradas (i.e., un atacante consigue las credenciales),
puede obtener acceso no autorizado al sistema y comprometer la
**confidencialidad, integridad y disponibilidad (CIA)** de los datos y
servicios.

## Ataques de contraseñas

- **Password spraying**: Consiste en probar una misma contraseña común (e.g.,
  `123456`, `password`, `contraseña`, `admin`) contra múltiples cuentas de
  usuario. Esta técnica es efectiva cuando muchos usuarios usan contraseñas
  débiles y permite al atacante evitar bloqueos por intentos fallidos masivos
  sobre una sola cuenta.

- **Ataque de diccionario**: Se utiliza un diccionario de contraseñas conocidas
  (frecuentes en filtraciones) para probar cada una de ellas.

- **Ataque de arcoíris**: Las contraseñas no suelen guardarse en texto plano,
  sino como hashes. A diferencia del diccionario, este ataque utiliza
  [tablas de hashes precalculados (rainbow tables)](https://es.wikipedia.org/wiki/Tabla_arco%C3%ADris).
  Cuando se encuentra el hash correcto, el atacante identifica la contraseña
  usada. Actualmente se mitiga con técnicas como el uso de **sal (salt)** y
  algoritmos de hashing lentos (e.g.,
  [bcrypt](https://en.wikipedia.org/wiki/Bcrypt),
  [Argon2](https://en.wikipedia.org/wiki/Argon2)).

- **Fuerza bruta**: Consiste en probar cada combinación posible dentro de un
  conjunto de caracteres (e.g., dígitos, letras, símbolos) hasta encontrar la
  contraseña correcta.

- **Phishing**: El atacante engaña al usuario para que revele sus credenciales
  directamente, a través de páginas falsas, correos electrónicos o mensajes
  fraudulentos.

- **Credential stuffing**: Uso de credenciales filtradas en otros servicios,
  aprovechando la reutilización de contraseñas por parte de los usuarios.

- **Intercepción de tráfico**: Mediante ataques MitM (Man-in-the-Middle) se
  intercepta el tráfico de red. Mientras el contenido del paquete se encuentre
  en texto plano (e.g., HTTP, Telnet), es decir, sin cifrar (a diferencia de
  HTTPS o SSH, se pueden leer datos de los paquetes, como las credenciales del
  usuario cuando inicia sesión.

## Credenciales vulnerables

### Contraseñas vulnerables

Existen muchas contraseñas vulnerables porque son contraseñas por defecto de
algún dispositivo o sistema, son muy comunes, se componen de datos personales,
han sido expuestas en brechas de seguridad o han sido vulneradas por algún
ataque de contraseña.

#### Contraseñas por defecto

- [A1 Security Cameras - Usuarios, contraseñas y direcciones IP por defecto en cámaras de seguridad](https://www.a1securitycameras.com/blog/default-username-passwords-ip-addresses-for-surveillance-cameras/)
- [IPVM - Directorios de contraseñas de cámaras IP](https://ipvm.com/reports/ip-cameras-default-passwords-directory)
- [Router Passwords - Contraseñas de routers y dispositivos de red](https://www.routerpasswords.com/)
- [SecLists - Credenciales por defecto](https://github.com/danielmiessler/SecLists/tree/master/Passwords/Default-Credentials)

### Cuentas vulnerables por brechas de seguridad

Las cuentas pueden verse comprometidas por brechas de seguridad; por ello es
recomendable, cuando sea posible, cambiar todos los datos expuestos (e.g.,
contraseñas, tarjetas de crédito/débito) y revisar alertas oficiales del
servicio afectado.

> [!TIP]
>
> Para disminuir la cantidad de datos que pueden exponerse en una brecha,
> elimina la información innecesaria de la cuenta (e.g., direcciones, tarjetas,
> números de teléfono) o elimina la cuenta si ya no la usas.
>
> Si es necesario, solicita a soporte técnico la eliminación permanente de tu
> cuenta, ya que muchos servicios solo ofrecen desactivación en lugar de
> borrado.

#### Herramientas para revisar si una cuenta ha sido comprometida

- [Have I Been Pwned](https://haveibeenpwned.com/)
- [Have I Been Pwned - Passwords](https://haveibeenpwned.com/Passwords)
- [Mozilla Monitor](https://monitor.mozilla.org/user/dashboard)
- [Malwarebytes - Huella digital](https://www.malwarebytes.com/digital-footprint)
- [Cybernews - Chequeo de brechas de datos personales](https://cybernews.com/personal-data-leak-check/)
- [LeakCheck](https://leakcheck.io/)

> [!IMPORTANT]
>
> Estas herramientas consultan brechas públicas; solo pueden indicar si tus
> datos aparecen en esas fuentes, no garantizan que una cuenta sea segura.
> Revisa avisos oficiales de los servicios y actúa (rotación de credenciales,
> MFA) si hay indicios de compromiso.

### Herramientas relacionadas con credenciales

Se distinguen dos grandes grupos: herramientas de cracking/recuperación de
contraseñas usadas en auditorías y herramientas OSINT para reconocimiento.

#### Cracking de contraseñas (uso legítimo en auditoría)

- **[Hashcat](https://hashcat.net/hashcat/)** - herramienta avanzada para
  descifrar hashes
- **[John the Ripper](https://www.openwall.com/john/)** - ampliamente utilizado
  en auditorías
- **[Hydra](https://github.com/vanhauser-thc/thc-hydra)** - permite ataques de
  fuerza bruta y diccionario contra varios protocolos

#### OSINT y generación de listas

- **[Cupp](https://github.com/Mebus/cupp)** - genera listas de contraseñas
  basadas en datos personales
- **[Sherlock](https://github.com/sherlock-project/sherlock)** - busca cuentas
  de redes sociales asociadas a un nombre de usuario
- **[Holehe](https://github.com/megadose/holehe)** - detecta presencia de un
  e-mail en numerosos servicios

## Lineamientos para la creación de contraseñas

Aquí se muestran lineamientos para crear contraseñas seguras. Se recomienda usar
generadores de contraseñas para obtener valores aleatorios y gestores para
almacenarlas.

- Usar contraseñas de al menos **12 caracteres** (recomendado mínimo: 15).
  Muchos servicios permiten hasta **64 caracteres**; evita límites artificiales
  cuando sea posible.

- Crear contraseñas complejas. Incluir una mezcla de:
  - Mayúsculas (A-Z)
  - Minúsculas (a-z)
  - Números (0-9)
  - Símbolos especiales (`!@#$%^&*()_-+=[]{};:'",.<>/?`)
  - Espacios (si el servicio lo permite)
  - Caracteres adicionales (si está permitido)

  > [!TIP]
  >
  > También es recomendable utilizar **Passphrase** fáciles de recordar, pero
  > largas y seguras (e.g., `Perro-Verde!Canta2025`). Adicionalmente, puedes
  > utilizar herramientas tales como:
  >
  > - [Keeper Passphrase Generator](https://www.keepersecurity.com/features/passphrase-generator/)
  > - [Use a passphrase](https://www.useapassphrase.com/)
  >
  > Para evaluar y garantizar la seguridad de tus contraseñas puedes usar:
  >
  > - [Timcutting - Entropía de contraseñas](https://timcutting.co.uk/tools/password-entropy)
  > - [Bitwarden - Fuerza de la contraseña](https://bitwarden.com/password-strength/)
  > - [Security.org - Fuerza de la contraseña](https://www.security.org/how-secure-is-my-password/)
  > - [Spectre - Generador de contraseñas replicable](https://spectre.app/)
  > - [Nordpass - Generador de contraseñas](https://nordpass.com/password-generator/)
  > - [Bitwarden - Generador de contraseñas](https://bitwarden.com/password-generator/)

- Evitar contraseñas fáciles de adivinar, por ejemplo:
  - Repeticiones o patrones comunes (e.g., `123456`, `000000`, `1234abcd`,
    `qwerty`)
  - Palabras de diccionarios de cualquier idioma
  - Nombres propios
  - Contraseñas filtradas en bases de datos públicas (e.g.,
    [SecLists - Leaked Databases](https://github.com/danielmiessler/SecLists/tree/master/Passwords/Leaked-Databases))
  - Secuencias de números o letras (e.g., `123456`, `abcdef`)
  - Información asociada a la cuenta (e.g., ID, nombre de usuario, e-mail)
  - Información personal (e.g., nombres, fechas importantes (e.g., de
    nacimiento, aniversarios), números de teléfono)

- Usar técnicas de ofuscación (útiles solo como complemento, no como única
  medida):
  - **Sustituciones inteligentes**:
    - `Smith` → `5m1Th` o `5mYth`
    - `Security` → `S3cur!t¥`

  - **Inserción de caracteres**:
    - Espacios o símbolos al azar: `G@ t0__2025` en lugar de `Gato`

## Gestión de cuentas y contraseñas

- Revisar periódicamente que las cuentas no hayan sido comprometidas (véase la
  sección
  [Cuentas vulnerables por brechas de seguridad](#cuentas-vulnerables-por-brechas-de-seguridad))

- Cambiar contraseñas periódicamente (e.g., cada 3-6 meses) e inmediatamente
  ante una brecha de seguridad o sospecha de compromiso de la contraseña

- No utilizar la misma contraseña (o patrones similares) en distintos servicios

- No reutilizar contraseñas viejas que puedan haber sido comprometidas

- No escribir contraseñas en físico o en archivos de texto plano. Si debes
  guardarlas, hazlo de forma cifrada:
  - Archivos cifrados (e.g., [VeraCrypt](https://veracrypt.io/en/Home.html),
    [GnuPG](https://gnupg.org/))

  - Gestores de contraseñas (e.g., [KeePass](https://keepass.info/),
    [Bitwarden](https://bitwarden.com/), [NordPass](https://nordpass.com/),
    [Proton Pass](https://proton.me/es-419/pass))

  > [!TIP]
  >
  > Si prefieres gestores locales (e.g., KeePass) reduces la dependencia de un
  > servicio en la nube; los gestores en la nube (e.g., Bitwarden) ofrecen
  > sincronización y facilidad de uso, sin embargo, son susceptibles a brechas
  > de seguridad, aumentando la posibilidad de que los atacantes puedan
  > conseguir acceso a tus contraseñas. Véase
  > [Keepass vs la nube](https://www.youtube.com/watch?v=uMDHPK-xyAA)

- Usar 2FA/MFA siempre que sea posible:
  - Aplicaciones de autenticación TOTP ([Aegis](https://aegisauth.com/),
    [Ente Auth](https://ente.io/auth/),
    [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=es_MX&pli=1)) -
    opción recomendada

  - Correos electrónicos para verificación - menos seguro que TOTP/security key

  - SMS/llamadas - **última opción** por riesgo de interceptación/port-out

  - Llaves de seguridad (e.g.,
    [YubiKey](https://www.yubico.com/la-yubikey/?lang=es)) - actualmente la
    opción más segura para MFA. Véase
    [Security keys for 2FA](https://www.youtube.com/watch?v=8Y77o23q_tg&pp=ygUVdGVjaG9yZSBoYXJkd2FyZSBrZXlz2AaLAg%3D%3D)

  > [!TIP]
  >
  > Personalmente no recomiendo apps de autenticación como Authy, Microsoft
  > Authenticator, o Google Authenticator. Véase
  > [Cómo usar TOTP para máxima seguridad](https://www.youtube.com/watch?v=iXSyxm9jmmo&t=394s)

- No compartir contraseñas por correo, chat o cualquier medio inseguro. Para
  utiliza herramientas seguras de compartición (e.g.,
  [One-Time Secret](https://onetimesecret.com/),
  [Vanish](https://www.vanish.so/), [Cryptgeon](https://cryptgeon.org/)).

  > [!NOTE]
  >
  > Existen gestores de contraseñas que tienen la opción de compartir
  > contraseñas, tal como NordPass y LastPass

- Cerrar sesión en dispositivos públicos y ajenos

  > [!TIP]
  >
  > Recomiendo utilizar el **modo incógnito** para evitar guardar historial,
  > sesiones abiertas, y cookies en el navegador. El **modo incógnito** no te
  > hace 100% anónimo, debido a que en el dispositivo guarda en el **DNS caché**
  > las páginas que accediste y el **proveedor de servicios de Internet (ISP)**
  > guarda logs acerca de las páginas que accediste; para ello recomiendo borrar
  > periódicamente el **DNS caché** (i.e., flush DNS), utilizar **DNS** privados
  > (véase
  > [Privacy Tools - Encrypted DNS](https://www.privacytools.io/encrypted-dns)),
  > y utilizar VPNs privados y seguros
  > [Privacy Tools - Best VPN for Privacy & Security](https://www.privacytools.io/privacy-vpn)

- Verificar URLs y certificados (e.g., comprobar HTTPS y certificado válido)
  antes de introducir credenciales

## Recursos recomendados

- [OWASP - Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
- [NIST SP 800-63B - Digital Identity Guidelines](https://pages.nist.gov/800-63-3/sp800-63b.html)
- [Techlore - Software, hardware and applications](https://techlore.tech/resources/#all-resources)
- [AlternativeTo](https://alternativeto.net/)
- [PrivacyTools](https://www.privacytools.io/)
- [Password Storage Tier List: encryption, hashing, salting, bcrypt, and beyond](https://youtu.be/qgpsIBLvrGY?si=MCw3l9rnIfFu3vid)

## Referencias

- Netacad (s.f.). _2.2 Methods of Infiltration_.
  <https://www.netacad.com/launch?id=dc0847b7-d6fc-4597-bc31-38ddd6b07a2f&tab=curriculum&view=dbdc2979-f15d-5751-ad0e-8a87ec6a4c5a>

- NetAcad (s.f.). _3.1 Protecting Your Devices and Network_.
  <https://www.netacad.com/launch?id=dc0847b7-d6fc-4597-bc31-38ddd6b07a2f&tab=curriculum&view=200e9011-e513-5d25-8d3b-e3d870bd3f5d>

- NIST (s.f.). _Digital Identity Guidelines_. <https://pages.nist.gov/800-63-3/>

- Proton (Octubre 05, 2023) _What is a password entropy?_
  <https://proton.me/blog/what-is-password-entropy>

- bk2204 (Nov 28, 2021). _How many bits of entropy should a password have to be
  reasonably future proof (10 years)?_
  <https://security.stackexchange.com/questions/257519/how-many-bits-of-entropy-should-a-password-have-to-be-reasonably-future-proof-1>

- Atoponce (2023). _Password length recommendations_.
  <https://www.reddit.com/user/atoponce/comments/186u5li/password_length_recommendations/>

- Techlore (s.f.). _Privacy & Security Resources_.
  <https://techlore.tech/resources/>
