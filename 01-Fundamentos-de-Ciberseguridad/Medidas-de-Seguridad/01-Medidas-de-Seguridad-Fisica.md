# Medidas de Seguridad Física

## Controles de acceso físico

Los **controles de acceso físico** son barreras físicas y procedimientos
diseñados para prevenir el contacto físico no autorizado con los sistemas. El
objetivo es impedir que personas sin autorización accedan a las instalaciones,
equipos y otros activos de la organización.

Por ejemplo, los _controles de acceso físico_ determinan **quiénes**, **dónde**
y **cuándo** pueden entrar o salir.

Algunos ejemplos de _controles de acceso físico_ son:

- Guardias que vigilan las instalaciones.
- Vallas y cercas perimetrales.
- Detectores de movimiento y sensores de presencia.
- Candados de cable para laptops (cable locks) que reducen el riesgo de robo de
  equipos portátiles.
- Puertas con control de acceso para prevenir entradas no autorizadas.
- Tarjetas de proximidad / RFID / sistemas de control de acceso por tarjeta.
- Perros de seguridad entrenados.
- Cámaras de videovigilancia que capturan y registran imágenes.
- Vestíbulos de seguridad o "mantraps" que escalonan y controlan el flujo de
  personas en zonas sensibles.
- Alarmas de intrusión y sensores (puertas/ventanas/rotura de cristales).

### Sistema de videovigilancia

Los **sistemas de videovigilancia** consisten en una red de cámaras instaladas
en un edificio o recinto. Estas cámaras permiten grabar y, opcionalmente, ser
monitorizadas en tiempo real desde un centro de control (CCTV). El objetivo es
disuadir actos maliciosos y mantener un registro de incidentes para
investigación y evidencia.

No se recomienda que los _sistemas de videovigilancia_ sean monitorizados
únicamente por personas ya que la atención disminuye con el tiempo. En cambio,
se recomienda complementar con **analítica de vídeo** (detección de intrusión,
detección de objetos, conteo de personas, detección de comportamiento anómalo) y
alertas automáticas para reducir la carga humana y mejorar tiempos de respuesta.

> [!IMPORTANT]
>
> En un _sistema de videovigilancia_ debemos de tener en cuenta las
> responsabilidades legales y de privacidad al grabar y conservar imágenes.

> [!NOTE]
>
> El coste de integrar _analítica de vídeo_ varía ampliamente según la
> complejidad, número de cámaras, licencias y proveedores; puede ir desde unos
> pocos miles hasta cifras mucho mayores en proyectos corporativos — es variable
> y debe cotizarse por proyecto.

### Racks cerrados (o de gabinetes)

Los **racks cerrados** o **gabinetes** son armarios donde se alojan servidores y
equipamiento de red para evitar manipulación física no autorizada (e.g.,
desconectar cables, insertar dispositivos USB). Deben combinarse con políticas
de acceso, registro de entrada/salida y sellos/precintos cuando proceda.

> [!TIP]
>
> Mantener un inventario actualizado del mobiliario y equipos (servidores,
> switches, routers, cámaras) facilita la detección de dispositivos no
> autorizados (e.g., routers o hubs instalados clandestinamente).

### Puertas con control de acceso

En una empresa, es importante, controlar a todo momento **qué**, **quiénes**, y
a **qué** áreas dentro del edificio pueden acceder, para ello se pueden
implementar puertas con control de acceso, aplicando los diferentes tipos
métodos de autenticación:

- **Algo que sabes**: PINs, contraseñas.
- **Algo que posees**: Tarjetas de acceso, llaves.
- **Algo que eres**: Datos biométricos que te identifican como personas tales
  como huellas, palmas, cara, ojos, voz.

Adicionalmente, se recomienda que las puertas de un edificio sean instaladas de
adentro hacia afuera, esto para que sea más fácil entrar a una habitación o al
mismo edificio y sea más difícil salir.

#### Tarjetas de acceso

