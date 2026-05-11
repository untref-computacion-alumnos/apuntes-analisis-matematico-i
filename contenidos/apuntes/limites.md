# Límites

## 1. Idea intuitiva del límite

Se empieza con un número $c$ y una función $f(x)$ definida cerca de $c$, aunque no necesariamente en el mismo $c$.

El número $L$ es el límite de $f$ cuando $x$ se aproxima (**tiende**) a $c$, y se escribe:

$$
\lim_{x \to c} f(x) = L
$$

Esto ocurre **si y sólo si** los valores de la función $f(x)$ se aproximan (tienden) a $L$ cuando $x$ se aproxima a $c$.

### 1.1. Ejemplo

Considerando la función $f(x) = x^{2} - 1$:

```{image} ../imagenes/apuntes/limites/imagen-1.png
:alt: $f(x) = x^{2} - 1$
:width: 100%
:height: 100%
:align: center
```

se tiene el siguiente cuadro:

| **$x$** | **$f(x)$** |
| :-----: | :--------: |
|   1.9   |    2.61    |
|  1.99   |   2.9601   |
|  1.999  |  2.996001  |
| 1.9999  | 2.99960001 |
| 2.0001  | 3.00040001 |
|  2.001  |  3.004001  |
|  2.01   |   3.0401   |
|   2.1   |    3.41    |

Cuando **$x$** se aproxima a **$2$**, tanto por la **izquierda** como por la **derecha**, tomando valores menores o mayores que **$2$**, $f(x)$ se aproxima, es decir, tiende cada vez más a **$3$**.

---

## 2. Definiciones y Casos Especiales

### 2.1. Definición conceptual del límite

Si $f(x)$ se aproxima arbitrariamente a un único número $L$ cuando $x$ se aproxima a $c$ por ambos lados, entonces el límite es $L$.

### 2.2. Límites laterales

Considerando la función: $f(x) = \frac{x^{2} - 1}{x - 1}$, donde $x \neq 1$:

```{image} ../imagenes/apuntes/limites/imagen-2.png
:alt: $f(x) = \frac{x^{2} - 1}{x - 1}$
:width: 100%
:height: 100%
:align: center
```

Esta función **no está definida** en $x = 1$, sin embargo, se estudia su comportamiento en los alrededores.

| **$x$** | **$0.5$** | **$0.75$** | **$0.9$** | **$0.99$** | **$0.999$** | **$1$** | **$1.001$** | **$1.01$** | **$1.1$** | **$1.25$** | **$1.5$** |
| :-----: | :-------: | :--------: | :-------: | :--------: | :---------: | :-----: | :---------: | :--------: | :-------: | :--------: | :-------: |
| $f(x)$  |   $1.5$   |   $1.75$   |   $1.9$   |   $1.99$   |   $1.999$   |   $?$   |   $2.001$   |   $2.01$   |   $2.1$   |   $2.25$   |   $2.5$   |

#### 2.2.1. Límite lateral por la izquierda

Se estudia el límite por la izquierda, con el signo $c^{-}$:

$$
\lim_{x \to c^{-}} f(x) = L
$$

#### 2.2.2. Límite lateral por la derecha

Se estudia el límite por la derecha, con el signo $c^{+}$:

$$
\lim_{x \to c^{+}} f(x) = L
$$

---

Estudiando los límites laterales de la función:

$$
\lim_{x \to 1^{-}} \frac{x^{2} - 1}{x - 1} = 2
$$

$$
\lim_{x \to 1^{+}} \frac{x^{2} - 1}{x - 1} = 2
$$

Entonces el límite:

$$
\lim_{x \to 1} \frac{x^{2} - 1}{x - 1} = 2
$$

#### 2.2.3. Ejemplo

Siendo $f(x) = \frac{1}{x - 1}$:

```{image} ../imagenes/apuntes/limites/imagen-3.png
:alt: $f(x) = \frac{1}{x - 1}$
:width: 100%
:height: 100%
:align: center
```

Se quiere calcular:

$$
\lim_{x \to 1} \frac{x^{2} - 1}{x - 1}
$$

- Por izquierda:

$$
\lim_{x \to 1^{-}} \frac{x^{2} - 1}{x - 1} = - \infty
$$

- Por derecha:

$$
\lim_{x \to 1^{+}} \frac{x^{2} - 1}{x - 1} = + \infty
$$

Por lo tanto:

$$
\lim_{x \to 1} \frac{x^{2} - 1}{x - 1} = \nexists
$$

### 2.3. Definición de Cauchy o Definición Formal

El límite de una función $y = f(x)$ es $L$, si es posible encontrar un valor de $f$ tan próximos a $L$ como se quiera, con la única condición de tomar valores de $x$ suficientemente próximos al punto $c$.

