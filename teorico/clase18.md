# CLASE 18 - 31/01/2025

## Particiones

### Ejemplo

Veamos todas las particiones posibles de $A = \{1,2,3\}$:

- $\{\{1,2,3\}\}$
- $\{\{1,2\},\{3\}\}$
- $\{\{1,3\},\{2\}\}$
- $\{\{2,3\},\{1\}\}$
- $\{\{1\},\{2\},\{3\}\}$

Por otro lado, no son particiones de $A$:

- $\{\{\emptyset\},\{1,3\},\{2\}\}$ porque tiene un conjunto vacío.
- $\{\{1,2\},\{2,3\}\}$ porque el elemento 2 está en dos subconjuntos diferentes.

### Definición alternativa (partición)

Una partición de un conjunto $A$ es una familia $(X_i)_{i\in I}: I \to P(A)$ tal que:

1. $X_i \neq \emptyset$ para todo $i \in I$.
2. $X_i \cap X_j = \emptyset$ para todos $i,j \in I, i\neq j$.
3. $\bigcup_{i\in I} X_i = A$.

### Proposición

1. Dada una relación de equivalencia $R$ en un conjunto $A$, las clases de equivalencia forman una partición de $A$.

    - $A/R$ es el conjunto de clases de equivalencia: $$A/R = \{[a] : a\in A\}$$
    - $A/R$ es una partición de $A$.

2. Dada una partición $P$ de un conjunto $A$, existe una relación de equivalencia $R$ en $A$ tal que $P = A/R$. Podemos definir la relación de equivalencia $R$ como: 

$$aRb \iff \exists X \in P, a,b \in X$$

3. Esta correspondencia define una biyección entre:

    - El conjunto de relaciones de equivalencia en $A$.
    - El conjunto de particiones de $A$.

### Teorema (conteo de particiones)

Para todo $n \in \mathbb{N}$, el número de particiones de un conjunto $A$ con $n$ elementos es $B_n$, el $n$-ésimo número de Bell definido por:

$$B_{n} = \sum_{k=0}^n S(n,k)$$