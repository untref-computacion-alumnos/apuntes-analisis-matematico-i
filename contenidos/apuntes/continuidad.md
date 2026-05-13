# Continuidad

(continuidad)=

Una función $f(x)$ es continua cuando su gráfica no presenta interrupciones, saltos o puntos aislados. Desde el análisis matemático, esto significa que el comportamiento local de la función coincide con su valor en el punto.

(continuidad-1-definicion-formal)=

## 1. Definición formal

(continuidad-1-1-continuidad-en-un-punto)=

### 1.1. Continuidad en un punto

Para que una función $f$ sea continua en un punto $x = a$, tienen que cumplirse simultáneamente ciertas condiciones:

- Existencia de la imagen.
- Existencia del límite.
- Igualdad.

(continuidad-1-1-1-existencia-de-la-imagen)=

#### 1.1.1. Existencia de la imagen

$f(a)$ tiene que estar definida, o sea, el punto $a$ pertenece al dominio de $f$.

(continuidad-1-1-2-existencia-del-limite)=

#### 1.1.2. Existencia del límite

Tiene que existir el límite:

$$
\lim_{x \to a} [f(x)]
$$

Esto implica que los límites laterales son iguales.

$$
\lim_{x \to a^{-}} [f(x)] = \lim_{x \to a^{+}} [f(x)]
$$

(continuidad-1-1-3-igualdad)=

#### 1.1.3. Igualdad

El valor del límite tiene que coincidir con el valor de la imagen.

$$
\lim_{x \to a} [f(x)] = f(a)
$$

(continuidad-1-2-continuidad-en-un-intervalo)=

### 1.2. Continuidad en un intervalo

(continuidad-1-2-1-intervalo-abierto)=

#### 1.2.1. Intervalo abierto

Es continua en un intervalo abierto $(a, b)$ si lo es en cada punto perteneciente al intervalo.

(continuidad-1-2-2-intervalo-cerrado)=

#### 1.2.2. Intervalo cerrado

Es continua en un intervalo cerrado si lo es en uno abierto $(a, b)$ y además posee continuidad lateral en los extremos.

$$
\lim_{x \to a^{+}} [f(x)] = f(a)
$$

$$
\lim_{x \to b^{-}} [f(x)] = f(b)
$$

---

(continuidad-2-propiedades)=

## 2. Propiedades

Si $f$ y $g$ son funciones continuas en $x = c$ se pueden aplicar ciertas propiedades.

(continuidad-2-1-suma)=

### 2.1. Suma

$f + g$ es continua en $c$.

(continuidad-2-2-resta)=

### 2.2. Resta

$f - g$ es continua en $c$.

(continuidad-2-3-producto)=

### 2.3. Producto

$f \cdot g$ es continua en $c$.

(continuidad-2-4-producto-por-un-escalar)=

### 2.4. Producto por un escalar

$k \cdot f$ es continua en $c$ para cualquier $k \in \mathbb{R}$.

(continuidad-2-5-cociente)=

### 2.5. Cociente

$\frac{f}{g}$ es continua en $c$ si $g(0) \neq 0$.

(continuidad-2-6-potencia)=

### 2.6. Potencia

$f^{g}$ es continua en $c$, dentro del dominio de definición.

(continuidad-2-7-composicion)=

### 2.7. Composición

Si $f$ es continua en $c$ y $g$ es continua en $f(c)$, entonces $(g o f)$ es continua en $c$.

---

(continuidad-3-familias-de-funciones-y-su-continuidad)=

## 3. Familias de funciones y su continuidad

(continuidad-3-1-polinomicas)=

### 3.1. Polinómicas

Son continuas en todo su dominio ($\mathbb{R}$).

$$
f(x) = a_{n}x^{n} + \dots + a_{1}x + a_{0}
$$

(continuidad-3-2-racionales)=

### 3.2. Racionales

Son continuas en su dominio, donde el denominador **no** es 0.

$$
f(x) = \frac{P(x)}{Q(x)}, \ Q(x) \neq 0
$$

(continuidad-3-3-radicales)=

### 3.3. Radicales

Son continuas en su dominio, teniendo en cuenta índices pares y valores negativos.

$$
f(x) = \sqrt[n]{x}, n \text{ es par}, x \geq 0
$$

(continuidad-3-4-trigonometricas)=