Se observa que, cuando los valores de $x$ se acercan a $c$ por derecha y por izquierda, los correspondientes valores de la función se van acercando a $L$.

Matemáticamente, el límite de una función se expresa de la siguiente forma (**Límite de Cauchy**):

$$
\lim_{x \to c} f(x) = L \iff \forall \epsilon > 0, \ \exists \delta(\epsilon) > 0 \ / \ 0 < |x - c| < \delta \Rightarrow |f(x) - L| < \epsilon
$$

Es decir:

> La función $f(x)$ tiene como límite a $L$ cuando $x$ tiende a $x_0$ si para un número real positivo $\epsilon$ mayor que cero, existe un número positivo $\delta$ dependiente de $\epsilon$ tal que para todos los valores de $x$ distintos que cumplan la condición $|x - x_0| < \delta$ se cumple que $|f(x) - L| < \epsilon$.

---

## 3. Comportamientos Infinitos

### 3.1. Límites infinitos

Se dan cuando la función $f(x)$ crece o decrece sin cota a medida que $x$ se aproxima a un valor finito $c$. Esto indica la presencia de una **asíntota vertical**.

#### 3.1.1 Ejemplo

Para la función:

$$
f(x) = \frac{1}{x - 1}
$$

```{image} ../imagenes/apuntes/limites/imagen-3.png
:alt: $f(x) = \frac{1}{x - 1}$
:width: 100%
:height: 100%
:align: center
```

- **Límite por izquierda**: $$\lim_{x \to 1^{-}} [\frac{1}{x - 1}] = - \infty$$
- **Límite por derecha**: $$\lim_{x \to 1^{+}} [\frac{1}{x - 1}] = + \infty$$
- **Conclusión**: $$\lim_{x \to 1} [\frac{1}{x - 1}] = \nexists$$

### 3.2. Límites en el infinito

Se definen cuando la variable independiente $x$ tiende a $+ \infty$ o $- \infty$. Si este límite es un valor finito $L$, la función posee una **asíntota horizontal** en $y = L$.

#### 3.2.1. Ejemplo

Para la función:

$$
f(x) = 2 - \frac{1}{x}
$$

```{image} ../imagenes/apuntes/limites/imagen-6.png
:alt: $f(x) = 2 - \frac{1}{x}$
:width: 100%
:height: 100%
:align: center
```

- **Límite por izquierda**: $$\lim_{x \to - \infty} [2 - \frac{1}{x}] = 2$$
- **Límite por derecha**: $$\lim_{x \to + \infty} [2 - \frac{1}{x}] = 2$$
- **Conclusión**: En esta función, el límite infinito se da en el origen.

---

## 4. Existencia del Límite

Para que exista el límite de una función en un punto, deben **existir** los límites **laterales** y ser **iguales**.

En la definición del límite se toman valores de $x$ próximos al valor $c$ en ambos lados de $c$. Puede ocurrir que el límite exista a condición de que se tomen valores de $x$ próximos pero sólo a un lado del punto $c$, esta idea lleva a los límites laterales.

Se escribe:

$$
\lim_{x \to c^{-}} f(x) = L
$$

$$
\lim_{x \to c^{+}} f(x) = L
$$

Para la existencia del límite de una función en un punto deben existir los límites laterales y coincidir, es decir:

$$
\exists \lim_{x \to c} f(x) \iff \lim_{x \to c^{-}} f(x) = \lim_{x \to c^{+}} f(x) = L
$$

ó

$$
\exist \lim_{x \to c} f(x) \iff \begin{cases}
\exist \lim_{x \to x^{-}} f(x) = L_{1} \\
\exist \lim_{x \to x^{+}} f(x) = L_{2} \\
L_{1} = L_{2}
\end{cases}
$$

### 4.1. Ejemplo

Con la siguiente función:

$$
f(x) = \begin{cases}
2, & \text{si } x < 1 \\
3, & \text{si } x \geq 1
\end{cases}
$$

Se quiere calcular, si es posible:

$$
\lim_{x \to 1} f(x)
$$

$$
\lim_{x \to c^{-}} f(x) = 2
$$

$$
\lim_{x \to c^{+}} f(x) = 3
$$

$$
\lim_{x \to c^{-}} f(x) \ne \lim_{x \to c^{+}} f(x)
$$

La función $f$ posee en el punto $x = 1$ un límite por izquierda que es $2$ y por derecha es $3$, la función no tiene límite en $x = 1$ porque $2 \neq 3$.

---

## 5. Propiedades de Límites

Si $\lim_{x \to c} f(x) = L_{1}$ y $\lim_{x \to c} g(x) = L_{2}$, entonces:

### 5.1. Punto único de un límite

Si existe el límite de una función en un punto, es único.

### 5.2. Suma de límites

$$
\lim_{x \to c} [f(x) + g(x)] = L_{1} + L_{2}
$$

