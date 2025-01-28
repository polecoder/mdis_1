# CLASE 11 - 27/01/2025

## Sucesiones y recurrencias

### Recordatorio

- Una sucesión (de números reales) es una función $a: \mathbb{N} \to \mathbb{R}$.

- Notaciones: $a_0 = a(0), a_1 = a(1), \ldots, a_n = a(n)$. Solemos representar toda la sucesión de la siguiente forma: $\{a_n\}_{n\in \mathbb{N}}$.

### Ejemplo 1

$a_0 = 5$, $a_{n+1} = 2a_n - 3$ para todo $n \in \mathbb{N}$.

Donde llamamos:

- $a_0$: término inicial
- $a_{n+1} = 2a_n - 3$: relación de recurrencia

Calculemos los primeros términos de la sucesión:

- $a_0 = 5$
- $a_1 = 2a_0 - 3 = 2\times 5 - 3 = 7$
- $a_2 = 2a_1 - 3 = 2\times 7 - 3 = 11$
- $a_3 = 2a_2 - 3 = 2\times 11 - 3 = 19$
- $a_4 = 2a_3 - 3 = 2\times 19 - 3 = 35$

**Pregunta natural:** Cómo puedo calcular $a_n$ para cualquier $n$, sin calcular todos los anteriores?

La idea para esto es encontrar el término general de la sucesión, donde $a_n$ se expresa en función de $n$. Más adelante tendremos herramientas para hallar este término general.

### Ejemplo 2

$a_0 = 0$, $a_1 = 1$, $a_{n+2}$ = $a_{n+1} + a_n$ para todo $n \in \mathbb{N}$.

Calculemos los primeros términos de la sucesión:

- $a_2 = a_1 + a_0 = 1 + 0 = 1$
- $a_3 = a_2 + a_1 = 1 + 1 = 2$
- $a_4 = a_3 + a_2 = 2 + 1 = 3$
- $a_5 = a_4 + a_3 = 3 + 2 = 5$
- $a_6 = a_5 + a_4 = 5 + 3 = 8$
- $a_7 = a_6 + a_5 = 8 + 5 = 13$

Mientras hallar el término general del primer caso podría haberse hecho de forma directa, en este caso no es tan sencillo. Por eso necesitamos herramientas para resolver este tipo de problemas.

## Progresiones geométricas

### Definición

Una sucesión $(a_n)_{n\in \mathbb{N}}$ es una progresión geométrica si existe una constante $r$ tal que:

$$
a_{n+1} = ra_n \quad \text{para todo } n \in \mathbb{N}
$$

Llamamos a $r$ la razón de la progresión geométrica.

#### Observación

Para conocer todos los términos de una progresión geómetrica nos basta con conocer la razón $r$ y algún término de la misma.

### Proposición

Si $(a_n)_{n\in \mathbb{N}}$ es una progresión geométrica con razón $r \in \mathbb{R}$ y $a_0 = a$ donde $a\in \mathbb{R}$, entonces:

$$
a_n = a \times r^n \quad \text{para todo } n \in \mathbb{N}
$$

#### Demostración

Se prueba por inducción completa.

### Ejemplo 3

Supongamos que $(a_n)_{n\in \mathbb{N}}$ es una progresión geométrica de razón 3 tal que $a_4 = 9$. Hallar $a_0$ y el término general de la sucesión.

Por la proposición anterior, tenemos que:

$$
a_n = a \times 3^n
$$

Por lo que $a_4 = a \times 3^4 = 9$. De aquí, despejamos $a$: $a = \frac{9}{3^4} = \frac{9}{81} = \frac{1}{9}$. Por lo tanto, el término general de la sucesión es:

$$
a_n = \frac{1}{9} \times 3^n = \frac{3^n}{9} = \frac{3^n}{3^2} = 3^{n-2}
$$

### Ejemplo 4

Tengo una cuenta de ahorro, y el banco me paga un interés anual de 6%, con interés compuesto mensual. Deposito $10000 al inicio del año. Al final del año, cuánto tengo en la cuenta?

La tasa mensual es 6%/12 = 0,5% = 0,005. Sea $a_n$ la suma después de n meses:

$$
a_0 = 10000, a_{n+1} = a_n + 0,005a_n = 1,005 \times a_n
$$

Con esto, podemos ver que $(a_n)_{n\in \mathbb{N}}$ es una progresión geométrica con razón $r = 1,005$. Por lo que el término general de la sucesión es:

$$
a_n = 10000 \times 1,005^n
$$

