# CLASE 8 - 25/01/2025

## Principio de inclusión-exclusión

### Demostración (principio de inclusión-exclusión)

Vamos a verificar que cada elemento $x\in U$ está contado la misma cantidad de veces en el lado izquierdo y el lado derecho de la igualdad deseada:

Fijado $x\in U$ se distinguen dos casos:

- Caso donde $x$ no cumple ninguna condición:

$$
\begin{align*}
    N(\overline{c_1}\cdots\overline{c_t}) &= N - S_1 + S_2 - S_3 + \ldots + (-1)^t S_n \\
    1 &= 1 - 0 + 0 - 0 + \ldots + (-1)^t0
\end{align*}
$$

- Veamos el caso interesante, cuando $x$ cumple alguna condición. Sea $p \geq 1$ el número de condiciones que cumple $x$

$$
\begin{align*}
    N(\overline{c_1}\cdots\overline{c_t}) &= N - S_1 + S_2 - S_3 + \ldots + (-1)^pS_p + \ldots + (-1)^t S_n \\
    0 &= 1 - p + C(p, 2) + C(p, 3) + \ldots + (-1)^pC(p,p) + 0 + \ldots + 0
\end{align*}
$$

Para entender la igualdad de abajo, veamos que:

- Para $N$ (la cantidad total de elementos), contamos a $x$ 1 vez
- Para $S_1$, lo estamos contando $p$ veces, ya que es el número de condiciones que cumple $x$
- Para $S_2$, lo estaremos contando $C(p, 2)$ veces, es decir, la cantidad de combinaciones de 2 condiciones entre las $p$ que cumple
- Así sucesivamente, hasta llegar a $S_p$ donde se ve que lo estaremos contando una sola vez. A partir de aquí no lo estaremos contando porque estaríamos contando elementos con $p+1$ condiciones cumplidas, cosa que $x$ no cumplen

Ahora podemos seguir con esa igualdad:

$$
0 = \sum_{k=0}^{p}(-1)^k C(p,k) = 0
$$

Sabemos que esto es 0 ya que lo probamos en alguna de las clases anteriores cuando hablamos sobre el teorema del binomio.

### Lema

Dados $n\in N, p\geq 1$, entre los números 1 y $n$ hay exactamente $\lfloor \frac{n}{p} \rfloor$ números divisibles por $p$

### Ejercicio

Cuántos enteros entre 1 y 100 no son divisibles por 2, 3 o 5?

Traduzcamos esto a un problema de inclusión-exclusión:

$U = {1, 2, \ldots, 100}$ y $N = 100$

- $c_1$: No ser divisible por 2
- $c_2$: No ser divisible por 3
- $c_3$: No ser divisible por 5

Usemos el lema para cálcular: 
- $N(c_1) = \lfloor \frac{100}{2} \rfloor = 50$
- $N(c_2) = \lfloor \frac{100}{3} \rfloor = 33$
- $N(c_3) = \lfloor \frac{100}{5} \rfloor = 20$
- $N(c_1c_2) = \lfloor \frac{100}{6} \rfloor = 16$
- $N(c_1c_3) = \lfloor \frac{100}{10} \rfloor = 10$
- $N(c_2c_3) = \lfloor \frac{100}{15} \rfloor = 6$
- $N(c_1c_2c_3) = \lfloor \frac{100}{30} \rfloor = 3$

Ahora veamos $S_1, S_2, S_3$:

- $S_1 = N(c_1) + N(c_2) + N(c_3) = 50 + 33 + 20 = 103$
- $S_2 = N(c_1c_2) + N(c_1c_3) + N(c_2c_3) = 16 + 10 + 6 = 32$
- $S_3 = N(c_1c_2c_3) = 3$

Entonces, por el principio de inclusión-exclusión:

$$
N(\overline{c_1}\overline{c_2}\overline{c_3}) = N - S_1 + S_2 - S_3 = 100 - 103 + 32 - 3 = 26
$$

Por lo tanto, hay 26 enteros entre 1 y 100 que no son divisibles por 2, 3 o 5.

### Ejercicio

Contar la cantidad de soluciones enteras del sistema:

$$
\begin{cases}
n_1 + n_2 + n_3 + n_4 = 18 \\
0 \leq n_i \leq 7 \text{ con } i = 1,2,3,4 \\
\end{cases}
$$

Este problema se puede traducir a un problema de inclusión-exclusión:

$U = \{(n_1, n_2, n_3, n_4) \in N^4 \text{ }  | \text{ } n_1 + n_2 + n_3 + n_4 = 18 \}$

$N = CR(4, 18) = C(21,18) = 1330$

Establezcamos las condiciones de una forma conveniente, para facilitar las cuentas:

- $c_1$: $n_1 \geq 8$
- $c_2$: $n_2 \geq 8$
- $c_3$: $n_3 \geq 8$
- $c_4$: $n_4 \geq 8$

Con esto, $N(\overline{c_1}\overline{c_2}\overline{c_3}\overline{c_4})$ es la cantidad de soluciones enteras del sistema inicial, ya que serán las que no cumple ninguna de las condiciones $c_i$, o sea $n_i$ será menor o igual a 7 para todo $i$.

Veamos cuánto vale cada $N(c_i)$, empezando con $N(c_1)$:

$$
n_1 + n_2 + n_3 + n_4 = 18 \text{ con } n_1 \geq 8 \\
n_1 + n_2 + n_3 + n_4 = 10
$$

Estos dos sistemas son equivalentes, por lo que $N(c_1) = CR(4, 10) = C(13, 10) = 286 $. De la misma forma, $N(c_2) = N(c_3) = N(c_4) = 286$

Ahora veamos $N(c_ic_j)$, empezando por $N(c_1c_2)$:

$$
n_1 + n_2 + n_3 + n_4 = 18 \text{ con } n_1 \geq 8, n_2 \geq 8 \\
n_1 + n_2 + n_3 + n_4 = 2
$$

Estos dos sistemas son equivalentes, por lo que $N(c_1c_2) = CR(4, 2) = C(5, 2) = 10 $. De la misma forma, $N(c_1c_3) = N(c_1c_4) = N(c_2c_3) = N(c_2c_4) = N(c_3c_4) = 10$

Finalmente, $N(c_ic_jc_k) = 0$ y $N(c_1c_2c_3c_4) = 0$, porque no hay soluciones a este problema cuando queremos igualar a un número negativo.