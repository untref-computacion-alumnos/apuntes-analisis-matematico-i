# Análisis de Funciones

## 1. Análisis de funciones a partir del gráfico

- **Dominio**: Conjunto de valores de $x$ para los que la función está definida.
- **Imagen**: Conjunto de valores de $y$ que la función efectivamente toma.
- **Puntos de corte**:
  - **Con eje $x$ (Raíces)**: Se obtienen resolviendo $f(x) = 0$.
  - **Con eje $y$ (Ordenada al origen)**: Se obtiene evaluando $f(0)$.
- **Intervalos de Positividad ($C^+$)**: $\{x \in Dom(f) \ / \ f(x) > 0\}$.
- **Intervalos de Negatividad ($C^-$)**: $\{x \in Dom(f) \ / \ f(x) < 0\}$.
- **Intervalos de Crecimiento ($I^\nearrow$)**: Intervalos de $x$ donde al aumentar la variable independiente, aumenta la imagen.
- **Intervalos de Decrecimiento ($I^\searrow$)**: Intervalos de $x$ donde al aumentar la variable independiente, disminuye la imagen.

### Ejemplo

$$
f(x) = x^{4} - 4x^{2} + 3
$$

![Imagen 1]()

- **Dominio**: $\mathbb{R}$ (todos los números reales)
- **Imagen**: $[-1, +\infty)$
- **Puntos de corte**:
  - **Con eje $x$**: resolver $x^{4} - 4x^{2} + 3 = 0 \rightarrow (x^{2}-1)(x^{2}-3) = 0 \rightarrow x = \pm 1, \pm \sqrt{3}$
  - **Con eje $y$**: $f(0) = 3 \rightarrow$ punto $(0, 3)$
- **Conjunto de positividad**: $(-\infty, -\sqrt{3}) \cup (-1, 1) \cup (\sqrt{3}, +\infty)$
- **Conjunto de negatividad**: $(-\sqrt{3}, -1) \cup (1, \sqrt{3})$
- **Conjunto de crecimiento**: $(-\sqrt{2}, 0) \cup (\sqrt{2}, +\infty)$
- **Conjunto de decrecimiento**: $(-\infty, -\sqrt{2}) \cup (0, \sqrt{2})$

---

## Funciones Polinómicas

### Función cuadrática

- Una función es una relación entre dos magnitudes, $x$ y $f(x)$, de manera que a cada valor de la primera magnitud le corresponde un único valor de la segunda, que se llama imagen.
- **Función cuadrática** es aquella función que está determinada por la ecuación de segundo grado (cuadrática) de la forma: $y = ax^{2} + bx + c$
- Donde $a, b$ y $c$ son números reales, y $a \neq 0$.
- La representación gráfica de una función cuadrática se denomina **parábola**.

#### Representación gráfica: Parábola

- Es una curva simétrica con respecto a una recta paralela al eje de las ordenadas, denominada **eje de simetría**.
- Se compone de todos los pares ordenados $(x, y)$ que satisfacen la ecuación $y = ax^{2} + bx + c$.
- Está determinada por un **vértice**, puntos de corte en los ejes y las **ramas de la parábola**.

![Imagen 2]()

#### Ramas de la parábola

Dependerá del coeficiente numérico $a$ de $x^{2}$:

- Si $a > 0$ (positivo), las ramas van hacia **arriba**.
- Si $a < 0$ (negativo), las ramas van hacia **abajo**.

![Imagen 3]()

#### Puntos de corte

- **Con el eje Y**: Determinado por el valor del término independiente $c$, ya que $f(0) = c$. Punto $(0, c)$.
- **Con el eje X**: Se iguala la función a cero $f(x) = 0$ y se resuelve mediante la fórmula:
  $$x_{1,2} = \frac{-b \pm \sqrt{b^{2} - 4ac}}{2a}$$

---

#### Ejemplo: $f(x) = x^{2} + 5x + 6$

1. **Intersección eje $y$**: $f(0) = 6 \rightarrow (0, 6)$
2. **Intersección eje $x$**:
   $$x_{1,2} = \frac{-5 \pm \sqrt{5^{2} - 4 \cdot 1 \cdot 6}}{2 \cdot 1} = \frac{-5 \pm 1}{2}$$
   $x_{1} = -2, x_{2} = -3$
