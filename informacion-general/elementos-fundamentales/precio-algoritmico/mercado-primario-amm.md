---
description: Emisión y redención de unidades de monedas estables
---

# Mercado primario AMM

## Resumen

Unidades de monedas estables pueden ser emitidas y redimidas en el mercado primario (PAMM).

No existe un emisor central. Los usuarios pueden emitir y redimir unidades de monedas estables directamente en el sistema sin-restricciones de Gyroscope. No existe una contraparte.

La estructura de el PAMM (es decir, las curvas de vinculación que determina los precios de cotización para emitir/redimir) es una función del coeficiente actual de la reserva y salidas de capital.

### Curva de redención estilizada del PAMM

Abajo de muestra la curva de redención estilizada del PAMM para diferentes coeficientes de reservas contra el ejemplo de una pool 50-50 de Uniswap.

![](<../../../.gitbook/assets/Stylized PAMM Redemption Curve v3.png>)

### Ejemplos y explicaciones detalladas

#### Redenciones con garantías cercanas al 100%

Si la moneda estable tiene un déficit de garantías y comienza a cotizar por debajo de la paridad, la curva de redención se establece cerca de $1 para facilitar buena liquidez alrededor de la paridad.

#### Redenciones con garantías muy debajo del 100%

Si constantes redenciones ocurren, es decir, la salida de capital se incrementa, la curva de redención se mueve eventualmente a la ‘fase de corto-circuito’. En este corto-circuito, la tasa de redención se reduce por debajo del coeficiente actual de la reserva, del cual las redenciones son siempre sostenibles.

En ese caso, la curva de vinculación del mercado de redención provee **cotizaciones de redención a la baja** como corto-circuito. El objetivo es desincentivar estampidas y ataques a la paridad de la moneda, permitiendo a los usuarios marcharse si así lo desean, pero recompensando a los usuarios que esperan a que la conmoción transitoria concluya.

Importantemente, incluso si los acreedores de monedas estables deciden marcharse, Gyroscope provee **motivos racionales para apostar que la moneda estable regresará a su precio objetivo**, conforme el precio de redención se recupera algorítmicamente hacia la paridad y las salidas de capital equilibran a cero o las reservas se recuperan (por ejemplo, mediante rendimientos).

El diseño del PAMM se especifica completamente, se caracteriza formalmente y se optimiza en nuestro documento técnico del PAMM, que será publicado pronto. Ver el [libro blanco](https://gyro.finance/pdfs/Gyroscope\_Lite\_Paper.pdf), secciones 3.1 (curva de emisión) y 3.4 (curva de redención) para detalles actualmente publicados.
