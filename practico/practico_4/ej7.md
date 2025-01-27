# Ejercicio 7

## Consigna

¿ De cuántas formas se puede factorizar el número $2310 = 2 \times 3 \times 5 \times 7 \times 11$ como producto de 2 factores positivos mayores que 1? ¿Y como producto de 3 factores positivos mayores que 1? En ambos casos el orden de los factores no importa.

## Resolución

Pensemos en el primer caso por fuerza bruta. Si queremos factorizar $2310$ en dos factores, podemos hacerlo de la siguiente forma:

**1 primo + 4 primos**
- $2310 = 2 \times 1155$
- $2310 = 3 \times 770$
- $2310 = 5 \times 462$
- $2310 = 7 \times 330$
- $2310 = 11 \times 210$

Esto es igual a $C(5, 1) = 5$

**2 primos + 3 primos**
- $2310 = 2 \times 3 \times 385$
- $2310 = 2 \times 5 \times 231$
- $2310 = 2 \times 7 \times 165$
- $2310 = 2 \times 11 \times 105$
- $2310 = 3 \times 5 \times 154$
- $2310 = 3 \times 7 \times 110$
- $2310 = 3 \times 11 \times 70$
- $2310 = 5 \times 7 \times 66$
- $2310 = 5 \times 11 \times 42$
- $2310 = 7 \times 11 \times 30$

Esto es igual a $C(5, 2) = 10$

Cómo no importa el orden, la respuesta es que hay 15 formas de factorizar $2310$ en 2 factores.

Veamos ahora como hacer la parte de 3 factores, para esto, veamos que la respuesta es equivalente al siguiente problema:

De cuántas formas puedo crear una función sobreyectiva entre $A = \{2, 3, 5, 7, 11\}$ y $B = \{x_1, x_2, x_3\}$? Dónde $x_1, x_2, x_3$ son los tres factores.

La respuesta es $Sob(5,3)$, pero en este caso, no debemos distinguir entre $x_1, x_2, x_3$ por lo que es $S(5,3)$.

$$
\begin{align*}
Sob(5,3) &= \sum_{k=0}^{3}(-1)^k C(n,k)(n-k)^5 \\
&= \binom{3}{0} 3^5 - \binom{3}{1} 2^5 + \binom{3}{2}1^5 - \binom{3}{3}0^5 \\
&= 150 \\
\end{align*}
$$

Ahora debemos dividir por $3!$ para obtener $S(5,3)$, que es el resultado de esta parte:

$$
S(5,3) = \frac{150}{6} = 25
$$