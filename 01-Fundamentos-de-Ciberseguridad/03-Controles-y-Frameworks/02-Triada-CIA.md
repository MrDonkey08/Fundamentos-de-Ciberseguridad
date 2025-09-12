# Triada CIA

**La tríada CIA** (del inglés _Confidentiality, Integrity, Availability_) es un
modelo fundamental en la seguridad de la información. Sirve como base para
evaluar riesgos y diseñar políticas y controles que protejan los activos de una
organización. Cada componente representa un principio esencial para mantener la
seguridad de los datos:

- **Confidencialidad**: Garantiza que solo las personas, entidades o procesos
  autorizados puedan acceder a información sensible. Su objetivo es prevenir el
  acceso no autorizado.

  La confidencialidad se implementa mediante mecanismos como el control de
  acceso, autenticación fuerte y cifrado de datos. Algoritmos de cifrado como
  AES (Advanced Encryption Standard) se utilizan comúnmente para proteger la
  información durante su almacenamiento o transmisión.

- **Integridad**: Asegura que los datos no sean alterados de manera no
  autorizada y que permanezcan precisos y consistentes a lo largo del tiempo.
  También implica que cualquier modificación legítima sea rastreable.

  La integridad se protege mediante sumas de verificación (checksums), funciones
  hash criptográficas como SHA-256, y técnicas como las firmas digitales que
  permiten verificar la autenticidad y exactitud de los datos.

- **Disponibilidad**: Garantiza que los sistemas, servicios y datos estén
  accesibles y operativos cuando se necesiten. Se busca minimizar interrupciones
  por fallos técnicos, ataques (como DDoS), errores humanos o desastres.

  Para asegurar la disponibilidad se emplean medidas como redundancia de
  hardware y red, sistemas de respaldo (backups), tolerancia a fallos, y planes
  de recuperación ante desastres.

## Referencias

- <https://www.coursera.org/learn/foundations-of-cybersecurity/lecture/wxo04/secure-design>
