---
description: >-
  Mecanismos adicionales que complementan los mecanismos primarios de
  estabilidad
---

# Mecanismos complementarios de estabilidad

Gyroscope también incorpora varios mecanismos complementarios de estabilidad, que trabajan en conjunto con los mecanismos principales de Gyroscope para fortalecer la estabilidad.

### Integración con préstamos apalancados

Similar al Módulo de Estabilidad de Paridad de Maker (PSM), el mecanismo principal de Gyroscope permite el intercambio de la moneda estable con \~$1 en valor de activos. Sin embargo, a diferencia del diseño de Maker lo hace mientras (1) permite diversificar todos los riesgos en la reserva, (2) no depende completamente de monedas estables custodiadas, y (3) preservando cierta resiliencia y flexibilidad para sobrevivir incluso si el valor de la reserva fluctúa.

El mecanismo de préstamo apalancado podría entonces otorgar otra manera en el cual los participantes en Gyroscope puedan soportar racionalmente la paridad si la reserva tiene insuficientes garantías. En particular, si el precio de GYD alguna vez cae significativamente por debajo de $1 (por ejemplo, si hay un colapso importante de las criptomonedas), entonces los acreedores apalancados serán capaces de cerrar sus posiciones apalancadas con descuento. Esto tiene el efecto adicional de reducir la oferta de GYD y retornar el precio de GYD hacia $1.

### Acciones para recapitalizar

La reserva puede ser recapitalizada mediante la subasta de tokens de gobernanza o futuros rendimientos de la reserva. Se incentiva la gobernanza de Gyroscope a hacer esto en momentos oportunos en lugar de actuar únicamente como respaldo de último recurso durante una crisis. Si los tiempos son buenos y la valuación del token de gobernanza es muy alta, gobernadores son incentivados a subastar anticipadamente nuevos tokens para impulsar la reserva. Ver _titulización de la reserva_ en el [libro blanco](https://gyro.finance/pdfs/Gyroscope\_Lite\_Paper.pdf).
