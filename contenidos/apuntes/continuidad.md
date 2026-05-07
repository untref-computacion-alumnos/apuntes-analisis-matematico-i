# Continuidad

## Continuidad en un punto

Una función es continua en el punto $x=a$ si y sólo si se verifica que:

- **La función está definida en él:** $f(a)$ existe.
- **La función tiene límite finito en ese punto:** $\lim_{x \to a} f(x)$ existe y es finito.
- **El valor que toma la función en ese punto es igual al límite en él:** $\lim_{x \to a} f(x) = f(a)$.

Simbólicamente:

$$
f(x) \text{ es continua en } x=a \iff \lim_{x \to a} f(x) = f(a)
$$

- Se dice que una función $f$ es **discontinua** en $x=a$ si no es continua en ese punto.

### Continuidad gráficamente

La idea de un gráfico continuo es que transcurre sin interrupción y sin cambios abruptos.

![Imagen 1]()

Consideremos los siguientes casos en $x=a$:

- **Caso 1:** $f(a)$ existe, $\lim_{x \to a} f(x)$ existe, pero $\lim_{x \to a} f(x) \neq f(a)$.
- **Caso 2:** $f(a)$ no existe.
- **Caso 3:** No existe $\lim_{x \to a} f(x)$.

![Imagen 2]()

---

## Familias de funciones continuas en sus dominios

- **Polinómicas:** $f(x) = a_{n}x^{n} + \dots + a_{1}x + a_{0}$.
- **Racionales:** $f(x) = \frac{P(x)}{Q(x)}$, salvo donde $Q(x) = 0$.
- **Raíces:** $f(x) = \sqrt[n]{x}$ (si $n$ es par, $x \geq 0$).
- **Trigonométricas:** $\sin(x), \cos(x), \tan(x), \dots$.
- **Exponenciales:** $f(x) = a^{x}$ con $a > 0$.
- **Logarítmicas:** $f(x) = \log_{a}(x)$ con $x > 0$.

### Propiedades (si $f$ y $g$ son continuas en $x=a$)

- **Suma y resta:** $f(x) \pm g(x)$ es continua.
- **Producto:** $f(x) \cdot g(x)$ es continua.
- **Cociente:** $\frac{f(x)}{g(x)}$ es continua si $g(a) \neq 0$.
- **Composición:** $f(g(x))$ es continua si $g$ es continua en $x$ y $f$ en $g(x)$.

---

## Discontinuidades

### Clasificación de las discontinuidades

- **Evitables:** Se puede remover la discontinuidad redefiniendo $f$. El límite existe.
- **Inevitable o esencial:** El límite no existe o es infinito. Pueden ser de salto finito o salto infinito.

![Imagen 3]()

#### Ejemplos de clasificación

1. **En $x=1$:** Existe el límite $\lim_{x \to 1} f(x)$. [Discontinua evitable]
2. **En $x=3$:** El $\lim_{x \to 3} f(x)$ no existe por salto. [Discontinua inevitable de salto]
3. **En $x=5$:** Existe el límite $\lim_{x \to 5} f(x)$ pero no coincide con la función. [Discontinua evitable]

![Imagen 4]()

---

## Asíntotas

### Asíntota Vertical (A.V.)

La recta $x=a$ es una asíntota vertical si:

$$
\lim_{x \to a} f(x) = \infty
$$

### Asíntota Horizontal (A.H.)

La recta $y=L$ es una asíntota horizontal si:

$$
\lim_{x \to \pm\infty} f(x) = L
$$

(siendo $L$ un número finito)

### Asíntota Oblicua

La recta $y = px + b$ ($p \neq 0$) es una asíntota oblicua si:

- **Pendiente:** $p = \lim_{x \to \infty} \frac{f(x)}{x}$.
- **Ordenada:** $b = \lim_{x \to \infty} [f(x) - p \cdot x]$.

---

## TEOREMAS DE CONTINUIDAD

### Continuidad en un intervalo

Una función es continua en un intervalo cerrado $[a, b]$ si es continua en todos los puntos de $(a, b)$ y además se cumple:

- $\lim_{x \to a^{+}} f(x) = f(a)$.
- $\lim_{x \to b^{-}} f(x) = f(b)$.

![Imagen 5]()

### Teorema del Valor Intermedio

Si $f$ es continua en $[a, b]$ y $N$ es cualquier número entre $f(a)$ y $f(b)$ (con $f(a) \neq f(b)$), entonces existe un número $c$ en $(a, b)$ tal que $f(c) = N$.

![Imagen 6]()

### Teorema de Bolzano (Corolario)

Si $f$ es continua en $[a, b]$ y el signo de $f(a) \neq$ signo de $f(b)$, entonces existe al menos un $c \in (a, b)$ tal que $f(c) = 0$.

### Teorema de Weierstrass

Toda función continua en un intervalo cerrado alcanza su máximo y mínimo absoluto dentro del intervalo o en sus extremos.

![Imagen 7]()