### 5.3. Producto por escalar a un límite

$$
\lim_{x \to c} [\alpha \cdot f(x)] = \alpha \cdot L_{1}
$$

### 5.4. Producto de límites

$$
\lim_{x \to a} [f(x) \cdot g(x)] = L_{1} \cdot L_{2}
$$

### 5.5. Cociente de límites

$$
\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L_{1}}{L_{2}} \iff L_{2} \neq 0
$$

### 5.6. Teorema del Sandwich

Sean:

- $x_{0} \in (a, b)$.
- $L \in \mathbb{R}$.
- $f$, $g$, $h$ funciones reales definidas en $(a, b)$, salvo quizás en $x_{0}$.

Tales que:

1. $$\forall x \in (a, b), \ x \neq x_{0} : g(x) \leq f(x) \leq h(x)$$
2. $$\lim_{x \to x_{0}} g(x) = \lim_{x \to x_{0}} = L$$

Entonces:

$$
\lim_{x \to x_{0}} f(x) = L
$$

#### 5.6.1. Ejemplo

Sea $f : \mathbb{R} \to \mathbb{R}$ tal que:

$$
\forall x \in \mathbb{R}, x \neq 0 : x^{2} - \frac{3}{4} \cdot x^{4} \leq f(x) \leq x^{2}
$$

Se quiere calcular:

$$
\lim_{x \to 0} \frac{f(x)}{x^{2}}
$$

Se pide calcular el límite de $\frac{f(x)}{x^{2}}$ cuando $x$ tiende a $0$. Como dato, $f$ es acotada:

$$
x^{2} - \frac{3}{4} \cdot x^{4} \leq f(x) \leq x^{2}
$$

Después, como $x \neq 0$ por dato, se divide por $x^{2}$ y resulta:

$$
1 - \frac{3}{4} \cdot x^{2} \leq \frac{f(x)}{x^{2}} \leq 1
$$

Entonces:

$$
\lim_{x \to 0} (1 - \frac{3}{4} \cdot x^{2}) = 1
$$

y

$$
\lim_{x \to 0} 1 = 1
$$

Por **Teorema del Sandwich**, resulta que:

$$
\lim_{x \to 0} \frac{f(x)}{x^{2}} = 1
$$

### 5.7. Límite de "Cero por Acotada"

Siendo $f$ una función real tal que $\lim_{x \to x_{0}} f(x) = 0$ y $g$ una función real acotada en $0 < |x - x_{0}| < \delta$, para $\delta > 0$.

Entonces:

$$
\lim_{x \to x_{0}} [f(x) \cdot g(x)] = 0
$$

("cero por acotada es cero")

> Las funciones $\sin(x)$ y $\cos(x)$ son ejemplos de funciones acotadas en $\mathbb{R}$.
>
> Se recuerda que $|\sin(x)| \leq 1$ y $|\cos(x)| \leq 1$, para todo $x \in \mathbb{R}$.

#### 5.7.1. Ejemplo

$$
\lim_{x \to 0} [\sin(\frac{1}{x}) \cdot \ln(x + 1)]
$$

$$
\lim_{x \to 0} [\sin(\frac{1}{x})] \cdot \lim_{x \to 0} [\ln(x + 1)]
$$

Función acotada:

$$
\lim_{x \to 0} [\sin(\frac{1}{x})]
$$

Función que da 0:

$$
\lim_{x \to 0} [\ln(x + 1)]
$$

Entonces:

$$
\lim_{x \to 0} [\sin(\frac{1}{x}) \cdot \ln(x + 1)] = 0
$$

### 5.8. Límite Trigonométrico Fundamental

$$
\lim_{x \to 0} f(x) \implies \lim_{x \to 0} \frac{\sin(f(x))}{f(x)} = 1
$$

1. Se sabe que:

   $$
   \sin(x) < x < \tan(x)
   $$

2. Dividiendo por $\sin(x)$, se obtiene:

   $$
   1 < \frac{x}{\sin(x)} < \frac{1}{\cos(x)}
   $$

3. Invirtiendo las expresiones (y cambiando el sentido de las desigualdades), queda:

   $$
   1 > \frac{\sin(x)}{x} > \cos(x)
   $$

4. Se calcula el $\lim_{x \to 0}$ considerando valores positivos de $x$:

   $$
   \lim_{x \to 0^{+}} 1 = 1
   $$

   $$
   \lim_{x \to 0^{+}} \cos(x) = 1
   $$

5. Por el **Teorema del Sándwich**, se concluye que:

   $$
   \lim_{x \to 0} \frac{\sin(x)}{x} = 1
   $$

### 5.9. Límite fundamental del número $e$

Con el límite:

$$
\lim_{x \to \infty} [(1 + \frac{1}{x})^{x}] = (1 + \frac{1}{(\infty)})^{(\infty)} = (1 + 0)^{(\infty)} = 1^{(\infty)} \rightarrow indeterminación
$$

Se verifican la siguientes propiedades:

1. $$\lim_{x \to + \infty} [(1 + \frac{1}{x})^{x}] = e$$
2. $$\lim_{x \to x_{0}} [(1 + \frac{1}{f(x)})^{f(x)}] = e \iff \lim_{x \to x_{0}} [f(x)] = \infty$$

## 6. Indeterminaciones

Las indeterminaciones **no** indican que el límite no existe, si no, que **no se puede anticipar el resultado**.

Se tienen que hacer operaciones adicionales para eliminar la indeterminación y averiguar entonces el valor del límite (en el caso de que exista). Ese valor puede ser un número finito, incluido el $0$, o $+ \infty$, o bien $- \infty$.

Las indeterminaciones más comunes son:

- $\frac{0}{0}$
- $\frac{\infty}{\infty}$
- $1^{\infty}$
- $\infty - \infty$
- $0 \cdot \infty$
- $0^{0}$
- $\infty^{0}$

### 6.1. Indeterminación $\frac{0}{0}$

- **Polinomios**: Factorizar y simplificar.
- **Radicales**: Multiplicar y dividir por el conjugado.
- **Trigonométricos**: Usar $\lim_{x \to 0} \frac{\sin(x)}{x} = 1$ o $\lim_{x \to 0} \frac{\tan(x)}{x} = 1$.

#### 6.1.1. Ejemplo con función racional con polinomios

$$
\lim_{x \to 2} [\frac{x^{3} - 2x^{2} - 6x + 12}{x^{2} + 3x - 10}] = \frac{(2)^{3} - 2(2)^{2} - 6(2) + 12}{(2)^{2} + 3(2) - 10} = \frac{8 - 8 - 12 + 12}{4 + 6 - 10} = \frac{0}{0} \rightarrow indeterminación
$$

$$
\lim_{x \to 2} [\frac{x^{3} - 2x^{2} - 6x + 12}{x^{2} + 3x - 10}]
$$

$$
\lim_{x \to 2} [\frac{(x - 2) \cdot (x^{2} - 6)}{(x - 2) \cdot (x + 5)}]
$$

$$
\lim_{x \to 2} [\frac{x^{2} - 6}{x + 5}] \rightarrow sin \ indeterminación
$$

$$
\lim_{x \to 2} [\frac{x^{2} - 6}{x + 5}] = \frac{(2)^{2} - 6}{(2) + 5} = \frac{4 - 6}{7} = \frac{-2}{7}
$$

#### 6.1.2. Ejemplo con función racional con radicación

$$
\lim_{x \to 2} [\frac{\sqrt{x^{2} + 5} - 3}{x^{2} - 2x}] = \frac{\sqrt{(2)^{2} + 5} - 3}{(2)^{2} - 2(2)} = \frac{\sqrt{4 + 5} - 3}{4 - 4} = \frac{\sqrt{9} - 3}{0} = \frac{3 - 3}{0} = \frac{0}{0} \rightarrow indeterminación
$$

$$
\lim_{x \to 2} [\frac{\sqrt{x^{2} + 5} - 3}{x^{2} - 2x}]
$$

$$
\lim_{x \to 2} [\frac{\sqrt{x^{2} + 5} - 3}{x^{2} - 2x} \cdot \frac{\sqrt{x^{2} + 5} + 3}{\sqrt{x^{2} + 5} + 3}]
$$

