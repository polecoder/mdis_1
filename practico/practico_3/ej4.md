# Ejercicio 4

## Consigna

Determine cuántas funciones $f: \{1, 2, \cdots, 10\} \rightarrow \{1, 2, 3, 4\}$ verifican que todo elemento del codominio $i \in \{1, 2, 3, 4\}$ tiene exactamente $i$ preimágenes.

## Resolución

Antes de empezar, para clarificar la consigna, estamos buscando las funciones $f$ que cumplan que cada elemento $i \in \{1, 2, 3, 4\}$ tenga exactamente $i$ preimágenes. Esto significa que 1 deberá tener 1 preimagen, 2 deberá tener 2 preimágenes y así sucesivamente.

Sabemos que para ser función, cada elemento del dominio $\{1, 2, \cdots, 10\}$ solo puede tener UNA única imagen asociada. Puedo establecer una regla del producto seleccionando las preimágenes de cada elemento $i$, entre paréntesis el valor de $i$ de cada caso:

$$
C(10, 1)
$$(1)

$$
C(9, 2)
$$(2)

$$
C(7, 3)
$$(3)

$$
C(4, 4)
$$(4)

Sumando lo obtenido vemos que el resultado es:


$$
C(10, 1)*C(9, 2)*C(7, 3)*C(4, 4)
$$


$$
\frac{10!}{9!1!} * \frac{9!}{7!2!} * \frac{7!}{4!3!} * 1
$$


$$
10 * 9*4 * 7*5 = 12600
$$
