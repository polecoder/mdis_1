# CLASE 9 - 27/1/2025

## Principio de inclusión-exclusión: Aplicaciones

### Problema

Dados dos conjuntos $A=\{a_1,a_2,\ldots,a_m\}$ y $B=\{b_1,b_2,\ldots,b_n\}$, queremos contar la cantidad de funciones $f:A\to B$ que son sobreyectivas.

Veamos de traducir este problema a algo más conocido utilizando el principio de inclusión-exclusión:

$U = \{ f: A \to B \text{ }|\text{ } f \text{ es sobreyectiva}\}$

$N = n^m$: esto es una simple regla del producto

Aquí establezcamos las condiciones de forma inteligente:

$c_i = \{b_i \text{ no es imagen de } A\}$

Veamos entonces los valores de $N$:

- $N(c_i) = (n-1)^m$ con $1 \leq i \leq n$
- $N(c_i c_j) = (n-2)^m$ con $1 \leq i, j \leq n$
- $\ldots$
- $N(c_{i_1} c_{i_2} \ldots c_{i_k}) = (n-k)^m$ con $1 \leq c_{i_1} , \ldots, i_k \leq n$

Veamos $S_k$ para todo $k$:

$$
\sum_{1\leq i_1 \leq \ldots \leq i_k \leq n}N(c_{i_1}\ldots c_{i_k}) = C(n, k) (n-k)^m
$$

Observemos que $C(n,k)$ aparece porque estamos eligiendo $k$ condiciones de $n$ posibles, tenemos que contemplar todas esas posibilidades.

Ahora, plantear el principio de inclusión-exclusión, nos da el resultado que estabamos buscando (llamamos $Sob(m,n)$ al resultado):

$$
\begin{align*}
Sob(m,n) &= N + \sum_{k=1}^{n}(-1)^k S_k \\
&= n^m + \sum_{k=1}^{n}(-1)^k C(n,k)(n-k)^m \\
&= \sum_{k=0}^{n}(-1)^k C(n,k)(n-k)^m
\end{align*}
$$

Observación: En el último paso se observa que $n^m = C(n, 0)(n-0)^m$, por lo que se incluye dicho término en la suma.

### Observación

Cuando $n=m$ toda función sobreyectiva es biyectiva (sabemos que la cantidad de funciones biyectivas es $n!$ donde $n$ es el cardinal de ambos conjuntos $A$ y $B$ con $f: A\to B$), por lo que $Sob(n,n) = n!$.

Además si $n < m$ no hay funciones sobreyectivas, por lo que $Sob(m,n) = 0$.

### Ejemplo

(a) En el supermercado, de cuántas maneras se pueden disponer 3 artículos $(A, B, C)$ en 2 bolsas ídenticas, sin dejar ninguna bolsa vacía?

(b) Lo mismo pero con 4 artículos $(A, B, C, D)$.

#### Solución (parte a)

Hagámoslo de forma manual:

- $\{\{A\}, \{B,C\}\}$
- $\{\{B\}, \{A,C\}\}$
- $\{\{C\}, \{A,B\}\}$

Por lo que hay 3 formas de hacerlo, recordar que el orden NO importa, es decir: $\{\{A\}, \{B,C\}\} = \{\{B,C\}, \{A\}\}$.

#### Solución (parte b)

Hagámoslo de forma manual:

- $\{\{A\}, \{B,C,D\}\}$
- $\{\{B\}, \{A,C,D\}\}$
- $\{\{C\}, \{A,B,D\}\}$
- $\{\{D\}, \{A,B,C\}\}$
- $\{\{A,B\}, \{C,D\}\}$
- $\{\{A,C\}, \{B,D\}\}$
- $\{\{A,D\}, \{B,C\}\}$

Por lo que hay 7 formas de hacerlo.

### Generalización

Si tenemos $m$ artículos y $n$ bolsas, cómo resolveríamos este problema?

Hagámoslo en dos pasos:

1. Colocar los $m$ artículos distinguibles en $n$ bolsas distinguibles.
    - Esto se responde con el número que cálculamos anteriormente: $Sob(m,n)$

2. Lo mismo pero ahora las bolsas son indistinguibles.
    - Utilizando el paso uno, deberíamos dividir por la cantidad de permutaciones de las bolsas. Nos quedamos con el resultado: $\frac{Sob(m,n)}{n!}$

Esta es la definición del número de Stirling de segunda clase, que se denota como:

$$
S(m,n) = \frac{Sob(m,n)}{n!} = \frac{1}{n!}\sum_{k=0}^{n}(-1)^k C(n,k)(n-k)^m
$$

## Desórdenes

### Definición

Un desorden (o desarreglo) de tamaño $n$ es una permutación de los elementos de un conjunto de tamaño $n$ que no deja ningún elemento en su lugar original.

Es lo mismo que decir: una biyección $f: \{1, \ldots, n\} \to \{1, \ldots, n\}$ tal que $f(i) \neq i$ para todo $i$.

### Notación

Denotamos $D(n)$ a la cantidad de desarreglos de tamaño $n$.

Ahora, veamos cómo calcular $D(n)$ utilizando el principio de inclusión-exclusión:

$U = \{ f: \{1, \ldots, n\} \to \{1, \ldots, n\} \text{ biyectiva} \}$

$N = n!$

Ahora las condiciones:

$c_i = \{i \text{ está en su lugar original}\}$

Veamos los valores de $N$:

- $N(c_i) = (n-1)!$ con $1 \leq i \leq n$
- $N(c_i c_j) = (n-2)!$ con $1 \leq i, j \leq n$
- $\ldots$
- $N(c_{i_1} c_{i_2} \ldots c_{i_k}) = (n-k)!$ con $1 \leq c_{i_1} , \ldots, i_k \leq n$

Veamos $S_k$ para todo $k$:

$$
\sum_{1\leq i_1 \leq \ldots \leq i_k \leq n}N(c_{i_1}\ldots c_{i_k}) = C(n, k) (n-k)!
$$

Ahora, planteando el principio de inclusión-exclusión:

$$
\begin{align*}
D(n) &= N + \sum_{k=1}^{n}(-1)^k S_k \\
&= n! + \sum_{k=1}^{n}(-1)^k C(n,k)(n-k)! \\
&= \sum_{k=0}^{n}(-1)^k C(n,k)(n-k)!
\end{align*}
$$

Observación: En el último paso se observa que $n! = C(n, 0)(n-0)!$, por lo que se incluye dicho término en la suma.

Podemos simplificar la fórmula anterior, expandiendo $C(n,k)$:

$$
\begin{align*}
D(n) &= \sum_{k=0}^{n}(-1)^k \frac{n!}{k!(n-k)!}(n-k)! \\
&= \sum_{k=0}^{n}(-1)^k \frac{n!}{k!} \\
&= n! \sum_{k=0}^{n}(-1)^k \frac{1}{k!}
\end{align*}
$$
