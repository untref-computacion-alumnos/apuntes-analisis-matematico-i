# Derivadas

(derivadas-1-introduccion)=

## 1. Introducción

De una función expresada algebraicamente $f(x)$ se puede conocer:

- Dominio.
- Cortes de la gráfica con el eje $X$ y eje $Y$.
- {ref}`Continuidad<continuidad-1-1-continuidad-en-un-punto>`.
- Asíntotas y ramas parabólicas.

Sin embargo, la fórmula es poco útil cuando se quiere conocer:

- **Intervalos de crecimiento**.
- **Intervalos de decrecimiento**.
- **Máximos relativos**.
- **Mínimos relativos**.

Para esto es necesario el estudio de las **derivadas**.

La clave para su estudio son las **rectas tangentes**.

**Ejemplo**:

$$
f(x) = x^{2}
$$

Su derivada es:

$$
f'(x) = 2x
$$

```{image} ../imagenes/apuntes/derivadas/imagen-1.png
:alt: $f(x) = x^{2}$
:width: 100%
:height: 100%
:align: center
```

(derivadas-1-1-pendiente-y-comportamiento)=

### 1.1. Pendiente y comportamiento

- **Máximo o mínimo**: La recta tangente es horizontal, o sea, la pendiente es $m = 0$.
- **Crecimiento**: La recta tangente tiene pendiente positiva, o sea, la pendiente es $m > 0$.
- **Decrecimiento**: La recta tangente tiene pendiente negativa, o sea, la pendiente es $m < 0$.

---

(derivadas-2-definicion-formal)=

## 2. Definición formal

Si se quiere calcular la pendiente, la recta $t$ tangente en un punto de abscisa $x = a$. Pero sólo se tiene el punto de tangencia $A$ de la recta $t$, y para hallar su pendiente se necesitan dos puntos.

¿Qué hacer? Se resuelve en varias etapas:

- Se calcula la pendiente de la recta secante $AP$ con las coordenadas de los dos puntos $A$ y $P$.
  $$
  m = \frac{f(a + h) - f(a)}{a + h - a} = \frac{f(a + h) - f(a)}{h}
  $$
  - Si $h$ es muy pequeño, **$a + h$** está muy cerca de $a$.
- $P$ está muy próximo a $A$.
- La secante $AP$ "casi" se confunde con la tangente $t$.
- La pendiente de la secante $AP$ es "casi" la pendiente de $t$.

Ahora bien, el valor de $h$ no puede ser $0$, aunque sí todo lo pequeño que se quiera. Y acá interviene el concepto de límite.

La derivada es un número que se obtiene mediante un límite:

$$
f'(x) = m_{t} = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h}
$$

Así la **derivada** es un número que se obtiene mediante un límite.

**En un punto $x = a$**:

$$
f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}
$$

(derivadas-2-1-ejemplo)=

### 2.1. Ejemplo

Se quiere calcular la derivada de la siguiente función para $x = 2$:

$$
f(x) = \frac{x^{2}}{4}
$$

(derivadas-2-1-1-una-forma-de-calcularlo)=

#### 2.1.1. Una forma de calcularlo

Se hace lo siguiente:

$$
\lim_{h \to 0} [\frac{f(x + h) - f(x)}{h}]
$$

Se remplazan $f(2 + h)$ y $f(2)$:

$$
f(2 + h) = \frac{(2 + h)^{2}}{4}
$$

$$
f(2) = \frac{(2)^{2}}{4} = \frac{4}{4} = 1
$$

Luego:

$$
\lim_{h \to 0} [\frac{\frac{(2 + h)^{2}}{4} - 1}{h}]
$$

$$
\lim_{h \to 0} [\frac{\frac{(2 + h)^{2}}{4} - \frac{4}{4}}{h}]
$$

$$
\lim_{h \to 0} [\frac{\frac{(2 + h)^{2} - 4}{4}}{h}]
$$

$$
\lim_{h \to 0} [\frac{(2 + h)^{2} - 4}{4} \cdot \frac{1}{h}]
$$

