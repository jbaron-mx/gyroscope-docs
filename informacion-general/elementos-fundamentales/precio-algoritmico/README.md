---
description: Estructura de mercado y precio
---

# Precio algorítmico

Gyroscope utiliza **dos diferentes tipos de mercados automatizados,** o por sus siglas en inglés _AMM_ (_Automated Market Maker_):

* Un mercado **Primario AMM** (PAMM) diseñado para cotizar los precios de emisión y redención de las unidades de monedas estables __ en función del impacto potencial a los activos subyacentes.
* Multiples mercados **Secundarios AMMs** (SAMMs) que concentran la liquidez entre la banda de precios establecida por el PAMM mediante _pools_ adaptadas en Balancer v2.

{% hint style="info" %}
La terminología de “mercado primario y secundario" se toma prestado de las finanzas tradicionales donde el mercado primario se refiere al ‘mercado emisor’ y el mercado secundario refiere a el ‘mercado de valores’ (por ejemplo, en ETFs).
{% endhint %}

## Interacción de mercados

Cada SAMM concentran la liquidez en rangos establecidos por el PAMM para los pares de reserva activo - moneda estable de Gyroscope. Esto garantiza pares altamente líquidos para entrar y salir de las monedas estables de Gyroscope. Los SAMMs son también independiente de otros: si el activo en par colapsa en un SAMM, entonces los pools restantes del SAMM pueden seguir funcionando, caso contrario con un típico pool de un AMM hoy en día. Los SAMMs formarán parte central de una red de pools interconectados que permitirán el enrutamiento eficiente de transacciones. Algunas bóvedas de reservas de Gyroscope desplegarán activos en pools que magnifiquen esta red, mientras otros AMM pools se conectarán con pares de activos en los SAMMs.

![](<../../../.gitbook/assets/SAMM and Reserve Pools Graphic.png>)

Una característica de este diseño es que induce un mecanismo de coordinación de la paridad, lo que fomenta alta liquidez alrededor de la paridad, mientras que reduce ataques especulativos y los efectos de estampidas bancarias con un corto-circuito en caso de ataques coordinados.
