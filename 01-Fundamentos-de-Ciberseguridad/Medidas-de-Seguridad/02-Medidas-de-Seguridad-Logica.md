# Medidas de Seguridad Lógica

La **seguridad lógica** consiste en la aplicación de barreras y procedimientos
que resguarden el acceso a los datos y solo se permita acceder a ellos a las
personas autorizadas para hacerlo. Se podría decir que básicamente es la
protección de la información en su propio medio contra robo o destrucción,
haciendo uso de la criptografía, firma digital, administración de la seguridad y
limitaciones de accesibilidad a los usuarios.

## Controles de Acceso Lógico

Los **controles de acceso lógico** son las soluciones hardware y software usadas
para gestionar el acceso a los recursos y los sistemas. Estas soluciones
tecnológicas incluyen herramientas y protocolos que los sistemas informáticos
usan para la identificación, autenticación, autorización y la gestión de
cuentas.

Algunos ejemplos de _controles de acceso lógico_ son:

- Encriptación es el proceso de tomar texto plano y convertirlo a texto cifrado.
- Las tarjetas inteligentes tienen un microchip integrado.
- Las contraseñas son cadenas de caracteres (_strings_) protegidos.
- Los datos biométricos son las características físicas únicas y medibles de los
  usuarios.
- La lista de control de accesos (ACLs) define permisos de acceso a recursos y
  el tipo de tráfico permitido en una red.
- Los protocolos son un conjunto de reglas que rigen el intercambio de datos
  entre dispositivos.
- Los firewalls evitan el tráfico de red no deseado.
- Los routers conectan al menos dos redes.
- Los sistemas de detección de intrusos (IDS) supervisan una red para detectar
  actividades sospechosas.
- Los umbrales de alerta son ciertos límites de error permitidos antes de
  activar una bandera roja.

## Controles de Acceso Administrativo

Los **controles de acceso administrativo** son las políticas y los
procedimientos definidos por las organizaciones para aplicar y hacer cumplir
todos los aspectos del control de accesos no autorizados.

- **Políticas**: Ideas o acciones aprobadas que guían el comportamiento.
- **Procedimientos**: Pasos detallados que una organización requiere para
  realizar una actividad.
- **Prácticas de contratación**: Definen los pasos que una organización toma
  para encontrar empleados calificados.
- **Revisión de antecedentes**: Revisión aplicada a un empleo para verificar sus
  empleos anteriores, historial crediticio e historial criminal.
- **Clasificación de datos**: Categoriza los datos en base a su nivel de
  sensibilidad.
- **Entrenamiento de seguridad**: Educa a los empleados acerca de las políticas
  de seguridad de una organización.
- **Revisiones**: Evalúan el rendimiento del trabajo de un usuario.

## Identificación

La **identificación** es el primer paso en el control de acceso, donde se
establece quién está solicitando acceso al sistema. Un identificador único
asegura la asociación apropiada entre actividades y sujetos permitidos. Un
nombre de usuario es el método más común para identificar a un usuario. Un
nombre de usuario puede ser una combinación alfanumérica, un número de
identificación personal (PIN), una tarjeta inteligente, o un dato biométrico,
tal como una huella, escaneo de retina o reconocimiento de voz.

Un identificador único asegura que un sistema pueda identificar a cada usuario
individualmente, permitiendo así a un usuario realizar acciones apropiadas en un
recurso en particular.

## Autenticación, Autorización, y Gestión de Cuentas (AAA)

Los conceptos de **control de acceso administrativo** involucran tres servicios
de seguridad: autenticación, autorización y gestión de cuentas. Estos servicios
proveen el framework principal para controlar el acceso, prevenir acceso no
autorizado a una computadora, red, base de datos o cualquier otro recurso de
datos.

- **Autenticación**: Verificación de la identidad de cada usuario, para prevenir
  acceso no autorizado. Los usuarios proveen su identidad con un nombre de
  usuario o ID. Adicionalmente, los usuarios necesitan verificar su identidad al
  proveer alguno de los siguientes:
  - Algo que saben (e.g., una contraseña).
  - Algo que poseen (e.g., un token o una tarjeta).
  - Algo que son (e.g., una huella dactilar).

- **Autorización**: Los servicios de autorización determinan cuáles recursos los
  usuarios pueden acceder con las operaciones que los usuarios pueden realizar.
  Algunos sistemas cumplen esto al utilizar una lista de control de acceso, o un
  ACL. Un ACL determina si un usuario tiene ciertos privilegios una vez que se
  autentica. La autorización también puede determinar _cuando_ un usuario tiene
  acceso a un recurso específico.

- **Gestión de cuentas**: Mantiene seguimiento de lo que los usuarios hacen,
  incluyendo a qué accedieron, la cantidad de tiempo y cualquier tipo de cambio
  que hicieron. En ciberseguridad, un sistema puede hacer seguimiento de cada
  transacción que realizas y provee resultados de auditoría. Administradores de
  sistemas pueden establecer políticas informáticas para permitir la auditoría
  del sistema.

## Gestión de Identidades Federadas

La **gestión de identidades federadas (FIM)** se refiere a las múltiples
empresas que permiten a sus usuarios utilizar las mismas credenciales de
identificación para conseguir acceso a las redes de todas las empresas en el
grupo. Mientras FIM provee conveniencia a los usuarios y administradores, si el
sistema es explotado por hackers, tendrán acceso a muchos sistemas en lugar de
solo uno.

Generalmente hablando, una identidad federada vincula la identidad electrónica
de una persona en distintos sistemas de gestión de identidad. Esto podría
permitir a varios sitios web usar las mismas credenciales de inicio de sesión
social (e.g., Google SSO, SAML, OAuth).

El objetivo de la gestión de la identidad federada es compartir información
automáticamente a través de los límites de la empresa. Desde la perspectiva del
usuario, esto significa un simple inicio de sesión en múltiples redes.

Es imperativo que las organizaciones examinen con lupa la información
identificativa que se comparte con los socios, incluso dentro del mismo grupo
empresarial. El compartir números de seguro social, nombres, y direcciones puede
permitir a los ladrones de identidad la oportunidad de robar esta información
desde un socio con una seguridad débil para perpetrar un fraude. La manera más
común de proteger la identidad federada es usar dispositivos autorizados tales
como estaciones de trabajo y teléfonos.

## Referencias

- NetAcad (s.f.). _3.2 Access Control_. Network Support and Security
  <https://www.netacad.com/launch?id=fa6ac75d-3afd-4bde-93f5-f164d8253ab6&tab=curriculum&view=891b93a4-a02e-50e1-bb17-dc28c62e13b4>

- Soto J., (s.f.). _Medidas de Protección Lógica_. Seguridad en la Información.
  <https://drive.google.com/file/d/14zmzxgYho2DMvGNSW0nQN6We-PuLATDZ/view>
