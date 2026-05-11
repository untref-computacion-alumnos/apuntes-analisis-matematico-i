# Continuidad

Una función $f(x)$ es continua cuando su gráfica no presenta interrupciones, saltos o puntos aislados. Desde el análisis matemático, esto significa que el comportamiento local de la función coincide con su valor en el punto.

## 1. Definición formal

### 1.1. Continuidad en un punto

Para que una función $f$ sea continua en un punto $x = a$, tienen que cumplirse simultáneamente ciertas condiciones:

- Existencia de la imagen.
- Existencia del límite.
- Igualdad.

#### 1.1.1. Existencia de la imagen

$f(a)$ tiene que estar definida, o sea, el punto $a$ pertenece al dominio de $f$.

#### 1.1.2. Existencia del límite

Tiene que existir el límite:

$$
\lim_{x \to a} [f(x)]
$$

Esto implica que los límites laterales son iguales.

$$
\lim_{x \to a^{-}} [f(x)] = \lim_{x \to a^{+}} [f(x)]
$$

#### 1.1.3. Igualdad

El valor del límite tiene que coincidir con el valor de la imagen.

$$
\lim_{x \to a} [f(x)] = f(a)
$$

### 1.2. Continuidad en un intervalo

#### 1.2.1. Intervalo abierto

Es continua en un intervalo abierto $(a, b)$ si lo es en cada punto perteneciente al intervalo.

#### 1.2.2. Intervalo cerrado

Es continua en un intervalo cerrado si lo es en uno abierto $(a, b)$ y además posee continuidad lateral en los extremos.

$$
\lim_{x \to a^{+}} [f(x)] = f(a)
$$

$$
\lim_{x \to b^{-}} [f(x)] = f(b)
$$

---

## 2. Propiedades

Si $f$ y $g$ son funciones continuas en $x = c$ se pueden aplicar ciertas propiedades.

### 2.1. Suma

$f + g$ es continua en $c$.

### 2.2. Resta

$f - g$ es continua en $c$.

### 2.3. Producto

$f \cdot g$ es continua en $c$.

### 2.4. Producto por un escalar

$k \cdot f$ es continua en $c$ para cualquier $k \in \mathbb{R}$.

### 2.5. Cociente

$\frac{f}{g}$ es continua en $c$ si $g(0) \neq 0$.

### 2.6. Potencia

$f^{g}$ es continua en $c$, dentro del dominio de definición.

### 2.7. Composición

Si $f$ es continua en $c$ y $g$ es continua en $f(c)$, entonces $(g o f)$ es continua en $c$.

---

## 3. Familias de funciones y su continuidad

### 3.1. Polinómicas

Son continuas en todo su dominio ($\mathbb{R}$).

$$
f(x) = a_{n}x^{n} + \dots + a_{1}x + a_{0}
$$

### 3.2. Racionales

Son continuas en su dominio, donde el denominador **no** es 0.

$$
f(x) = \frac{P(x)}{Q(x)}, \ Q(x) \neq 0
$$

### 3.3. Radicales

Son continuas en su dominio, teniendo en cuenta índices pares y valores negativos.

$$
f(x) = \sqrt[n]{x}, n \text{ es par}, x \geq 0
$$

### 3.4. Trigonométricas

$\sin(x)$ y $\cos(x)$ son continuas en $\mathbb{R}$. $\tan(x)$ es discontinua en $x = \frac{\pi}{2} + k\pi$.

$$
\sin(x), \cos(x), \tan(x), \dots
$$

### 3.5. Exponenciales

Son continuas en todo su dominio ($\mathbb{R}$).

$$
f(x) = a^{x}, a > 0
$$

### 3.6. Logarítmicas

Son continuas en $(0, + \infty)$.

$$
f(x) = \log_{a}(x), x > 0
$$

---

## 3. Discontinuidades

Las discontinuidades se pueden clasificar en **evitables** y **esenciales**.

### 3.1. Evitables

Existe el límite finito $L$, pero $f(c) \neq L$ o $f(c)$ no existe.

Se puede remover la discontinuidad redefiniendo $f$.

El límite existe.

#### 3.1.1. Ejemplo

$$
f(x) = \frac{x^{2} - 1}{x - 1}
$$

En $x = 1$.

- El límite existe.
- $f(1)$ no existe.

### 3.2. Esenciales

No existe el límite finito en el punto.

Pueden dividirse en **salto finito** y **salto infinito**.

#### 3.2.1. Salto finito

Ambos son finitos.

$$
\lim_{x \to c^{-}} [f(x)] \neq \lim_{x \to c^{+}} [f(x)]
$$

#### 3.2.2. Salto infinito

Al menos un límite lateral tiende a $\plusmn \infty$, o sea, tiene una **asíntota vertical**.

**Por ejemplo**:

$$
f(x) = \frac{1}{x - 2}
$$

En $x = 2$ hay una discontinuidad esencial.

---

## 4. Comportamiento asintótico

### 4.1. Asíntota vertical

La recta $x = c$ es una asíntota vertical si:

$$
\lim_{x \to c} f(x) = \plusmn \infty
$$

### 4.2. Asíntota horizontal

La recta $y = L$ es una asíntota horizontal si:

$$
\lim_{x \to \pm\infty} f(x) = L
$$

> Siendo $L$ un número finito.

### 4.3. Asíntota oblicua

La recta $y = px + b$ ($p \neq 0$) es una asíntota oblicua si:

- **Pendiente**: $p = \lim_{x \to \infty} \frac{f(x)}{x}$.
- **Ordenada**: $b = \lim_{x \to \infty} [f(x) - p \cdot x]$.

---

## 5. Teoremas

### 5.1. Teorema del Valor Intermedio

Si $f$ es continua en $[a, b]$, la función toma todos los valores correspondientes entre $f(a)$ y $f(b)$.

O sea, para cualquier $N$ entre $f(a)$ y $f(b)$, existe un $c \in (a, b)$ tal que $f(c) = N$.

### 5.2. Teorema de Bolzano (Corolario)

Si $f$ es continua en el intervalo cerrado $[a, b]$ y tiene distinto signo en sus extremos $(f(a) \cdot g(b) < 0)$, entonces existe por lo menos un punto $c \in (a, b)$ tal que $f(c) = 0$.

Este punto es una **raíz** de la función.

### 5.3. Teorema de Weierstrass

Toda función continua en un intervalo cerrado alcanza su máximo y mínimo absoluto dentro del intervalo o en sus extremos.

Si $f$ es continua en un intervalo cerrado $[a, b]$, entonces $f$ alcanza siempre un **máximo absoluto** y un **mínimo absoluto** dentro de dicho intervalo.
