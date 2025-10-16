# Principios de Seguridad de OWASP

El _Open Web Applications Security Project_ (OWASP)

- **Minimizar la superficie de ataque**: La superficie de ataque se refiere a
  todas la vulnerabilidades potenciales que un actor de amenaza podría explotar.

  Para minimizar la superficie de ataque y evitar incidentes, los equipos de
  seguridad pueden deshabilitar funciones de software, restringir el acceso a
  ciertos activos, o establecer requisitos de contraseñas más complejos.

- **Principio del menor privilegio**: Establece que los usuarios se les otorgue
  la mínima cantidad de accesos necesarios para realizar sus actividades
  diarias.

- **Defensa en profundidad**: Las organizaciones deberían tener múltiples
  controles de seguridad para mitigar riesgos y amenazas. Algunos ejemplos son:
  - 2FA/MFA
  - Firewalls
  - IDS/IPS
  - Configuraciones de permisos

- **Separación de funciones**: Acciones críticas deberían depender de varias
  personas, cada una de las cuales debe seguir el principio del menor
  privilegio.

- **Mantener la seguridad simple**: Evitar soluciones complicadas innecesarias.
  La complejidad hace la seguridad más difícil.

- **Arreglar problemas de seguridad correctamente**: Cuando un incidente de
  seguridad sucede, identifica la raíz de la causa, contenga el impacto e
  identifica vulnerabilidades, y pruebas de conducta para asegurar que la
  corrección se realice correctamente.

## Principios de seguridad de OWASP adicionales

- **Establecer valores seguros por defecto**: Significa que cuando un control
  falla o se detiene, debería hacerlo por defecto a su opción más segura.

- **Fallar seguramente**: Se refiere a que cuando un control falla o se detiene,
  debe hacerlo por defecto a su opción más segura. Por ejemplo, cuando un
  firewall falla debería simplemente cerrar todas las conexiones y bloquear
  todas las nuevas, en lugar de empezar a aceptarlo todo.

- **No confiar en servicios**: Muchas Organizaciones trabajan con socios
  terceros. Estos socios externos a menudo cuentan con diferentes políticas de
  seguridad que la organización. La organización no debería explícitamente
  confiar que los sistemas de los socios son seguros.

- **Evitar seguridad por oscuridad**: La seguridad de los sistemas clave, no
  debería en mantener los detalles ocultos.

  La seguridad de una aplicación no debe basarse en mantener en secreto el
  código fuente. Su seguridad debe basarse en muchos otros factores, como
  políticas razonables de contraseñas, defensa en profundidad, límites a las
  transacciones comerciales, una arquitectura de red sólida y controles de
  fraude y auditoría.

## Referencias

- Google (s.f.). _More about OWASP security principles_. Play It Safe: Manage
  Security Risks.
  <https://www.coursera.org/learn/manage-security-risks/supplement/J6QBR/more-about-owasp-security-principles>