$$
\lim_{h \to 0} [\frac{(2 + h)^{2} - 4}{4h}]
$$

$$
\lim_{h \to 0} [\frac{4 + 4h + h^{2} - 4}{4h}]
$$

$$
\lim_{h \to 0} [\frac{4h + h^{2}}{4h}]
$$

$$
\lim_{h \to 0} [\frac{h \cdot (4 + h)}{4h}]
$$

$$
\lim_{h \to 0} [\frac{4 + h}{4}]
$$

$$
\lim_{h \to 0} [\frac{4 + h}{4}] = \frac{4 + (0)}{4} = \frac{4}{4} = 1
$$

$$
f'(2) = 1
$$

(derivadas-2-1-2-otra-forma-de-calcularlo)=

#### 2.1.2. Otra forma de calcularlo

Se calculan los siguiente:

$$
f(x) = \frac{x^{2}}{4}
$$

$$
f(2) = \frac{(2)^{2}}{4} = \frac{4}{4} = 1
$$

Se calcula el límite:

$$
\lim_{x \to 2} [\frac{\frac{x^{2}}{4} - \frac{4}{4}}{x - 2}]
$$

$$
\lim_{x \to 2} [\frac{\frac{x^{2} - 4}{4}}{x - 2}]
$$

$$
\lim_{x \to 2} [\frac{x^{2} - 4}{4} \cdot \frac{1}{x - 2}]
$$

$$
\lim_{x \to 2} [\frac{(x + 2) \cdot (x - 2)}{4} \cdot \frac{1}{x - 2}]
$$

$$
\lim_{x \to 2} [\frac{x + 2}{4}]
$$

$$
\lim_{x \to 2} [\frac{x + 2}{4}] = \frac{(2) + 2}{4} = \frac{4}{4} = 1
$$

$$
f'(2) = 1
$$

(derivadas-2-1-3-en-x-=-a)=

#### 2.1.3. En $x = a$

En $x = a$:

$$
\lim_{h \to 0} = [\frac{f(a + h) - f(a)}{h}] = m_{t} = f'(a)
$$

Siendo $x = a + h \implies h = x - a$ si $h \to 0 \implies x \to a$.

$$
\lim_{h \to 0} = [\frac{f(a + h) - f(a)}{h}]
$$

$$
\lim_{x \to a} = [\frac{f(a + (x - a)) - f(a)}{x - a}]
$$

$$
\lim_{x \to a} = [\frac{f(a + x - a) - f(a)}{x - a}]
$$

$$
\lim_{x \to a} = [\frac{f(x) - f(a)}{x - a}]
$$

