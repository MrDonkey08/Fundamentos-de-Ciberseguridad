# Los Dominios de Seguridad CISSP

## 1. Seguridad y gestión de riesgos

El dominio de **seguridad y gestión de riesgos** establece los principios
fundamentales sobre los que se basa toda la seguridad de la información dentro
de una organización. Implica identificar, evaluar y priorizar los riesgos, así
como implementar controles apropiados para mitigarlos.

La **postura de seguridad** de una organización se refiere a su capacidad de
proteger sus activos de información, responder a amenazas, y adaptarse a cambios
en el entorno operativo, legal o tecnológico. Factores clave que influyen en
esta postura incluyen:

- **Metas y objetivos de seguridad**: Establecer metas claras permite alinear la
  estrategia de seguridad con los objetivos del negocio y proteger activos
  críticos como la _PII_ (Personally Identifiable Information – Información
  Personal Identificable), _PHI_ (Protected Health Information), _IP_
  (Intellectual Property), etc.

- **Gestión de riesgos**: Incluye la identificación, evaluación, tratamiento,
  monitoreo y comunicación de riesgos. Las organizaciones deben seguir marcos
  como ISO 31000, NIST RMF o COSO ERM para estructurar sus programas de gestión
  de riesgos.

- **Mitigación de riesgos**: Consiste en aplicar controles administrativos,
  técnicos o físicos para reducir la probabilidad o impacto de amenazas. Esto
  incluye respuestas planificadas ante incidentes de seguridad, como brechas de
  datos.

- **Cumplimiento normativo (_compliance_)**: Abarca la adherencia a leyes,
  regulaciones, estándares y políticas internas. Ejemplos incluyen GDPR, HIPAA,
  SOX, PCI-DSS, entre otros. Este cumplimiento es esencial para evitar sanciones
  legales y proteger la reputación.

- **Planes de continuidad del negocio y recuperación ante desastres (BCP/DRP)**:
  Estrategias diseñadas para mantener las operaciones críticas y recuperar
  servicios tras interrupciones. Estos planes deben probarse y actualizarse
  regularmente.

- **Aspectos legales y regulatorios**: Involucra leyes nacionales e
  internacionales relacionadas con la privacidad, la ciberseguridad, la
  propiedad intelectual, la evidencia digital (_digital forensics_) y los
  contratos.

- **Ética profesional y organizacional**: Los profesionales certificados deben
  adherirse al _Código de Ética del (ISC)_, el cual incluye proteger la
  sociedad, actuar con honor, proporcionar servicios competentes, y avanzar la
  profesión.

### Seguridad de la información (_InfoSec_)

La seguridad de la información se refiere a la protección de la
**confidencialidad, integridad y disponibilidad** (la conocida **triada CIA**)
de la información, sin importar la forma que esta adopte.

Las organizaciones deben implementar programas estructurados de seguridad de la
información que incluyan:

- **Planes de concientización y capacitación**: Incluyen entrenamiento continuo
  del personal para reducir errores humanos y mejorar la cultura de seguridad.

- **Playbooks o runbooks**: Guías estructuradas para responder ante incidentes
  específicos, como ataques de phishing, ransomware o pérdida de dispositivos.

- **Procesos clave de InfoSec**:
  - Gestión de incidentes
  - Gestión de vulnerabilidades
  - Seguridad de aplicaciones
  - Seguridad en la nube
  - Seguridad de redes e infraestructura
  - Gestión de accesos e identidades (IAM)
  - Gestión de políticas de seguridad

## 2. Seguridad de los activos

El dominio de la **seguridad de los activos** implica la gestión de los procesos
de ciberseguridad de los activos organizativos, incluido el almacenamiento,
mantenimiento, retención, y destrucción de los datos digitales y físicos.

Realizar un análisis del impacto en la seguridad, establecer un plan de
recuperación, y gestionar la exposición de los datos dependerá del nivel de
riesgo asociado con cada activo.

Los analistas de seguridad pueden necesitar almacenar, mantener y retener datos
al crear respaldos y asegurarse de que sean capaz de restablecer el entorno si
un incidente de seguridad de seguridad compromete la seguridad los datos de la
organización.

## 3. Arquitectura e ingeniería de seguridad

El dominio de **arquitectura e ingeniería de seguridad** se encarga de gestionar
la seguridad de los datos. Asegura la existencia de herramientas sistemas, y
procesos eficaces que ayudan a proteger los activos y datos de la organización.

Un aspecto importante de este dominio es el concepto de responsabilidad
compartida. La **responsabilidad compartida** significa que todos los individuos
involucrados toman un rol activo en reducir el riesgo durante el diseño de un
sistema de seguridad. Principios de diseño relacionados a este dominio incluyen:

- Modelado de amenazas
- Mínimo privilegio
- Defensa en profundidad
- Fallar seguramente
- Separación de funciones
- Simplicidad
- Cero confianza
- Confiar, pero verificar

## 4. Seguridad de las comunicaciones y las redes

El dominio de **seguridad de las comunicaciones y las redes** se enfoca en
gestionar y proteger las redes físicas y las comunicaciones inalámbricas. Esto
incluye comunicaciones on-site, remotas y en la nube.

Las organizaciones con entornos de trabajo remotos, híbridos y on-site deben
asegurarse de que lo datos permanezcan seguros.

Diseñar controles de seguridad (e.g., acceso de red restringido) pueden ayudar a
proteger a usuarios y red de una organización mantenerse segura cuando los
empleados viajan o trabajan fuera de la oficina principal.

