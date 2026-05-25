# Números factoriales y aproximación polinómica

Para entender la utilidad práctica de los factoriales, es conveniente analizar un problema de conteo y ordenamiento combinatorio clásico:

```{admonition} Problema
---
class: attention
---
Si una persona tiene 5 tareas diferentes por realizar, ¿de cuántas formas distintas puede ordenarlas cronológicamente?
```

Para asignar una tarea a la primera posición cronológica se dispone de 5 opciones posibles. Una vez ocupado ese lugar, restan 4 opciones elegibles para la segunda posición, 3 para la tercera, 2 para la cuarta y un único elemento para la última tarea. Aplicando el principio multiplicativo de conteo se obtiene el total de permutaciones posibles:

$$
5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120
$$

Este producto sucesivo decreciente de números naturales se expresa matemáticamente mediante la notación compacta de $5!$ y se lee formalmente como **cinco factorial**.

---

(numeros-factoriales-1-definicion)=

## 1. Definición

El factorial de un número natural $n$ se define formalmente como el producto continuo de todos los números naturales anteriores a él e inclusive de forma decreciente hasta la unidad:

$$
n! = n \cdot (n - 1) \cdot (n - 2) \cdot \dots \cdot 2 \cdot 1 \quad \text{donde } n \in \mathbb{N}
$$

(numeros-factoriales-1-1-propiedades-operatorias)=

### 1.1. Propiedades operatorias

El cálculo analítico y la simplificación de expresiones factoriales se rige por las siguientes propiedades fundamentales:

(numeros-factoriales-1-1-1-caso-base)=

#### 1.1.1. Caso base

Para dar consistencia matemática al álgebra combinatoria y permitir el correcto desarrollo de las fórmulas polinómicas de Taylor cuando se evalúa la derivada de orden cero, se define convencionalmente que:

$$
0! = 1
$$

(numeros-factoriales-1-1-2-propiedad-de-recurrencia)=

#### 1.1.2. Propiedad de recurrencia

Establece que el factorial de cualquier número entero positivo puede descomponerse como el producto de ese mismo número por el factorial de su antecesor. Esta propiedad es la herramienta principal para simplificar cocientes en límites y criterios de convergencia de series:

$$
n! = n \cdot (n - 1)!
$$

---

(numeros-factoriales-2-aproximacion-de-funciones)=

## 2. Aproximación de funciones

El objetivo central es aproximar localmente el comportamiento de una función $f(x)$ que admite derivadas sucesivas mediante un polinomio algebraico estructurado $p(x)$ en las inmediaciones de un punto de interés centrado en $x_{0}$.

Para lograr que el polinomio emule geométricamente a la curva con la mayor fidelidad posible, se impone la condición de rigidez de que tanto el valor de la función como el de sus derivadas de orden superior coincidan exactamente en el punto de contacto $x_{0}$:

- $p(x_{0}) = f(x_{0})$
- $p'(x_{0}) = f'(x_{0})$
- $p''(x_{0}) = f''(x_{0})$

(numeros-factoriales-2-1-polinomio-de-taylor-de-grado-1)=

### 2.1. Polinomio de Taylor de grado 1

La aproximación más simple es el desarrollo lineal de primer orden. Esta estructura geométrica coincide de forma exacta con la ecuación de la recta tangente calculada en el punto $x_{0}$:

$$
p_{1}(x) = f(x_{0}) + f'(x_{0}) \cdot (x - x_{0})
$$

(numeros-factoriales-2-2-polinomio-de-taylor-de-grado-2)=

### 2.2. Polinomio de Taylor de grado 2

Para capturar la curvatura y la concavidad local de la función original, se propone un polinomio genérico de segundo grado estructurado de la siguiente forma:

$$
p_{2}(x) = a \cdot (x - x_{0})^{2} + b \cdot (x - x_{0}) + c
$$

Para hallar los coeficientes $\{a, b, c\}$, se deriva sucesivamente el polinomio y se aplican las condiciones de igualdad en el centro $x = x_{0}$:

(numeros-factoriales-2-2-1-evaluacion-por-imagen)=

#### 2.2.1. Evaluación por imagen

$$
p_{2}(x_{0}) = a \cdot (x_{0} - x_{0})^2 + b \cdot (x_{0} - x_{0}) + c = c \implies c = f(x_{0})
$$

(numeros-factoriales-2-2-2-evaluacion-por-derivada-primera)=

#### 2.2.2. Evaluación por derivada primera

