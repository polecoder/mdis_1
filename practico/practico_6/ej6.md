# Ejercicio 6

## Consigna

Determinar la cantidad de relaciones R que se pueden definir sobre el conjunto $A = \{a, b, c, d\}$que verifican simultáneamente las 3 condiciones siguientes: $R$ es simétrica; $(a, b) \in R$; $(c, c) \in R$.

## Resolución

Veamos todos los pares ordenados posibles en $A$ para definir una relación con los tres datos que nos proporcionan:

$$
\begin{matrix}
(a, a) & (a, b) & (a, c) & (a, d) \\
(b, a) & (b, b) & (b, c) & (b, d) \\
(c, a) & (c, b) & (c, c) & (c, d) \\
(d, a) & (d, b) & (d, c) & (d, d) \\
\end{matrix}
$$

Sabemos que:

- $(a, b) \in R$, por lo que: $(b, a) \in R$ por simetría.
- $(c, c) \in R$.

Con estos datos, y sumando que $R$ es simétrica, tenemos que contar las posibilidades con los pares del tríangulo superior izquierdo de la matriz, ya que el resto se deduce por simetría.

Entonces, la cantidad de relaciones posibles es $2^8 = 256$.
