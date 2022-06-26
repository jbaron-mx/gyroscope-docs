---
description: Resilientes principios de gobernanza utilizados en Gyroscope
---

# Principios de gobernanza

{% hint style="info" %}
_Esta documentación describe los mecanismos diseñados de Gyroscope formulados a través de la investigación y el desarrollo académico. Gyroscope está diseñado para ser completamente descentralizado, con Gyro DAO como responsable de definir cuales mecanismos son incorporados al diseño final y lanzamiento del sistema Gyroscope._
{% endhint %}

Gyroscope está diseñado para forjar un ciclo virtuoso entre sus diferentes usuarios: acreedores de Gyro Dollars, gobernadores y proveedores pasivos de liquidez (LPs).

![](<../../.gitbook/assets/Governance Flow Chart (1).png>)

Lee más para aprender cómo el diseño de Gyroscope fomenta este ciclo virtuoso.

### **La gobernanza de hoy en día no tiene fondos protegidos**

Al igual que los políticos y banqueros, los gobernadores en sistemas DeFi pueden ser de vista-corta y centrarse en ganancias inmediatas en lugar del beneficio a largo plazo. También pueden ser totalmente mal-intencionados, especialmente en DeFi donde los gobernadores son prácticamente anónimos. Nosotros denominamos estos problemas de vista-corta y abusos al sistema como valor extraíble de gobernanza (GEV en inglés), que necesita ser minimizada para mantener un protocolo DeFi seguro. Lee más en nuestro reciente artículo sobre [GEV](https://ournetwork.substack.com/p/our-network-deep-dive-2) y en nuestro documento sobre [DeFi](https://arxiv.org/abs/2101.08778) (sección V.C y VI.B).

### **Gobernanza reinventada**

Motivado por la investigación académica, Gyroscope propone varios mecanismos nuevos de gobernanza que ayudan a alinear a los gobernadores con los intereses a largo plazo de el protocolo al minimizar el GEV.

¿Cómo? En cualquier moneda estable algorítmica funcional, alguien siempre paga \~$1 por cada nueva moneda estable emitida. A donde se destina este $1 es lo crítico. En diseños actuales, una parte o todo de este dólar se destina al bolsillo de alguien más: por ejemplo, accionistas en diseños de acciones de señoreaje. Para el interés propio a largo plazo del protocolo, esto es un error. Esto reduce la participación de los gobernadores en el juego mientras que debería ser lo contrario e incrementarla. Mientras que los rendimientos en granjas sean lo suficientemente grande a corto plazo, no tienen motivo alguno para preocuparse por la pequeña participación que puedan perder si no salen a tiempo.

El diseño de Gyroscope es diferente. A largo plazo, el sistema descentralizado de Gyroscope podría generar flujos de capital para operaciones. Una pregunta clave del diseño es cómo estos flujos de capital pueden ser distribuidos para incentivar a los participantes. Gyroscope propone un nuevo principio de gobernanza llamado Flujos de Capital Condicionales, que coloca a los gobernadores en un rol de recibir recompensas en relación a la salud del sistema a futuro. El mecanismo funciona reteniendo flujos de capital operacional en la reserva del protocolo y liberando a futuro las recompensas relacionadas a estos flujos de capital a los gobernadores si el sistema se mantiene saludable. Si el sistema se vuelve inestable, los flujos de capital son por defecto retenidos para conservar estabilidad. Los gobernadores, que tienen el importante rol de gestionar y sanar la reserva del protocolo, son desincentivados de tomar decisiones riesgosas, ya que coloca sus actuales recompensas en riesgo (comparado a banqueros quienes no tienen que devolver sus bonos si el banco colapsa). Si los tiempos son buenos y el token de gobernanza se valúa muy alto, los gobernadores son incentivados a subastar con anticipación nuevos tokens para impulsar la reserva.

¿Pero cómo sabemos que los gobernadores no pueden abusar de su poder en otras formas? Gyroscope propone otro nuevo principio de gobernanza llamado Aprobación Optimista, que encamina a los gobernadores a través de un sistema de pesos y contrapesos. En este mecanismo, si los gobernadores tratan de desviarse de la visión compartida de el protocolo, los acreedores de Gyro dólares pueden ejercer poderes de veto opcionales durante un período de tiempo para detenerlo. Por lo general, los acreedores de Gyro dólares no necesitan hacer nada si las acciones de gobierno son sólidas. Sin embargo, si las acciones de gobierno son contenciosas, los acreedores de Gyro dólares pueden ejercer la opción de veto, y si suficientes hacen lo mismo, la acción será bloqueada.

Gyroscope se trata de empoderar a la comunidad para que gobierne su propio dinero, haciendo que sus usuarios sean sus dueños. Proporciona los mejores mecanismos de su clase para hacer que esto cobre vida. La equidad y la descentralización son las principales prioridades en la distribución de tokens de gobernanza.
