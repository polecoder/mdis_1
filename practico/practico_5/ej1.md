# Ejercio 1

## Consigna

En cada caso hallar el término $a_{100}$:

(a) $a_{n+1} − 3a_n = 0, \forall n\in\mathbb{N}, \text{ con }a_{50} = 2\times 3^{-8}$

(b) $a_{n+2} + 4a_n = 0, \forall n\in\mathbb{N}, \text{ con } a0 = a1 = 1$ (sugerencia: use el cambio de variable $b_n := a_{2n}$).

## Resolución (parte a)

Esta es una ecuación lineal de primer orden homogénea. La solución general es de la forma $a_n = \alpha \times 3^n$. Para hallar $\alpha$ usamos la condición inicial $a_{50} = 2\cdot 3^{-8}$:

$$
\begin{align*}
a_{50} &= \alpha \times 3^{50} = 2 \times 3^{-8} \\
&\Rightarrow \alpha = 2 \times \frac{3^{-8}}{3^{50}} = 2 \times 3^{-58}
\end{align*}
$$

Por lo tanto, la solución es $a_n = 2 \times 3^{-58} \times 3^n = 2 \times 3^{n-58}$.

Ahora evaluemos $a_{100}$:

$$
a_{100} = 2 \times 3^{100-58} = 2 \times 3^{42}
$$

## Resolución (parte b)

Acá podemos usar el cambio de variable sugerido para simplificar la ecuación. Si definimos $b_n := a_{2n}$, entonces la ecuación se convierte en:

$$
b_{n+1} + 4b_n = 0
$$

No tenemos problemas en hacerlo de esta forma porque podremos cálcular $a_{100}$ a partir de $b_{50}$.

La solución general de esta ecuación es de la forma $b_n = \beta \times (-4)^n$. Para hallar $\beta$ usamos la condición inicial $b_0 = a_0 = 1$:

$$
b_0 = \beta \times (-4)^0 = \beta = 1
$$

Entonces la solución general de $b_n$ es la siguiente:

$$
b_n = 1 \times (-4)^n = (-4)^n \quad \forall n\in\mathbb{N}
$$

Buscamos $b_{50} = a_{100}$:

$$b_{50} = (-4)^{50}$$