---
description: >-
  Procesos de gobernanza eficientes y controlados al otorgar derechos de veto a
  los usuarios.
---

# Aprobación Optimista

La aprobación optimista es un nuevo principio de gobernanza que permite que los cambios sean condicionales y estén sujetos a un proceso de bloqueo de tiempo y veto. Es un mecanismo muy flexible que puede ser utilizado tanto para agilizar los procesos de gobernanza y para alinear de mejor forma los incentivos entre los participantes del protocolo, no solamente en Gyroscope pero también en la gobernanza de DeFi en general.

Lee [aquí](https://ournetwork.substack.com/p/our-network-deep-dive-2) nuestra investigación que introduce a la aprobación optimista.

La aprobación optimista puede ayudar para alinear incentivos entre diferente tipos de participantes: uno es quien posee poderes de gobernanza (gobernadores) y otro (guardianes) es quien tiene el poder para opcionalmente ejercer veto durante un período de bloqueo de tiempo. Por lo general, los guardianes no necesitan involucrarse en la gobernanza del día a día, pero el veto les otorga la habilidad de bloquear propuestas maliciosas qué podrían desviar de la visión de el protocolo.

El marco de aprobación optimista generaliza quien tiene poderes de gobierno y quien tiene derechos de veto durante un tiempo de retraso. Además, el mecanismo está parametrizado por (1) la duración inicial del bloqueo de tiempo, (2) el umbral de votación del guardian para aumentar la duración del bloqueo de tiempo y (3) el umbral de votación del guardian para lograr el veto.

### Alineando incentivos de gobernanza

En la primera aplicación de Gyroscope, la aprobación optimista está diseñada para otorgar a los usuarios del protocolo un poder de veto para detener los cambios de gobierno con los que no están de acuerdo. En este caso, los usuarios del protocolo cumplen el rol de guardián para asistir la visión del protocolo (por ejemplo, de mantener la estabilidad). El mecanismo introduce controles y equilibrios en el poder de los gobernadores. Si los gobernadores intentan desviarse de la visión compartida del protocolo, los acreedores de Gyro dólares podrán ejercer poderes de veto opcionales durante el tiempo de retraso para detenerlo. Por lo general, los acreedores de Gyro dólares no necesitarán hacer nada si las acciones de gobierno son sólidas. Sin embargo, si las acciones de gobernanza son contenciosas, los acreedores de Gyro dólares pueden ejercer el veto para bloquear la acción.

{% hint style="info" %}
La aprobación optimista se ideo inicialmente como un medio para eludir una conjetura de imposibilidad en torno a un gobierno descentralizado seguro que surge de los modelos en nuestro documento [Stablecoins 2.0](https://arxiv.org/abs/2006.12388) (Conjetura 1).
{% endhint %}
