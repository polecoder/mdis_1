# Ejercicio 3

## Consigna

¿De cuántas maneras diferentes puede un Rey, desplazarse desde la esquina inferior izquierda (a1) hasta la esquina superior derecha (h8) de un tablero de ajedrez, admitiendo únicamente movimientos hacia arriba o hacia la derecha (no se permite movimiento en diagonal)?

## Resolución

Observemos que para llegar a la esquina superior derecha (e8), necesitaríamos 14 movimientos, ya que no se admiten movimientos en diagonal, ni en direcciones contrarias al punto de llegada (es decir ni hacia abajo ni hacia la izquierda). Transformemos el problema a contar cuantas palabras de tamaño 14 puedo formar las letras $\{A, D\}$, A representando arriba y D representando derecha.

Observemos que:

$$
AAAAAAADDDDDDD \neq ADADADADADAD
$$

Esto nos indica que el orden nos da dos formas diferentes de resolver el problema, por lo que la respuesta nos la darán las permutaciones con repetición:

$$
\frac{14!}{7!7!}
$$

Donde: 14 es el número de letras que componene una solución, 7 es el número de símbolos "A" que tenemos, y lo mismo para las "D". Por esto divido dos veces por la cantidad de permutaciones de las "A" y las "D".
