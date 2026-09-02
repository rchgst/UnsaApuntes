# Trabajo Práctico N° 2: Teoría del Error Numérico

**Cátedra:** Programación Numérica / Cálculo Numérico  
**Institución:** Universidad Nacional de Salta — Facultad de Ciencias Exactas (Departamento de Informática)  

---

### **Ejercicio N° 1**
Represente el conjunto de la Maya $F(2,3,-1,1)$ y verifique si se cumple el valor teórico para:
- La menor mantisa representable.
- La mayor mantisa representable.
- La cantidad total de números representables.
- La distancia entre $2$ representantes consecutivos bajo un mismo exponente.

**Solución:**
$$\begin{matrix}
\text{Todas las mantisas normalizadas posibles:} \\ \\
0.100 \\
0.101 \\
0.110 \\
0.111 \\ \\
\text{La menor mantisa representable se obtiene con la fórmula: } \beta^{-t} \text{ con } t \text{ dígitos.} \\
\text{La mayor mantisa representable se obtiene con la fórmula: } 1 - \beta^{-t} \text{ con } t \text{ dígitos.} \\ \\
\text{La cantidad total de números representables se calcula con: } 2 \cdot (\beta - 1) \cdot \beta^{t-1} \cdot (U - L + 1) \\ \\
\text{La distancia entre dos representantes de una malla es: } \beta^{e-t} \\ \\
\text{mantisa}_{\min} = \beta^{-t} = 2^{-3} = \frac{1}{8} = 0.125 \\
\text{mantisa}_{\max} = 1 - \beta^{-t} = 1 - \frac{1}{8} = \frac{7}{8} = 0.875 \\
\text{total} = 2 \cdot (\beta - 1) \cdot \beta^{t-1} \cdot (U - L + 1) = 2(2 - 1)(2^{3-1})(1 - (-1) + 1) = 24 \\
D = \beta^{e-t} = 2^{e-3}
\end{matrix}$$

---

### **Ejercicio N° 2**
Realizar las conversiones de cada caso. Determinar el error relativo en base decimal cometido al representar $x$ en la maya dada por redondeo simétrico.

- **i)** Sea $F(3, 2, -1, 2)$ y $x = 1.85)_{10}$
- **ii)** Sea $F(2, 3, -2, 3)$ y $x = 1.2)_{10}$
- **iii)** Sea $F(3, 2, -1, 2)$ y $x = 1.89)_{10}$
- **iv)** Sea $F(2, 3, -2, 3)$ y $x = 0.7)_{10}$

**Criterio de Redondeo Simétrico:**
$$\bar{x} = \begin{cases} a\beta^e + 1\beta^{e-t} & \text{si } b \ge 0.5 \\ a\beta^e & \text{si } b < 0.5 \end{cases}$$

**Solución:**

$$\begin{matrix}
i)~~~ F(3,2,-1,2) \\
x = 1.85)_{10} \Rightarrow 1.211\dots)_{3} \\
1.85)_{10} = 0.1211221122112\dots \times 3^1 \\
x = 0.12 \cdot 3 + 0.011221 \cdot 3^{-1} \\
\text{como } 0.011\dots < 0.5 \\
\bar{x} = 0.12 \cdot 3)_{3} = 1.2)_{3} = 1.666\dots)_{10} \\ \\
\text{error: } \left| \frac{1.85 - 1.66}{1.85} \right| = 0.1027027027\dots
\end{matrix}$$

$$\begin{matrix}
ii)~~~ F(3,2,-1,2) \\
x = 1.89)_{10} \Rightarrow 1.220\dots)_{3} \\
1.89)_{10} = 0.1220\dots \cdot 3^1 \\
x = 0.12 \cdot 3^1 + 0.20\dots \cdot 3^{-1} \\
\text{como } 0.20\dots \ge 0.5 \\
\bar{x} = (0.12 + 0.01) \cdot 3^1)_{3} = 0.20 \cdot 3^1)_{3} = 2.0)_{3} = 2)_{10} \\ \\
\text{error: } \left| \frac{1.89 - 2}{1.89} \right| = 0.0582010582\dots
\end{matrix}$$