Las **tarjetas de acceso** son medios físicos de autenticación. Pueden usar
diversas tecnologías: tarjetas de proximidad RFID (125 kHz), tarjetas 13.56 MHz
(e.g., MIFARE, iCLASS) y, en algunos casos, NFC (una variante de RFID pensada
para interacción corto alcance con smartphones). El lector valida el
identificador y, si el usuario tiene los permisos, desbloquea la puerta.

Si bien facilitan la gestión, las tarjetas no son infalibles: pueden ser
prestadas, robadas, clonadas o encontradas. Por eso se recomienda:

- Uso de políticas de control de tarjetas (desactivación inmediata al
  reportarlas como perdidas).
- Registros de acceso y revisiones periódicas.
- Implementar factores adicionales de control (e.g., PIN, autenticación
  biométrica o control por tiempo/rol) para áreas críticas.

#### Sistemas biométricos

Un **sistema biométrico** verifica la identidad de un usuario en base a rasgos
fisiológicos o de comportamiento (huella, iris, voz, etc.). Son piezas útiles en
la autenticación física, pero no son invulnerables; su diseño debe contemplar
gestión de falsos positivos/negativos, protección de plantillas biométricas y la
posibilidad de spoofing.

##### Huellas dactilares

Las **huellas dactilares** se basa en el principio en que no existen dos huellas
dactilares idénticas. Cada huella tiene un conjunto de pequeños arcos, ángulos,
bucles, remolinos, etc. característicos llamados **minucias**, y la posición
relativa de cada una de estas se analiza para validar.

Las **huellas dactilares** son analizadas por un escáner táctil, analiza las
minucias y si cumple con una coincidencia mínima al registro, a un escaneo
previamente guardado, el sistema valida exitosamente su autenticidad.

##### Sistema de verificación de patrones oculares

Un **sistema de verificación de patrones oculares** está basado en patrones de
iris o de retina y a día de hoy se consideran como los más efectivos, ya que en
200 millones de personas la probabilidad de coincidencia es casi del 0%. Existen
dos formas de escanear los ojos: - **Escáner de retina**: Mide el patrón de
venas en el fondo del ojo, el cual se obtiene proyectando una luz infrarroja a
través de la pupila. - **Escáner de iris**: Se realiza utilizando una
videocámara. Examina los patrones de color únicos de los surcos de la parte
coloreada de nuestros ojos. Este método es el más preciso.

##### Verificación de voz

La **verificación de voz** compara características de la voz (rasgos espectrales
y características temporales) con plantillas previamente registradas. Existen
tres modos habituales:

- **Dependiente del texto**: el usuario dice siempre la misma frase registrada
  (e.g., una contraseña de voz).
- **Texto aleatorio** (frase aleatoria): el sistema pide que se diga una frase
  generada al azar.
- **Independiente del texto**: el usuario puede decir cualquier frase

La verificación de voz extrae características (e.g., coeficientes cepstrales u
otras representaciones espectrales) y construye una "huella de voz".

> [!CAUTION]
>
> Cabe destacar que con el auge de la IA, hoy en día existen modelos capaces de
> replicar la voz, por lo que este método de autenticación ya no es recomendado.

## Medidas de seguridad contra alteración del entorno

### Electricidad

Un aspecto crítico en centros de datos, empresas tecnológicas y cualquier
instalación dependiente de energía eléctrica es el **sistema eléctrico**. Además
de dimensionar y proteger las líneas, conviene cumplir con normas y estándares
locales/regionales para asegurar confiabilidad y seguridad (e.g., en EE. UU. la
FERC-NERC; en México la CENACE, etc.). Al diseñar una instalación hay que
analizar los dispositivos eléctricos, su consumo y la topología de alimentación
redundante.

Cuando la luz regresa tras un corte pueden ocurrir sobretensiones transitorias
(picos). Por eso se usan supresores de sobretensión, UPS y estrategias de
conmutación segura.

Al diseñar sistemas eléctricos se debe contemplar una adecuada puesta a tierra,
medición de la resistencia de la toma a tierra, selección y correcta instalación
de electrodos (varillas, mallas), y un esquema de equipotencialidad para evitar
diferencias de potencial peligrosas entre equipos. Además, para zonas propensas
a descargas atmosféricas, se recomienda estudiar e instalar protección contra
rayos conforme a normas aplicables.

