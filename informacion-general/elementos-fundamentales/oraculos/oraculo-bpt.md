---
description: Metodología e implementación del token Balancer Pool LP Token (BPT)
---

# Oráculo BPT

Para establecer los precios de los tokens LP, no es suficiente si simplemente sumamos la valuación de todos los activos en el pool ya que esto fácilmente manipulable. Usamos un procedimiento mas robusto para calcular el valor de los tokens Balancer LP.

Para dada una pool de Balancer conteniendo activos 1, ..., n se define lo siguiente:

$$
w_i = \text{weight of asset } i \\
r_i = \text{amount (in \# tokens) of asset } i \\
p_i = \text{price of asset } i \\
S = \text{total \# BPT tokens}
$$

El producto constante de una pool de Balancer es

$$
k = \prod_{i=1}^{n} r_i^{w_i}
$$

A destacar que las cantidades $$r_i$$ son fácilmente manipulables, pero el producto $$k$$ no lo es. Y conforme requerimos oráculos para cotizaciones de activos en otro lado, podemos suponer que los precios $$p_i$$ tampoco son fácilmente manipulables (los controles para protegerse contra esto se discutirán en otro lugar).

Para crear oráculos de BPT resistentes a manipulación, será suficiente expresar cotizaciones de tokens BPT en términos de variables resistentes a manipulación $$w_i, p_i, k, S$$.

El valor de portafolio del pool de Balancer puede ser calculado como

$$
\text{BPT total value} = k \prod_{i=1}^n \left( \frac{p_i}{w_i} \right)^{w_i}
$$

Entonces, a su vez, el precio de BPT puede ser calculado como