$$\begin{matrix}
iii)~~~ F(2,3,-2,3) \\
x = 1.2)_{10} \Rightarrow 1.00110011\dots)_{2} \\
1.2)_{10} = 0.100110011\dots \cdot 2^1 \\
x = 0.100 \cdot 2^1 + 0.110011\dots \cdot 2^{-2} \\
\text{como } 0.1100\dots \ge 0.5 \\
\bar{x} = (0.100 + 0.001) \cdot 2^1)_{2} = 0.101 \cdot 2^1)_{2} = 1.01)_{2} = 1.25)_{10} \\ \\
\text{error: } \left| \frac{1.2 - 1.25}{1.2} \right| = 0.0416666666\dots
\end{matrix}$$

$$\begin{matrix}
iv)~~~ F(2,3,-2,3) \\
x = 0.7)_{10} \Rightarrow x = 0.1011001100\dots)_{2} \\
x = 0.101 \cdot 2^0 + 0.1001100\dots \cdot 2^{-3} \\
\text{como } 0.1001100\dots > 0.5 \\
\bar{x} = 0.110)_{2} = 0.75)_{10} \\ \\
\text{error: } \left| \frac{0.7 - 0.75}{0.7} \right| = 0.07142857143
\end{matrix}$$

---

### **Ejercicio N° 3**
Sea $f(x) = \dfrac{1 - \cos(x)}{x^2}$.

*Nota: Usar calculadora.*

Completar la siguiente tabla:

| $x$      | $f(x)$           | $\overline{f(x)}$ | Error Abs.     | Error Rel.     | Error Porc. |
| :------- | :--------------- | :---------------- | :------------- | :------------- | :---------- |
| `0.1`    | `0.499583472197` | $0.000152308671$  | $0.4994311635$ | $0.9996951286$ |             |
| `0.01`   | `0.4999958333`   | $0.000152308709$  | $0.4998435246$ | $0.9996953801$ |             |
| `0.001`  | `0.49999996`     | $0.000152308721$  | $0.4998476513$ | $$             |             |
| `0.0001` | `0.5`            | $0.000152311497$  | $0.4998476885$ | $4             |             |

> [!NOTE]
> **Consultar**

---

### **Ejercicio N° 4**
Determinar el error analítico de la serie $e^x$. Calcular la aproximación de $e^{0.4}$ de tal manera que en comparación con $e^{0.4} = 1.491824698\dots$, el error relativo sea menor o igual que $0.005$. Usar la serie:

$$e^x = \sum_{k=0}^{\infty} \frac{x^k}{k!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \dots$$

**Solución:**
$$\sum_{k=0}^3 \frac{x^k}{k!} = 1 + 0.4 + \frac{(0.4)^2}{2!} + \frac{(0.4)^3}{3!} = 1.490666667$$

$$\text{Error Relativo: } \left| \frac{1.491824698 - 1.490666667}{1.491824698} \right| = 0.0007762513930 \le 0.005$$

---

### **Ejercicio N° 5**
Usando la expresión:
$$\operatorname{seno}(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \dots$$

Calcular $\operatorname{seno}(0.5)$ y $\operatorname{seno}(\pi/2)$ de manera que sin considerar los errores aritméticos, el error por truncamiento sea menor que $10^{-5}$.

> [!NOTE]
> **Consultar**

---

### **Ejercicio N° 6**
Sean $a = 0.7221 \times 10^4$, $b = 0.4275 \times 10^{-2}$ y $c = 0.7645 \times 10^1$.  
Suponiendo mantisa normalizada, $t = 4$ y redondeo simétrico, realizar las siguientes operaciones y determinar los errores aritméticos:
- **a)** $((a + b) + c)$
- **b)** $((a - b) - c)$
- **c)** $a \cdot (b / c)$

**Solución:**

$$\begin{matrix}
a)~~~((a+b)+c) \\
(7221 + 0.004275) + 7.645 = 7228.649275 \rightarrow \text{resultado sin error.} \\ \\
0.7221 \cdot 10^4 + 0.4275 \cdot 10^{-2} = 7221.004275 = 0.7221004275 \cdot 10^4 \\
x = 0.7221 \cdot 10^4 + 0.004275 \cdot 10^0 \\
\text{como } d_5 = 0 < 5 \Rightarrow \bar{x}_1 = 0.7221 \cdot 10^4 = 7221 \\ \\
0.7221 \cdot 10^4 + 0.7645 \cdot 10^1 = 7228.645 = 0.7228645 \cdot 10^4 \\
x = 0.7228 \cdot 10^4 + 0.645 \cdot 10^0 \\
\text{como } d_5 = 6 \ge 5 \Rightarrow \bar{x} = 0.7229 \cdot 10^4 = 7229 \\ \\
\text{error: } \left| \frac{7228.649275 - 7229}{7228.649275} \right| = 0.00004851874 \Rightarrow 0.004851874 \% \\ \\ \\

