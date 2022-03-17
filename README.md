---
description: Documentación del protocolo Gyroscope
---

# Introducción

Esta documentación describe el diseño teórico de los mecanismos del protocolo Gyroscope formulado por FTL Labs mediante la investigación y el desarrollo académico. Gyro DAO es responsable del lanzamiento de Gyroscope y de la toma de decisiones sobre los mecanismos a incorporar al diseño final.

Ante cualquier información incompleta u obsoleta, por favor enviar una solicitud de cambio al repositorio gyroscope-docs.

## El Protocolo Gyroscope

La misión de Gyroscope es construir infraestructura pública y robusta para las finanzas decentralizadas (DeFi). La pieza central es una moneda estable completamente respaldada con reservas todo-terreno y vinculación algorítmica del precio:

* **Una moneda estable completamente respaldada**: la moneda estable de Gyroscope pretende alcanzar un coeficiente de reserva del 100% a largo plazo, donde cada unidad de moneda estable esté respaldada por 1 USD en valor de garantías.
* **Una reserva todo-terreno**: la reserva es una canasta de activos digitales controlados por el protocolo que conjuntamente respaldan la moneda estable emitida. Inicialmente todos los activos serán otras monedas estables. La reserva pretende diversificar todos los riesgos en DeFi en la mayor medida posible. Mas allá del riesgo de precio, también se considera el riesgo de censura, regulatorio, de contraparte, de oráculo y de gobernanza.
* **Vinculación algorítmica del precio**: los precios de emisión y redención de las monedas estables son definidos algorítmicamente para lograr mantener la paridad de precio lo más ajustada posible y de esta forma hacer que el proyecto tenga viabilidad a largo plazo haciendo frente a posibles crisis en el corto plazo.

