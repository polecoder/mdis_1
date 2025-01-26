# Ejercicio 8

## Consigna

(a) ¿Cuántas formas hay de sentar 5 personas en 12 sillas puestas en línea?

(b) Ídem pero las personas no deben quedar sentadas en asientos contiguos.

## Resolución (parte a)

La solución para esta parte es simplemente:

$$
C(12,5)
$$

Esto porque puedo pensar las sillas como un conjunto $S=\{s_1, s_2, \cdots, s_{12} \}$ y aquí debo elegir 5. Si importa el orden en que elegimos las sillas, la respuesta sería:

$$
A(12,5)
$$

## Resolución (parte b)

En esta parte veamos de cambiar el problema a algo más conocido. Pensemos en que para que las personas no se sienten en sillas contiguas, tiene que haber al menos una silla entre dos personas. Llamemos $x_i$ al espacio que hay entre dos personas de la siguiente forma:

- $x_0$: El espacio desde la primer silla hasta la primer persona, puede ser 0

- $x_1$: El espacio entre la primer persona hasta la segunda, $x_1 \geq 1$ porque las sillas no pueden ser contiguas

- $x_2$: El espacio entre la segunda persona hasta la tercera, $x_2 \geq 1$ porque las sillas no pueden ser contiguas

- $x_3$: El espacio entre la tercer persona hasta la cuarta, $x_3 \geq 1$ porque las sillas no pueden ser contiguas

- $x_4$: El espacio entre la cuarta persona hasta la quinta, $x_4 \geq 1$ porque las sillas no pueden ser contiguas

- $x_5$: El espacio entre la quinta persona hasta la última silla, puede ser 0

Con esta información, y además sabiendo que los espacios tienen que sumar 7, podemos decir que:

$$
x_0 + x_1 + x_2 + x_3 + x_4 + x_5 = 7 \text{ con } x_1 \geq 1, x_2 \geq 1, x_3 \geq 1, x_4 \geq 1
$$

Esto es lo mismo que:

$$
y_0 + y_1 + y_2 + y_3 + y_4 + y_5 = 3
$$

Pero ahora sin restricciones sobre las variables. La respuesta a este problema es:

$$
CR(6, 3) = C(8, 3) = \frac{8!}{3!5!} = 8*7 = 56
$$
