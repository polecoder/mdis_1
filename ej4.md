# Ejercicio 4

## Consigna

¿Cuántos enteros positivos entre 1 y 9.999.999 inclusive cumplen que la suma de sus dígitos
es igual a 31?

## Resolución

Veamos que podemos plantear la siguiente ecuación:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 + x_7 = 31\\ 
\text{ con } x_i \leq 9
$$

Esto contempla todas las posibilidades, incluidos números con menos de 7 dígitos, ya que los dígitos faltantes serían 0.

Este es un problema conocido, planteemos el principio de inclusión-exclusión:

El universo son las soluciones al problema:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 + x_7 = 31 \text{ (sin restricciones)}
$$

Entonces $N = CR(7, 31) = C(37, 31)$

Para definir las condiciones, pensemos que queremos obtener los $x_i \leq 9$.

- $c_1$: $x_1 \geq 10$
- $c_2$: $x_2 \geq 10$
- $c_3$: $x_3 \geq 10$
- $c_4$: $x_4 \geq 10$
- $c_5$: $x_5 \geq 10$
- $c_6$: $x_6 \geq 10$
- $c_7$: $x_7 \geq 10$

Cálculemos $N(c_i)$ teniendo en cuenta que es equivalente a la solución de:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 + x_7 = 21
$$

Entonces $N(c_i) = CR(7, 21) = C(27, 21)$

Ahora calculemos $N(c_i c_j)$:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 + x_7 = 11
$$

Entonces $N(c_i c_j) = CR(7, 11) = C(17, 11)$

Ahora veamos $N(c_i c_j c_k)$:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 + x_7 = 1
$$

Entonces $N(c_i c_j c_k) = CR(7, 1) = C(7, 1) = 7$

A partir de acá, sabemos que ninguna combinación de 4 o más condiciones va a tener solución.

Calculemos $S_1, S_2, S_3$:

- $S_1 = C(7,1) * C(27,21) = 7 * C(27,21)$
- $S_2 = C(7,2) * C(17,11) = 21 * C(17,11)$
- $S_3 = C(7,3) * 7 = 35 * 7 = 245$

Con esto planteemos el principio de inclusión-exclusión:

$$
\begin{align*}
N(\overline{c_1}\overline{c_2}\overline{c_3}\overline{c_4}\overline{c_5}\overline{c_6}\overline{c_7}) &= N - S_1 + S_2 - S_3 \\
&= C(37,31) - 7 * C(27,21) + 21 * C(17,11) - 245
\end{align*}
$$

Esto resuelve el ejercicio
