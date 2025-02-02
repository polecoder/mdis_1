# Ejercicio 2

## Consigna

Hallar la cantidad de relaciones de orden en $\{1, 2, 3, 4\}$ tales que $1 > 2 > 3$.

## Resolución

Veamos como sería el diagrama de Hasse en general para las condiciones dadas:

```mermaid
graph TD
    1((1))
    2((2))
    3((3))

    1 --- 2
    2 --- 3
```

Esta cadena estará presente en todas las relaciones de orden que encontremos, veamos las formas posibles de agregar el 4 con más diagramas de Hasse:

### CASO 1

```mermaid
graph TD
    1((.))
    2((.))
    3((.))
    4((.))

    1 --- 2
    2 --- 3
    3 --- 4
```

Para este caso tenemos 4 posibilidades, veamos los casos posibles, que son los siguientes:

- $4 > 1 > 2 > 3$
- $1 > 4 > 2 > 3$
- $1 > 2 > 4 > 3$
- $1 > 2 > 3 > 4$

### CASO 2

El 4 está en el primer nivel

Tenemos las siguientes posibilidades:

- $1 > 2 > 3$ y $4$ no está relacionado con ninguno de los elementos
- $1 > 2 > 3$ y $2 > 4$
- $1 > 2 > 3$ y $1 > 4$

### CASO 3

El 4 está en el segundo nivel

Tenemos las siguientes posibilidades:

- $1 > 2 > 3$ y $4 > 3$
- $1 > 2 > 3$ y $4 > 3$ y $1 > 4$

### CASO 4

El 4 está en el tercer nivel

Tenemos las siguientes posibilidades:

- $1 > 2 > 3$ y $4 > 2$

## Conclusión

La cantidad de relaciones de orden posibles es $4 + 3 + 2 + 1 = 10$. Para resolver este tipo de ejercicios, siempre es conveniente ver todas las posibilidades que tenemos para hacer un diagrama de Hasse.

