# Fundamentos de Ciberseguridad

La **ciberseguridad** es el conjunto de reglas, planes y acciones que permiten
asegurar la **confidencialidad**, **integridad** y **disponibilidad** de la
información al proteger redes, dispositivos y personas frente a accesos no
autorizados o explotaciones maliciosas.

## Datos

### Datos personales

- La **personally identifiable information (PII)** o **información personalmente
  identificable** es cualquier tipo de información usada para inferir la
  identidad de un usuario. Algunos ejemplos son:
  - Nombre completo
  - Fecha de nacimiento
  - Dirección física
  - Número telefónico
  - Dirección de correo electrónico
  - Dirección IP

- La **sensitive personally identifiable information (SPII)** o **información
  sensible personalmente identificable** es un tipo específico PII que está
  sujeto a directrices de gestión más estrictas. Algunos ejemplos son:
  - Números de seguro social (NSS)
  - Información médica
  - Información médica financiera
  - Datos biométricos

### Datos organizativos

#### Datos tradicionales

Los datos tradicionales son generados y mantenidos comúnmente por todas las
organizaciones, pequeñas y grandes. Incluyen lo siguiente:

- Los **datos transaccionales**, tal como los detalles relacionados a
  compraventa, actividades de producción y operaciones organizativas, tal como
  cualquier información usada para hacer decisiones de empleo.

- La **propiedad intelectual** tal como patentes, marcas registradas y nuevos
  planes de productos, los cuales ayudan a una organización ganar ventaja
  económica respecto a su competencia. Esta información es a menudo considerada
  un secreto comercial y perderlo puede causar daños desastrosos al futuro de la
  empresa.

- Los **datos financieros** cuentas de ingresos, estados financieros (balances),
  y estados de flujo efectivo que permiten conocer la salud de una empresa.

#### Datos de Internet de las cosas (IoT) y big data

IoT es una red de objetos físicos (sensores, cámaras, actuadores, etc.)
conectados a Internet que generan grandes volúmenes de datos. El crecimiento del
almacenamiento en la nube y la virtualización ha favorecido el surgimiento de
Big Data, lo que plantea nuevos retos de seguridad y privacidad.

## El cubo de la ciberseguridad (McCumber)

El cubo de McCumber es un framework de modelo creado por John McCumber en 1991
para ayudar a las organizaciones a establecer y evaluar iniciativas de la
seguridad de la información al considerar todos los factores que los afectan.
Este modelo de seguridad tiene tres dimensiones:

1. **Principios de seguridad**
2. **Estados de la datos**
3. **Protección de los datos**

#### Principios de seguridad

La primera dimensión del cubo de la ciberseguridad identifica los objetivos para
proteger el ciberespacio. Los principios de **confidencialidad, integridad y
disponibilidad** de datos (la **triada CID**) proveen un enfoque el cuál permite
al experto en ciberseguridad priorizar acciones cuando se protege a un sistema:

- **Confidencialidad**: Conjunto de reglas que garantizan que la información
  sensible sea revelada solo a personas, recursos, y procesos autorizados.
  Algunos métodos para asegurar la _confidencialidad_ son:
  - Encriptación de los datos (e.g., AES para almacenamiento o transmisión)
  - Comprobación de la identidad mediante controles de acceso (lógicos y
    físicos).
  - Autenticación multifactor (MFA), o autenticación de dos factores (2FA)".
  - Least Privilage Access (LPA), o Principio del Mínimo Acceso

- **Integridad**: Asegura que los datos de un sistema no sean modificados de
  manera accidental o intencional (e.g., por personas no autorizadas). También
  implica que cualquier modificación legítima sea rastreable. Algunos métodos
  para asegurar la _integridad_ son:
  - Funciones hash criptográficas (e.g., SHA-256)
  - Firmas digitales
  - Checksums
  - Control de versiones (e.g., Git)

- **Disponibilidad**: Se refiere a que los usuarios autorizados sean capaces de
  acceder a los sistemas y los datos cuando y donde sean necesarios. Se busca
  minimizar interrupciones por fallos técnicos, ataques (e.g., DDoS), errores
  humanos, o desastres. Algunos métodos para asegurar la _integridad_ son:
  - Redundancia y tolerancia al fallo
  - Respaldos de los datos y sistemas de información (e.g., bases de datos)
  - Actualización del software y los sistemas operativos, especialmente de los
    parches de seguridad
  - Mantenimiento de equipos
  - Planes de recuperación ante desastres

#### Estados de los datos

El dominio del ciberespacio contiene una cantidad considerable de datos
importantes críticos. La segunda dimensión del cubo de la ciberseguridad
representa los tres estados posibles de los datos:

- **En procesamiento**: Datos siendo utilizados para realizar operaciones, tal
  como actualizar una base de datos.

- **En almacenamiento o reposo**: Datos guardados almacenamiento persistente
  (e.g., HDD, SSD), tal como bases de datos.

