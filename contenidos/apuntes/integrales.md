# Integrales

## Introducción al concepto

El objetivo es encontrar una función $y$ cuya derivada sea conocida. Por ejemplo, si se pide hallar una función tal que su derivada sea $y' = 2$, existen múltiples posibilidades:

- $f_{1}(x) = 2x$
- $f_{2}(x) = 2x - 3$
- $f_{3}(x) = 2x + 9$

De igual manera, si se busca una función $f$ cuya derivada sea $f'(x) = 3x^2$, las opciones incluyen:

- $f_{1}(x) = x^3$
- $f_{2}(x) = x^3 - 5$
- $f_{3}(x) = x^3 + 97$

En general, si $F(x)$ es una función tal que $F'(x) = f(x)$, entonces cualquier función de la forma $F(x) + C$ (donde $C$ es una constante real) también cumple la condición.

### La Antiderivada o Primitiva

Se dice que una función $F$ es una **antiderivada** o **primitiva** de $f$ en un intervalo $I$ si $F'(x) = f(x)$ para todo $x$ en $I$.

La **Integral Indefinida** representa el conjunto de todas las antiderivadas de una función y se denota como:

$$
\int f(x) \, dx = F(x) + C
$$

Donde:

- $\int$: signo de integral.
- $f(x)$: integrando.
- $dx$: diferencial de $x$, indica la variable de integración.
- $C$: constante de integración.

### Reglas Básicas de Integración

- **Integral de una potencia:** $\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$.
- **Integral de una constante por una función:** $\int k \cdot f(x) \, dx = k \int f(x) \, dx$.
- **Integral de una suma o resta:** $\int [f(x) \pm g(x)] \, dx = \int f(x) \, dx \pm \int g(x) \, dx$.

### Tabla de Integrales Inmediatas

- $\int e^x \, dx = e^x + C$
- $\int \frac{1}{x} \, dx = \ln|x| + C$
- $\int \sin x \, dx = -\cos x + C$
- $\int \cos x \, dx = \sin x + C$
- $\int \frac{1}{1+x^2} \, dx = \arctan(x) + C$

---

## Condiciones iniciales y ecuaciones diferenciales

Una ecuación que involucra derivadas de una función desconocida se denomina **ecuación diferencial**. Resolverla implica encontrar la función original mediante la integración.

### Problema de Valor Inicial

Cuando se añade una condición específica (punto por el que pasa la curva), se puede hallar el valor exacto de la constante $C$, obteniendo una **solución particular** en lugar de una familia de soluciones.

**Ejemplo de aplicación:**
Resolver la ecuación diferencial $y' = \frac{1}{x^2+1}$ sujeta a la condición $y(\pi/2) = 0$:

1. **Separación y planteo:** $\frac{dy}{dx} = \frac{1}{x^2+1} \Rightarrow dy = \frac{1}{x^2+1} dx$.
2. **Integración:** $\int dy = \int \frac{1}{x^2+1} dx \Rightarrow y = \arctan(x) + C$ (Familia de soluciones).
3. **Uso de la condición inicial:** $0 = \arctan(\pi/2) + C \Rightarrow 0 \approx 1,0038 + C \Rightarrow C \approx -1,0038$.
4. **Solución particular:** $y = \arctan(x) - 1,0038$.

---

## Métodos de integración

### Método de Sustitución (Cambio de Variable)

Se utiliza para transformar una integral compleja en una inmediata mediante un cambio de variable $u = g(x)$.
Pasos:

1. Elegir una parte del integrando como $u$.
2. Calcular $du = g'(x) dx$.
3. Reemplazar todo en la integral en términos de $u$.
4. Integrar y volver a la variable original $x$.

### Integración por Partes

Se basa en la derivada de un producto. La fórmula es:

$$
\int u \, dv = u \cdot v - \int v \, du
$$
