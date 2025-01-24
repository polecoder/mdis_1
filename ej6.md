# Ejercicio 6

## Consigna

Exprese los resultados de las siguientes preguntas como una combinación con repetición.

(a) ¿Cuántas fichas diferentes hay en el juego popular del dominó?

(b) ¿Cuántos resultados diferentes se pueden obtener al arrojar simultáneamente 3 dados idénticos?

## Resolución (parte a)

En el dominó las fichas están compuestas por dos selecciones diferentes de un número del 0 al 6.

**Observación**: es importante entender que la ficha 2/1 es la misma ficha que 1/2

Podemos pensar el problema cómo elegir 2 números entre 7 posibles usando el esquema de las $x$ y los separadores $|$, esto tendrá en cuenta la observación, ya que 2/1 será tendrá la misma representación que 1/2 en este esquema, veámoslo con además otros ejemplos:

$$
|x|x||||
$$(1,2)

$$
||x||||x
$$(2,6)

$$
x|||x|||
$$(0,3)

$$
||xx||||
$$(2,2)

Este problema se traduce a reordenar 2 pelotas indistinguibles en 7 cajitas diferentes, entonces la respuesta es:

$$
CR(7, 2) = C(8, 2)
$$

$$
\frac{8!}{6!2!} = \frac{8*7}{2} = 4*7 = 28 
$$

**Recordatorio**:

$$
CR(n, k) = C(n+k-1, k)
$$

## Resolución (parte b)

Esta parte es un poco diferente ya que un dado común tiene 6 caras con números entre: $\{1,2,3,4,5,6\}$, aunque la forma de resolverlo es exactamente la misma, utilizando tres $x$ en vez de solo dos.

Tengamos en cuenta que ahora son 6 valores posibles, por lo tanto 5 separadores. Veamos algunos ejemplos:

$$
x|x|x|||
$$(1,2,3)

$$
x||x||x|
$$(1,3,5)

$$
|||xx||x
$$(4,4,6)

Entonces la respuesta es:

$$
CR(6,3)
$$

Por completitud veamos cuando vale este número:

$$
CR(6,3) = C(8,3) = \frac{8!}{5!3!} = 8*7 = 56
$$