#### UPS o SAI

Los **Uninterruptible Power Supply (UPS)** o **Sistemas de Alimentación
Ininterrumpida (SAI)** proporcionan respaldo inmediato por batería y protección
contra fluctuaciones y picos, evitando apagones abruptos en equipos críticos.
Existen distintos tipos/topologías (offline, line-interactive, doble conversión
online) con características y niveles de protección distintos.

Existen desde UPS domésticos, los cuales, similar a una multicontactos, se
conectan a un enchufe y proveen múltiples salidas, algunas de ellas con respaldo
de batería.

Dependiendo de la capacidad de la batería del UPS y el consumo de energía de los
dispositivos conectados, puede proveer energía desde unos minutos hasta varias
horas (en aplicaciones domésticas) o días (en instalaciones industriales de gran
capacidad).

La mayoría de los UPS utilizan baterías de plomo-ácido selladas (VRLA),
específicamente del tipo AGM o Gel, las cuales no ocupan mantenimiento. Por otra
parte, existen UPS que utilizan baterías de plomo-ácido inundadas, baterías que
son muy usadas en vehículos. Estas baterías inundadas pueden perder eficiencia
con el tiempo debido a la evaporación del agua destilada, por lo que es
necesario rellenarlas con agua destilada periódicamente

#### Tomas a tierra

En un **sistema eléctrico** es indispensable instalar **tomas a tierra** ya que
estas evitan que equipos eléctricos con fugas de electricidad puedan darnos
descargas eléctricas, ya que la electricidad tiende a seguir el camino con menor
resistencia eléctrica, es decir, hacia la toma a tierra.

> [!IMPORTANT]
>
> Para instalar una toma a tierra, tenemos que tener en cuenta cosas cómo la >
> medición de la resistencia, el tipo de varilla, preparación del suelo, >
> profundidad de la varilla, tapa de registro (para mantenimiento), tipo de >
> conexión, etc.

> [!TIP]
>
> Para determinar si un _sistema eléctrico_ cuenta con una toma a tierra basta >
> con ver si se encuentra instalado una conexión que va hacia una varilla de >
> cobre enterrado en la tierra o si en los cables que se encuentran en un >
> enchufe hay un tercera línea (por lo general verde), es decir, un cable a >
> parte del fase y neutro.

#### Ruido eléctrico

El **ruido eléctrico** abarca transitorios, oscilaciones y ruidos (EMI) que
pueden afectar equipos sensibles. Para mitigarlo:

- Segregar cargas inductivas (motores, bombas) en circuitos distintos de los
  equipos críticos.
- Usar filtros EMI/ RFI y supresores de sobretensión.
- Mantener buen apantallamiento y continuidad de las mallas de tierra.

### Ventilación y aire acondicionado

Los equipos electrónicos requieren condiciones ambientales controladas para
garantizar funcionamiento y vida útil. Las temperaturas operativas recomendadas
varían según el equipo:

- **Equipos de oficina**: rango operativo amplio (e.g., 16–32°C), con confort
  humano óptimo alrededor de 20–24°C.
- **Servidores y equipos críticos**: ASHRAE recomienda un rango de entrada de
  aire típico **18–27°C** (64–81°F) para la mayoría de equipos y ofrece límites
  "permitidos" más amplios según la clase del equipo.

#### Sistemas de climatización

Para entornos críticos:

- **Aires acondicionados de precisión**: controlan temperatura (e.g., ±1°C),
  humedad y filtración, y están diseñados para operación 24/7.
- **Sistemas de ventilación**: deben asegurar flujo de aire, distribución
  uniforme y buen intercambio térmico.

#### Control de humedad

El control de humedad es importante para evitar corrosión y descargas
electrostáticas. Las guías ASHRAE muestran rangos aceptables amplios (20–80% RH)
pero, por prácticas operativas y para minimizar ESD y corrosión, suele
mantenerse una banda recomendada más estrecha (e.g., 45–55% RH) en muchas salas
técnicas; la configuración final debe basarse en el equipo instalado y las
condiciones locales. ([ASHRAE][8])

#### Mantenimiento

