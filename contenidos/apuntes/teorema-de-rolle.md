# Teorema de Rolle

## Definición

Sea $f(x)$ una función tal que:

- Es continua en el intervalo cerrado $[a,b]$.
- Es diferenciable en el intervalo abierto $(a,b)$.
- $f(a) = f(b) = 0$.

Entonces existe un número $c$ tal que $a < c < b$ y $f'(c) = 0$.

### Interpretación geométrica

En algún punto $C$ de la curva sobre el intervalo abierto $(a,b)$, la **recta tangente $T$ es paralela al eje X**. Esto implica que la pendiente en ese punto es nula.

### Ejemplo de aplicación

Verificar que la función $f(x) = x^{3} - 2x^{2} - x + 2$ cumple las hipótesis en $[-1, 2]$:

1. **Continuidad y Diferenciabilidad**: Por ser una función polinomial, es continua y diferenciable en todo punto $x$.
2. **Raíces**: Se debe verificar $f(-1) = 0$ y $f(2) = 0$.
3. **Cálculo de $c$**: Se deriva la función $f'(x) = 3x^{2} - 4x - 1 = 0$.
   - Las raíces son $x = \frac{2 \pm \sqrt{7}}{3}$.
   - Ambos valores pertenecen al intervalo $(-1, 2)$, por lo tanto, $c = \frac{2 \pm \sqrt{7}}{3}$.

---

## TEOREMA DEL VALOR MEDIO (TVM)

### Definición TEOREMA DEL VALOR MEDIO (TVM)

Sea $f(x)$ una función tal que:

- Es continua en el intervalo cerrado $[a,b]$.
- Es diferenciable en el intervalo abierto $(a,b)$.

Entonces existe un número $c$ tal que $a < c < b$ y:
$$f'(c) = \frac{f(b) - f(a)}{b - a}$$

### Interpretación geométrica TEOREMA DEL VALOR MEDIO (TVM)

En algún punto $P$ de la curva sobre el intervalo abierto $(a,b)$, la **recta tangente $T$ es paralela al segmento $AB$** (la secante que une los extremos).

### Observaciones

- La fórmula también se escribe como: $f(b) - f(a) = f'(c) \cdot (b - a)$.
- El **Teorema de Rolle** es un caso particular del TVM cuando $f(a) = f(b) = 0$.

---

## REGLA DE L'HÔPITAL

Se utiliza para resolver indeterminaciones del tipo $\frac{0}{0}$ o $\frac{\infty}{\infty}$.

### Teorema

Suponga que $f(a) = g(a) = 0$, que $f$ y $g$ son derivables cerca de $a$, y $g'(x) \neq 0$. Entonces:
$$\text{Si } \lim_{x \to a} \frac{f(x)}{g(x)} = \frac{0}{0} \Rightarrow \lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

### Casos de Indeterminación

- **$\infty - \infty$**: Se resuelve realizando la resta algebraica para llevarla a $\frac{0}{0}$ o $\frac{\infty}{\infty}$.
- **$0 \cdot \infty$**: Se transforma mediante una inversión: $f \cdot g = \frac{f}{1/g}$.
- **$0^{0}, 1^{\infty}, \infty^{0}$**: Se aplica logaritmo natural ($\ln$) y luego la función exponencial ($e$) para bajar el exponente.

---

## GRÁFICA DE FUNCIONES (Guía de análisis)

### Paso 1: Análisis previo al cálculo

- Indicar el **dominio**.
- Verificar **simetría** (par o impar).
- Encontrar **intersecciones** con los ejes.

### Paso 2: Análisis con cálculo

- **Primera derivada ($f'$)**: Puntos críticos, intervalos de crecimiento ($f' > 0$) y decrecimiento ($f' < 0$), máximos y mínimos.
- **Segunda derivada ($f''$)**: Concavidad (hacia arriba si $f'' > 0$, hacia abajo si $f'' < 0$) y puntos de inflexión.
- **Asíntotas**: Horizontales y verticales mediante límites.

**Resumen del ejemplo $f(x) = \frac{\ln x}{x}$**:

- **Dominio**: $x > 0$.
- **Máximo local**: En $x = e$.
- **Punto de Inflexión**: En $x = e^{3/2}$.
- **Asíntotas**: $y = 0$ (horizontal) y $x = 0$ (vertical).
