# Primer Teorema Fundamental del Cálculo Integral y su aplicación

## Definición

Si $f$ es continua en un intervalo abierto $I$ que contiene a $a$, entonces, para todo $x$ en el intervalo se cumple:

$$
\frac{d}{dx} \left[ \int_{a}^{x} f(t) \, dt \right] = f(x)
$$

## Conceptos Clave

- El teorema fundamental del cálculo indica que la **derivación** y la **integración** son operaciones inversas.
- Al integrar una función continua y luego derivarla, se recupera la función original.

## Consecuencia del Teorema (Regla de la Cadena aplicada)

Si los límites de integración son funciones de $x$, la derivada se calcula como:

$$
\frac{d}{dx} \int_{a(x)}^{b(x)} f(t) \, dt = f[b(x)] \cdot b'(x) - f[a(x)] \cdot a'(x)
$$

---

## Integrales Impropias

Se presentan cuando el intervalo de integración es infinito o cuando la función presenta una discontinuidad infinita en el intervalo.

### Caso 1: Intervalos Infinitos

Si $f$ es continua en el intervalo $[a, +\infty)$, entonces:

$$
\int_{a}^{+\infty} f(x) \, dx = \lim_{r \to +\infty} \int_{a}^{r} f(x) \, dx
$$

Si el límite existe y es finito, la integral es **convergente**. Si el límite no existe o es infinito, la integral es **divergente**.

### Caso 2: Integración en toda la recta real

Para integrar desde $-\infty$ hasta $+\infty$, se divide la integral en un punto $c$:

$$
\int_{-\infty}^{+\infty} f(x) \, dx = \lim_{r \to +\infty} \int_{-r}^{c} f(x) \, dx + \lim_{r \to +\infty} \int_{c}^{r} f(x) \, dx
$$

Ambas partes deben converger para que la integral total sea convergente.

---

## Ejemplos de aplicación

### Ejemplo 1: Derivada de una integral

Hallar $F'(x)$ si $F(x) = \int_{2}^{x} (t^2 + 1) \, dt$:
Aplicando el teorema directamente:

$$
F'(x) = x^2 + 1
$$

### Ejemplo 2: Integral Impropia Convergente

Calcular $\int_{-\infty}^{+\infty} \frac{1}{1+x^2} \, dx$:

1. Se divide la integral en $c = 0$.
2. Se calculan las primitivas: $\int \frac{1}{1+x^2} \, dx = \arctan(x)$.
3. Se aplican los límites:
   - $\lim_{r \to +\infty} \arctan(x) \big|_{0}^{r} = \frac{\pi}{2} - 0 = \frac{\pi}{2}$
   - $\lim_{r \to +\infty} \arctan(x) \big|_{-r}^{0} = 0 - (-\frac{\pi}{2}) = \frac{\pi}{2}$
4. Resultado final: $\frac{\pi}{2} + \frac{\pi}{2} = \pi$.

### Ejemplo 3: Integral Impropia Divergente

Analizar la convergencia de $\int_{1}^{+\infty} \frac{1}{x} \, dx$:

$$
\lim_{r \to +\infty} \int_{1}^{r} \frac{1}{x} \, dx = \lim_{r \to +\infty} [\ln|x|]_{1}^{r} = \lim_{r \to +\infty} (\ln r - \ln 1) = \infty
$$

La integral **diverge**.