Realizar mantenimiento preventivo cada **3–6 meses** es buena práctica e
incluiría:

- Limpieza y/o cambio de filtros.
- Verificación de niveles de refrigerante.
- Calibración y verificación de sensores de temperatura/ humedad.
- Inspección de ductos, sellos y flujo de aire por rack (sensores en
  intake/front de racks).

### Sistemas de Incendio

Al momento de instalar **sistemas de incendio**, es importante estudiar el
entorno, observar qué tipos de incendio pueden ocurrir, qué se debe proteger en
cada de área, etc. Por ejemplo, en un _centro de datos_, se debe evitar
_sistemas de incendio_ que puedan dañar a los servidores y, en general, a los
dispositivos electrónicos. En un _centro de datos_, se optan por soluciones como
cámaras de eliminación de oxígeno o extinción por arena.

#### Alarmas contra incendio

Es importante instalar **alarmas contra incendios** automáticas, las cuales
pueden ya sea **activar un _sistema anti-incendio_** o **activar alertar a los
usuarios**. Asimismo, es importante instalar alarmas manuales para que en caso
de que la alarma falle y alguna persona detecte fuego o algún peligro que lo
provoque (e.g., un tanque de gas abierto), pueda alertar a los demás.

#### Extintores y tipos de incendio

Es importante instalar estratégicamente los tipo de extintores adecuados de
acuerdo al tipo de incendio qué puede ocurrir en cada una de las áreas dentro
del negocio:

| **Tipo de fuego/extintor**   | **Ejemplos**                                                                       |
| ---------------------------- | ---------------------------------------------------------------------------------- |
| **A - Materiales sólidos**   | Madera, caucho, pólvora, plásticos, papel, telas                                   |
| **B - Líquidos inflamables** | Petróleo y sus derivados, aceites, y solventes                                     |
| **C - Eléctricos**           | Equipos eléctricos energizados (e.g., motores, tableros, instalaciones eléctricas) |
| **D - Metales combustibles** | Magnesio, sodio, potasio, aluminio                                                 |
| **K - Cocinas comerciales**  | Grasas y aceites de origen animal o vegetal                                        |

Al intentar mitigar incendios con los extintores o herramientas o métodos
inadecuados, puede no solo no mitigar el incendio, sino causar accidentes, por
ejemplo:

- En un incendio eléctrico, el agua puede causar la electrocución de una
  persona.
- En un incendio dónde hay grasas y aceites (e.g., en una cocina), el agua puede
  incluso avivar la llama.

> [!TIP]
>
> En caso de no haber un extintor disponible, puedes optar por intentar apagar
> el fuego siempre y cuando sea seguro hacerlo; recuerda, eliminar el oxígeno o
> aislar el combustible puede extinguir el fuego. En caso de no poder extinguir
> el fuego, es importante evacuar y avisar a emergencias.

Por último, es vital capacitar al personal sobre los tipos de incendios, uso de
extintores y procedimientos de evacuación.

## Medidas de seguridad ante desastres naturales

### Desastres naturales

#### Tormentas eléctricas

Las tormentas eléctricas pueden producir descargas peligrosas y daños por
sobretensión, causando daños severos a personas, equipos, infraestructura de una
empresa, etc.

Para protegerse ante las tormentas eléctricas, una empresa puede instalar
**sistemas pararrayos**, sistemas que se instalan en el techo del edificio y los
cuáles capturan las descargas atmosféricas y las conducen de manera segura hacia
el **sistema de puesta a tierra**.

Durante las tormentas eléctricas, es esencial seguir las recomendaciones
generales de seguridad:

- Refugio en edificios.
- Alejarse de árboles y puntos altos.
- Evitar el contacto con metales.
- En caso de estar dentro de un vehículo cerrado, mantenerse dentro de él. La
  estructura metálica del vehículo actúa como una jaula de Faraday, por lo que
  es relativamente segura, pero no se debe tocar la carrocería.

### Respaldo de datos

La política de seguridad debe contemplar copias de respaldo (backups) regulares
para evitar pérdida de información por destrucción física del soporte o
desastres naturales. Los respaldos se clasifican de la siguiente manera:

