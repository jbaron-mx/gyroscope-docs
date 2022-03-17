---
description: La intuición detrás del mecanismo algorítmico de estabilidad de precio
---

# Intuición económica

## Resumen

La reserva de Gyroscope está diseñada para servir como un portafolio todo-terreno, diversificando no sólo el riesgo de precio pero también de contraparte, de censura y regulatorio. Al hacerlo, mantiene las propuestas de valor originales de las finanzas decentralizadas (DeFi).

Destacar que la reserva no es gestionada por ningún tercero o custodio. Los activos son almacenados en contratos inteligentes públicos y sin-custodios.

Sin embargo, no existe portafolio de cripto-activos que pueda diversificar completamente estos riesgos y aún así podrían ocurrir shocks a los activos en reserva. Como tal, Gyroscope está explícitamente diseñado para desalentar ataques especulativos a la paridad en el caso de que tales shocks afecten la salud de la reserva. De forma predeterminada, se procura una reserva ligeramente mayor a 100% en un robusto arreglo de activos (la primera línea de defensa de la reserva todo-terreno). Se mantienen mecanismos adicionales en caso de shocks que afecten la reserva.

En tiempos de crisis, se pretende que el interés de los usuarios esté en esperar para redimir en lugar de vender en perdida. Si esperan, los usuarios podrán acceder a una tasa de redención más favorable. A su vez, esto hace que cualquier ataque especulativo sea menos rentable.

En el corazón de este diseño hay juego económico formal. La intuición es la siguiente:

> Usuarios forman creencias del valor fundamental de la moneda estable. Basadas en el valor de la reserva y que tan aceptada y utilizada es la moneda estable. Pero los usuarios también forman creencias sobre las creencias de otros participantes del mercado (y así sucesivamente). _**Gyroscope coordina estas creencias**_. Ya que el valor de la reserva es observable en-cadena, así como también las reglas que gobiernan cómo será utilizada, entonces los usuarios racionales implícitamente concuerdan si atacan o defienden la paridad ya que _**sólo ganan si forman mayoría**_.

Como resultado, con una reserva suficientemente grande y una aceptación suficiente de la moneda estable, el valor de la moneda estable será estable en $1 en un amplio rango de condiciones de mercado. Mientras la paridad podría romperse en situaciones extremas, por diseño la reserva es difícil de agotar en el corto a mediano plazo y, siempre que el ecosistema de criptomonedas se recupere, puede recuperarse eventualmente.
