# CLASE 7 - 21/01/2024

## Principio de inclusión y exclusión

### Marco de trabajo

Se consideran:

- Un conjunto finito $U$ con $N$ elementos
- Condiciones $c_1, \ldots, c_t$ satisfechas por algunos elementos de $U$

Se escribe:

- $N(c_i)$ la cantidad de elementos de $U$ que satisfacen la condición $c_i$
- $N(c_i c_j)$ la cantidad de elementos de $U$ que satisfacen las condiciones $c_i$ y $c_j$ (con $ij$ distintos)
- $\ldots$
- $N(c_i c_j \ldots c_t)$ la cantidad de elementos de $U$ que cumplen todas las condiciones.

También se escribe:

- $N(\overline{c_i} \overline{c_j} \ldots \overline{c_t})$ la cantidad de elementos de $U$ que no cumple ninguna condición

### Teorema (inclusión-exclusión)

Dado un conjunto finito $U$ de $N$ elementos y $t \geq 1$ condiciones $c_1, \ldots, c_t$ sobre los elementos de $U$, tenemos que :

$$
\begin{align*}
N(\overline{c_i} \overline{c_j} \ldots \overline{c_t}) = N &- (N(c_1) + N(c_2) + \ldots + N(c_t)) \\
&+ (N(c_1c_2) + N(c_1c_3) + \ldots + N(c_{t-1} c_t)) \\
&- (N(c_1c_2c_3) + \ldots + N(c_{t-2}c_{t-1}c_t)) \\
&+ \ldots \\
&+ (-1)^t(N(c_1c_2\ldots c_t))
\end{align*}
$$

Esto es equivalente a:

$$
\begin{align*}
N(\overline{c_i} \overline{c_j} \ldots \overline{c_t}) = N &- \sum_{1\leq i \leq t} N(c_i) \\
&+ \sum_{1\leq i_1, i_2 \leq t} N(c_{i_1}c_{i_2}) \\
&- \sum_{1\leq i_1, i_2, i_3 \leq t} N(c_{i_1}c_{i_2}c_{i_3}) \\
&+ \ldots \\
&+ (-1)^t(N(c_1c_2\ldots c_t))
\end{align*}
$$

Llamando a cada sumatoria $S_1, S_2, \ldots, S_t$, reducimos a:

$$
N - S_1 + S_2 - S_3 + \ldots + (-1)^tS_t \\
\text{con } S_k = \sum_{1\leq i_1, \ldots, i_k \leq t} N(c_{i_1} \ldots c_{i_k})
$$

Esto concluye el teorema. La demostración se encuentra en la clase que viene.