- **Respaldos internos**: Copias en servidores o almacenamiento dentro de la
  organización (útiles para recuperación rápida ante corrupción o ciertos
  ataques).
- **Respaldos externos / offsite**: Copias fuera del sitio (otra ubicación
  física o en la nube) que protegen contra desastres locales.

Es importante definir RTO (tiempo objetivo de recuperación) y RPO (punto
objetivo de recuperación) y automatizar y verificar regularmente los respaldos y
sus restauraciones.

> [!IMPORTANT]
>
> Realizar backups con la frecuencia necesaria para cumplir el RPO definido;
> además, probar periódicamente la restauración para garantizar la validez de
> los respaldos.

#### Protección de los respaldos de datos

Es importante establecer una **política para las copias de seguridad**, el cuál
establezca en dónde se almacenarán los respaldos, ya sea en la nube o en algún
medio local.

En caso de optar por guardar los respaldos en un medio local es necesario
establecer políticas que, al igual que con el resto de equipos (e.g.,
computadoras, servidores, dispositivos de red), estos sean protegidos
físicamente, garantizando la triada CID.

Primeramente debemos de pensar en dónde se almacenarán los dispositivos de
respaldo. Un error muy habitual es almacenarlos en lugares cercanos al SITE de
operaciones

Para proteger aún más la información respaldada, se puede optar por mecanismos
de cifrado para garantizar la confidencialidad de los datos.

### Centros de datos y servidores

Al instalar un centro de datos es de vital importancia elegir la ubicación más
idónea, considerando el entorno y cómo puede afectar a nuestro centro de datos,
por lo que se recomienda:

- Elegir zonas de baja sismicidad.
- Evitar áreas inundables o con riesgo de inundación.
- Considerar clima local y accesibilidad de servicios (energía, comunicaciones).
- Evitar proximidad a fuentes de vibración y fuentes de ondas electromagnéticas
  (e.g., líneas ferroviarias).
- Evitar industrias o instalaciones de alto riesgo.

Adicionalmente, al instalar un centro de datos se recomienda:

- Redundancia de suministro eléctrico y comunicaciones.
- Accesibilidad controlada para personal técnico.
- Diseño de plantillas antisísmicas, anclajes para racks y fijaciones si la
  región lo requiere.
- En entornos costeros considerar ubicaciones en plantas superiores o medidas de
  mitigación contra inundaciones; en zonas con tormentas eléctricas, proteger
  con supresores y pararrayos según normativa aplicable.

## Recursos recomendados

- [Cenace](https://www.gob.mx/cenace)
- [Seminario puesta a tierra - Genrod](https://www.youtube.com/watch?v=TylWWBLAL5g)

## Referencias

- NetAcad (s.f.). _3.2 Access Control_. Network Support and Security.
  <https://www.netacad.com/launch?id=fa6ac75d-3afd-4bde-93f5-f164d8253ab6&tab=curriculum&view=891b93a4-a02e-50e1-bb17-dc28c62e13b4>

- ACI Learning, Wes B., & Deal L. (febrero, 2024). _Physical Security_. Security
  Fundamentals.
  <https://subscription.packtpub.com/video/security/9781835463376/p1/video1_6/physical-security>

- RealPars (julio 29, 2019)_. ¿Qué es un SAI? (Sistema de Alimentación
  Ininterrumpida)_. <https://www.youtube.com/watch?v=bj5KpFR_LPU>

- Sfdx Show (julio 03, 2022). _Se rompió Hace 3 años 😱 y No quería tirarlo 😅
  UPS/SAI_ <https://www.youtube.com/watch?v=XyDBbUuAajI>

- Electrovoltec (abril 08, 2023). _⚡COMO INSTALAR PUESTA a TIERRA FISICA para
  CASA en 8 Pasos │ 🚫5 Errores a Evitar│CURSO Paso a Paso_.
  <https://www.youtube.com/watch?v=m625oJ1oudE>

- Soto J., (s.f.). _Medidas de Protección Física_. Seguridad en la Información.
  <https://drive.google.com/file/d/15K__4wGt3Dk9sUWxN7bKl44UskQ5FMNH/view>
