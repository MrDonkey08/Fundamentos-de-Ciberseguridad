# TCSEC: Niveles y Clases de Seguridad

El **Trusted Computer System Evaluation Criteria (TCSEC)**, conocido como
_Orange Book_, es el estándar del Departamento de Defensa de los Estados Unidos
para evaluar la seguridad de sistemas informáticos. El documento tuvo borradores
públicos en 1982 y la versión oficial se publicó en 1983; fue la guía principal
del llamado _Rainbow Series_ y más tarde fue reemplazado por estándares
internacionales como Common Criteria.

TCSEC define cuatro clases jerárquicas principales —D, C, B y A—, donde cada
clase incluye y refuerza los requisitos de la anterior. Las subdivisiones más
comunes son:

- **D** - protección mínima.
- **C1/C2** - protección discrecional.
- **B1/B2/B3** - protección obligatoria.
- **A1** - protección verificada.

Además del control funcional, TCSEC hace hincapié en requisitos de
**aseguramiento** (e.g., pruebas, especificación y verificación, gestión de
configuración) y en la protección continua del Trusted Computing Base (TCB).

## Nivel D: Protección Mínima

Incluye sistemas evaluados que no alcanzan los requisitos mínimos para las
clases C o superiores. Son sistemas con controles de seguridad insuficientes o
inexistentes. (e.g., sistemas como MS-DOS o Macintosh System 7).

### Características Típicas

- Protección mínima o nula del sistema operativo y hardware.
- Autenticación débil o inexistente; separación de usuarios pobre o ausente.
- No se garantiza la confidencialidad ni la integridad frente a accesos no
  autorizados.

## Nivel C: Protección Discrecional

### Clase C1: Protección de Seguridad Discrecional

Introducción a la identificación y autenticación de usuarios y a controles
básicos de acceso discrecional para proteger la confidencialidad de los datos de
cada usuario. Se reconoce explícitamente la figura del administrador del sistema
con privilegios ampliados.

#### Requisitos de Clase C1

- Identificación y autenticación de usuarios.
- Separación de usuarios y datos (perfiles/propietarios de objeto).
- Control de acceso discrecional (DAC) que permita restringir accesos a nivel de
  usuario/objeto.
- Documentación de usuario y manuales operativos.

### Clase C2: Protección de Acceso Controlado

Extiende C1 con controles más granulares y gestión de cuentas orientada a la
operación práctica (gestión de inicios de sesión, políticas de contraseñas,
etc.). Introduce capacidades de auditoría y gestión más estricta de objetos
reutilizables.

#### Requisitos de Clase C2

- DAC más detallado (control de acceso a nivel de objeto/operación).
- Gestión de cuentas y procedimientos de inicio de sesión.
- Registros de auditoría protegidos.
- Medidas para la reutilización segura de objetos (e.g., limpieza de
  almacenamiento).
- Aislamiento de recursos y controles administrativos.

## Nivel B: Protección Obligatoria

En esta familia se introduce la seguridad multinivel mediante **etiquetado**
(labels) y **MAC**: cada sujeto y cada objeto tiene una etiqueta de seguridad y
las decisiones de acceso se basan en reglas del sistema, no en la discreción del
propietario. Además, se exige mayor **aseguramiento** (pruebas, análisis de
canales encubiertos, gestión de configuración).

### Clase B1: Protección de Seguridad Etiquetada

Soporta seguridad multinivel mediante la asignación de etiquetas a objetos y
sujetos (e.g., niveles como _Top Secret_, _Secret_, _Confidential_ y categorías
temáticas como _contabilidad_). El dueño del objeto ya no puede eludir las
restricciones que impone el MAC.

#### Requisitos de Clase B1

- Declaración informal del modelo de política de seguridad.
- Implementación de control de acceso obligatorio (MAC) sobre sujetos/objetos
  seleccionados.
- Etiquetado y capacidades de exportación etiquetada (label export).
- Requisitos de verificación y pruebas más estrictos.

### Clase B2: Protección Estructurada

Refuerza B1 con un modelo de política más formal y aplicación de MAC y DAC a un
conjunto más amplio de objetos. Se presta atención a la separación de funciones,
gestión de la configuración y análisis de canales encubiertos (covert channels).

#### Requisitos de Clase B2

- Modelo de política de seguridad claramente definido y formalizado.
- Aplicación extendida de MAC y DAC a sujetos y objetos.
- Trusted path (canal confiable) para la autenticación de usuarios cuando
  procede.
- Análisis y mitigación de canales encubiertos; control de recursos y
  limitaciones (e.g., ancho de banda).
- Separación de roles (operador vs administrador ) y gestión de configuración
  rigurosa.

### Clase B3: Dominios de Seguridad

Introduce restricciones arquitectónicas significativas: la parte del sistema
responsable de la política de seguridad (TCB) debe ser lo suficientemente
pequeña y examinable para permitir verificación y pruebas exhaustivas. Se exige
que el sistema cumpla los requisitos del _reference monitor_ y que existan
procedimientos fiables de recuperación.

#### Requisitos de Clase B3

- Satisface las tres propiedades del reference monitor (completitud de
  mediación, imparcialidad y verificabilidad).
- Estructura que excluye código no esencial del TCB (principio de mínima
  superficie de confianza).
- Ingeniería de sistemas para minimizar la complejidad.
- Auditoría y registro de eventos relevantes para la seguridad.
- Procedimientos confiables de recuperación y ruta confiable al TCB para
  autenticación.
- Mayor análisis de canales encubiertos y sincronización.

## Nivel A: Protección Verificada

### Clase A1: Diseño Verificado

A1 exige, además de los requisitos funcionales de B3, el uso de
**especificaciones y técnicas formales** para el diseño y la verificación de la
seguridad del sistema. El objetivo es proporcionar un alto grado de
aseguramiento mediante verificación matemática donde sea posible.

#### Requisitos de Clase A1

- Funcionalmente equivalente a B3 en capacidades de protección.
- Especificación formal de alto nivel y técnicas de verificación formales para
  el diseño.
- Procedimientos formales de gestión del desarrollo y distribución (gestión del
  ciclo de vida, control de cambios, distribución segura).
- Pruebas y verificación que demuestren que la TCB cumple la especificación
  formal.

## Referencias

- Wikipedia (agosto 27, 2025). _Trusted Computer System Evaluation Criteria_.
  <https://en.wikipedia.org/wiki/Trusted_Computer_System_Evaluation_Criteria>

- Soto J., (s.f.). _Medidas de Protección Lógica_. Seguridad en la Información.
  <https://drive.google.com/file/d/14zmzxgYho2DMvGNSW0nQN6We-PuLATDZ/view>
