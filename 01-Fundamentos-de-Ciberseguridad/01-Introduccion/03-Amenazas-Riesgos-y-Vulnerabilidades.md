# Amenazas, Riesgos, y Vulnerabilidades

## Amenazas

Una **amenaza** es cualquier circunstancia o evento que puede impactar
negativamente a los activos.

### Tipos de amenazas

- Malware
- Ataques
  - Ataques de red
  - Ataques físicos
  - Ataques de ingeniería social
    - Phishing
  - Ataques de contraseñas
  - Explotación de vulnerabilidades zero-day

### Actores de amenaza

Un **threat actor**, o **actor de amenaza** es cualquier persona o grupo de
personas que presenta un riesgo de seguridad. Un actor de amenaza comprende
tanto **actores maliciosos (atacantes)** como **actores no maliciosos** (o no
mal intencionados). Este riesgo puede relacionarse con computadoras,
aplicaciones, redes y datos.

#### Amenazas internas

Las **amenazas internas** son usualmente realizadas por empleados y
ex-empleados, socios de confianza y personal contratado al accidental o
intencionalmente:

- Manejar inapropiadamente datos confidenciales

- Facilitar ataques externos al conectar una memoria USB infectada en la
  computadora del sistema de la organización

- Introducir malware en la red de la organización al hacer clic en emails o
  sitios web maliciosos

- Amenazar las operaciones de servidores internos o dispositivos de la
  infraestructura de red

Las **amenazas internas** pueden abusar de su acceso autorizado para obtener
datos que pueden dañar a una organización. Sus intenciones pueden incluir:

- Sabotaje
- Corrupción
- Espionaje
- Acceso de datos no autorizado
- Filtración de datos

#### Amenazas externas

Las **amenazas externas** pueden ser realizadas por atacantes principiantes o
expertos fuera de la organización al:

- Explotar vulnerabilidades en la red
- Ganar acceso no autorizado a dispositivos de cómputo
- Usar ingeniería social para ganar acceso no autorizado a datos de la
  organización

#### APT

Los **advanced persistent threats (APTs)** o **amenazas persistentes avanzadas**
tienen una gran experiencia en acceder a la red de la organización sin
autorización. Las APT tienden a investigar a sus objetivos (e.g., grandes
empresas o entidades gubernamentales) con antelación y pueden permanecer
indetectados por un período extenso de tiempo. Sus motivaciones pueden incluir:

- Dañar la infraestructura crítica, tal como plantas de energía y recursos
  naturales
- Ganar acceso a propiedad intelectual, tal como secretos de negocios o patentes

## Riesgos

Un **riesgo** es la probabilidad de que una amenaza explote una vulnerabilidad y
cause daño a un activo. Se calcula como:

$$
\text{Riesgo} = \text{Amenaza} \times \text{Vulnerabilidad} \times
\text{Impacto}
$$

**Riesgo = Amenaza × Vulnerabilidad × Impacto**.

### Gestión de riesgos

- **Identificar** los riesgos dentro de un sistema

- **Evaluar** la probabilidad y la severidad (o nivel de impacto) de cada uno de
  los riesgos. La evaluación de riesgos se puede llevar a cabo mediante una
  matriz de probabilidad/severidad

- **Prioritizar** los riesgos, determinar cuáles riesgos atender primero o
  darles mayor importancia

- **Controlar** los riesgos, tomar acciones para disminuir la probabilidad y la
  severidad de los riesgos

> [!TIP]
>
> Se recomienda seguir el **Risk Management Framework**, el cual es un estándar
> en ciberseguridad que establece cómo llevar a cabo una gestión de riesgos de
> manera eficaz.

## Vulnerabilidades

Una **vulnerabilidad** es una debilidad que puede ser explotada por una amenaza.
Por lo tanto, las organizaciones deben inspeccionar regularmente las
vulnerabilidades de sus sistemas.

### Tipos de vulnerabilidades

- **Contraseñas débiles**: Contraseñas comunes, cortas, patrones o secuencias
  numéricas o alfabéticas; contraseñas asociadas con datos personales (PII),
  datos de la cuenta (e.g., nombre de usuario o correo), de la empresa (e.g.,
  nombre de la empresa), del servicio (e.g., Netflix), del dispositivo (e.g.,
  router)

- **Sistemas sin parchear**: Sistemas que siguen teniendo soporte, pero no se
  les aplican parches de seguridad

- **Hardware desactualizado**: El hardware viejo puede ser propenso a
  vulnerabilidades de hardware y/o puede ya no tener soporte para parches de
  seguridad

- **Protocolos inseguros**: Protocolos que no garantizan la triada CID (e.g.,
  Telnet, HTTP, FTP)

- **Configuraciones débiles o por defecto**: Fáciles de descubrir por
  documentación oficial o externa. También incluye **contraseñas por defecto**

- **Sistemas legacy**: Sistemas que ya no tienen soporte del fabricante, es
  decir, ya no reciben parches de seguridad

## Referencias

- Google (s.f.). _Threats, risks, and vulnerabilities_. Play It Safe: Manage
  Security Risks.
  <https://www.coursera.org/learn/manage-security-risks/lecture/QsFVe/threats-risks-and-vulnerabilities>

- NetAcad (s.f.). _1.4 Cyber Attackers_. _Introduction to Cybersecurity_.
  <https://www.netacad.com/launch?id=dc0847b7-d6fc-4597-bc31-38ddd6b07a2f&tab=curriculum&view=4e8a0baa-d5b9-5f43-b61c-869857aa5571>

- Google (s.f.). _Manage common threats, risks, and vulnerabilities_. Play It
  Safe: Manage Security Risks.
  <https://www.coursera.org/learn/manage-security-risks/supplement/xBXUk/manage-common-threats-risks-and-vulnerabilities>
