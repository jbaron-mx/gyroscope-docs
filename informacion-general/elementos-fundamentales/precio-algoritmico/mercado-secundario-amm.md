---
description: Concentrando liquidez dentro la banda de precios establecida por el PAMM
---

# Mercado secundario AMM

## Resumen

En Gyroscope, el mercado secundario AMM concentra la liquidez dentro una banda que da seguimiento a los precios cotizados de emisión y redención establecidos por el mercado primario AMM.

Con reservas saludables, la liquidez del SAMM se concentra dentro de una banda estrecha. Si ocurre un shock a la reserva y el PAMM establece nuevos precios de redención (como fue descrito aquí) esta banda de precios se extenderá. Notablemente, la liquidez del SAMM:

* SAMMs son **redundantes** (es decir, proveen diferentes rutas de entrada/salida de GYD) y
* SAMMs son **independientes** de otros (ejemplo, si el activo en par colapsa, los pools restantes del SAMM aún pueden funcionar, caso contrario con un pool típico de Curve).

### Curva de redención estilizada del SAMM

Abajo de muestra la curva de redención estilizada del SAMM contra el ejemplo de una pool 50-50 de Uniswap.

![Los SAMMs concentran liquidez dentro una banda cotizada por el PAMM (aquí se muestra una configuración de shock donde la estructura del PAMM cambia).](https://2063019688-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MU527HCtxlYaQoNazhF%2Fuploads%2FC3g43sqN1FurvpJBThOL%2FGraph%206%20v2.png?alt=media\&token=71aa066b-8a6f-43a4-a5f2-737712ac9e07)

Los diseños del SAMM incorporan formas de curva de vinculación optimizadas y mecanismos de reserva virtual. Estos se especifican completamente, se caracterizan formalmente y se optimizan en nuestro documento técnico del SAMM, que será publicado pronto. Ver el libro blanco, sección 3.5 para más detalles.
