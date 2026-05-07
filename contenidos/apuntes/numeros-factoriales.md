# Números Factoriales

## Introducción al concepto

Para entender la utilidad de los factoriales, consideremos un problema de conteo: Si una persona tiene 5 tareas diferentes, ¿de cuántas maneras puede ordenarlas?

Para la primera posición tiene 5 opciones, para la segunda 4, y así sucesivamente:

$$
5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120
$$

Este producto se expresa como $5!$ ("Cinco factorial").

## Definición y Propiedades

El factorial de un número natural $n$ se define como el producto de todos los números naturales anteriores a él e inclusive:

$$
n! = n \times (n-1) \times (n-2) \times \dots \times 1 \quad \text{donde } n \in \mathbb{N}
$$

**Propiedades fundamentales:**

- **Caso base:** $0! [cite_start]= 1$.
- **Recurrencia:** $n! [cite_start]= n \times (n-1)!$.

---

## APROXIMACIÓN DE FUNCIONES

### Planteo del Problema

[cite_start]El objetivo es aproximar una función $f(x)$ derivable mediante un polinomio $p(x)$ en las cercanías de un punto $x_{0}$. Para que la aproximación sea precisa, se busca que el polinomio y sus derivadas coincidan con los de la función en dicho punto:

- $p(x_{0}) = f(x_{0})$
- $p'(x_{0}) = f'(x_{0})$
- $p''(x_{0}) = f''(x_{0})$

### Polinomio de Taylor de Grado 1 (Recta Tangente)

La aproximación más simple es la lineal, que coincide con la ecuación de la recta tangente en $x_{0}$:

$$
p_{1}(x) = f(x_{0}) + f'(x_{0})(x - x_{0})
$$

### Polinomio de Taylor de Grado 2

Buscamos un polinomio de la forma $p_{2}(x) = a(x - x_{0})^{2} + b(x - x_{0}) + c$. Al imponer las condiciones de igualdad de derivadas, obtenemos:

- $c = f(x_{0})$
- $b = f'(x_{0})$
- $a = \frac{f''(x_{0})}{2}$

Resultando en:

$$
p_{2}(x) = f(x_{0}) + f'(x_{0})(x - x_{0}) + \frac{f''(x_{0})}{2}(x - x_{0})^{2}
$$

### Polinomio de Taylor de Orden $n$

Generalizando para una función con derivadas sucesivas hasta el orden $n$, el polinomio se define como:

$$
p_{n}(x) = f(x_{0}) + f'(x_{0})(x - x_{0}) + \frac{f''(x_{0})}{2!}(x - x_{0})^{2} + \dots + \frac{f^{(n)}(x_{0})}{n!}(x - x_{0})^{n}
$$

En notación de sumatoria:

$$
p_{n}(x) = \sum_{k=0}^{n} \frac{f^{(k)}(x_{0})}{k!}(x - x_{0})^{k}
$$

### Ejemplo de Aplicación

Para la función $f(x) = e^{x}$ centrada en $x_{0} = 0$:

1. Como todas las derivadas de $e^{x}$ son $e^{x}$, en $x=0$ todas valen $1$ ($f^{(k)}(0) = 1$).
2. El polinomio de orden 3 resulta:
    $$
    p_{3}(x) = 1 + x + \frac{1}{2}x^{2} + \frac{1}{6}x^{3}
    $$

### Resto de Taylor

La diferencia entre la función real y el polinomio de aproximación se denomina **Resto** ($R_{n}(x)$):

$$
R_{n}(x) = f(x) - p_{n}(x)
$$

Según la **Forma de Lagrange**, el resto se puede expresar como:

$$
R_{n}(x) = \frac{f^{(n+1)}(c)}{(n+1)!}(x - x_{0})^{n+1}
$$

donde $c$ es un valor comprendido entre $x$ y $x_{0}$.