3. **Vértice**:
   $x_{v} = -\frac{b}{2a} = -\frac{5}{2} = -2.5$
   $y_{v} = f(-2.5) = (-2.5)^{2} + 5(-2.5) + 6 = -0.25$
   $V = (-2.5, -0.25)$

![Imagen 4]()

- **Dominio**: $\mathbb{R}$
- **Imagen**: $[-0.25, +\infty)$

#### Formas de expresión

- **Polinómica**: $f(x) = ax^{2} + bx + c$
- **Factorizada**: $f(x) = a(x - x_{1})(x - x_{2})$
- **Canónica**: $f(x) = a(x - x_{v})^{2} + y_{v}$

---

## Función Polinómica (Grado 3)

Ejemplo: $f(x) = x^{3} - 3x + 2$

![Imagen 5]()

- **Dominio**: $\mathbb{R}$ | **Imagen**: $\mathbb{R}$
- **Corte eje $y$**: $(0, 2)$
- **Corte eje $x$**: $(-2, 0)$ y $(1, 0)$
- **Positividad**: $(-2, 1) \cup (1, +\infty)$
- **Negatividad**: $(-\infty, -2)$
- **Crecimiento**: $(-\infty, -1) \cup (1, +\infty)$
- **Decrecimiento**: $(-1, 1)$

---

## Función Radical

Expresión: $f(x) = \sqrt{x}$

![Imagen 6]()

- **Dominio**: $[0, \infty)$
- **Imagen**: $[0, \infty)$
- **Características**: Creciente en todo su dominio, siempre positiva, punto mínimo en cero.

**Ejemplo**: $f(x) = 5\sqrt{6x+3} - 1$

- **Dominio**: $6x + 3 \geq 0 \rightarrow x \geq -0.5$
- **Raíces**: $x = -0.46$ (aprox)

---

## Función Exponencial

Definida como $f(x) = a^{x}$, con $a > 0$ y $a \neq 1$.

![Imagen 7]()

- **Si $a > 1$**: La función es creciente.
- **Si $0 < a < 1$**: La función es decreciente.
- **Dominio**: $\mathbb{R}$
- **Imagen**: $(0, +\infty)$
- **Asíntota Horizontal**: $y = 0$

---

## Logaritmo

La operación $y = \log_{a}(x)$ significa que $a^{y} = x$.

- $a$: base ($a > 0, a \neq 1$)
- $x$: argumento ($x > 0$)

### Función Logarítmica

$f(x) = \log_{a}(x)$

![Imagen 8]()

- **Dominio**: $(0, +\infty)$
- **Imagen**: $\mathbb{R}$
- **Asíntota Vertical**: $x = 0$
- **Crecimiento**: Creciente si $a > 1$, decreciente si $0 < a < 1$.

---

## Trigonometría

### Razones trigonométricas

En un triángulo rectángulo:

- $\sin \theta = \frac{\text{cateto opuesto}}{\text{hipotenusa}}$
- $\cos \theta = \frac{\text{cateto adyacente}}{\text{hipotenusa}}$
- $\tan \theta = \frac{\text{cateto opuesto}}{\text{cateto adyacente}}$

![Imagen 9]()

### Funciones Trigonométricas

#### Seno ($y = \sin x$)

- **Dom**: $\mathbb{R}$ | **Im**: $[-1, 1]$
- **Cortes eje $x$**: $x = n\pi, n \in \mathbb{Z}$

#### Coseno ($y = \cos x$)

- **Dom**: $\mathbb{R}$ | **Im**: $[-1, 1]$
- **Cortes eje $x$**: $x = \frac{\pi}{2} + n\pi, n \in \mathbb{Z}$

#### Parámetros generales: $y = A \sin(B(x + C)) + D$

- **Amplitud**: $|A|$
- **Periodo**: $2\pi/B$
- **Desplazamiento vertical**: $D$

---

## Función Módulo (Valor Absoluto)

Definida como:
$$|x| = \begin{cases} -x & \text{si } x < 0 \\ x & \text{si } x \geq 0 \end{cases}$$

![Imagen 10]()

---

## Función Racional

Formada por el cociente de dos polinomios: $f(x) = \frac{Q(x)}{P(x)}$, con $P(x) \neq 0$.

- **Dominio**: $\mathbb{R}$ excepto los valores que anulan el denominador.
- **Asíntotas**: Puede tener verticales, horizontales u oblicuas.

![Imagen 11]()
