# Ejercicio 2

## Consigna

Se tira un dado 6 veces. Calcular la cantidad de formas en que podemos obtener un número múltiplo de 18 como suma de las 6 tiradas del dado. Tomar en cuenta el orden de los valores obtenidos en el dado.
Por ejemplo, los resultados en orden (6, 6, 2, 2, 1, 1) y (6, 2, 6, 2, 1, 1) cuentan a favor como casos diferentes.

## Resolución

Primero tenemos que traducir el problema a algo más conocido. Podemos empezar con dos casos:

- $x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 18$ con $1 \leq x_i \leq 6$

- $x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 36$ con $1 \leq x_i \leq 6$

Desarrollando un poquito más ambos casos llegamos a:

- $x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 12$ con $x_i \leq 5$

- $x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 30$ con $x_i \leq 5$ 

Ahora si, podemos plantear el principio de inclusión-exclusión para resolver el problema. Partamos por el caso 1:

El universo son las soluciones al problema:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 12 \text{ (sin restricciones)}
$$

Entonces $N = CR(6, 12) = C(17, 12) = \frac{17*16*15*14*13}{5*4*3*2*1} = 17*2*14*13 = 6188$

Para definir las condiciones, pensemos que queremos obtener los $x_i \leq 5$.

- $c_1$: $x_1 \geq 6$
- $c_2$: $x_2 \geq 6$
- $c_3$: $x_3 \geq 6$
- $c_4$: $x_4 \geq 6$
- $c_5$: $x_5 \geq 6$
- $c_6$: $x_6 \geq 6$

Cálculemos $N(c_i)$ teniendo en cuenta que es equivalente a la solución de:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 6
$$

Entonces $N(c_i) = CR(6, 6) = C(11, 6) = \frac{11*10*9*8*7}{5*4*3*2*1} = 11*3*2*7 = 462$

Ahora calculemos $N(c_i c_j)$:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 = 0
$$

Es trivial ver que hay una sola solución, entonces $N(c_i c_j) = 1$

A partir de acá, sabemos que ninguna combinación de 3 o más condiciones va a tener solución.

Calculemos $S_1, S_2$:

- $S_1 = N(c_1) + N(c_2) + N(c_3) + N(c_4) + N(c_5) + N(c_6) = 6*462 = 2772$

- $S_2 = C(6, 2)*1 = 15$

Con esto planteemos el principio de inclusión-exclusión:

$$
N(\overline{c_1}\overline{c_2}\overline{c_3}\overline{c_4}\overline{c_5}\overline{c_6})= N - S_1 + S_2 = 6188 - 2772 + 15 = 3421
$$

Completemos observando que la solución al segundo problema es trivial. Solo existe una forma de obtener 36 con 6 dados. Entonces la solución al problema es: $3421 + 1 = 3422$