$$
p_{2}'(x) = 2 \cdot a \cdot (x - x_{0}) + b \implies p_{2}'(x_{0}) = 2 \cdot a \cdot (x_{0} - x_{0}) + b = b \implies b = f'(x_{0})
$$

(numeros-factoriales-2-2-3-evaluacion-por-derivada-segunda)=

#### 2.2.3. Evaluación por derivada segunda

$$
p_{2}''(x) = 2 \cdot a \implies p_2''(x_0) = 2 \cdot a \implies 2 \cdot a = f''(x_{0}) \implies a = \frac{f''(x_{0})}{2}
$$

Sustituyendo los coeficientes en la propuesta inicial, el polinomio cuadrático de Taylor resulta:

$$
p_{2}(x) = f(x_{0}) + f'(x_{0}) \cdot (x - x_{0}) + \frac{f''(x_{0})}{2} \cdot (x - x_{0})^{2}
$$

(numeros-factoriales-2-3-polinomio-de-taylor-de-orden-n)=

### 2.3. Polinomio de Taylor de orden $n$

Generalizando el procedimiento analítico mediante inducción para una función que admite derivadas hasta un orden finito $n$, los coeficientes de las potencias sucesivas quedan determinados por el operador factorial en sus denominadores. El polinomio aproximador general se define como:

$$
p_{n}(x) = f(x_{0}) + f'(x_{0}) \cdot (x - x_{0}) + \frac{f''(x_{0})}{2!} \cdot (x - x_{0})^{2} + \dots + \frac{f^{n}(x_{0})}{n!} \cdot (x - x_{0})^{n}
$$

Utilizando la notación de sumatoria compacta (**símbolo Sigma**), se expresa formalmente como:

$$
p_{n}(x) = \sum_{k = 0}^{n} \frac{f^{k}(x_{0})}{k!} \cdot (x - x_{0})^{k}
$$

```{admonition} A tener en cuenta
---
class: important
---
Donde $f^{k}$ representa la derivada de orden $k$ de la función, asumiendo convencionalmente que la derivada de orden cero $f^{0}$ es la función original $f$ sin derivar.
```

(numeros-factoriales-2-4-ejemplo-practico-funcion-maclaurin)=

### 2.4. Ejemplo práctico: Función Maclaurin

Se desarrolla el polinomio de Taylor centrado en el origen $x_{0} = 0$ (caso especial denominado Polinomio de Maclaurin) para la función trascendente fundamental $f(x) = e^{x}$:

1. Debido a las propiedades operacionales de la función exponencial, todas sus derivadas sucesivas replican de forma idéntica a la misma función ($f^{k}(x) = e^{x}$). Al evaluar cada una de ellas en el centro del desarrollo $x = 0$, se obtiene que todos los coeficientes diferenciales valen la unidad:

   $$
   f^{k}(0) = e^{0} = 1 \quad \forall k \in \mathbb{N}_{0}
   $$

2. Sustituyendo estos valores en la fórmula general y calculando los factoriales de los denominadores ($2! = 2 \cdot 1 = 2$ y $3! = 3 \cdot 2 \cdot 1 = 6$), el polinomio aproximador de orden 3 resulta:

   $$
   p_{3}(x) = 1 + x + \frac{1}{2!} \cdot x^{2} + \frac{1}{3!} \cdot x^{3} = 1 + x + \frac{1}{2} \cdot x^{2} + \frac{1}{6} \cdot x^{3}
   $$

(numeros-factoriales-2-5-resto-de-taylor-y-estimacion-del-error)=

### 2.5. Resto de Taylor y estimación del error

Dado que un polinomio de grado finito no puede replicar con exacta fidelidad el recorrido infinito de una función trascendente, la diferencia cuantitativa existente entre el valor real de la función y el valor estimado por el polinomio en cualquier punto $x$ se define formalmente como el término del **Resto** o error de truncamiento ($R_{n}(x)$):

$$
R_{n}(x) = f(x) - p_{n}(x)
$$

Según el desarrollo matemático de la **Forma de Lagrange**, es posible cuantificar analíticamente el comportamiento de este término de error expresándolo de forma análoga a un término polinómico, pero utilizando la derivada de orden inmediatamente superior calculada en un punto flotante:

$$
R_{n}(x) = \frac{f^{n + 1}(c)}{(n + 1)!} \cdot (x - x_{0})^{n + 1}
$$

Donde $c$ es un valor real intermedio desconocido que se encuentra estrictamente comprendido dentro del intervalo abierto determinado entre el centro de aproximación $x_{0}$ y el punto de evaluación de la variable $x$ ($c \in (x_{0}, x)$ o $c \in (x, x_{0})$).
