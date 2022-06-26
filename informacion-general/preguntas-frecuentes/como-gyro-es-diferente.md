---
description: Diferenciando Gyro de otras monedas estables
---

# ¿Cómo Gyro es diferente?

Gyro está diseñado para ser la moneda todo-terreno de DeFi. Gyro está diseñado para abordar de forma única los siguientes mayores retos para las monedas estables sin-custodios.

1. **Escalabilidad**: la habilidad para soportar altos niveles de demanda en forma sostenible. Mientras nos agradan las monedas estables con garantías excedentes como Dai, estas se apoyan de el mercado de apalancamiento al alza de ETH para escalar, del cual ya han tenido problemas antes y probablemente los tendrán de nuevo.
2. **Fiable durante crisis**: la habilidad de mantener la paridad dentro de un rango ajustado mientras hay turbulencias de mercado sin invocar suposiciones de confianza (por ejemplo, atarse a USDC).
3. Gobernanza alineada: tener un mecanismo de gobernanza que incentive la salud a largo plazo de la moneda estable, en lugar de ganancias a corto plazo.&#x20;

Expandimos estas ideas en una serie de tres partes: [Parte I](https://medium.com/gyroscope-protocol/gyroscope-is-different-part-1-72dcb8c303a4), [Parte III](https://medium.com/gyroscope-protocol/gyroscope-is-different-part-2-algorithmic-stablecoins-78c53c005e89), Parte III (pronto).

| En comparación a                                         | Diseño mejorado de Gyroscope                                                                                                                                    |
| -------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Meta monedas estables                                    | Mejor segregación de riesgos: [Parte I](https://medium.com/gyroscope-protocol/gyroscope-is-different-part-1-72dcb8c303a4)                                       |
| Monedas estables algorítmicas                            | Resiliencia por sobre crisis de confianza: [Parte II](https://medium.com/gyroscope-protocol/gyroscope-is-different-part-2-algorithmic-stablecoins-78c53c005e89) |
| Monedas estables custodiadas y basadas en apalancamiento | Parte III (pronto)                                                                                                                                              |

## Meta monedas estables

Las meta monedas estables están compuestas de una canasta de otras monedas estables. La idea es que la canasta diversifique los riesgos de las monedas estables individuales. Esto puede crear un nuevo tipo de riesgo para la moneda estable, llamado riesgo de componibilidad: el riesgo de que un problema en un sistema pueda permear hacia otros sistemas. Para mayor discusión, vea nuestro [artículo aquí](https://medium.com/gyroscope-protocol/gyroscope-is-different-part-1-72dcb8c303a4). La reserva todo-terreno de Gyroscope está diseñada para ser resistente a estos riesgos de componibilidad.

## Monedas estables algorítmicas

Las monedas estables algorítmicas pretenden mantener un precio estable al adaptar automáticamente la oferta de la moneda estable con la demanda. Hasta este punto las monedas estables algorítmicas han intentado abordar el reto de escalabilidad de una forma defectuosa: al intentar producir tantas monedas estables con tan pocos activos en garantías como sea posible. Por ejemplo, los diseño tipo Basis intentan mantener las monedas estables sin garantía. Estos y otros diseños de acciones de señoreaje parecidos, basados en "garantías endógenas", confian en un sentimiento de expectaciones auto-cumplidas sobre el sistema or sus futuros flujos de capital. Sin embargo, estos flujos de capital son muy frágiles y puede desaparecer en una crisis. Otros intentos más recientes recaen entre estos tipos de diseños y diseño de reserva completa.

Esto esta defectuoso porque es innecesario para la escalabilidad y puede venir a expensas del sistema. Para ver por qué, considera que en cualquier moneda estable funcional, alguien siempre compra monedas estables recién emitidas por $1. La pregunta clave es a donde va este $1. En los diseños con déficit de garantías, mucho de este se destina a los participantes del protocolo a expensas de la salud del sistema.

Gyroscope no es como esas monedas estables algorítmicas. En su lugar, cada uno de los $1 recibidos por una nueva moneda estable se destina a la reserva procurando ser 100% respaldada. Esto es tan escalable como otros diseños algorítmicos, simplemente desvía las ganancias por señoreaje a los lugares correctos.&#x20;

Para mayor discusión de como Gyroscope se compara con monedas estables algorítmicas, incluyendo resistencia a estampidas bancarias, lea nuestro [artículo aquí](https://medium.com/gyroscope-protocol/gyroscope-is-different-part-2-algorithmic-stablecoins-78c53c005e89).

![](<../../.gitbook/assets/Algorithmic Stablecoins Confidence Crisis Flow Chart.png>)

## Monedas estables custodiadas y basadas en apalancamiento

Pronto. Lea anticipadamente en nuestro documento [Stablecoins 2.0](https://arxiv.org/abs/2006.12388)