## 5. Identificación y gestión de accesos

El dominio de **identificación y gestión de accesos (IAM)** se centra en
mantener los datos seguros. Para ello, se asegura de que los usuarios sigan
políticas establecidas para el control y el manejo de activos físicos y lógicos
tal como la la autenticación (i.e., asegurar la identidad del usuario) y la
accesibilidad (i.e., establecer qué activos puede acceder un usuario)

En esencia, este dominio es referido como el principio del mínimo privilegio, el
cual consiste en proporcionar solo el acceso y autorización mínimamente
requeridos para realizar una tarea.

### Componentes de IAM

- **Identificación**: Proceso mediante el cual una identidad se presenta a un
  sistema. Involucra el uso de identificadores únicos, tales como:
  - Nombres de usuario
  - Número de empleado
  - Tarjeta de acceso

- **Autenticación**: Proceso de verificar que la identidad presentada por un
  sujeto es legítima al proporcionar un elemento adicional. Los métodos de
  autenticación se clasifican de la siguiente manera:
  - Algo que saben (e.g., una contraseña)
  - Algo que poseen (e.g., un token o una tarjeta)
  - Algo que son (e.g., una huella)

- **Autorización**: Los servicios de autorización determinan el nivel de acceso
  de un usuario autenticado, es decir, establecen **qué recursos** puede acceder
  y **qué operaciones** puede realizar en base a las políticas establecidas.

  Algunos sistemas cumplen esto al utilizar una lista de control de acceso, o un
  ACL. Un ACL determina ya sea si un usuario tiene ciertos privilegios una vez
  que se autentica.

  La autorización también puede determinar _cuándo_ un usuario tiene acceso a un
  recurso específico.

- **Responsabilidad y Rendición de Cuentas (Accountability)**: Consiste en el
  seguimiento y registro de las acciones de cada uno de los usuarios, tal como
  intentos de inicio de sesión. Esto permite detectar abusos, fallos de
  seguridad y realizar investigaciones forenses.

## 6. Evaluación y pruebas de seguridad

El dominio de **evaluación y pruebas de seguridad** se centra en identificar y
mitigar los riesgos, amenazas, y vulnerabilidades. La evaluación de seguridad
ayuda a las organizaciones a determinar si sus internos están seguros o en
riego. Las organizaciones pueden contratar _penetration testers_ (probadores de
penetración), comúnmente referidos como _pen testers_, para encontrar
vulnerabilidades que podrían ser explotadas por actores de amenazas.

Este dominio sugiere a las organizaciones hacer pruebas de los controles de
seguridad y recopilar y analizar los datos. Adicionalmente, enfatiza la
importancia de llevar a cabo auditorías de seguridad para monitorizar y reducir
la probabilidad de una brecha de datos. Para contribuir a este tipo de tareas,
los profesionales de ciberseguridad pueden auditar los permisos de usuario para
validar que los usuarios poseen los niveles correctos de acceso a los sistemas
internos.

## 7. Operaciones de seguridad

El dominio de **operaciones de seguridad** consiste en la investigación de una
brecha de datos potencial y de la implementación de las medidas preventivas
después de que un incidente de seguridad ha ocurrido. Esto incluye el uso de
estrategias, procesos y herramientas tales como:

- Entrenamiento y concienciación
- Reportes y documentación
- Detección y prevención de intrusos
- Herramientas SIEM
- Gestión de logs
- Gestión de incidentes
- Playbooks
- Análisis forenses post-breach
- Reflexión acerca de las lecciones aprendidas

Los profesionales de ciberseguridad involucrados en este dominio trabajan como
un equipo para gestionar, prevenir, e investigar amenazas, riesgos y
vulnerabilidades. Estos individuos son capacitados para encargarse de los
ataques activos. Una vez que una amenaza es identificada, el equipo trabaja
cuidadosamente para mantener los datos y la información privada segura de
actores de amenaza.

## 8. Seguridad en el desarrollo de software

El dominio de **seguridad en el desarrollo de software** se enfoca en el uso de
prácticas y guidelines (lineamientos) de programación segura para desarrollar
aplicaciones seguras.

La seguridad debe ser incorporada en cada elemento del ciclo de vida del
desarrollo del software, desde el diseño y el desarrollo hasta las pruebas y el
lanzamiento. Para garantizar la seguridad, el proceso de desarrollo de software
debe tener en cuenta la seguridad en cada paso.

Realizar pruebas de seguridad del software puede ayudar a asegurar que las
vulnerabilidades son identificados y mitigados correctamente. Es necesario
disponer de un sistema para probar las convenciones de programación, los
ejecutables del software y las medidas de seguridad integradas en el software.
Una parte esencial del proceso de desarrollo de software consiste en contar con
profesionales de control de calidad y pen testers para asegurar de que el
software cumpla los estándares de seguridad y rendimientos.

Utiliza prácticas de código seguro, los cuales son un conjunto de lineamientos
recomendados que son usados para crear aplicaciones y servicios seguros.

## Referencias

- <https://www.coursera.org/learn/manage-security-risks/lecture/KgUAD/explore-the-cissp-security-domains-part-1>

- <https://www.coursera.org/learn/manage-security-risks/lecture/mKNXE/explore-the-cissp-security-domains-part-2>

- <https://www.coursera.org/learn/manage-security-risks/supplement/TluHD/security-domains-cybersecurity-analysts-need-to-know>