(derivadas-2-1-4-hallando-f-'-(x))=

#### 2.1.4 Hallando $f'(x)$

Siendo:

$$
f(x) = \frac{x^{2}}{4}
$$

Hallar $f'(x)$.

$$
\lim_{h \to 0} [\frac{f(x + h) - f(x)}{h}] = m_{t} = f'(x)
$$

$$
\lim_{h \to 0} [\frac{f(x + h) - f(x)}{h}]
$$

$$
f(x + h) = \frac{(x + h)^{2}}{4} = \frac{x^{2} + 2xh + h^{2}}{4}
$$

$$
f'(x) = \lim_{h \to 0} [\frac{\frac{x^{2} + 2xh + h^{2}}{4} - \frac{x^{2}}{4}}{h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{\frac{x^{2} + 2xh + h^{2} - x^{2}}{4}}{h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{\frac{\cancel{x^{2}} + 2xh + h^{2} - \cancel{x^{2}}}{4}}{h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{\frac{2xh + h^{2}}{4}}{h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{2xh + h^{2}}{4} \cdot \frac{1}{h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{h \cdot (2x + h)}{4} \cdot \frac{1}{h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{h \cdot (2x + h)}{4h}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{\cancel{h} \cdot (2x + h)}{4\cancel{h}}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{2x + h}{4}]
$$

$$
f'(x) = \lim_{h \to 0} [\frac{2x + h}{4}] = \frac{2x + (0)}{4} = \frac{2x}{4} = \frac{1x}{2} = \frac{1}{2}x
$$

---

(derivadas-3-tabla-de-derivadas)=

## 3. Tabla de derivadas

| **Función**          | **Derivada**                                      | **Ejemplo**                                                                    |
| :------------------- | :------------------------------------------------ | ------------------------------------------------------------------------------ |
| $f(x) = k$           | $f'(x) = 0$                                       | $f(x) = 5 \Longrightarrow f'(x) = 0$                                           |
| $f(x) = x$           | $f'(x) = 1$                                       | $f(x) = x \Longrightarrow f'(x) = 1$                                           |
| $f(x) = ax$          | $f'(x) = a$                                       | $f(x) = 7x \Longrightarrow f'(x) = 7$                                          |
| $f(x) = ax + b$      | $f'(x) = a$                                       | $f(x) = 7x + 6 \Longrightarrow f'(x) = 7$                                      |
| $f(x) = x^{n}$       | $f'(x) = n \cdot x^{n - 1}$                       | $f(x) = x^3 \Longrightarrow f'(x) = 3x^{2}$                                    |
| $f(x) = \sqrt{x}$    | $f'(x) = \frac{1}{2 \cdot \sqrt{x}}$              | $f(x) = \sqrt{x} \Longrightarrow f'(x) = \frac{1}{2 \cdot \sqrt{x}}$           |
| $f(x) = \sqrt[n]{x}$ | $f'(x) = \frac{1}{2 \cdot \sqrt[n]{x^{n - 1}}}$   | $f(x) = \sqrt[3]{x} \Longrightarrow f'(x) = \frac{1}{2 \cdot \sqrt[3]{x^{2}}}$ |
| $f(x) = e^{x}$       | $f'(x) = e^{x}$                                   | $f(x) = e^{x} \Longrightarrow f'(x) = e^{x}$                                   |
| $f(x) = a^{x}$       | $f'(x) = a^{x} \cdot \ln(a)$                      | $f(x) = 4^{x} \Longrightarrow f'(x) = 4^{x} \cdot \ln(4)$                      |
| $f(x) = \ln(x)$      | $f'(x) = \frac{1}{x}$                             | $f(x) = \ln(2x) \Longrightarrow f'(x) = \frac{1}{2x}$                          |
| $f(x) = \log_{a}(x)$ | $f'(x) = \frac{1}{x  \cdot \ln(a)}$               | $f(x) = \log_{5}{x} \Longrightarrow f'(x) = \frac{1}{x \cdot \ln(5)}$          |
| $f(x) = \sin(x)$     | $f'(x) = \cos(x)$                                 | $f(x) = \sin(x) \Longrightarrow f'(x) = \cos(x)$                               |
| $f(x) = \cos(x)$     | $f'(x) = -\sin(x)$                                | $f(x) = \cos(x) \Longrightarrow f'(x) = -\sin(x)$                              |
| $f(x) = \tan(x)$     | $f'(x) = \frac{1}{\cos^{2}(x)} = 1 + \tan^{2}(x)$ | $f(x) = \tan(x) \Longrightarrow f'(x) = 1 + \tan^{2}(x)$                       |

---

(derivadas-4-reglas)=

## 4. Reglas

(derivadas-4-1-suma-de-funciones)=

### 4.1. Suma de funciones

$$
f(x) = u(x) + v(x) \Longrightarrow f'(x) = u'(x) + v'(x)
$$

(derivadas-4-1-1-ejemplo)=

#### 4.1.1. Ejemplo

$$
f(x) = 5x^{2} + 7x - 6
$$

$$
f'(x) = (5x^{2})' + (7x)' - (6)'
$$

$$
(5x^{2})' = 5 \cdot 2x^{2 - 1} = 5 \cdot 2x^{1} = 5 \cdot 2x = 10x
$$

$$
(7x)' = 7
$$

$$
(6)' = 0
$$

$$
f'(x) = 10x + 7
$$

(derivadas-4-2-resta-de-funciones)=

### 4.2. Resta de funciones

$$
f(x) = u(x) - v(x) \Longrightarrow f'(x) = u'(x) - v'(x)
$$

(derivadas-4-2-1-ejemplo)=

#### 4.2.1. Ejemplo

$$
f(x) = 4x^{6} - 3x^{5} - 10x^{2} - 5x - 16
$$

$$
(4x^{6})' = 4 \cdot 6x^{6 - 1} = 4 \cdot 6x^{5} = 24x^{5}
$$

$$
(3x^{5})' = 3 \cdot 5x^{5 - 1} = 3 \cdot 5x^{4} = 15x^{4}
$$

$$
(10x^{2})' = 10 \cdot 2x^{2 - 1} = 10 \cdot 2x = 20x
$$

$$
(5x)' = 5
$$

$$
(16)' = 0
$$

$$
24x^{5} - 15x^{4} - 20x - 5
$$

(derivadas-4-3-producto-de-funciones)=

### 4.3. Producto de funciones

$$
f(x) = u(x) \cdot v(x) \Longrightarrow f'(x) = u'(x) \cdot v(x) + u(x) \cdot v'(x)
$$

(derivadas-4-3-1-ejemplo)=

#### 4.3.1. Ejemplo

$$
f(x) = (8x^{2} - 5x) \cdot (13x^{2} + 4)
$$

$$
(8x^{2} - 5x)' = (8 \cdot 2x^{2 - 1}) - (5) = 16x - 5
$$

$$
(13x^{2} + 4)' = (13 \cdot 2x^{2 - 1}) + (0) = 26x
$$

$$
f'(x) = (16x - 5) \cdot (13x^{2} + 4) + (8x^{2} - 5x) \cdot (26x)
$$

$$
f'(x) = 208x^{3} + 64x - 65x^{2} - 20 + 208x^{3} - 130x^{2}
$$

$$
f'(x) = 416x^{3} - 195x^{2} + 64x - 20
$$

(derivadas-4-4-cociente-de-funciones)=

### 4.4. Cociente de funciones

$$
f(x) = \frac{u(x)}{v(x)} \Longrightarrow f'(x) = \frac{u'(x) \cdot v(x) - u(x)) \cdot v'(x)}{v^{2}(x)}
$$

