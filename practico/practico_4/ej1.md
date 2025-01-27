# Ejercicio 1

## Consigna

(a) ¿Cuántos números naturales entre 1 y 105 inclusive no son múltiplos de 3, 5 ni 7?

(b) ¿Cuántos números naturales entre 1 y 1155 inclusive son múltiplos de 3 pero no de 5, 7 ni 11?

## Resolución (parte a)

Utilicemos el principio de inclusión-exclusión:

$U = \{1, 2, \ldots, 105\}$, $N = 105$

Ahora establezcamos las condiciones:

- $c_1$: múltiplos de 3
- $c_2$: múltiplos de 5
- $c_3$: múltiplos de 7

Utilizando el lema visto en la clase 8 del teórico, calculemos N para cada condición:

- $N(c_1) = \lfloor \frac{105}{3} \rfloor = 35$
- $N(c_2) = \lfloor \frac{105}{5} \rfloor = 21$
- $N(c_3) = \lfloor \frac{105}{7} \rfloor = 15$

Ahora calculemos las intersecciones:

- $N(c_1 c_2) = \lfloor \frac{105}{15} \rfloor = 7$
- $N(c_1 c_3) = \lfloor \frac{105}{21} \rfloor = 5$
- $N(c_2 c_3) = \lfloor \frac{105}{35} \rfloor = 3$
- $N(c_1 c_2 c_3) = \lfloor \frac{105}{105} \rfloor = 1$

Cálculemos $S_1, S_2, S_3$:

- $S_1 = N(c_1) + N(c_2) + N(c_3) = 35 + 21 + 15 = 71$

- $S_2 = N(c_1 c_2) + N(c_1 c_3) + N(c_2 c_3) = 7 + 5 + 3 = 15$

- $S_3 = N(c_1 c_2 c_3) = 1$

Entonces planteamos el principio de inclusión-exclusión:

$$
\begin{align*}
N(\overline{c_1}\overline{c_2}\overline{c_3}) &= N - S_1 + S_2 - S_3 \\
&= 105 - 71 + 15 - 1 = 48
\end{align*}
$$

## Resolución (parte b)

Utilicemos el principio de inclusión-exclusión:

$U = \{n\in N, n \leq 1155 \text{ }|\text{ } n \text{ es múltiplo de 3}\}$, $N = \lfloor \frac{1155}{3} \rfloor = 385$

Ahora establezcamos las condiciones:

- $c_1$: múltiplos de 5
- $c_2$: múltiplos de 7
- $c_3$: múltiplos de 11

Utilizando el lema visto en la clase 8 del teórico, calculemos N para cada condición:

- $N(c_1) = \lfloor \frac{1155}{3\times 5} \rfloor = \frac{1155}{15} = 77$
- $N(c_2) = \lfloor \frac{1155}{3\times 7} \rfloor = \frac{1155}{21} = 55$
- $N(c_3) = \lfloor \frac{1155}{3\times 11} \rfloor = \frac{1155}{33} = 35$

Ahora calculemos las intersecciones:

- $N(c_1 c_2) = \lfloor \frac{1155}{3\times 5\times 7} \rfloor = \frac{1155}{105} = 11$
- $N(c_1 c_3) = \lfloor \frac{1155}{3\times 5\times 11} \rfloor = \frac{1155}{165} = 7$
- $N(c_2 c_3) = \lfloor \frac{1155}{3\times 7\times 11} \rfloor = \frac{1155}{231} = 5$
- $N(c_1 c_2 c_3) = \lfloor \frac{1155}{3\times 5\times 7\times 11} \rfloor = \frac{1155}{1155} = 1$

Observemos que esta vez tenemos que multiplicar el denominador, ya que estamos buscando múltiplos de 3.

Cálculemos $S_1, S_2, S_3$:

- $S_1 = N(c_1) + N(c_2) + N(c_3) = 77 + 55 + 35 = 167$
- $S_2 = N(c_1 c_2) + N(c_1 c_3) + N(c_2 c_3) = 11 + 7 + 5 = 23$
- $S_3 = N(c_1 c_2 c_3) = 1$

Entonces planteamos el principio de inclusión-exclusión:

$$
\begin{align*}
N(\overline{c_1}\overline{c_2}\overline{c_3}) &= N - S_1 + S_2 - S_3 \\
&= 385 - 167 + 23 - 1 = 240
\end{align*}
$$
