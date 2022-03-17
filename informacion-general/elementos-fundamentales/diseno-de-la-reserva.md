---
description: Estratificando los activos en reserva para un diseño resiliente
---

# Diseño de la reserva

## Filosofía del diseño

Las reservas de Gyroscope han sido diseñadas para maximizar la resiliencia del sistema. Para ese objetivo, el riesgo debe ser 'estratificado' o aislado. Los problemas que ocurran en un sistema no deben permear hacia otros sistemas conectados.

{% hint style="info" %}
Por ejemplo, las posiciones LP en el pool Y de Curve se expone a riesgos compuestos de USDT, Dai, USDC, TUSD, Compound, Aave y Curve. En el diseño de un pool _AMM_ de Curve, si uno de esos componentes llegara a fallar, el valor total del pool se iría a cero.

Esto es comúnmente referido cómo 'riesgo de componibilidad' o también 'riesgo de contagio'.
{% endhint %}

## Implementación

De esta manera, la reserva de Gyroscope está separada en bóvedas en el nivel base (triángulos en la figura posterior) con riesgos contenidos. Hay pocos riesgos traslapados entre bóvedas. De forma que el colapso de una bóveda individual no tiene efecto en el resto de las bóvedas.

Si alguna bóveda fuera a colapsar (si un triángulo es removido de la figura posterior), el sistema de Gyroscope podría mantenerse estable en $1 mediante la vinculación algorítmica del precio respaldada por las reservas no afectadas (descritas aquí). Después del colapso de una bóveda, las reservas de Gyroscope pueden recuperarse en su totalidad mediante rendimientos generados por los activos en reserva de las bóvedas restantes. Esta resiliencia, es decir, la habilidad de Gyroscope de mantener su funcionalidad incluso si partes del sistema colapsan y la habilidad de recuperarse son elementos clave del diseño de Gyroscope.

Abajo se muestra una representación gráfica de la configuración de reservas de Gyroscope.

![Gyroscope estratifica riesgos de componibilidad. El colapso de una bóveda individual (triángulos) no permea al resto.](https://2063019688-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MU527HCtxlYaQoNazhF%2Fuploads%2FVsLqI7lD76gKFaQYklY6%2FVaults%20Graphic%20v2.png?alt=media\&token=4795d72e-d265-464b-b6f5-1d7dbe4c1e56)