(derivadas-4-4-1-ejemplo)=

#### 4.4.1. Ejemplo

$$
f(x) = \frac{4x - 5}{3x + 2}
$$

$$
u(x) = 4x - 5
$$

$$
v(x) = 3x + 2
$$

$$
u'(x) = (4x - 5)' = 4
$$

$$
v'(x) = (3x + 2)' = 3
$$

$$
f'(x) = \frac{((4) \cdot (3x + 2)) - ((4x - 5) \cdot (3))}{(3x + 2)^{2}}
$$

$$
f'(x) = \frac{(12x + 8) - (12x - 15)}{(3x)^{2} + 2 \cdot 3x \cdot 2 + (2)^{2}}
$$

$$
f'(x) = \frac{12x + 8 - 12x + 15}{3^{2} \cdot x^{2} + 12x + 4}
$$

$$
f'(x) = \frac{23}{9x^{2} + 12x + 4}
$$

(derivadas-4-5-regla-de-la-cadena)=

### 4.5. Regla de la cadena

Si $y = f(u)$ y $u = g(x)$ entonces:

$$
\frac{d}{dx} f[g(x)] = f'[g(x)] \cdot g'(x)
$$

(derivadas-4-5-1-consideraciones)=

#### 4.5.1 Consideraciones

- **Interpretación**: La {ref}`regla de la cadena<derivadas-4-5-regla-de-la-cadena>` dice que la tasa de cambio de la función compuesta es el producto de la tasa de cambio de la función externa evaluada en la interna, por la tasa de cambio de la propia función interna.
- **Derivadas sucesivas**: Este resultado puede volver a derivarse siguiendo las reglas de producto y cadena nuevamente si se requiere obtener la **derivada segunda** ($f''$).
- **Puntos críticos**: Se debe recordar que se puede usar esta regla para determinar los **valores extremos** de una función (máximos y mínimos relativos) igualando la derivada a cero.

