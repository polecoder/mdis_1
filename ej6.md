# Ejercicio 6

## Consigna

Hallar la cantidad de permutaciones de los dígitos de 123456789 tales que:

(a) Ningún dígito está en su posición original.

(b) Los dígitos pares no están en su posición original.

(c) Los dígitos pares no están en su posición original y los primeros cuatro dígitos son precisamente 1,
2, 3 y 4, en algún orden.

## Resolución (parte a)

Esto es exactamente un desarreglo de tamaño 9, por lo que la cantidad de permutaciones que cumplen con la condición es $D(9)$.

$$
\begin{align*}
D(9) &= 9! \sum_{k=0}^{9} (-1)^k \frac{1}{k!} \\
&= 9! \left(1 - \frac{1}{1!} + \frac{1}{2!} - \frac{1}{3!} + \ldots + (-1)^9 \frac{1}{9!}\right)
\end{align*}
$$

## Resolución (parte b)

Acá podemos plantear el principio de inclusión-exclusión:

El universo es el conjunto de permutaciones de los dígitos de 123456789, por lo que $N=9!$

Definimos las condiciones $c_i$ como "el dígito $2i$ está en su posición original".

Entonces, $N(c_i) = 8!$ para todo $i$.
Seguimos el mismo razonamiento para:

- $N(c_i c_j) = 7!$ para todo $i \neq j$
- $N(c_i c_j c_k) = 6!$ para todo $i \neq j \neq k$
- $N(c_1 c_2 c_3 c_4) = 5!$

Cálculemos $S_1,S_2, S_3,S_4$:

- $S_1 = 4\times 8!$
- $S_2 = 6\times 7!$
- $S_3 = 4\times 6!$
- $S_4 = 5!$

Entonces, la cantidad de permutaciones que cumplen con la condición es:

$$
\begin{align*}
N - S_1 + S_2 - S_3 + S_4 &= 9! - 4\times 8! + 6\times 7! - 4\times 6! + 5! \\
&= 229080
\end{align*}
$$

## Resolución (parte c)

Para esta parte, usaremos la regla del producto, mezclado con el principio de inclusión-exclusión:

1. Hallar la cantidad de permutaciones de 1234 que no dejan ningún dígito par en su posición inicial
2. Hallar la cantidad de permutaciones de 56789 que no dejan ningún dígito par en su posición inicial

Luego, multiplicamos ambos resultados.

### Parte 1

Aquí aplicamos el principio de inclusión-exclusión:

El universo son todas las permutaciones de 1234, por lo que $N=4!$

Definimos las condiciones $c_i$ como "el dígito $2i$ está en su posición original".

Entonces, $N(c_i) = 3!$ para todo $i$. Seguimos el mismo razonamiento para: $N(c_1 c_2) = 2!$

Entonces el resultado de esta parte es:

$$
\begin{align*}
N - S_1 + S_2 &= 4! - 2\times 3! + 2! \\
&= 14
\end{align*}
$$

### Parte 2

El universo son todas las permutaciones de 56789, por lo que $N=5!$

Definimos las condiciones $c_i$ como "el dígito $2i + 4$ está en su posición original".

Entonces, $N(c_i) = 4!$ para todo $i$. Seguimos el mismo razonamiento para: $N(c_1 c_2) = 3!$

Entonces el resultado de esta parte es:

$$
\begin{align*}
N - S_1 + S_2 - S_3 &= 5! - 2\times 4! + 3! \\
&= 78
\end{align*}
$$

### Resultado

Multiplicamos ambos resultados:

$$
14 \times 78 = 1092
$$