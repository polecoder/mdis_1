# CLASE 15 - 30/01/2025

## Relaciones

### Definición (composición de relaciones):

Dados tres conjuntos $A,B,C$ y relaciones $R\subset A\times B, S\subset B\times C$, definimos la composición de $R$ y $S$ como:

$$S\circ R = \{(a, c) \in A\times C \mid \exists b\in B: (a, b)\in R \land (b, c)\in S\}$$

### Ejemplo

Sean $A=\{1, 2, 3\}, B=C=\{x, y, z, t\}$ y las relaciones $R, S$:

$$R=\{(1, x), (1, z), (3, x), (3, z), (3, t)\}$$

$$S=\{(y, y), (z, z), (t, x), (t,z)\}$$

La mejor forma de calcular $R\circ S$ es usando el diagrama sagital:

```mermaid
graph LR
    
```

**Observación**: La relación compuesta se escribe al revés de la función compuesta.

**Observación**: La composición de relaciones es asociativa, es decir que: dadas $R\subset A\times B, S\subset B\times C, T\subset C\times D$ 

$$(S\circ R)\circ T = S\circ (R\circ T)$$

### Definición (matriz asociada a una relación)

Dados $A = \{a_1, a_2, \ldots, a_m\}$ y $B = \{b_1, b_2, \ldots, b_n\}$, y una relación $R\subset A\times B$, la matriz asociada a $R$ es la matriz $M=(M_{i,j}): m\times n$ tal que:

$$
M_{i,j} = 
\begin{cases}
1 & \text{si } (a_i, b_j)\in R \\ 
0 & \text{si } (a_i, b_j)\not\in R 
\end{cases}
$$

### Definición (producto modificado)

Dadas dos matrices asociadas a una relación $M$ y $N$, definimos el producto modificado de $M=(M_{i,j}): m\times n$ y $N=(N_{j,k}): n\times p$ como la matriz $MN = (MN_{i,k})$ tal que:

$$MN_{i,k} = \sum_{j=1}^{n} M_{i,j}N_{j,k} \quad 1 \leq i \leq m \text{ y }1 \leq k \leq p$$

Con una suma $(+, \sum)$ definida por:
- $0 + 0 = 0$
- $0 + 1 = 1$
- $1 + 1 = 1$


### Ejemplo

$$
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\times
\begin{pmatrix}
1 & 1 \\
1 & 0 
\end{pmatrix}
\ = \
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
$$

Donde: 

- $r_{1,1} = 1 + 1 = 1$
- $r_{1,2} = 1 + 0 = 1$
- $r_{2,1} = 0 + 1 = 1$
- $r_{2,2} = 0 + 0 = 0$

### Proposición

Dados tres conjuntos $A = \{a_1, a_2, \ldots, a_m\}, B = \{b_1, b_2, \ldots, b_n\}$ y $C = \{c_1, c_2, \ldots, c_p\}$ y dos relaciones $R\subset A\times B$ y $S\subset B\times C$, tenemos que:

$$Mat(R\circ S) = Mat(R) \times Mat(S)$$

Donde $\times$ es el producto modificado. 

### Definición (precedencia de matrices)

Dadas dos matrices $M,N: m\times n$, decimos que $M$ precede a $N$ cuando $M_{i,j} \leq N_{i,j}  \quad \forall i, j \mid 1\leq i \leq m \text{ y } 1\leq j\leq n$.
Cuando pasa esto, lo escribimos como $M\leq N$.

### Conteo de la cantidad de relaciones

Dados dos conjuntos finitos $A$ y $B$, con $|A| = m$ y $|B| = n$, entonces: $|A\times B| = mn$. La cantidad de relaciones posibles es equivalente a hallar el cardinal de: $P(A\times B)$, que es el conjunto potencia de $A\times B$. Entonces:

$$|P(A\times B)| = 2^{mn}$$

Veamos que pasa si $A=B$, $|A| = n$, $A = \{a_1, \ldots, a_n\}$. Podemos representar cada relación $R \subset A^2$ como una matriz cuadrada de $n\times n$ donde cada elemento de la matriz es 0 o 1. Si $a_iRa_j$, entonces la entrada $i, j$ de la matriz es 1, y 0 en caso contrario.

Que nos dice la matriz asociada a la relación $R$ sobre la relación?

- **Reflexividad**: La diagonal de la matriz es 1. Entonces la cantidad de relaciones reflexivas posibles es $2^{n^2 - n}$ (porque los $n$ elementos de la diagonal están fijados).

- **Irreflexividad**: La diagonal de la matriz es 0. Entonces la cantidad de relaciones irreflexivas posibles es $2^{n^2 - n}$ (porque los $n$ elementos de la diagonal están fijados).

- **Simetría**: Esto significa que $\forall x,y \in A, xRy \Rightarrow yRx$. Entonces, para todos los elementos de la matriz $M_{i,j} = M_{j,i}$, o sea que $M = M^t$. La cantidad de relaciones simétricas está dada por contar solo el triángulo superior de la matriz, que tiene $\sum_{k=1}^{n}k = \frac{n(n+1)}{2}$ elementos. Entonces, la cantidad de relaciones simétricas posibles es $2^{\frac{n(n+1)}{2}}$.

- **Antisimetría**: Esto significa que $\forall x,y \in A, xRy, yRx \Rightarrow x = y$. Esto nos da una matriz que en donde la diagonal puede ser cualquiera, pero el resto de la matriz puede ser cualquiera, excepto que si $M_{i,j} = 1$, entonces $M_{j,i} \neq 1$. Esto es equivalente a solo construir el triangulo superior de la matriz (sin la diagonal), pero con tres posibilidades para cada elemento: 0, 1, o 2. Entonces, la cantidad de relaciones antisimétricas posibles es $2^n \times 3^{\frac{n(n-1)}{2}}$. El $2^n$ es para contar las posibilidades de la diagonal, que solo tiene 2 posibilidades

- **Transitividad**: Esto significa que $\forall x,y,z \in A, xRy, yRz \Rightarrow xRz$. Esto es equivalente a decir que $R\circ R \subset R$ que también es equivalente a decir que $M\times M \leq M$, con $\times$ representando el producto modificado. No sabemos calcular la cantidad de relaciones transitivas posibles con las herramientas de este curso

## Órdenes parciales y diagramas de Hasse

### Definición (orden parcial)

Un órden parcial sobre $A$ es una relación binaria $R\subset A^2$ que cumple las siguientes propiedades:

1. **Reflexividad**: $\forall x\in A, xRx$.
2. **Antisimetría**: $\forall x,y\in A, xRy, yRx \Rightarrow x = y$.
3. **Transitividad**: $\forall x,y,z\in A, xRy, yRz \Rightarrow xRz$.

### Definición (orden lineal/total)

Un órden parcial $\leq$ sobre un conjunto $A$ es lineal/total cuando: $\forall x,y\in A, x\leq y \lor y\leq x$. Es decir, para cualquier par de elementos, tengo una comparación posible entre ellos

### Ejemplos

1. La relación $x\leq y$ en $\mathbb{N}$ es una relación de orden total.
2. Dado un conjunto $U$, la relación de inclusión $X\subset Y$ es una relación de orden parcial en $P(U)$ (el conjunto potencia de U). Esta es una relación de orden parcial, pero no total.
3. Dado un alfabeto $\sum$ (un conjunto de símbolos), se escribe $\sum^*$ al conjunto de todas las palabras finitas sobre $\sum$. Definimos la relación $P$ como $xPy \iff x$ es prefijo de $y$. Esta es una relación de orden parcial, pero no total.
