# Límites

## Idea intuitiva del límite

Empezamos con un número $c$ y una función $f$ definida cerca de $c$, aunque no necesariamente en el mismo $c$.

El número $L$ es el límite de $f$ cuando $x$ se aproxima (tiende) a $c$, y se escribe:

$$
\lim_{x \to c} f(x) = L
$$

Esto ocurre si y sólo si los valores de la función $f(x)$ se aproximan (tienden) a $L$ cuando $x$ se aproxima a $c$.

### Ejemplo numérico

Consideremos la función: $f(x) = x^{2} - 1$.

| $x$    | $f(x)$     |
| ------ | ---------- |
| 1.9    | 2.61       |
| 1.99   | 2.9601     |
| 1.999  | 2.996001   |
| 1.9999 | 2.99960001 |
| 2.0001 | 3.00040001 |
| 2.001  | 3.004001   |
| 2.01   | 3.0401     |
| 2.1    | 3.41       |

![Imagen 1]()

Cuando $x$ se aproxima a 2, tanto por la izquierda como por la derecha, tomando valores menores o mayores que 2, $f(x)$ se aproxima, es decir, tiende cada vez más a 3.

---

## Límites laterales

Consideremos la función: $f(x) = \frac{x^{2}-1}{x-1}$ donde $x \neq 1$. Esta función no está definida en $x=1$; sin embargo, estudiamos su comportamiento en los alrededores.

- **Por la izquierda:** $\lim_{x \to a^{-}} f(x) = L$.
- **Por la derecha:** $\lim_{x \to a^{+}} f(x) = L$.

En este caso, $\lim_{x \to 1} \frac{x^{2}-1}{x-1} = 2$.

---

## Definiciones y Casos Especiales

### Definición conceptual

Si $f(x)$ se aproxima arbitrariamente a un único número $L$ cuando $x$ se aproxima a $a$ por ambos lados, entonces el límite es $L$.

### Límites infinitos y en el infinito

- Si una función $f(x)$ crece indefinidamente cuando $x \to a$, el límite es $+\infty$ o $-\infty$.
- También se definen límites cuando la variable tiende a $+\infty$ o $-\infty$.

![Imagen 2]()

### Definición de Cauchy (Formal)

$$
\lim_{x \to a} f(x) = L \iff \forall \epsilon > 0, \exists \delta(\epsilon) > 0 \ / \ 0 < |x - a| < \delta \Rightarrow |f(x) - L| < \epsilon
$$

---

## Existencia del Límite

Para que exista el límite de una función en un punto, deben existir los límites laterales y ser iguales:

$$
\exists \lim_{x \to a} f(x) \iff \lim_{x \to a^{-}} f(x) = \lim_{x \to a^{+}} f(x) = L
$$

**Ejemplo de no existencia:**

Sea $f(x) = \begin{cases} 2, & \text{si } x < 1 \\ 3, & \text{si } x \geq 1 \end{cases}$.
Como el límite por izquierda es 2 y por derecha es 3 ($2 \neq 3$), la función no tiene límite en $x = 1$.

---

## Álgebra de Límites

Si $\lim_{x \to a} f(x) = L_{1}$ y $\lim_{x \to a} g(x) = L_{2}$, entonces:

1. El límite es único.
2. Suma: $\lim_{x \to a} [f(x) + g(x)] = L_{1} + L_{2}$.
3. Producto por escalar: $\lim_{x \to a} [\alpha f(x)] = \alpha L_{1}$.
4. Producto: $\lim_{x \to a} [f(x)g(x)] = L_{1}L_{2}$.
5. Cociente: $\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L_{1}}{L_{2}}$ (si $L_{2} \neq 0$).

---

## Teoremas Especiales

### Teorema del Sandwich

Si $g(x) \leq f(x) \leq h(x)$ y $\lim_{x \to x_{0}} g(x) = \lim_{x \to x_{0}} h(x) = l$, entonces $\lim_{x \to x_{0}} f(x) = l$.

### Límite de "Cero por Acotada"

Si $\lim_{x \to x_{0}} f(x) = 0$ y $g(x)$ es una función acotada, entonces:
$$\lim_{x \to x_{0}} f(x) \cdot g(x) = 0$$

---

## Indeterminaciones

Las indeterminaciones más comunes son:
$\frac{0}{0}, \frac{\infty}{\infty}, \infty - \infty, 0 \cdot \infty, 1^{\infty}, 0^{0}, \infty^{0}$.

### Resolución de Indeterminaciones $0/0$

- **Polinomios:** Factorizar y simplificar.
- **Radicales:** Multiplicar y dividir por el conjugado.
- **Trigonométricos:** Usar $\lim_{x \to 0} \frac{\sin x}{x} = 1$ o $\lim_{x \to 0} \frac{\tan x}{x} = 1$.

### Resolución de Indeterminaciones $\infty/\infty$

- Se extrae "factor común forzado" (la mayor potencia) en el numerador y denominador para simplificar.

### El número $e$ (Indeterminación $1^{\infty}$)

$$
\lim_{x \to \infty} \left( 1 + \frac{1}{x} \right)^{x} = e
$$

Si $\lim_{x \to x_{0}} f(x) = \infty$, entonces $\lim_{x \to x_{0}} \left( 1 + \frac{1}{f(x)} \right)^{f(x)} = e$.

---

## Cambio de Variable

Para resolver límites complejos, se puede sustituir la variable.
**Ejemplo:** $\lim_{x \to \pi} \frac{\sin x}{x - \pi}$.
Sea $t = x - \pi$. Si $x \to \pi$, entonces $t \to 0$.
El límite resulta: $\lim_{t \to 0} \frac{\sin(t+\pi)}{t} = \lim_{t \to 0} \frac{-\sin t}{t} = -1$.