$$
\lim_{x \to 2} [\frac{(\sqrt{x^{2} + 5} - 3) \cdot (\sqrt{x^{2} + 5} + 3)}{(x^{2} - 2x) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{(\sqrt{x^{2} + 5} - 3)^{2}}{(x^{2} - 2x) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{\sqrt{x^{2} + 5}^{2} - 3^{2}}{(x^{2} - 2x) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{x^{2} + 5 - 9}{(x^{2} - 2x) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{x^{2} - 4}{(x^{2} - 2x) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{(x + 2) \cdot (x - 2)}{(x^{2} - 2x) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{(x + 2) \cdot (x - 2)}{x \cdot (x - 2) \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{x + 2}{x \cdot (\sqrt{x^{2} + 5} + 3)}]
$$

$$
\lim_{x \to 2} [\frac{x + 2}{x \cdot (\sqrt{x^{2} + 5} + 3)}] = \frac{(2) + 2}{(2) \cdot (\sqrt{(2)^{2} + 5} + 3)} = \frac{4}{2 \cdot (\sqrt{4 + 5} + 3)} = \frac{4}{2 \cdot (\sqrt{9} + 3)} = \frac{4}{2 \cdot (3 + 3)} = \frac{4}{2 \cdot 6} = \frac{4}{12} = \frac{1}{3} \rightarrow sin \ indeterminación
$$

#### 6.1.3. Ejemplo con función trigonométrica

$$
\lim_{x \to 0} [\frac{\sin(3x)}{5x}] = \frac{\sin(3(0))}{5(0)} = \frac{\sin(0)}{0} = \frac{0}{0} \rightarrow indeterminación
$$

$$
\lim_{x \to 0} [\frac{\sin(3x)}{5x}]
$$

$$
\lim_{x \to 0} [\frac{\sin(3x)}{3x} \cdot \frac{3}{5}]
$$

Por **Límite Trigonométrico Fundamental**:

$$
\lim_{x \to 0} [\frac{\sin(3x)}{3x}] = 1
$$

Entonces:

$$
1 \cdot \frac{3}{5} = \frac{3}{5}
$$

#### 6.1.4. Ejemplo con función trigonométrica con $\tan(x)$

$$
\lim_{x \to 0} [\frac{\tan(x)}{x}]
$$

$$
\lim_{x \to 0} [\frac{\sin(x)}{x \cdot \cos(x)}]
$$

$$
\lim_{x \to 0} [\frac{\sin(x)}{x} \cdot \frac{1}{\cos(x)}]
$$

Por **Límite Trigonométrico Fundamental**:

$$
\lim_{x \to 0} [\frac{\sin(x)}{x}] = 1
$$

Además:

$$
\frac{1}{\cos(0)} = \frac{1}{1} = 1
$$

Entonces:

$$
1 \cdot 1 = 1
$$

#### 6.1.5. Ejemplo con función trigonométrica con otra resta

$$
\lim_{x \to 0} [\frac{1 - \cos(x)}{x}] = \frac{1 - \cos((0))}{0} = \frac{1 - 1}{0} = \frac{0}{0} \rightarrow indeterminación
$$

$$
\lim_{x \to 0} [\frac{1 - \cos(x)}{x}]
$$

$$
\lim_{x \to 0} [\frac{1 - \cos(x)}{x} \cdot \frac{1 + \cos(x)}{1 + \cos(x)}]
$$

$$
\lim_{x \to 0} [\frac{(1 - \cos(x)) \cdot (1 + \cos(x))}{x \cdot (1 + \cos(x))}]
$$

$$
\lim_{x \to 0} [\frac{1 - \cos^{2}(x)}{x \cdot (1 + \cos(x))}]
$$

$$
\lim_{x \to 0} [\frac{\sin^{2}(x)}{x \cdot (1 + \cos(x))}]
$$

$$
\lim_{x \to 0} [\frac{\sin(x)}{x} \cdot \frac{\sin(x)}{1 + \cos(x)}]
$$

Por **Límite Trigonométrico Fundamental**:

$$
\lim_{x \to 0} [\frac{\sin(x)}{x}] = 1
$$

Además:

$$
\frac{\sin(0)}{1 + \cos(0)} = \frac{0}{1 + 1} = \frac{0}{2} = 0
$$

Entonces:

$$
1 \cdot 0 = 0
$$

### 6.2. Indeterminación $\frac{\infty}{\infty}$

Se extrae "factor común forzado" (la mayor potencia) en el numerador y denominador para simplificar.

#### 6.2.1. Ejemplo con función racional con polinomios

$$
\lim_{x \to \infty} [\frac{3x^{4} + 5x - 4}{5x^{4} + x^{2} + 1}] = \frac{3(\infty)^{4} + 5(\infty) - 4}{5(\infty)^{4} + (\infty)^{2} + 1} = \frac{\infty + \infty - \infty}{\infty + \infty + \infty} = \frac{\infty}{\infty} \rightarrow indeterminación
$$

$$
\lim_{x \to \infty} [\frac{3x^{4} + 5x - 4}{5x^{4} + x^{2} + 1}]
$$

$$
\lim_{x \to \infty} [\frac{x^{4} \cdot (\frac{3x^{4}}{x^{4}} + \frac{5x}{x^{4}} - \frac{4}{x^{4}})}{x^{4} \cdot (\frac{5x^{4}}{x^{4}} + \frac{x^{2}}{x^{4}} + \frac{1}{x^{4}})}]
$$

$$
\lim_{x \to \infty} [\frac{x^{4} \cdot (3 + \frac{5}{x^{3}} - \frac{4}{x^{4}})}{x^{4} \cdot (5 + \frac{1}{x^{2}} + \frac{1}{x^{4}})}]
$$

$$
\lim_{x \to \infty} [\frac{3 + \frac{5}{x^{3}} - \frac{4}{x^{4}}}{{5 + \frac{1}{x^{2}} + \frac{1}{x^{4}}}}]
$$

$$
\lim_{x \to \infty} [\frac{3 + \frac{5}{x^{3}} - \frac{4}{x^{4}}}{{5 + \frac{1}{x^{2}} + \frac{1}{x^{4}}}}] = \frac{3 + \frac{5}{(\infty)^{3}} - \frac{4}{(\infty)^{4}}}{{5 + \frac{1}{(\infty)^{2}} + \frac{1}{(\infty)^{4}}}} = \frac{3 + \frac{5}{\infty} - \frac{4}{\infty}}{{5 + \frac{1}{\infty} + \frac{1}{\infty}}} = \frac{3 + 0 - 0}{{5 + 0 + 0}} = \frac{3}{5}
$$

#### 6.2.2. Ejemplo con función racional con radicación

$$
\lim_{x \to + \infty} [\frac{x^{3}}{\sqrt{x^{6} + 4}}] = \frac{(\infty)^{3}}{\sqrt{(\infty)^{6} + 4}} = \frac{\infty}{\sqrt{\infty + 4}} = \frac{\infty}{\sqrt{\infty}} = \frac{\infty}{\infty} \rightarrow indeterminación
$$

$$
\lim_{x \to + \infty} [\frac{x^{3}}{\sqrt{x^{6} + 4}}]
$$

$$
\lim_{x \to + \infty} [\frac{\frac{x^{3}}{x^{3}}}{\frac{1}{x^{3}} \cdot \sqrt{x^{6} + 4}}]
$$

$$
\lim_{x \to + \infty} [\frac{1}{\frac{1}{x^{3}} \cdot \sqrt{x^{6} + 4}}]
$$

$$
\lim_{x \to + \infty} [\frac{1}{\sqrt{\frac{1}{x^{6}}} \cdot \sqrt{x^{6} + 4}}]
$$

$$
\lim_{x \to + \infty} [\frac{1}{\sqrt{\frac{x^{6} + 4}{x^{6}}}}]
$$

$$
\lim_{x \to + \infty} [\frac{1}{\sqrt{1 + \frac{4}{x^{6}}}}]
$$

$$
\lim_{x \to + \infty} [\frac{1}{\sqrt{1 + \frac{4}{x^{6}}}}] = \frac{1}{\sqrt{1 + \frac{4}{(\infty)^{6}}}} = \frac{1}{\sqrt{1 + \frac{4}{\infty}}} = \frac{1}{\sqrt{1 + 0}} = \frac{1}{\sqrt{1}} = \frac{1}{1} = 1
$$

### 6.3. Indeterminación $1^{\infty}$

#### 6.3.1. Ejemplo 1

$$
\lim_{x \to + \infty} [(1 + \frac{1}{2x})^{x}] = (1 + \frac{1}{2(\infty)})^{(\infty)} = (1 + \frac{1}{\infty})^{\infty} = (1 + 0)^{\infty} = 1^{\infty}
$$

$$
\lim_{x \to + \infty} [(1 + \frac{1}{2x})^{x}]
$$

$$
\lim_{x \to + \infty} [(1 + \frac{1}{2x})^{\frac{2 \cdot x}{2}}]
$$

$$
\lim_{x \to + \infty} [(1 + \frac{1}{2x})^{2x \cdot \frac{1}{2}}]
$$

$$
\lim_{x \to + \infty} [((1 + \frac{1}{2x})^{2x})^{\frac{1}{2}}]
$$

$$
\lim_{x \to + \infty} [(1 + \frac{1}{2x})^{2x}]^{\lim_{x \to + \infty} [\frac{1}{2}]}
$$

Por el **Límite Fundamental del Número $e$**:

$$
\lim_{x \to + \infty} [((1 + \frac{1}{2x})^{2x})] = e
$$

Y:

$$
\lim_{x \to + \infty} [\frac{1}{2}] = \frac{1}{2}
$$

Entonces:

$$
\lim_{x \to + \infty} [(1 + \frac{1}{2x})^{2x}]^{\lim_{x \to + \infty} [\frac{1}{2}]} = e^{\frac{1}{2}}
$$

#### 6.3.2. Ejemplo 2

$$
\lim_{x \to + \infty} [(\frac{x - 1}{x + 1})^{x}] = (\frac{(\infty) - 1}{(\infty) + 1})^{(\infty)} = (\frac{\infty}{\infty})^{\infty} = 1^{\infty}
$$

$$
\lim_{x \to + \infty} [(\frac{x - 1}{x + 1})^{x}]
$$

$$
\lim_{x \to + \infty} [(\frac{x - 1}{x + 1} + 1 - 1)^{x}]
$$

$$
\lim_{x \to + \infty} [(\frac{x - 1 - x - 1}{x + 1} + 1)^{x}]
$$

$$
\lim_{x \to + \infty} [(\frac{- 2}{x + 1} + 1)^{x}]
$$

$$
\lim_{x \to + \infty} [(\frac{\frac{- 2}{- 2}}{\frac{x + 1}{- 2}} + 1)^{x}]
$$

$$
\lim_{x \to + \infty} [(\frac{1}{\frac{x + 1}{- 2}} + 1)^{x}]
$$

$$
\lim_{x \to + \infty} [(\frac{1}{\frac{x + 1}{- 2}} + 1)^{\frac{x \cdot \frac{x + 1}{- 2}}{\frac{x + 1}{- 2}}}]
$$

$$
\lim_{x \to + \infty} [(\frac{1}{\frac{x + 1}{- 2}} + 1)^{x \cdot \frac{x + 1}{- 2} \cdot \frac{-2}{x + 2}}]
$$

$$
\lim_{x \to + \infty} [((\frac{1}{\frac{x + 1}{- 2}} + 1)^{\frac{x + 1}{- 2}})^{x \cdot \frac{- 2}{x + 1}}]
$$

$$
\lim_{x \to + \infty} [((\frac{1}{\frac{x + 1}{- 2}} + 1)^{\frac{x + 1}{- 2}})^{\frac{- 2x}{x + 1}}]
$$

$$
\lim_{x \to + \infty} [((\frac{1}{\frac{x + 1}{- 2}} + 1)^{\frac{x + 1}{- 2}})]^{\lim_{x \to + \infty} [\frac{- 2x}{x + 1}]}
$$

$$
\lim_{x \to + \infty} [(1 + \frac{1}{\frac{x + 1}{- 2}})^{\frac{x + 1}{- 2}}]^{\lim_{x \to + \infty} [\frac{- 2x}{x + 1}]}
$$

Por el **Límite Fundamental del Número $e$**:

$$
\lim_{x \to + \infty} [(1 + \frac{1}{\frac{x + 1}{- 2}})^{\frac{x + 1}{- 2}}] = e
$$

Y:

$$
\lim_{x \to + \infty} [\frac{- 2x}{x + 1}] = \frac{- 2(\infty)}{(\infty) + 1} = \frac{- 2}{1} = - 2
$$

Entonces:

$$
\lim_{x \to + \infty} [(\frac{x - 1}{x + 1})^{x}] = e^{- 2}
$$

### 6.4. Indeterminación $\infty - \infty$

#### 6.4.1. Ejemplo 1

$$
\lim_{x \to \infty} [\sqrt{x^{2} + 1} - \sqrt{x^{2} - 5}] = \sqrt{(\infty)^{2} + 1} - \sqrt{(\infty)^{2} - 5} = \sqrt{\infty + 1} - \sqrt{\infty - 5} = \sqrt{\infty} - \sqrt{\infty} = \infty - \infty
$$

$$
\lim_{x \to \infty} [\sqrt{x^{2} + 1} - \sqrt{x^{2} - 5}]
$$

$$
\lim_{x \to \infty} [\sqrt{x^{2} + 1} - \sqrt{x^{2} - 5} \cdot \frac{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

$$
\lim_{x \to \infty} [\frac{\sqrt{x^{2} + 1} - \sqrt{x^{2} - 5}}{1} \cdot \frac{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

$$
\lim_{x \to \infty} [\frac{(\sqrt{x^{2} + 1} - \sqrt{x^{2} - 5}) \cdot (\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5})}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

$$
\lim_{x \to \infty} [\frac{(\sqrt{x^{2} + 1} - \sqrt{x^{2} - 5})^{2}}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

$$
\lim_{x \to \infty} [\frac{\sqrt{x^{2} + 1}^{2} - \sqrt{x^{2} - 5}^{2}}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

$$
\lim_{x \to \infty} [\frac{x^{2} + 1 - x^{2} + 5}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

$$
\lim_{x \to \infty} [\frac{6}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}]
$$

Entonces:

$$
\lim_{x \to \infty} [\frac{6}{\sqrt{x^{2} + 1} + \sqrt{x^{2} - 5}}] = \frac{6}{\sqrt{(\infty)^{2} + 1} + \sqrt{(\infty)^{2} - 5}} = \frac{6}{\sqrt{\infty + 1} + \sqrt{\infty - 5}} = \frac{6}{\sqrt{\infty} + \sqrt{\infty}} = \frac{6}{\infty + \infty} = \frac{6}{\infty} = 0
$$

#### 6.4.2. Ejemplo 2

$$
\lim_{x \to 0} [\frac{1}{x^{4}} - \frac{1}{x^{2}}] = \frac{1}{(0)^{4}} - \frac{1}{(0)^{2}} = \frac{1}{0} - \frac{1}{0} = \infty - \infty
$$

Para esta función, conviene efectuar las restas y después calcular el límite:

$$
\lim_{x \to 0} [\frac{1}{x^{4}} - \frac{1}{x^{2}}]
$$

$$
\lim_{x \to 0} [\frac{1 - x^{2}}{x^{2}}]
$$

Entonces:

$$
\lim_{x \to 0} [\frac{1 - x^{2}}{x^{2}}] = \frac{1 - (0)^{2}}{(0)^{2}} = \frac{1 - 0}{0} = \frac{1}{0} = \infty
$$

#### 6.4.3. Ejemplo 3

$$
\lim_{x \to 0} [\frac{1}{\sin^{2}(x)} - \cot^{2}(x)] = \frac{1}{\sin^{2}(0)} - \cot^{2}(0) = \frac{1}{0} - \infty = \infty - \infty
$$

$$
\lim_{x \to 0} [\frac{1}{\sin^{2}(x)} - \cot^{2}(x)]
$$

$$
\lim_{x \to 0} [\frac{1}{\sin^{2}(x)} - \frac{\cos^{2}(x)}{\sin^{2}(x)}]
$$

$$
\lim_{x \to 0} [\frac{1 - \cos^{2}(x)}{\sin^{2}(x)}]
$$

$$
\lim_{x \to 0} [\frac{\sin^{2}(x)}{\sin^{2}(x)}]
$$

$$
\lim_{x \to 0} [\frac{\sin^{2}(x)}{\sin^{2}(x)}] = 1
$$

### 6.5. Límite de funciones exponenciales

#### 6.5.1. Ejemplo

$$
\lim_{x \to \infty} [3^{- x + 2}]
$$

$$
\lim_{x \to \infty} [3^{- x} \cdot 3^{2}]
$$

$$
\lim_{x \to \infty} [\frac{1}{3^{x}} \cdot 3^{2}]
$$

$$
\lim_{x \to \infty} [\frac{1}{3^{x}}] \cdot \lim_{x \to \infty} [3^{2}]
$$

$$
\lim_{x \to \infty} [\frac{1}{3^{x}}] \cdot 3^{2}
$$

$$
3^{2} \cdot \lim_{x \to \infty} [\frac{1}{3^{x}}]
$$

$$
3^{2} \cdot \frac{\lim_{x \to \infty} [1]}{\lim_{x \to \infty} [3^{x}]}
$$

$$
3^{2} \cdot \frac{1}{\lim_{x \to \infty} [3^{x}]}
$$

$$
3^{2} \cdot \frac{1}{\infty} = 3^{2} \cdot 0 = 0
$$

## 7. Cambio de Variable

Para resolver límites complejos, se puede sustituir la variable.

### 7.1. Ejemplo 1

$$
\lim_{x \to \pi} [\frac{\sin(x)}{x - \pi}]
$$

Se puede hacer $t = x - \pi$, $\implies x \to \pi \iff t \to 0$.

Se sustituye $1$ y $2$ en $\pi$ y se obtiene:

$$
\lim_{x \to \pi} [\frac{\sin(x)}{x - \pi}]
$$

$$
\lim_{t \to 0} [\frac{\sin(t + \pi)}{t}]
$$

$$
\lim_{t \to 0} [\frac{- \sin(t)}{t}]
$$

$$
- \lim_{t \to 0} [\frac{\sin(t)}{t}]
$$

$$
- \lim_{t \to 0} [\frac{\sin(t)}{t}] = - 1
$$

### 7.2. Ejemplo 2

$$
\lim_{x \to 1} [\frac{x^{2} - \sqrt{x}}{\sqrt{x} - 1}] = \frac{(1)^{2} \sqrt{(1)}}{\sqrt{(1)} - 1} = \frac{1 - 1}{1 - 1} = \frac{0}{0}
$$

$$
\lim_{x \to 1} [\frac{x^{2} - \sqrt{x}}{\sqrt{x} - 1}]
$$

Se sustituye $x = t^{2} : x \to 1$, $\sqrt{x} = t$, $1 = t : t \to 1$

Entonces

$$
\lim_{t \to 1} [\frac{t^{2^{2}} - \sqrt{t^{2}}}{\sqrt{t^{2}} - 1}]
$$

$$
\lim_{t \to 1} [\frac{t^{4} - t}{t - 1}]
$$

$$
\lim_{t \to 1} [\frac{t \cdot (t^{3} - 1)}{t - 1}]
$$

Por diferencia de cubos perfectos:

$$
\lim_{t \to 1} [\frac{t \cdot (t - 1) \cdot (t^{2} + t + 1)}{t - 1}]
$$

$$
\lim_{t \to 1} [t \cdot (t^{2} + t + 1)]
$$

$$
\lim_{t \to 1} [t \cdot (t^{2} + t + 1)] = (1) \cdot ((1)^{2} + (1) + 1) = 1 \cdot (1 + 1 + 1) = 1 \cdot (3) = 3
$$
