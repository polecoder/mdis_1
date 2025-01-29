# CLASE 12 - 28/01/2025

## Ecuación líneal homogénea de segundo orden

### Ejemplo

Sucesión de Fibonacci: $(F_n)_{n \in \mathbb{N}}$:

$F_n = F_{n-1} + F_{n-2} \quad \text{con } F_0 = 0 \text{ y } F_1 = 1$

La correspondiente ecuación líneal de segundo orden es:

$$F_{n-2} + F_{n-1} - F_n = 0$$

Ahora, cómo podemos hallar el término general? Vayamos por pasos:

(1) Sea $S$ el conjunto de todas las sucesiones $(a_n)_{n \in \mathbb{N}}$ que satisfacen la ecuación $a_{n-2} + a_{n-1} - a_n = 0 \quad \forall n\in\mathbb{N}$.

$$
S = \{(a_n)_{n \in \mathbb{N}} \in \mathbb{R}^\mathbb{N}\quad | \quad \forall n\in\mathbb{N}, a_{n-2} + a_{n-1} - a_n = 0\}
$$

(2) Queremos determinar las progresiones geométricas $(a_n)_{n \in \mathbb{N}}$ que cumplen $a_{n-2} + a_{n-1} - a_n = 0 \quad \forall n\in\mathbb{N}$

Sea $a_n = \alpha\times r^n$ una progresión geométrica no nula (con $\alpha, r \in \mathbb{R}, \alpha, r \neq 0$). Veamos cuando $(a_n)_{n \in \mathbb{N}} \in S$

$$
\begin{align}
(a_n)_{n \in \mathbb{N}} \in S &\iff a_{n-2} + a_{n-1} - a_n = 0  \quad\forall n\in\mathbb{N} \\
&\iff \alpha r^{n-2} + \alpha r^{n-1} - \alpha r^n = 0 \quad\forall n\in\mathbb{N} \\
&\iff r^{n-2} + r^{n-1} - r^n = 0 \quad\forall n\in\mathbb{N} \\
&\iff r^2 + r - 1 = 0 \quad \text{si n = 0} \\
&\iff r \text{ es raíz de } x^2 + x - 1 = 0
\end{align}
$$

Observación: En el paso 3 divido por $\alpha$ que es distinto de 0.

Haciendo las cuentas llegamos a las raíces:

$$
r_1 = \frac{1 + \sqrt{5}}{2} \\
r_2 = \frac{1 - \sqrt{5}}{2}
$$

Entonces: $(a_n)_{n \in \mathbb{N}} = \alpha \times \left(\frac{1 + \sqrt{5}}{2}\right)^n$ y $(a_n)_{n \in \mathbb{N}} = \beta \times \left(\frac{1 - \sqrt{5}}{2}\right)^n$ con $\alpha, \beta \in \mathbb{R}$

(3) Observemos que de forma general, dadas dos sucesiones $(a_n)_{n \in \mathbb{N}}$ y $(b_n)_{n \in \mathbb{N}}$ tales que $(a_n)_{n \in \mathbb{N}} \in S$ y $(b_n)_{n \in \mathbb{N}} \in S$, entonces $\forall \alpha, \beta \in \mathbb{R}$, $(\alpha a_n + \beta b_n)_{n \in \mathbb{N}} \in S$.

Observación: $S$ es un subespacio vectorial de $\mathbb{R}^\mathbb{N}$

Por lo tanto el conjunto $S$ contiene al menos todas las sucesiones de la forma:

$$
(a_n)_{n \in \mathbb{N}} = \alpha \times \left(\frac{1 + \sqrt{5}}{2}\right)^n + \beta \times \left(\frac{1 - \sqrt{5}}{2}\right)^n \quad \forall \alpha, \beta \in \mathbb{R}
$$

Se puede demostrar que todos los elementos de $S$ son de la forma anterior. La prueba está relacionada con demostrar que $(a_n)_{n \in \mathbb{N}} = \alpha \times \left(\frac{1 + \sqrt{5}}{2}\right)^n$ y $(a_n)_{n \in \mathbb{N}} = \beta \times \left(\frac{1 - \sqrt{5}}{2}\right)^n$ son una base de $S$.

(4) Por lo anterior, sabemos que existen coeficientes $\alpha, \beta \in \mathbb{R}$ tales que:

$$
F_n = \alpha \times \left(\frac{1 + \sqrt{5}}{2}\right)^n + \beta \times \left(\frac{1 - \sqrt{5}}{2}\right)^n
$$

Tenemos que:

$$
\begin{cases}
F_0 = \alpha\times 1 + \beta\times 1 = 0 \\
F_1 = \alpha \times \frac{1 + \sqrt{5}}{2} + \beta \times \frac{1 - \sqrt{5}}{2} = 1
\end{cases}
$$

Esto nos lleva a:

$$
\begin{cases}
\beta = -\alpha \\
\alpha \times \left( \frac{1 + \sqrt{5}}{2}  - \frac{1 - \sqrt{5}}{2} \right) = 1
\end{cases}
$$

Terminando las cuentas llegamos a:

$$
\begin{cases}
\alpha = \frac{1}{\sqrt{5}} \\
\beta = -\frac{1}{\sqrt{5}}
\end{cases}
$$

Entonces el término general de la sucesión de Fibonacci es:

$$
\begin{align*}
F_n &= \frac{1}{\sqrt{5}} \times \left( \frac{1 + \sqrt{5}}{2} \right)^n - \frac{1}{\sqrt{5}} \times \left( \frac{1 - \sqrt{5}}{2} \right)^n \\
F_n &= \frac{1}{\sqrt{5}} \times \left( \left( \frac{1 + \sqrt{5}}{2} \right)^n - \left( \frac{1 - \sqrt{5}}{2} \right)^n \right)
\end{align*}
$$

### Observación

Veamos algunos casos particulares de una ecuación lineal de segundo orden:

$$
Aa_{n-2} + Ba_{n-1} + Ca_n = 0
$$

Veamos los casos particulares donde:

- A = 0: entonces la ecuación se reduce a una ecuación lineal de primer orden.
- C = 0: entonces la ecuación se reduce a una ecuación lineal de primer orden, que empieza en 1 en vez de 0
- B = 0: entonces la ecuación se reduce a una ecuación lineal de primer orden, pero que da saltos. En este caso la ecuación anterior es equivalente a tomar dos sucesiones $(x_n)_{n \in\mathbb{N}} = a_{2n} $ y $(y_n)_{n \in\mathbb{N}} = a_{2n+1}$ y resolver dos ecuaciones lineales de primer orden. Tendremos que la ecuación inicial es lo mismo que resolver:

$$
\begin{cases}
A x_{n-1} + C x_n = 0 \\
A y_{n-1} + C y_n = 0
\end{cases}
$$