### 3.4. Trigonométricas

$\sin(x)$ y $\cos(x)$ son continuas en $\mathbb{R}$. $\tan(x)$ es discontinua en $x = \frac{\pi}{2} + k\pi$.

$$
\sin(x), \cos(x), \tan(x), \dots
$$

(continuidad-3-5-exponenciales)=

### 3.5. Exponenciales

Son continuas en todo su dominio ($\mathbb{R}$).

$$
f(x) = a^{x}, a > 0
$$

(continuidad-3-6-logaritmicas)=

### 3.6. Logarítmicas

Son continuas en $(0, + \infty)$.

$$
f(x) = \log_{a}(x), x > 0
$$

---

(continuidad-4-discontinuidades)=

## 4. Discontinuidades

Las discontinuidades se pueden clasificar en **evitables** y **esenciales**.

(continuidad-4-1-evitables)=

### 4.1. Evitables

Existe el límite finito $L$, pero $f(c) \neq L$ o $f(c)$ no existe.

Se puede remover la discontinuidad redefiniendo $f$.

El límite existe.

(continuidad-4-1-1-ejemplo)=

#### 4.1.1. Ejemplo

$$
f(x) = \frac{x^{2} - 1}{x - 1}
$$

En $x = 1$.

- El límite existe.
- $f(1)$ no existe.

(continuidad-4-2-esenciales)=

### 4.2. Esenciales

No existe el límite finito en el punto.

Pueden dividirse en **salto finito** y **salto infinito**.

(continuidad-4-2-1-salto-finito)=

#### 4.2.1. Salto finito

Ambos son finitos.

$$
\lim_{x \to c^{-}} [f(x)] \neq \lim_{x \to c^{+}} [f(x)]
$$

(continuidad-4-2-2-salto-infinito)=

#### 4.2.2. Salto infinito

Al menos un límite lateral tiende a $\plusmn \infty$, o sea, tiene una **asíntota vertical**.

**Por ejemplo**:

$$
f(x) = \frac{1}{x - 2}
$$

En $x = 2$ hay una discontinuidad esencial.

---

(continuidad-5-comportamiento-asintotico)=

## 5. Comportamiento asintótico

(continuidad-5-1-asintota-vertical)=

### 5.1. Asíntota vertical

La recta $x = c$ es una asíntota vertical si:

$$
\lim_{x \to c} f(x) = \plusmn \infty
$$

(continuidad-5-2-asintota-horizontal)=

### 5.2. Asíntota horizontal

La recta $y = L$ es una asíntota horizontal si:

$$
\lim_{x \to \pm\infty} f(x) = L
$$

> Siendo $L$ un número finito.

(continuidad-5-3-asintota-oblicua)=

### 5.3. Asíntota oblicua

La recta $y = px + b$ ($p \neq 0$) es una asíntota oblicua si:

- **Pendiente**: $p = \lim_{x \to \infty} \frac{f(x)}{x}$.
- **Ordenada**: $b = \lim_{x \to \infty} [f(x) - p \cdot x]$.

---

(continuidad-6-teoremas)=

## 6. Teoremas

(continuidad-6-1-teorema-del-valor-intermedio)=

### 6.1. Teorema del Valor Intermedio

Si $f$ es continua en $[a, b]$, la función toma todos los valores correspondientes entre $f(a)$ y $f(b)$.

O sea, para cualquier $N$ entre $f(a)$ y $f(b)$, existe un $c \in (a, b)$ tal que $f(c) = N$.

(continuidad-6-2-teorema-de-bolzano-(corolario))=

### 6.2. Teorema de Bolzano (Corolario)

Si $f$ es continua en el intervalo cerrado $[a, b]$ y tiene distinto signo en sus extremos $(f(a) \cdot g(b) < 0)$, entonces existe por lo menos un punto $c \in (a, b)$ tal que $f(c) = 0$.

Este punto es una **raíz** de la función.

(continuidad-6-3-teorema-de-weierstrass)=

### 6.3. Teorema de Weierstrass

Toda función continua en un intervalo cerrado alcanza su máximo y mínimo absoluto dentro del intervalo o en sus extremos.

Si $f$ es continua en un intervalo cerrado $[a, b]$, entonces $f$ alcanza siempre un **máximo absoluto** y un **mínimo absoluto** dentro de dicho intervalo.
