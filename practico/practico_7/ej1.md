# Ejercicio 1

Para cada uno de los órdenes (A, ≤) siguientes, dibujar el diagrama de Hasse.

(a) $A = \{1, 2, 3, 4, 12\}$ y $\leq$ es el orden de divisibilidad ($x \leq y$ sii $y$ es múltiplo de $x$).
(b) $A$ es el conjunto de todos los subconjuntos de $\{1, 2, 3\}$ y $\leq$ es la inclusión $\subset$.

## Resolución (parte a)

```mermaid
graph TD
    12((12))
    4((4))
    3((3))
    2((2))
    1((1))

    12 --- 4
    12 --- 3
    4 --- 2
    3 --- 1
    2 --- 1
```

Tener en cuenta para este punto que las flechas no van. Están por un tema del lenguaje que se usa para visualizar los dibujos.

## Resolución (parte b)

```mermaid
graph TD
    123((123))
    12((12))
    13((13))
    23((23))
    1((1))
    2((2))
    3((3))
    Vacío((Vacío))

    123 --- 12
    123 --- 13
    123 --- 23
    12 --- 1
    12 --- 2
    13 --- 1
    13 --- 3
    23 --- 2
    23 --- 3
    1 --- Vacío
    2 --- Vacío
    3 --- Vacío
```

Tener en cuenta para este punto que las flechas no van. Están por un tema del lenguaje que se usa para visualizar los dibujos.