# Ejercicio 2

## Consigna

Resolver las relaciones de recurrencia:

(a) $a_{n+2} = 5a_{n+1} - 6a_n$, con $a_0 = 1, a_1 = 3$

(b) $b_{n+2} - 6b_{n+1} + 9b_n = 0$, con $b_0 = 5, b_1=27$

## Resolución (parte a)

Pasemos todo para un lado para ver el polinomio característico:

$$a_{n+2} - 5a_{n+1} + 6a_n = 0$$

Entonces tenemos que hallar las raíces de:

$$P(x) = x^2 - 5x + 6$$

$$
\begin{align*}
x &= \frac{5 \pm \sqrt{25 - 24}}{2\times1} \\
&= \frac{5 \pm 1}{2}
\end{align*}
$$

Entonces:

$$
r_1 = 3; \quad r_2 = 2
$$

Con esto establecemos la solución general de $a_n$ como:

$$
a_n = \alpha \cdot 3^n + \beta \cdot 2^n
$$

Ahora usemos las condiciones iniciales para determinar la solución particular:

$$
\begin{cases}
a_0 = \alpha + \beta = 1 \Rightarrow \beta = 1-\alpha \\
a_1 = \alpha \cdot 3 + \beta \cdot 2 = 3
\end{cases}
$$

Sigamos el segundo caso:

$$
\begin{align*}
\alpha \cdot 3 + \beta \cdot 2  = 3 \\
\alpha \cdot 3 + (1-\alpha)\cdot 2 = 3 \\
\alpha + 2 = 3 \\
&\Rightarrow\alpha = 1 \\
&\Rightarrow \beta = 1 - 1 = 0
\end{align*}
$$

Entonces la solución particular es:

$$a_n = 3^n \quad \forall n \in \mathbb{N}$$

## Resolución (parte b)

Nuevamente veamos el polinomio caractéristico:

$$P(x) = x^2 - 6x + 9 = 0$$

Hallemos las raíces:

$$
\begin{align*}
x &= \frac{6 \pm \sqrt{36 - 36}}{2\cdot1} \\
&= 3
\end{align*}
$$

Tenemos raíz doble en $x=3$, por lo que la solución general es:

$$b_n = \alpha\cdot 3^n + \beta\cdot n 3^n$$

Ahora usamos las condiciones iniciales para encontrar la solución particular:

$$
\begin{cases}
b_0 = 5 = \alpha + \beta\cdot 0 \Rightarrow \alpha = 5 \\
b_1 = 27 = \alpha \cdot 3 + \beta \cdot 3 = 3\beta + 15 
\end{cases}
$$

Siguiendo la segunda ecuación:

$$\beta = \frac{27-15}{3} = 4$$

En conclusión, la solución particular es:

$$b_n = 5\cdot3^n + 4\cdot n3^n $$