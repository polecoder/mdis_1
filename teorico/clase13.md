# CLASE 13 - 28/01/2025

## Ecuación lineal homogénea de segundo orden

### Forma general de resolución

Dada la ecuación lineal homogénea de segundo orden:

$$Aa_{n+2} + Ba_{n+1} + Ca_n = 0 \quad \text{con }A,B,C \neq 0$$

Llamamos polinomio característico de la ecuación al polinomio:

$$P(x) = Ax^2 + Bx + C$$

### Proposición

Dado $r\in\mathbb{R}$, entonces $r$ es raíz del polinomio característico $P(x)$ si y solo si $a_n = r^n \quad\forall n\in\mathbb{N}$ es solución de la ecuación lineal homogénea de segundo orden.

#### Demostración

Sea $a_n = r^n \quad\forall n\in\mathbb{N}$ una progresión geométrica que cumple con la ecuación $Aa_{n+2} + Ba_{n+1} + Ca_n = 0 \quad(1)$. Entonces:

$$
\begin{align*}
(a_n)_{n\in\mathbb{N}} \text{ es solución de (1)} &\iff Aa_{n+2} + Ba_{n+1} + Ca_n &= 0 \\
&\iff Ar^{n+2} + Br^{n+1} + Cr^n &= 0 \\
&\iff r^n(Ar^2 + Br + C) &= 0 \\
&\iff Ar^2 + Br + C &= 0
\end{align*}
$$

Sea $\delta = B^2 + 4AC$ el discriminante de $P(x)$. Entonces:

- Si $\delta > 0$, entonces $P(x)$ tiene dos raíces reales distintas $r_1, r_2$ y la solución general de la ecuación es:

$$a_n = \alpha r_1^n + \beta r_2^n \quad\forall n\in\mathbb{N}$$

- Si $\delta = 0$, entonces $P(x)$ tiene una raíz real doble $r_1 = r_2 = \frac{-B}{2A}$ y la solución general de la ecuación es:

$$a_n = \alpha r_1^n + \beta n r_1^n \quad\forall n\in\mathbb{N}$$

- Si $\delta < 0$, entonces $P(x)$ tiene dos raíces complejas conjugadas. Este caso no se trabajará en este curso.

### Proposición (para $\delta > 0$)

Cada solución $(a_n)_{n\in\mathbb{N}}$ a la ecuación lineal de segundo orden es de la forma:

$$a_n = \alpha r_1^n + \beta r_2^n \quad\forall n\in\mathbb{N}$$

#### Demostración

Sea $(a_n)_{n\in\mathbb{N}}$. Queremos hallar $\alpha, \beta \in\mathbb{R}$ tales que:

$$a_n = \alpha r_1^n + \beta r_2^n \quad\forall n\in\mathbb{N}$$

Esto implica lo siguiente:

$$
\begin{cases}
a_0 &= \alpha \times 1 + \beta \times 1 \\
a_1 &= \alpha r_1 + \beta r_2
\end{cases}
$$

Esto nos da un sistema compatible determinado, con solución $\binom{\alpha}{\beta}$ única. Con esto, podemos verificar por inducción fuerte que:

$$a_n = \alpha r_1^n + \beta r_2^n \quad\forall n\in\mathbb{N}$$

### Proposición (para $\delta = 0$)

La sucesión $a_n = n\times r^n$ es solución de la ecuación lineal homogénea de segundo orden.

#### Demostración

La demostración es basada en hacer las cuentas sustituyendo $a_n = n\times r^n$ en la ecuación.

### Proposición (para $\delta = 0$)

Todas las soluciones de la ecuación lineal homogénea de segundo orden son de la forma:

$$a_n = \alpha r^n + \beta n r^n \quad\forall n\in\mathbb{N}$$

#### Demostración

Supongamos que $(a_n)_{n\in\mathbb{N}}$ es solución de la ecuación lineal homogénea de segundo orden. Entonces:

$$
\begin{cases}
\alpha\times 1 + 0 &= a_0 \\
\alpha r + \beta r &= a_1
\end{cases}
$$

Se observa facilmente que queda un sistema compatible determinado con solución única $\binom{\alpha}{\beta}$. Con esto, podemos verificar por inducción fuerte que:

$$a_n = \alpha r^n + \beta n r^n \quad\forall n\in\mathbb{N}$$

## Ecuaciónes lineales no homogéneas

### Forma general (de segundo orden)

Dada la ecuación lineal no homogénea de segundo orden:

$$Aa_{n+2} + Ba_{n+1} + Ca_n = f(n) \quad\text{con }A,B,C\neq 0$$

Llamamos ecuación homogénea asociada a:

$$Ab_{n+2} + Bb_{n+1} + Cb_n = 0$$

#### Notación

Llamamos $E_{nh}$ a la ecuación lineal no homogénea y $E_h$ a la ecuación homogénea asociada.

### Observación

Si tengo una solución particular $(a_n)_{n\in\mathbb{N}}$ de $E_{nh}$ y $(b_n)_{n\in\mathbb{N}}$ es solución de $E_h$, entonces $(a_n + b_n)_{n\in\mathbb{N}}$ es solución general de $E_{nh}$.

Esto porque:

$$
A(a_{n+2} + b_{n+2}) + B(a_{n+1} + b_{n+1}) + C(a_n + b_n) = f(n) + 0
$$

### Conclusión

Todas las soluciones de la ecuación lineal no homogénea de segundo orden son de la forma:

$$S_{g} = S_{p} + S_{h}$$

Donde:

- $S_{g}$ es la solución general de la ecuación lineal no homogénea.
- $S_{p}$ es una solución particular de la ecuación lineal no homogénea.
- $S_{h}$ es la solución general de la ecuación homogénea asociada.

### Ejemplo

Resolver la ecuación:

$$a_{n+1}-3a_n = 5\times 7^n \quad \forall n \in \mathbb{N}$$

Con condición inicial $a_0 = 2$.

(1) Hallemos la solución general de la ecuación homogénea asociada $S_h$:

$$a_{n+1} - 3a_n = 0 \quad \forall n \in \mathbb{N}$$

La solución general de la ecuación homogénea asociada es:

$$a_n = \beta 3^n \quad \forall n \in \mathbb{N}$$

Observación: Esto se deriva de que en forma general, la solución de una ecuación lineal homogénea de primer grado es:

$$a_n = \alpha (-\frac{B}{A})^n \quad \forall n \in \mathbb{N}$$

(2) Hallemos una solución particular de la ecuación no homogénea $S_p$, para esto se suele probar con algo que se parezca a $f(n)$, para poder simplificar la expresión. Veamos que pasa si probamos con $a_n = \alpha 7^n$:

$$
\begin{align*}
a_{n+1} - 3a_n &= 5\times 7^n \\
\alpha 7^{n+1} - 3\alpha 7^n &= 5\times 7^n \\
7\alpha - 3\alpha &= 5 \\
4\alpha &= 5 \\
\alpha &= \frac{5}{4}
\end{align*}
$$

Entonces, $a_n = \frac{5}{4} 7^n \quad\forall n\in\mathbb{N}$ es solución particular de la ecuación no homogénea.

(3) La solución general de la ecuación no homogénea es:

$$a_n = \frac{5}{4} 7^n + \beta 3^n \quad\forall n\in\mathbb{N}$$

(4) Hallemos $\beta$ usando la condición inicial $a_0 = 2$:

$$
\begin{align*}
a_0 &= \frac{5}{4} 7^0 + \beta 3^0 \\
2 &= \frac{5}{4} + \beta \\
\beta &= 2 - \frac{5}{4} = \frac{3}{4}
\end{align*}
$$

Entonces, la solución general de la ecuación es:

$$a_n = \frac{5}{4} 7^n + \frac{3}{4} 3^n \quad\forall n\in\mathbb{N}$$