(derivadas-4-5-2-ejemplo)=

#### 4.5.2 Ejemplo

Considerando la siguiente función compuesta:

$$
f(x) = (3x^{2} - 5x)^{4}
$$

Función externa:

$$
f(x) = g(x)^{4}
$$

Función interna:

$$
g(x) = 3x^2 - 5x
$$

Se deriva cada parte por separado:

$$
f'(x) = 4 \cdot g(x)^{4 - 1} = 4 \cdot g(x)^{3}
$$

$$
g'(x) = (3 \cdot 2x^{2 - 1}) - (5) = 6x - 5
$$

Aplicando la regla de la cadena:

$$
f'(x) = (4 \cdot (3x^{2} - 5x)^{3}) \cdot (6x - 5)
$$

---

(derivadas-5-aplicaciones-geometricas)=

## 5. Aplicaciones geométricas

La derivada de una función en un punto $x_{0}$ denotada como $f'(x_{0})$, representa geométricamente la **pendiente de la recta tangente** a la gráfica de la función en el punto $P = (x_{0}, f(x_{0}))$.

A partir de este concepto, se definen dos rectas fundamentales:

(derivadas-5-1-recta-tangente)=

### 5.1. Recta tangente

Es la recta que mejor aproxima a la función en las proximidades del punto de tangencia. Su pendiente es $m_{t} = f'(x_{0})$.

Utilizando la ecuación de la recta de punto-pendiente:

$$
y - y_{0} = m \cdot (x - x_{0})
$$

Se obtiene la **ecuación de la recta tangente**:

$$
y - f(x_{0}) = f'(x_0) \cdot (x - x_{0})
$$

(derivadas-5-2-recta-normal)=

### 5.2. Recta normal

La recta normal a una curva en un punto dado es la recta que pasa por dicho punto y es **perpendicular** a la recta tangente.

Por la condición de perpendicularidad entre rectas, si la pendiente de la tangente es $m_{t}$, la pendiente de la normal ($m_{n}$) tiene que ser su recíproca opuesta:

$$
m_{n} = - \frac{1}{f'(x_{0})} \text{ siempre que } f'(x_{0}) \neq 0
$$

La **ecuación de la recta normal** queda definida como:

$$
y - f(x_{0}) = - \frac{1}{f'(x_{0})} \cdot (x - x_{0})
$$

(derivadas-5-3-ejemplo)=

### 5.3. Ejemplo

Hallar las ecuaciones de la recta tangente y normal a la función $f(x) = x^{2} + 3x$ en el punto de absisa $x_{0} = 1$.

1. Hallar la ordenada del punto $y_{0}$.
   Se evalúa la función en $x_{0}$:
   $$
   f(1) = (1)^{2} + 3(1) = 1 + 3 = 4 \implies P = (1, 4)
   $$
2. Calcular la derivada genérica.
   $$
   f'(x) = 2x + 3
   $$
3. Calcular la pendiente de la tangente $m_{t}$.
   Se evalúa la derivada en $x_{0}$:
   $$
   m_{t} = f'(1) = 2(1) + 3 = 2 + 3 = 5
   $$
4. Armar las ecuaciones:
   - Recta tangente:
     $$
     y - 4 = 5 \cdot (x - 1)
     $$
     $$
     y = 5x - 5 + 4 \implies y = 5x - 1
     $$
   - Recta normal (siendo la pendiente $m_{n} = - \frac{1}{5}$):
     $$
     y - 4 = - \frac{1}{5} \cdot (x - 1)
     $$
     $$
     y = - \frac{1}{5}x + \frac{1}{5} + 4 \implies y = - \frac{1}{5}x + \frac{21}{5}
     $$

(derivadas-5-3-1-casos-especiales-(propiedades))=

#### 5.3.1. Casos especiales (propiedades)

- **Tangente horizontal**: Si $f'(x_{0}) = 0$, la recta tangente es $y = f(x_{0})$ (paralela al eje $x$). En este caso, la recta normal es vertical: $x = x_{0}$
- **Tangente vertical**: Si el límite del cociente incremental tiende a infinito, la recta tangente es $x = x_{0}$ y la normal es $y = f(x_{0})$.

---

(derivadas-6-relacion-entre-continuidad-y-derivabilidad)=

## 6. Relacion entre continuidad y derivabilidad

**Proposición**: Siendo $f$ una función real definida en $(a, b)$ y siendo $x_{0} \in (a, b)$.

Entonces $f$ es derivable en $x_{0} \implies f$ es continua en $x_{0}$.

Equivalentemente: $f$ no es continua en $x_{0} \implies f$ no es derivable en $x_{0}$.

- **Observación**: Hay funciones continuas en un punto que no son derivables en ese punto.

(derivadas-6-1-ejemplo)=

### 6.1. Ejemplo

$y = |x|$ es continua en $0$, pero no es derivable en dicho punto.

$$
f'(0^{+}) = \lim_{h \to 0^{+}} [\frac{f(a + h) - f(a)}{h}] = \lim_{h \to 0^{+}} [\frac{- h}{h}] = 1
$$

$$
f'(0^{-}) = \lim_{h \to 0^{-}} [\frac{f(a + h) - f(a)}{h}] = \lim_{h \to 0^{+}} [\frac{- h}{h}] = - 1
$$

Como las derivadas laterales en $x = 0$ son diferentes, la función no es derivable en dicho punto.

(derivadas-6-2-ejemplo)=

### 6.2. Ejemplo

Estudiar la continuidad y derivabilidad de $f$ en $x = 1$, con la función:

$$
f(x) = \begin{cases}
- 4x + 5 & \text{si } x \leq 1 \\
- 2x^{2} + 3 & \text{si } x > 1
\end{cases}
$$

Se comprueba la derivabilidad en $x = 1$:

$$
\lim_{h \to 0^{-}} [\frac{f(1 + h) - f(1)}{h}] = \lim_{h \to 0^{-}} [\frac{(- 4 \cdot (1 + h) + 5) - 1}{h}] = \lim_{h \to 0^{-}} [\frac{- 4 - 4h + 5 - 1}{h}] = \lim_{h \to 0^{-}} [\frac{- \cancel{4} - 4h + \cancel{5} - \cancel{1}}{h}] = \lim_{h \to 0^{-}} [\frac{- 4h}{h}] = \lim_{h \to 0^{-}} [\frac{- 4\cancel{h}}{\cancel{h}}] = -4
$$

$$
\lim_{h \to 0^{+}} [\frac{f(1 + h) - f(1)}{h}] = \lim_{h \to 0^{+}} [\frac{(- 2 \cdot (1 + h)^{2} + 3) - 1}{h}] = \lim_{h \to 0^{+}} [\frac{- 2 \cdot (1 + 2h + h^{2}) + 3 - 1}{h}] = \lim_{h \to 0^{+}} [\frac{- 2 - 4h - 2h^{2} + 2}{h}] = \lim_{h \to 0^{+}} [\frac{- \cancel{2} - 4h - 2h^{2} + \cancel{2}}{h}] = \lim_{h \to 0^{+}} [\frac{- 4h - 2h^{2}}{h}] = \lim_{h \to 0^{+}} [\frac{- 4h - 2h \cdot h}{h}] = \lim_{h \to 0^{+}} [\frac{- 4h - 2h \cdot \cancel{h}}{\cancel{h}}] = \lim_{h \to 0^{+}} [- 4 - 2h] = (- 4 - 2(0)) = - 4 - 0 = - 4
$$

Como las derivadas laterales en $x = 1$ son iguales, la función es derivable en dicho punto.

Por proposición resulta que si $f$ es derivabler en $x = 1$ entonces $f$ es continua en $x = 1$.

Se comprueba la continuidad en $x = 1$.

$$
f(x) = \begin{cases}
- 4x + 5 & \text{si } x \leq 1 \\
- 2x^{2} + 3 & \text{si } x > 1
\end{cases}
$$

$$
f(1) = - 4(1) + 5 = - 4 + 5 = 1
$$

$$
\lim_{x \to 1^{-}} [- 4x + 5] = - 4(1) + 5 = - 4 + 5 = 1
$$

$$
\lim_{x \to 1^{+}} [- 2x^{2} + 3] = - 2(1)^{2} + 3 = - 2(1) + 3 = - 2 + 3 = 1
$$

Se concluye que $f$ es continua en $x = 1$.

---

(derivadas-7-derivadas-sucesivas)=

## 7. Derivadas sucesivas

Si $f$ es una función derivable en $(a, b)$, la asignación $x \to f'(x)$, para todo $x \in (a, b)$ define una nueva función real $f'$, denominada función derivada de $f$ con $Dom(f') = (a, b)$.

Si a su vez, la función $f'$ es derivable en $(c, d)$, queda definida otra nueva función real $(f')'$, la derivada de $f'$, con dominio $(c, d)$. Esta nueva función se denomina derivada segunda de la función $f$ y se la nota $f''$.

Recursivamente, mientras sigan siendo derivables en algún intervalo abierto, se definen las derivadas sucesivas de $f$. La derivada tercera $f'''$, cuarta $f''''$, etc.

(derivadas-7-1-ejemplo)=

### 7.1. Ejemplo

Para la función:

$$
f(x) = x^{6} + \sin(x) + e^{x}
$$

Calcular las derivadas sucesivas hasta el orden 5 de la función:

$$
f'(x) = 6x^{5} + \cos(x) + e^{x}
$$

$$
f''(x) = 30x^{4} - \sin(x) + e^{x}
$$

$$
f'''(x) = 120x^{3} - \cos(x) + e^{x}
$$

$$
f''''(x) = 360x^{2} + \sin(x) + e^{x}
$$

$$
f'''''(x) = 720x + \cos(x) + e^x
$$

---

(derivadas-8-derivada-de-funcion-inversa)=

## 8. Derivada de función inversa

Sea $f : [a, b] \to [c, d]$ biyectiva, luego, existe $f^{-1} : [c, d] \to [a, b]$, su función inversa, entonces:

1. Si $f$ es continua en $[a, b]$ entonces $f^{-1}$ es continua en $[c, d]$.
2. Si $f$ es derivable en $x_{0} \in (a, b)$ y $f'(x_{0}) \neq 0$, entonces $f^{-1}$ es derivable en $f(x_{0})$ y además $(f^{-1})' \cdot f(x_{0}) = \frac{1}{f'(x_{0})}$.

Llamando $y_{0} = f(x_{0})$ y teniendo en cuenta que entonces $x_{0} = f^{-1}(y_{0})$, puede reescribirse en la forma $(f^{-1})' \cdot (y_{0}) = \frac{1}{f'(f^{-1}(y_{0}))}$.

Esto permite calcular la derivada de la función inversa de una función dada sin necesidad de calcular la función inversa.

(derivadas-8-1-ejemplo)=

### 8.1. Ejemplo

Calcular $f(^{-1})' \cdot (3)$ si $f(x) = x^{5} + x^{3} + 1$

Aplicando la fórmula:

$$
(f^{-1})' \cdot (3) = \frac{1}{f'(f^{-1}(3))} \text{ y } y_{0} = 3
$$

Resulta que $y_{0} = 3$ cuando $3 = x^{5} + x^{3} + 1 \implies x_{0} = 1$

Se obtiene:

$$
(f^{-1})' \cdot (3) = \frac{1}{5x^{4} + 3x^2}_{x_{0} = 1} = \frac{1}{8}
$$

---

(derivadas-9-derivacion-de-funcion-implicita)=

## 9. Derivación de función implícita

(derivadas-9-1-funcion-explicita)=

### 9.1. Función explícita

Una función explícita es aquella en la que la variable dependiente (generalmente $y$) está despejada directamente en función de la variable independiente (generalmente $x$).

$$
y = 2x + 3, \ y = \sin(x), \ y = x^{2} + 5
$$

(derivadas-9-2-funcion-implicita)=

### 9.2. Función implicita

Una función implícita es aquella en la que la variable dependiente y la independiente aparecen mezcladas en una ecuación, sin que $y$ esté necesariariamente despejada.

$$
x^{2} + y^{2} - 25 = 0
$$

Sin embargo, hay procedimientos para calcular la derivada de este tipo de funciones, esto se conoce como **derivación implícita**.

(derivadas-9-3-derivacion-implicita)=

### 9.3. Derivación implícita

Para derivar una función definida implícitamente por una ecuación del tipo $F(x, y) = 0$, se deben seguir estos pasos:

1. **Derivar ambos miembros** de la ecuación con respecto a $x$.
2. Aplicar la **{ref}`regla de la cadena<derivadas-4-5-regla-de-la-cadena>`** cada vez que se derive un término que contenga a $y$ (recordando que $y$ es una función de $x$). Así, la derivada de $y^{n}$ va a ser $n \cdot y^{n - 1} \cdot y'$.
3. **Agrupar los términos** que contienen $y'$ en un miembro de la ecuación y los que no lo contienen en el otro.
4. **Factorizar** $y'$ y despejarlo para obtener la expresión de la derivada.

(derivadas-9-3-1-ejemplo)=

#### 9.3.1. Ejemplo

Dada la ecuación de la circunferencia centrada en el origen:

$$
x^{2} + y^{2} = 25
$$

1. Se derivan ambos miembros respecto a $x$:
   $$
   \frac{d}{dx}(x^{2}) + \frac{d}{dx}(y^{2}) = \frac{d}{dx}(25)
   $$
   $$
   2x + 2y \cdot y' = 0
   $$
2. Se despeja $y'$:
   $$
   2y \cdot y' = - 2x
   $$
   $$
   y' = \frac{- 2x}{2y} \implies \mathbf{y' = - \frac{x}{y}}
   $$

```{admonition} Nota
---
class: note
---
La derivada depende de ambas variables, lo cual es lógico ya que para una misma $x$ puede haber dos valores de $y$.
```

(derivadas-9-3-2-ejemplo)=

#### 9.3.2. Ejemplo 2

Hallar $y'$ en la ecuación:

$$
x^{3} + y^{3} = 6xy
$$

1. Se deriva respecto a $x$ (aplicando la {ref}`regla del producto<derivadas-4-3-producto-de-funciones>` en el miembro derecho):
   $$
   3x^{2} + 3y^{2} \cdot y' = 6 \cdot (1 \cdot y + x \cdot y')
   $$
   $$
   3x^{2} + 3y^{2} \cdot y' = 6y + 6xy'
   $$
2. Agrupamos los términos con $y'$ a la izquierda:
   $$
   3y^{2} \cdot y' - 6xy' = 6y - 3x^{2}
   $$
3. Factorizamos $y'$ y despejamos:
   $$
   y' (3y^{2} - 6x) = 6y - 3x^{2}
   $$
   $$
   y' = \frac{6y - 3x^{2}}{3y^{2} - 6x} \implies \mathbf{y' = \frac{2y - x^{2}}{y^{2} - 2x}}
   $$

```{admonition} Relación con la recta tangente
---
class: note
---
Recordar que una vez obtenida la expresión de $y'$, se puede calcular la pendiente de la recta tangente en cualquier punto $(x_{0}, y_{0})$ que pertenezca a la curva simplemente reemplazando ambas coordenadas en la fórmula de la derivada implícita.
```