b)~~~((a-b)-c) \\
(7221 - 0.004275) - 7.645 = 7213.350725 \rightarrow \text{resultado sin error.} \\ \\
0.7221 \cdot 10^4 - 0.4275 \cdot 10^{-2} = 7220.995725 = 0.7220995725 \cdot 10^4 \\
x = 0.7220 \cdot 10^4 + 0.995725 \cdot 10^0 \\
\text{como } d_5 = 9 \ge 5 \Rightarrow \bar{x}_1 = 0.7221 \cdot 10^4 = 7221 \\ \\
0.7221 \cdot 10^4 - 0.7645 \cdot 10^1 = 7213.355 = 0.7213355 \cdot 10^4 \\
x = 0.7213 \cdot 10^4 + 0.355 \cdot 10^0 \\
\text{como } d_5 = 3 < 5 \Rightarrow \bar{x} = 0.7213 \cdot 10^4 = 7213 \\ \\
\text{error: } \left| \frac{7213.350725 - 7213}{7213.350725} \right| = 0.00004862165 \Rightarrow 0.004862165 \% \\ \\ \\

c)~~~a \cdot (b / c) \\
7221 \cdot \left( \frac{0.004275}{7.645} \right) = 4.0379038587 \rightarrow \text{resultado sin error.} \\ \\
\frac{0.4275 \cdot 10^{-2}}{0.7645 \cdot 10^1} = 0.559189012\dots \times 10^{-3} \\
x = 0.5591 \cdot 10^{-3} + 0.89012\dots \cdot 10^{-7} \\
\text{como } d_5 = 8 \ge 5 \Rightarrow \bar{x}_1 = 0.5592 \cdot 10^{-3} \\ \\
(0.7221 \cdot 10^4) \cdot (0.5592 \cdot 10^{-3}) = 4.0379832 = 0.40379832 \cdot 10^1 \\
x = 0.4037 \cdot 10^1 + 0.9832 \cdot 10^{-3} \\
\text{como } d_5 = 9 \ge 5 \Rightarrow \bar{x} = 0.4038 \cdot 10^1 = 4.038 \\ \\
\text{error: } \left| \frac{4.0379038587 - 4.038}{4.0379038587} \right| = 0.00002380963 \Rightarrow 0.002380963 \%
\end{matrix}$$

---

### **Ejercicio N° 7**
Mediante gráficas de proceso estudiar la propagación de errores de:
- $v = 4a^2 + 3a$
- $w = a^2 + 2a + 1$, con $e_a \ne 0$

Se recomienda determinar $\delta(z)_{a \rightarrow \infty}$ y $\delta(z)_{a \rightarrow 0}$.

**Inciso a)**
![[TP2 2026-08-22 21.13.17.excalidraw]]

> [!NOTE]
> **Consultar**

**Inciso b)**
![[grafo2.excalidraw]]

$$\delta(w) = \left[ \left( (2\delta(a) + \delta(\times_1))\frac{a^2}{a^2+2a} \right) + \left( (\delta(a) + \delta(\times_2))\frac{2a}{a^2+2a} \right) + \delta(+_1) \right] \frac{a^2+2a}{a^2+2a+1} + \delta(+_2)$$

$$\text{Sea } \delta = \text{mayor}[\delta(a), \delta(\times_1), \delta(\times_2), \delta(+_1), \delta(+_2)] \Rightarrow$$

$$\begin{aligned}
\delta(w) &\le \left[ 3\delta \frac{a^2}{a^2+2a} + 2\delta \frac{2a}{a^2+2a} + \delta \right] \frac{a^2+2a}{(a+1)^2} + \delta \\
&= \left[ \frac{3a^2 + 4a}{a^2+2a} + 1 \right] \delta \cdot \frac{a^2+2a}{(a+1)^2} + \delta \\
&= \left[ \frac{3a + 4}{a + 2} + 1 \right] \delta \cdot \frac{a(a+2)}{(a+1)^2} + \delta \\
&= \left( \frac{4a + 6}{a + 2} \right) \cdot \frac{a(a+2)}{(a+1)^2}\delta + \delta \\
&= \left( \frac{4a^2 + 6a}{(a+1)^2} + 1 \right) \delta
\end{aligned}$$

