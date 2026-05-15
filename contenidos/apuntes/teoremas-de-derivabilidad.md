# Teoremas y reglas de derivabilidad

(teoremas-de-derivabilidad-1-teorema-de-rolle)=

## 1. Teorema de Rolle

Sea $f(x)$ una función tal que:

- Es continua en el intervalo cerrado $[a, b]$.
- Es derivable en el intervalo abierto $(a, b)$.
- $f(a) = f(b) = 0$.

Entonces existe un número $c \in (a, b)$ y $f'(c) = 0$.

(teoremas-de-derivabilidad-1-1-interpretacion-geometrica)=

### 1.1. Interpretación geométrica

En algún punto $C$ de la curva sobre el intervalo abierto $(a, b)$, la **recta tangente $T$ es paralela al eje x**.

Esto implica que la pendiente en ese punto es nula.

(teoremas-de-derivabilidad-1-1-1-ejemplo)=

### 1.1.1. Ejemplo

Verificar que la función $f(x) = x^{3} - 2x^{2} - x + 2$ cumple las hipótesis del {ref}`teorema de Rolle<teoremas-de-derivabilidad-1-teorema-de-rolle>` en el intervalo cerrado $[-1, 2]$ y encontrar todos los puntos $c$ tales que $f'(c) = 0f$ y  $- 1 < c < 2$:

1. **Continuidad y Diferenciabilidad**: Por ser una función polinomial, es continua y diferenciable en todo punto $x$.
2. **Raíces**: Se debe verificar $f(-1) = 0$ y $f(2) = 0$.
3. **Cálculo de $c$**: Se deriva la función $f'(x) = 3x^{2} - 4x - 1 = 0$.
   - Las raíces son $x = \frac{2 \pm \sqrt{7}}{3}$.
   - Los dos valores pertenecen al intervalo $(-1, 2)$, por ende, $c = \frac{2 \pm \sqrt{7}}{3}$.

(teoremas-de-derivabilidad-1-1-2-ejemplo)=

### 1.1.2. Ejemplo

Hallar un punto $c$, correspondiente al Teorema de Rolle, para $f(x) = x^{3} - 3x^{2}$ en $[0, 3]$.

- $f$ es continua en $[0, 3]$ porque es una función **polinómica**.
- La derivada de un polinomio da un polinomio, por lo que es derivable en $\mathbb{R}$.
- $f'(x) = 3x^{2} - 6x$.
  - $Dom (f') = \mathbb{R}$
  - Es derivable en $(0, 3)$.
- $f(0) = (0)^{3} - 3(0)^{2} = 0$
- $f(3) = (3)^{3} - 3(3)^{2} = 27 - 27 = 0$

Por el {ref}`teorema de Rolle<teoremas-de-derivabilidad-1-teorema-de-rolle>`, $c \in (0, 3) \ / \ f'(c) = 0$

Rolle sólamente garantiza la existencia del punto.

$$
3c^{2} - 6c = 0 \implies 3c \cdot (c - 2) = 0 \implies c = 0 \ \text{ó} \ c = 2
$$

---

(teoremas-de-derivabilidad-2-teorema-del-valor-medio-de-lagrange)=

## 2. Teorema del valor medio de Lagrange

Sea $f(x)$ una función tal que:

- Es continua en el intervalo cerrado $[a, b]$.
- Es derivable en el intervalo abierto $(a, b)$.

Entonces existe un número $c \in (a, b)$ tal que:

$$
f'(c) = \frac{f(b) - f(a)}{b - a}
$$

(teoremas-de-derivabilidad-2-1-interpretacion-geometrica)=

### 2.1. Interpretación geométrica

En algún punto $P$ de la curva sobre el intervalo abierto $(a,b)$, la **recta tangente $T$ es paralela al segmento $AB$** (la secante que une los extremos).

(teoremas-de-derivabilidad-2-2-observaciones)=

### 2.2. Observaciones

- La fórmula también se escribe como: $f(b) - f(a) = f'(c) \cdot (b - a)$.
- El **Teorema de Rolle** es un caso particular del TVM cuando $f(a) = f(b) = 0$.

---

(teoremas-de-derivabilidad-3-regla-de-lhopital)=

## 3. Regla de L'Hôpital

Se utiliza para resolver indeterminaciones del tipo $\frac{0}{0}$ o $\frac{\infty}{\infty}$.

(teoremas-de-derivabilidad-3-1-teorema)=

### 3.1. Teorema

Suponga que $f(a) = g(a) = 0$, que $f$ y $g$ son derivables cerca de $a$, y $g'(x) \neq 0$. Entonces:
$$\text{Si } \lim_{x \to a} \frac{f(x)}{g(x)} = \frac{0}{0} \Rightarrow \lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

(teoremas-de-derivabilidad-3-2-casos-de-indeterminacion)=

### 3.2. Casos de indeterminación

- **$\infty - \infty$**: Se resuelve realizando la resta algebraica para llevarla a $\frac{0}{0}$ o $\frac{\infty}{\infty}$.
- **$0 \cdot \infty$**: Se transforma mediante una inversión: $f \cdot g = \frac{f}{1/g}$.
- **$0^{0}, 1^{\infty}, \infty^{0}$**: Se aplica logaritmo natural ($\ln$) y luego la función exponencial ($e$) para bajar el exponente.

---

(teoremas-de-derivabilidad-4-grafica-de-funciones)=

## 4. Gráfica de funciones

(teoremas-de-derivabilidad-4-1-analisis-previo-al-calculo)=

### 4.1. Análisis previo al cálculo

- Indicar el **dominio**.
- Verificar **simetría** (par o impar).
- Encontrar **intersecciones** con los ejes.

(teoremas-de-derivabilidad-4-2-analisis-con-calculo)=

### 4.2. Análisis con cálculo

- **Primera derivada ($f'$)**: Puntos críticos, intervalos de crecimiento ($f' > 0$) y decrecimiento ($f' < 0$), máximos y mínimos.
- **Segunda derivada ($f''$)**: Concavidad (hacia arriba si $f'' > 0$, hacia abajo si $f'' < 0$) y puntos de inflexión.
- **Asíntotas**: Horizontales y verticales mediante límites.

(teoremas-de-derivabilidad-4-3-resumen  )=

### 4.3. Resumen

$$
f(x) = \frac{\ln x}{x}
$$

- **Dominio**: $x > 0$.
- **Máximo local**: En $x = e$.
- **Punto de Inflexión**: En $x = e^{3/2}$.
- **Asíntotas**: $y = 0$ (horizontal) y $x = 0$ (vertical).
