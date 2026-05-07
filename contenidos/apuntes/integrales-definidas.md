# Integrales Definidas

## Introducción: El Problema del Área

Para motivar el concepto, consideremos el cálculo del área de un terreno irregular limitado por una curva (por ejemplo, el pie de un río) modelada por una función cuadrática $y = f(x) = 0.001x^2$.

### Sumas de Riemann

¿Cómo se calcularía de forma aproximada el área de una región $R$ bajo una curva?
Se divide el intervalo $[a, b]$ en $n$ subintervalos y se utilizan rectángulos para aproximar el área total.

- **Suma inferior:** Utiliza el valor mínimo de la función en cada subintervalo.
- **Suma superior:** Utiliza el valor máximo de la función en cada subintervalo.

A medida que el número de rectángulos aumenta ($n \to \infty$), la aproximación se vuelve más exacta, convergiendo al valor del área real.

### Definición de Integral Definida

Si $f$ es una función continua definida en $[a, b]$, la **integral definida** de $f$ desde $a$ hasta $b$ es el límite de las sumas de Riemann:

$$
\int_{a}^{b} f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x
$$

Donde:

- $a$: Límite inferior de integración.
- $b$: Límite superior de integración.
- $f(x)$: Integrando.

### Propiedades de la Integral Definida

1. **Linealidad:** $\int_{a}^{b} [f(x) \pm g(x)] \, dx = \int_{a}^{b} f(x) \, dx \pm \int_{a}^{b} g(x) \, dx$.
2. **Producto por constante:** $\int_{a}^{b} k \cdot f(x) \, dx = k \int_{a}^{b} f(x) \, dx$.
3. **Aditividad del intervalo:** $\int_{a}^{b} f(x) \, dx = \int_{a}^{c} f(x) \, dx + \int_{c}^{b} f(x) \, dx$.
4. **Inversión de límites:** $\int_{a}^{b} f(x) \, dx = -\int_{b}^{a} f(x) \, dx$.

---

## Teorema Fundamental del Cálculo

### Regla de Barrow

Si $f$ es continua en $[a, b]$ y $F$ es cualquier antiderivada de $f$, entonces:

$$
\int_{a}^{b} f(x) \, dx = F(b) - F(a)
$$

Esto permite calcular integrales definidas sin recurrir al límite de las sumas, utilizando la primitiva de la función.

---

## Cálculo de Áreas

### Caso 1: Área bajo una curva (Función positiva)

Si $f(x) \geq 0$ en $[a, b]$, el área es simplemente:

$$
Area = \int_{a}^{b} f(x) \, dx
$$

### Caso 2: Área entre una curva y el eje X (Función con cambios de signo)

Si la función tiene tramos negativos, el área total es la suma de las integrales de los valores absolutos:

$$
Area = \int_{a}^{c} f(x) \, dx - \int_{c}^{b} f(x) \, dx
$$
(Donde el tramo $[c, b]$ es negativo).

**Ejemplo:** Hallar el área limitada por $y = x^3 - 6x^2 + 8x$ y el eje OX.

1. Se encuentran los ceros de la función: $\{0, 2, 4\}$.
2. Se integra por tramos:
    $$
    Area(R) = \int_{0}^{2} (x^3 - 6x^2 + 8x) \, dx - \int_{2}^{4} (x^3 - 6x^2 + 8x) \, dx = 8 \, u^2
    $$

### Caso 3: Área entre dos curvas

Si $f(x) \geq g(x)$ en $[a, b]$, el área de la región encerrada entre ambas es:

$$
Area = \int_{a}^{b} [f(x) - g(x)] \, dx
$$

**Ejemplo:** Hallar el área entre $y = x^2$ y $y = 2x - 3$ entre $x = 2$ y $x = 4$.

$$
Area = \int_{2}^{4} [x^2 - (2x - 3)] \, dx = \frac{38}{3} \, u^2
$$
