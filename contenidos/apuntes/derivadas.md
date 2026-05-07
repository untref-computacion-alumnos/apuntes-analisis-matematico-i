# Derivadas

## Definición de Derivada

Hasta el momento, de una función expresada algebraicamente $f(x)$ podemos conocer:

- Dominio
- Cortes de la gráfica con el eje X y eje Y
- Continuidad
- Asíntotas y ramas parabólicas

Sin embargo, la fórmula es poco útil cuando quiero conocer:

- **Intervalos de crecimiento / decrecimiento**
- **Máximos y mínimos relativos**

Para estos puntos es necesario el estudio de las **DERIVADAS**. La clave son las **rectas tangentes**.

![Imagen 1]()

### Pendiente y Comportamiento

- **Máximo o mínimo:** La recta tangente es horizontal (pendiente $m=0$).
- **Crecimiento:** La recta tangente tiene pendiente positiva ($m>0$).
- **Decrecimiento:** La recta tangente tiene pendiente negativa ($m<0$).

---

## Definición Formal

La derivada es un número que se obtiene mediante un límite:
$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

**En un punto $x=a$:**
$$f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

---

## Tabla de Derivadas (Funciones Simples)

| Función         | Derivada                  |
| :-------------- | :------------------------ |
| $f(x) = k$      | $f'(x) = 0$               |
| $f(x) = x$      | $f'(x) = 1$               |
| $f(x) = ax + b$ | $f'(x) = a$               |
| $f(x) = x^{n}$  | $f'(x) = n \cdot x^{n-1}$ |
| $f(x) = e^{x}$  | $f'(x) = e^{x}$           |
| $f(x) = \ln(x)$ | $f'(x) = \frac{1}{x}$     |
| $f(x) = \sin x$ | $f'(x) = \cos x$          |
| $f(x) = \cos x$ | $f'(x) = -\sin x$         |

---

## Reglas de Derivación

- **Suma/Resta:** $[u(x) \pm v(x)]' = u'(x) \pm v'(x)$
- **Producto:** $[u(x) \cdot v(x)]' = u'(x) \cdot v(x) + u(x) \cdot v'(x)$
- **Cociente:** $\left[\frac{u(x)}{v(x)}\right]' = \frac{u'(x) \cdot v(x) - u(x) \cdot v'(x)}{v^{2}(x)}$
- **Regla de la cadena (Composición):** $\frac{d}{dx} f(g(x)) = f'(g(x)) \cdot g'(x)$

---

## Rectas Tangente y Normal

Para una función en un punto $(x_{0}, y_{0})$:

- **Recta Tangente:** $y - y_{0} = f'(x_{0})(x - x_{0})$.
- **Recta Normal:** $y - y_{0} = -\frac{1}{f'(x_{0})}(x - x_{0})$.

![Imagen 2]()

---

## Continuidad y Derivabilidad

**Proposición:** Si $f$ es derivable en $x_{0} \Rightarrow f$ es continua en $x_{0}$.

- El recíproco no siempre es cierto. Ejemplo: $y = |x|$ es continua en 0 pero no es derivable allí porque sus derivadas laterales son distintas ($1$ y $-1$).

---

## Derivadas Sucesivas

Si $f'$ es derivable, su derivada se denomina **derivada segunda** ($f''$). Se pueden definir sucesivamente la tercera ($f'''$), cuarta ($f^{(iv)}$), etc.

**Ejemplo:** $f(x) = x^{6} \rightarrow f'(x) = 6x^{5} \rightarrow f''(x) = 30x^{4}$.

---

## Derivada de Función Inversa

Si $f$ es derivable y $f'(x_{0}) \neq 0$, entonces:
$$(f^{-1})'(f(x_{0})) = \frac{1}{f'(x_{0})}$$

---

## Derivación Implícita

Se utiliza cuando "y" no está despejada. Se derivan ambos miembros respecto a $x$ tratando a $y$ como una función de $x$ (aplicando regla de la cadena).

**Ejemplo:** $x^{2} + y^{2} = 25$
$2x + 2y \cdot y' = 0 \rightarrow y' = -\frac{x}{y}$.