$$\begin{aligned}
1)~~ \lim_{a \to 0} \delta(w) &= \left( \frac{0}{1} + 1 \right)\delta = \delta \\
2)~~ \lim_{a \to \infty} \delta(w) &= (4 + 1)\delta = 5\delta
\end{aligned}$$

---

### **Ejercicio N° 8**
Sean $x_1 = 0.5$, $x_2 = 2.5$, $x_3 = 50$, $x_4 = 100$ y $\delta = 0.025$.  
Se utiliza una calculadora que genera error de $\delta$ en la representación del resultado de la suma. Se sabe que el resultado exacto es $z = x_1 + x_2 + x_3 + x_4 = 153$.  
Utilizando expresiones del error propagado, indique cuál de las siguientes formas ($u$ o $v$) conviene sumar. Justifique su respuesta:
- $u = ((x_1 + x_2) + x_3) + x_4$
- $v = ((x_4 + x_3) + x_2) + x_1$

**Solución:**
$$\begin{matrix}
u = (((0.5 + 2.5)(1 + 0.025) + 50)(1 + 0.025) + 100)(1 + 0.025) = 158.2619219 \\
v = (((100 + 50)(1 + 0.025) + 2.5)(1 + 0.025) + 0.5)(1 + 0.025) = 164.6726562 \\ \\
\text{error}(u): \left| \frac{153 - 158.2619219}{153} \right| = 0.03439164641 \Rightarrow 3.439164641 \% \\ \\
\text{error}(v): \left| \frac{153 - 164.6726562}{153} \right| = 0.07629187059 \Rightarrow 7.629187059 \%
\end{matrix}$$

---

### **Ejercicio N° 9**
Sean:
$$u = \sum_{i=1}^{n} x_i \quad \text{y} \quad v = \sum_{i=1}^{n} x_i y_i$$

Determinar una cota para el error relativo propagado, suponer datos exactos.

**Solución:**
$$\begin{matrix}
\text{1) Cota para } u = \sum_{i=1}^{n} x_i: \\ \\
\bar{u} = x_1(1+\delta)^{n-1} + x_2(1+\delta)^{n-1} + x_3(1+\delta)^{n-2} + \dots + x_n(1+\delta) \\
\text{Aplicando } (1+\delta)^k \le 1 + 1.01k\delta: \\
|\bar{u} - u| \le 1.01(n-1)\delta \sum_{i=1}^{n} |x_i| \\ \\
\delta(u) = \frac{|\bar{u} - u|}{|u|} \le 1.01(n-1)\delta \cdot \frac{\sum_{i=1}^{n} |x_i|}{\left|\sum_{i=1}^{n} x_i\right|} \\ \\ \\

\text{2) Cota para } v = \sum_{i=1}^{n} x_i y_i: \\ \\
\bar{v} = (x_1 y_1)(1+\delta)^n + (x_2 y_2)(1+\delta)^n + (x_3 y_3)(1+\delta)^{n-1} + \dots + (x_n y_n)(1+\delta)^2 \\
\text{Aplicando } (1+\delta)^k \le 1 + 1.01k\delta: \\
|\bar{v} - v| \le 1.01 n \delta \sum_{i=1}^{n} |x_i y_i| \\ \\
\delta(v) = \frac{|\bar{v} - v|}{|v|} \le 1.01 n \delta \cdot \frac{\sum_{i=1}^{n} |x_i y_i|}{\left|\sum_{i=1}^{n} x_i y_i\right|}
\end{matrix}$$

---

## **Bloque de Programación**

1. Diseñar un programa que permita convertir un número de la base $\beta$ en otra de base $\beta'$, sabiendo que tanto la base $\beta$ como $\beta'$ son enteros en el rango $[2, 16]$. El programa deberá:
   - Mostrar el número en la base $\beta'$ con todos sus dígitos (cuando sea posible) en punto flotante normalizado, y sin normalizar.
   - Mostrar el número de la base $\beta'$ en los dos formatos de representación: por corte y por redondeo simétrico, según la cantidad de dígitos $t$ de precisión ingresado por el usuario. Ambos formatos deberán mostrarse en punto flotante normalizado y sin normalizar.

2. Programar una calculadora básica que contemple las operaciones: suma, resta, multiplicación y división sobre una malla con sistema de numeración decimal y mantisa de $t$ dígitos.
   - Al presionarse la tecla `"="`, deberá mostrar además del resultado de la operación, el error absoluto y relativo generado.