Entonces la respuesta es $a_{12} = 10000 \times 1,005^{12} \approx \$10617$.

### Ejemplo 5

Formato de papel $A_n (n \in \mathbb{N})$.
Un formato de papel está definido por dos números $a$ y $b$ tales que $0 < a \leq b$, donde $a$ es el ancho y $b$ el alto. Queremos definir una sucesión de formatos $(A_n)_{n\in \mathbb{N}} = (a_n, b_n)_{b \in \mathbb{N}}$ tal que:

1. La superficie del formato $A_0$ es $1m^2$. Es decir, $a_0 \times b_0 = 1$.
2. Para todo $n \in \mathbb{N}$, el formato $A_{n+1}$ es el formato $A_n$ dividido en dos, de forma que el alto del formato $A_{n+1}$ es el ancho del formato $A_n$ y el ancho del formato $A_{n+1}$ es la mitad del alto del formato $A_n$. Es decir, $a_{n+1} = \frac{b_n}{2}$ y $b_{n+1} = a_n$
3. Todos los formatos $A_n = (a_n, b_n)$ tienen el mismo aspecto, es decir, $\frac{b_n}{a_n} = \frac{b_0}{a_0} = k$ con $k$ constante.

Hallar las dimensiones de $A_n$ para todo $n \in \mathbb{N}$.

Primero determinemos $k$:

$$
k = \frac{b_n}{a_n} = \frac{b_{n+1}}{a_{n+1}} = \frac{a_n}{\frac{b_n}{2}} = 2 \times \frac{a_n}{b_n} = \frac{2}{k} \\
k^2 = 2 \Rightarrow k = \sqrt{2} \quad \text{(porque } k > 0 \text{)}
$$

Por lo que $b_n = \sqrt{2} \times a_n$ para todo $n \in \mathbb{N}$.

Usando el punto (1), podemos determinar $a_0$ y $b_0$:

$$
a_0b_0 = 1 \Rightarrow a_0 \times \sqrt{2} \times a_0 = 1 \Rightarrow a_0^2 = \frac{1}{\sqrt{2}} \Rightarrow a_0 = \frac{1}{\sqrt[4]{2}} \\
b_0 = \frac{1}{a_0} = \sqrt[4]{2}
$$

Entonces $(a_0, b_0)$ = $\left(\frac{1}{\sqrt[4]{2}}, \sqrt[4]{2}\right)$, que en centímetros es apróximadamente $(84.1cm, 118.9cm)$.

Ahora observamos que:

$$
a_{n+1} = \frac{b_n}{2} = \frac{\sqrt{2} \times a_n}{2} = \frac{1}{\sqrt{2}}\times a_n
$$

Entonces $(a_n)_{n \in \mathbb{N}}$ es una progresión geométrica de razón $\frac{1}{\sqrt{2}}$, con término inicial $a_0 = \frac{1}{\sqrt[4]{2}}$. Por lo que el término general de la sucesión es:

$$
a_n = \frac{1}{\sqrt[4]{2}} \times \left(\frac{1}{\sqrt{2}}\right)^n \\
b_n = \sqrt{2}\times a_n = {\sqrt[4]{2}}\times\left(\frac{1}{\sqrt{2}}\right)^n
$$

## Ecuación líneal homogénea de primer orden

Se llama ecuación lineal del primer orden a toda relación de recurrencia de la forma:

$$
Aa_{n+1} + Ba_n = f(n) \quad \text{con } A,B \in \mathbb{R}, A \neq 0, f:\mathbb{N} \to \mathbb{R}
$$

Cuando $f(n) = 0$ para todo $n \in \mathbb{N}$, se llama ecuación líneal __homogénea__ de primer orden.

### Teorema

Las sucesiones $(a_n)_{n \in \mathbb{N}}$ que satisfacen la ecuación lineal homogénea de primer orden:

$$
Aa_{n+1} + Ba_n = 0 \quad \text{con }A,B\in\mathbb{R}, A\neq 0
$$

Son las sucesiones de la forma:

$$
a_n = a_0 \times (-\frac{B}{A})^n
$$

## Ecuación líneal homogénea de segundo orden

Se llama ecuación lineal del segundo orden a toda relación de recurrencia de la forma:

$$
Aa_{n+2} + Ba_{n+1} + Ca_n = f(n) \quad \text{con } A,B,C \in \mathbb{R}, A \neq 0, f:\mathbb{N} \to \mathbb{R}
$$

Cuando $f(n) = 0$ para todo $n \in \mathbb{N}$, se llama ecuación líneal __homogénea__ de segundo orden.