{% hint style="info" %}
El protocolo Gyroscope será lanzado en Ethereum. El protocolo aún está en desarrollo. Una [versión gamificada en Kovan Testnet](https://docs.gyro.finance/testnet/testnet-walk-through) está disponible para introducir a los usuarios a los conceptos clave en varios niveles de fácil acceso.
{% endhint %}

## Mecanismos de estabilidad fundamentales

### Escenario A: la moneda estable se valúa por encima del precio objetivo

Si el precio sube por encima del precio objetivo, más monedas estables pueden ser emitidas y vendidas en el mercado y las ganancias destinadas a aumentar la reserva. Esto es efectivamente un **ciclo de arbitraje cerrado al alza**. Para prevenir una excesiva expansión de la oferta de monedas estables en reacción a un evento transitorio de mercado (cómo la pérdida de confianza en otra moneda estable), la emisión podría ser temporalmente deshabilitada si la entrada de capital es cuantiosa y la moneda estable se encuentra con excedente de garantías.

{% hint style="info" %}
Esto es parte del componente algorítmico del diseño de Gyroscope: Esta previsto hacer la transición hacia tarifas de emisión dinámicas mediante el uso de curvas de vinculación (bonding curves) que calculen los flujos de capital para emitir/redimir monedas estables.
{% endhint %}

### Escenario B: la moneda estable se valúa por debajo del precio objetivo

Dependiendo de si el 100% de la oferta de monedas estables está respaldada por el valor de la reserva o no, este escenario se desenvuelve diferente:

* Con reservas saludables el mismo ciclo de arbitraje existe como al alza. Monedas estables pueden ser compradas en el mercado y redimidas por $1 USD en valor de activos en reserva. Este es el caso predeterminado, como se describe en la primera línea de defensa del diseño de reserva todo-terreno, que hace al respaldo de activos tan robusto como es posible.
* Si hay un shock importante a la reserva, existen adicionales lineas de defensa, incluyendo la vinculación algorítmica del precio.

## Líneas de defensa del protocolo

**Múltiples líneas de defensa existen para mantener al sistema estable**. La **primera línea de defensa es la reserva todo-terreno** que almacena todas las ganancias provenientes de la emisión y además diversifica todos los riesgos en DeFi en la mayor medida de lo posible. Esto procura tener activos en garantía suficientes como escenario predeterminado. La reserva todo-terreno diversifica mas allá del riesgo de precio, también considera el riesgo de censura, regulatorio, de contraparte, de oráculo y de gobernanza.

{% hint style="info" %}
Mientras la reserva será inicialmente y casi exclusivamente compuesta de otras monedas estables, esto podría cambiar a largo plazo. Un shock importante a la reserva sólo podría ocurrir si hay problemas incluso más grandes en otros sistemas DeFi, de los cuales Gyroscope podría posibilitar el resultado menos perjudicial.
{% endhint %}

![La reserva de Gyroscope está diseñada para segregar diferentes riesgos en diferentes bóvedas (triángulos).](https://2063019688-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MU527HCtxlYaQoNazhF%2Fuploads%2FVsLqI7lD76gKFaQYklY6%2FVaults%20Graphic%20v2.png?alt=media\&token=4795d72e-d265-464b-b6f5-1d7dbe4c1e56)

**Si hay un shock grave a la reserva, entonces la segunda línea de defensa, la cotización algorítmica de Gyroscope toma el control**. Si la unidad de moneda estable se encuentra con déficit de garantías, la curva de vinculación del mercado de redención provee cotizaciones a la baja como corto-circuito para mantener al sistema sostenible. Este mecanismo de estabilidad debería ser raramente necesario, pero existe cómo plan de contingencia y utiliza el diseño multi-mercado de Gyroscope que concentra la liquidez entre los precios de cotización de las curvas de vinculación para la emisión/redención de la moneda estable.

El objetivo de reducir la cotización de redención sirve para desincentivar una estampida bancaria (bank run) y ataques a la paridad de la moneda y recompensar a aquellos usuarios que esperan a que la crisis transitoria concluya de forma sostenible. Mientras la habilidad de los participantes para marcharse del sistema es retenida, Gyroscope, de forma importante provee razones para apostar que la moneda estable regresará a su precio objetivo, conforme el precio de redención se recupera algorítmicamente hacia la paridad y las salidas de capital equilibran a cero o las reservas se recuperan (ej. mediante rendimientos).

{% hint style="info" %}
La intuición del juego de coordinación para mantener la paridad de la moneda es la siguiente:

Usuarios forman creencias del valor fundamental de la moneda estable. Basadas en el valor de la reserva y que tan aceptada y utilizada es la moneda estable. Pero los usuarios también forman creencias sobre las creencias de otros participantes del mercado (y así sucesivamente). Gyroscope coordina estas creencias. Ya que el valor de la reserva es observable en-cadena, así como también las reglas que gobiernan cómo será utilizada, entonces los usuarios racionales implícitamente concuerdan si atacan o defienden la paridad ya que sólo ganan si forman mayoría. Esto pretende adelantarse a crisis de confianza.
{% endhint %}

**Las líneas de defensa terciarias** incluyen mecanismos que permiten a las reservas recuperarse o expandir el respaldo de activos. La reserva puede, por ejemplo, recapitalizarse mediante la subasta de tokens de gobernanza. De hecho, se incentiva la gobernanza de Gyroscope a hacer esto en momentos oportunos para formar 'colchones' de activos contra shocks, en lugar de actuar únicamente como respaldo de último recurso durante una crisis. El mecanismo de Gyroscope también funciona de la mano con mecanismos de préstamos apalancados (cómo Maker) para fortalecer la estabilidad.

## Infraestructura complementaria

Productos adicionales surgen del diseño de Gyroscope. Por ejemplo, un intercambio decentralizado (DEX) altamente líquido que pueda soportar colapsos de activos digitales surgiría naturalmente del diseño de Gyroscope. Este diseño puede ser conceptualizado como una red de creadores de mercado automatizados de mercados secundarios, pools de reservas y pools externos que permitirán el enrutamiento eficiente de transacciones. Creadores de mercado automatizados de mercados secundarios (SAMMs) ofrecen rutas redundantes y altamente liquidas para la entrada y salida de monedas estables Gyroscope, mientras que el creador de mercado automatizado de mercados primarios (PAMM) sería el mercado de emisión y redención. Para más detalles por favor lea las descripciones del PAMM y SAMM.

![El SAMM y pool de reserva de Gyroscope forman un DEX donde la liquidez es robusta ante colapsos del pool.](https://2063019688-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MU527HCtxlYaQoNazhF%2Fuploads%2F4pUejKivkcxjlbQiDbux%2FAMMs%20Graphic%20Rounded%20Edges.png?alt=media\&token=5316b320-5fbf-4dbf-9486-9ae990be5f91)