- **En transmisión o tránsito**: Datos que viajan entre sistemas de información,
  tal como datos viajando en redes.

Como profesionales de ciberseguridad debemos garantizar la seguridad de datos en
cada uno de sus estados.

#### Protección de los datos

La tercera dimensión del cubo de ciberseguridad define los pilares en los que
necesitaremos basar nuestras defensas de ciberseguridad para proteger los datos
y la infraestructura en el campo digital.

- **Concienciación, entrenamiento y educación**: Medidas establecidas por una
  organización para asegurar que todos los usuarios tengan conocimiento acerca
  de las amenazas de seguridad potenciales y las acciones que pueden tomar para
  proteger los sistemas de información. Por ejemplo:
  - Programas de entrenamiento
  - Simulacros de phishing
  - Campañas de concienciación

- La **tecnología** se refiere a las soluciones de software y hardware diseñadas
  para proteger los sistemas de información. Por ejemplo:
  - Firewalls
  - Sistemas de detección/prevención de intrusos (IDS/IPS)
  - Encriptación
  - Soluciones EDR
  - SIEM
  - Herramientas de gestión de parches.

- La **política y las prácticas** se refieren a los controles administrativos,
  que proveen unas bases del cómo la organización implementará. Por ejemplo:
  - Controles administrativos
  - Políticas de acceso
  - Clasificación de datos
  - Procedimientos de respuesta a incidentes.

### Activos y gestión de riesgos

Un **activo** es cualquier elemento valioso para la organización (datos,
sistemas, hardware).

Un **riesgo** es cualquier evento que pueda afectar la _confidencialidad_,
_integridad_, o _disponibilidad_ de un _activo_.

#### Clasificación de activos

Los activos se pueden clasificar según su _nivel de riesgo_:

- **Activo de bajo riesgo**: Información que no dañaría la reputación, las
  operaciones en ejecución, y las finanzas de la organización si es
  comprometida.

- **Activo de medio riesgo**: Información que no está disponible al público y
  puede causar daños a la reputación, las operaciones en ejecución y las
  finanzas de la organización si es comprometida.

- **Activo de alto riesgo**: Información protegida por regulaciones y leyes, la
  cuál si es comprometida, tendría impactos negativos severos a la reputación,
  las operaciones en ejecución y las finanzas de la organización si es
  comprometida.

## Incidentes de seguridad

Un **incidente de seguridad** es un evento que explota una vulnerabilidad en
sistemas o procesos.

### Brechas de datos

Una **brecha de datos** es cualquier incidente de seguridad en el que partes no
autorizadas acceden a información sensible o confidencial, incluidos datos
personales y datos organizativos.

#### Consecuencias de una brecha de datos

- **Daño a la reputación**: Una brecha de seguridad puede tener impactos
  negativos a largo plazo en la reputación de la organización que ha tardado
  años en forjarse.

  Los clientes, especialmente aquellos que hayan sido perjudicados por la
  brecha, tendrán que ser notificados y pueden buscar una compensación y/o
  dirigirse a un competidor confiable y seguro. Los empleados también pueden
  optar por marcharse ante un escándalo.

  Dependiendo de la severidad de la brecha, puede tomar mucho tiempo reparar la
  reputación de la organización.

- **Vandalismo** Un hacker o un grupo de hackers puede vandalizar el sitio web
  de una organización, publicando información falsa. Estos hackers incluso
  podrían editar detalles de tu organización, tales como direcciones o números
  de teléfono, lo cuál puede llegar a ser difícil de detectar.

- **Robo**: Una brecha de datos involucra incidentes donde los datos personales
  sensibles han sido robados. Los cibercriminales pueden hacer uso de esta
  información, haciéndola pública o explotándola para robar el dinero o la
  identidad de un individuo.

- **Pérdida de ingresos**: Los impactos financieros de una brecha de seguridad
  pueden ser devastadores. Por ejemplo, los hackers pueden tumbar el sitio web
  de una organización, impidiéndole hacer negocios en línea. La pérdida de
  información de los clientes puede impedir el crecimiento y la expansión de la
  empresa. Puede exigir nuevas inversiones en la infraestructura de seguridad de
  una organización. Y no olvidemos que las organizaciones pueden enfrentarse a
  costosas multas o sanciones si no protegen los datos en línea.

- **Daño a la propiedad intelectual**: Una brecha de seguridad puede tener
  impactos devastadores en la competitividad de una organización, especialmente
  si los hackers llegan a tener acceso a la información confidencial, secretos
  comerciales y propiedad intelectual.

## Referencias

- <https://www.netacad.com/launch?id=4ab42845-d7db-4c94-b8f1-5b5d2fdcb79b&tab=curriculum&view=91d46f8f-195f-50b1-8aeb-01f35676c080>

- <https://www.coursera.org/learn/manage-security-risks/lecture/QsFVe/threats-risks-and-vulnerabilities>

- <https://www.coursera.org/learn/foundations-of-cybersecurity/lecture/wxo04/secure-design>
