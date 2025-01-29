---
header-includes: |
  \usepackage{cancel}
---

# CLASE 14 - 29/01/2025

## Relaciones

### Definición (producto cartesiano):

El producto cartesiano de dos conjuntos $A$ y $B$ se define como el conjunto de todos los pares ordenados $(a, b)$ donde $a \in A$ y $b \in B$.

$$A \times B = \{(a, b) \mid a \in A, b \in B\}$$

En caso de que $A = B$, se denota $A^2$.

#### Observación

El orden de los elementos en el par ordenado es importante. Es decir, $(a, b) \neq (b, a)$ si $a \neq b$.

### Ejemplo

Sean $A = \{1, 2\}$ y $B = \{3, 4\}$. Entonces, 
- $A \times B = \{(1, 3), (1, 4), (2, 3), (2, 4)\}$.
- $B \times A = \{(3, 1), (3, 2), (4, 1), (4, 2)\}$.

De este ejemplo vemos que en general, el producto cartesiano NO es commutativo: $A \times B \neq B \times A$.

### Proposición

Sean $A$, $B$ y $C$ conjuntos finitos. Entonces, $A \times B$ también es finito y:

$$|A \times B| = |A| \cdot |B|$$

Donde $|A|$ denota la cantidad de elementos de $A$ o el cardinal de $A$.

### Definición (relación)

Dados dos conjuntos $A$ y $B$, llamamos:
- una relación de $A$ en $B$ a todo subconjunto $R \subset (A \times B)$.

- una relación binaria en $A$ a todo subconjunto $R \subset A^2$.

Dados $R\subset A\times B, x\in A, y\in B$, se escriben:

- $xRy$ si $(x, y) \in R$.
- $x \cancel{R} y$ si $(x, y) \not\in R$.

### Ejemplo 1

Sea $A = \{1, 2, 3\}, B = \{x, y, z, t\}$, definimos $R$:

$$R=\{(1, x), (1, z), (2, z), (2, t)\}$$

Entonces, $R$ es una relación de $A$ en $B$. Llamamos a este tipo de definición, definición por extensión.

### Ejemplo 2

Sea $A=B=P(\{1, 2, 3\})$, que es el conjunto potencia de $\{1, 2, 3\}$, o sea todos los subconjuntos de dicho conjunto. Definimos $R$:

$$R=\{(X, Y) \in P(\{1, 2, 3\})^2 \mid X \subset Y\}$$

Algunos elementos que están relacionados podrían ser:

- $\{1, 2\} R \{1, 2, 3\}$
- $\{\empty\} R \{2, 3\}$
- $\{1, 2\} R \{1, 2\}$

Llamamos a este tipo de definición, definición por comprensión.

### Ejemplo 3

Sea $A=B=\mathbb{Z}$. Fijamos n $\in \mathbb{Z}^+$ y definimos la congruencia módulo $n$ par:

$xR_ny \iff x-y \text{ es múltiplo de }n$

### Representación de una relación