# Universidad Nacional de Salta
## Facultad de Ciencias Exactas - Departamento de Informática
**Programación Numérica / Cálculo Numérico**  
**Trabajo Práctico Nº 4: Raíces de Polinomios**

---

# Bloque 1

### Ejercicio Nº 1
Dados los polinomios:
$$P(x) = x^4 - 3x^3 + \frac{3}{2}x + \frac{1}{4} \quad , \quad Q(x) = x^2 - \frac{5}{2}x + 7$$

Realizar las siguientes operaciones:
- **a)** $P(x) / Q(x)$
- **b)** $P(x) - Q(x)$
- **c)** $P(x) \cdot Q(x)$
- **d)** $P(x) + Q(x)$

**Solución:**
* **a)** La solución de este inciso se encuentra en el ejercicio 2.
* **b)**
  $$x^4 - 3x^3 + \frac{3}{2}x + \frac{1}{4} - \left(x^2 - \frac{5}{2}x + 7\right) = x^4 - 3x^3 - x^2 + 4x - \frac{27}{4}$$
* **c)**
  $$
  \begin{aligned}
  &\left(x^4 - 3x^3 + \frac{3}{2}x + \frac{1}{4}\right)\left(x^2 - \frac{5}{2}x + 7\right) \\
  &= x^4\left(x^2 - \frac{5}{2}x + 7\right) - 3x^3\left(x^2 - \frac{5}{2}x + 7\right) + \frac{3}{2}x\left(x^2 - \frac{5}{2}x + 7\right) + \frac{1}{4}\left(x^2 - \frac{5}{2}x + 7\right) \\
  &= x^6 - \frac{5}{2}x^5 + 7x^4 - 3x^5 + \frac{15}{2}x^4 - 21x^3 + \frac{3}{2}x^3 - \frac{15}{4}x^2 + \frac{21}{2}x + \frac{1}{4}x^2 - \frac{5}{8}x + \frac{7}{4} \\
  &= x^6 - \frac{11}{2}x^5 + \frac{29}{2}x^4 - \frac{39}{2}x^3 - \frac{7}{2}x^2 + \frac{79}{8}x + \frac{7}{4}
  \end{aligned}
  $$
* **d)**
  $$x^4 - 3x^3 + \frac{3}{2}x + \frac{1}{4} + x^2 - \frac{5}{2}x + 7 = x^4 - 3x^3 + x^2 - x + \frac{29}{4}$$

---

### Ejercicio Nº 2
Utilizando el método de Horner dividir los siguientes polinomios y en todos los casos expresarlo de la forma:
$$P(x) = C(x) \cdot Q(x) + R(x)$$

| Inciso | $P_i(x)$ | $Q_i(x)$ |
| :----: | :------------------------------------------- | :--------------------------- |
| **a)** | $P_1(x) = 2x^6 + x^3 + 3x + 2$ | $Q_1(x) = x + 1$ |
| **b)** | $P_2(x) = x^3 - 2x^2 + 5x + 3$ | $Q_2(x) = x - 2$ |
| **c)** | $P_3(x) = 2x^6 + x^3 + 3x + 2$ | $Q_3(x) = 2x + 2$ |
| **d)** | $P_4(x) = x^3 - \frac{2}{5}x^2 + 5x + 3$ | $Q_4(x) = 5x - 2$ |
| **e)** | $P_{5}(x) = x^4 - 3x^3 + \frac{3}{2}x + \frac{1}{4}$ | $Q_{5}(x) = x^2 - \frac{5}{2}x + 7$ |

![[ruffiniEjercicio2a.excalidraw]] ![[ruffiniEjercicio2b.excalidraw]]
![[ruffiniEjercicio2c.excalidraw]]
![[ruffiniEjercicio2d.excalidraw]]
![[ruffiniEjercicio2e.excalidraw]]

---

### Ejercicio Nº 3
Usando el método de Newton para polinomios, encontrar la raíz positiva del siguiente polinomio:
$$P(x) = 3x^2 - x$$

**Solución:**
consultar!!!

---

### Ejercicio Nº 4
Determinar las raíces enteras y racionales del siguiente polinomio:
$$P(x) = x^4 - \frac{7}{6}x^3 - \frac{37}{6}x^2 + \frac{4}{3}x + 2$$

**Solución:**

Nos interesará más el polinomio expresado sin fracciones, para ello:
$$6P(x) = P^*(x) = 6x^4 - 7x^3 - 37x^2 + 4x + 12$$

Las posibles raíces enteras de $P(x)$ son los divisores de 12:
$$\{ \pm 1, \pm 2, \pm 3, \pm 4, \pm 6, \pm 12 \}$$

Evaluando con Horner los divisores de 12 tenemos que:
$$
\begin{aligned}
P^*(1) &= -18 & P^*(-1) &= -20 & P^*(2) &= -80 & P^*(-2) &= 0 \\
P^*(3) &= 0 & P^*(-3) &= 330 & P^*(4) &= 540 & P^*(-4) &= 1372 \\
P^*(6) &= 4992 & P^*(-6) &= 7920 & P^*(12) &= 107100 & P^*(-12) &= 131100
\end{aligned}
$$

Luego, las posibles raíces racionales son:
$$\left\{ \pm \frac{1}{2}, \pm \frac{1}{3}, \pm \frac{1}{6}, \pm \frac{2}{3}, \pm \frac{3}{2}, \pm \frac{4}{3} \right\}$$

Evaluando las fracciones en el método de Horner tenemos:
$$
\begin{aligned}
P^*\left( \frac{1}{2} \right) &= 6.25 & P^*\left( -\frac{1}{2} \right) &= 0 \\
P^*\left( \frac{1}{3} \right) &= 10.37 & P^*\left( -\frac{1}{3} \right) &= 5.\bar{5} \\
P^*\left( \frac{1}{6} \right) &= 12.27 & P^*\left( -\frac{1}{6} \right) &= 9.67 \\
P^*\left( \frac{2}{3} \right) &= 0
\end{aligned}
$$

Encontramos todas las raíces del polinomio, las cuales son:
$$CS = \left\{ -2, 3, -\frac{1}{2}, \frac{2}{3} \right\}$$

---

### Ejercicio Nº 5
Encontrar cotas para las raíces reales por los métodos de Lagrange, Laguerre y Newton. Comparar.
- **a)** $P(x) = 4x^4 - 5x^2 + 1$
- **b)** $P(x) = x^3 - 3x^2 - 2x + 5$

**Solución:**

#### a) $P(x) = 4x^4 - 5x^2 + 1$

##### Método de Lagrange

$$
\lambda_{2}^{+} = 1 + \sqrt[k]{\frac{A}{a_{0}}} \implies \lambda_{2}^{+} = 1 + \sqrt{\frac{5}{4}} \approx 2.118033
$$

- **Cambio de variable 1:** $t^{n}P\left(\frac{1}{t}\right) \implies t^4\left(\frac{4}{t^4}\right) - t^4\left(\frac{5}{t^2}\right) + t^4 = t^4 - 5t^2 + 4$
  $$
  \lambda_{2}^{+}(t) = 1 + \sqrt{5} \approx 3.236067
  $$
  $$
  t < 3.236067 \implies \frac{1}{t} > \frac{1}{3.236067} \implies x > 0.309017 \implies \lambda_{1}^{+} \approx 0.309017
  $$

- **Cambio de variable 2:** $t^n P\left(-\frac{1}{t}\right) \implies t^4\left(\frac{4}{t^4}\right) - t^4\left(\frac{5}{t^2}\right) + t^4 = t^4 - 5t^2 + 4$
  $$
  \lambda_{2}^{+}(t) = 3.236067
  $$
  $$
  t < 3.236067 \Rightarrow \frac{1}{t} > \frac{1}{3.236067} \Rightarrow -\frac{1}{t} < -\frac{1}{3.236067} \implies x < -\frac{1}{3.236067} \Rightarrow \lambda_{2}^{-} \approx -0.309017
  $$

- **Cambio de variable 3:** $P(-t) \implies 4(-t)^4 - 5(-t)^2 + 1 = 4t^4 - 5t^2 + 1$
  $$
  \lambda_{2}^{+}(t) = 2.118033
  $$
  $$
  t < 2.118033 \implies -t > -2.118033 \implies x > -2.118033 \implies \lambda_{1}^{-} = -2.118033
  $$

> **Conclusión Lagrange:**  
> - Las raíces negativas están dentro del intervalo: $(-2.118033, -0.309016)$  
> - Las raíces positivas están dentro del intervalo: $(0.309016, 2.118033)$

---

##### Método de Laguerre

Definición:
$$
P_n(x) = (x - L)C_{n-1}(x) + r : \text{todos los coeficientes de } C_{n-1}(x) > 0 \land r > 0 \implies \lambda_{2}^{+} = L
$$

Usando Ruffini:
- Para $x = 1$: $P(1) = (x-1)(4x^3 + 4x^2 - x - 1) \rightarrow -x < 0$
- Para $x = 2$: $P(2) = (x-2)(4x^3 + 8x^2 + 11x + 22) + 45 \implies \text{todos los coeficientes y el resto son } > 0$
$$
\lambda_{2}^{+} = 2
$$

- **Cambio de variable:** $t^n P\left(\frac{1}{t}\right) \implies t^4 - 5t^2 + 4$
  $$
  \lambda_{2}^{+}(t) = 3 \implies t < 3 \implies \frac{1}{t} > \frac{1}{3} \implies x > \frac{1}{3} \implies \lambda_{1}^{+} = 0.\bar{3}
  $$

- **Cambio de variable:** $t^n P\left(-\frac{1}{t}\right) \implies t^4 - 5t^2 + 4$
  $$
  \lambda_{2}^{+}(t) = 3 \implies t < 3 \implies \frac{1}{t} > \frac{1}{3} \implies -\frac{1}{t} < -\frac{1}{3} \implies x < -\frac{1}{3} \implies \lambda_{2}^{-} = -0.\bar{3}
  $$

- **Cambio de variable:** $P(-t) \implies 4t^4 - 5t^2 + 1$
  $$
  \lambda_{2}^{+}(t) = 2 \implies t < 2 \implies -t > -2 \implies x > -2 \implies \lambda_{1}^{-} = -2
  $$

> **Conclusión Laguerre:**  
> - Las raíces negativas están dentro del intervalo: $(-2, -0.\bar{3})$  
> - Las raíces positivas están dentro del intervalo: $(0.\bar{3}, 2)$

---

##### Método de Newton

Derivamos el polinomio hasta obtener una constante y evaluamos en todas las derivadas un número. Si el número evaluado es positivo en todos los casos, esa es la cota superior positiva:

$$
\begin{aligned}
P(x) &= 4x^4 - 5x^2 + 1 \\
P'(x) &= 16x^3 - 10x \\
P''(x) &= 48x^2 - 10 \\
P'''(x) &= 96x \\
P^{(4)}(x) &= 96
\end{aligned}
$$

Evaluando en $x = 2$:
$$
P(2) = 45 > 0,~~~ P'(2) = 108 > 0,~~~ P''(2) = 182 > 0,~~~ P'''(2) = 192 > 0,~~~ P''''(2) = 96 > 0,~~ \lambda_{2}^{+} = 2
$$

- **Cambio de variable:** $t^n P\left(\frac{1}{t}\right) \implies t^4 - 5t^2 + 4$
  $$
  P'(t) = 4t^3 - 10t, \quad P''(t) = 12t^2 - 10, \quad P'''(t) = 24t, \quad P^{(4)}(t) = 24
  $$
  $$
  \lambda_{2}^{+}(t) = 3 \implies t < 3 \implies \frac{1}{t} > \frac{1}{3} \implies x > \frac{1}{3} \implies \lambda_{1}^{+} = \frac{1}{3}
  $$

- **Cambio de variable:** $t^n P\left(-\frac{1}{t}\right) \implies t^4 - 5t^2 + 4$
  $$
  \lambda_{2}^{+}(t) = 3 \implies t < 3 \implies \frac{1}{t} > \frac{1}{3} \implies -\frac{1}{t} < -\frac{1}{3} \implies x < -\frac{1}{3} \implies \lambda_{2}^{-} = -\frac{1}{3}
  $$

- **Cambio de variable:** $P(-t) \implies 4t^4 - 5t^2 + 1$
  $$
  \lambda_{2}^{+}(t) = 2 \implies t < 2 \implies -t > -2 \implies x > -2 \implies \lambda_{1}^{-} = -2
  $$

> **Conclusión Newton:**  
> - Las raíces negativas se encuentran dentro del intervalo: $\left(-2, -\frac{1}{3}\right)$  
> - Las raíces positivas se encuentran dentro del intervalo: $\left(\frac{1}{3}, 2\right)$

---

### Ejercicio Nº 6
Separar las raíces reales por el método de Sturm de:
- **a)** $P(x) = 4x^4 - 5x^2 + 1$
- **b)** $P(x) = x^3 - 3x^2 - 2x + 5$

**Solución:**
**a)**$$
Consultar!!!!!
$$
**b)**$$
\begin{gather}
\text{calculamos primeros las cotas de raices positivas y negatvas, usando newton quedan:} \\ \\
P(x)=x^3-3x²-2x+5. \quad P'(x)=3x²-3x-2. \quad P''(x)=6x-3. \quad P'''(x)=6 \\ \\
\text{luego si }x=4 \Rightarrow P(4)=13>0. \quad P'(4)=34>0. \quad P''(4)=21>0 . \quad P'''(4)=6>0 \Rightarrow \lambda_{2}^+=4 \\ \\
\text{cambio de variable:} \quad t³P\left( \frac{1}{t} \right)=t³\left( \frac{1}{t³} \right)-t³\left( \frac{3}{t²} \right)-t³\left( \frac{2}{t} \right)+5t³ \\ \\
P(t)=5t³-2t²-3t+1. \quad P'(t)=15t²-4t-3. \quad P''(t)=30t-4. \quad P'''(t)=30 \\ \\
\text{si }t=1 \Rightarrow P(1)=1>0. \quad P'(1)= 8>0. \quad P''(1)= 26>0. \quad P'''(1)=30>0 \Rightarrow \lambda_{1}^+=1 \\ \\
\text{cambio de variable:}\quad t³P\left( -\frac{1}{t} \right) = t³\left( -\frac{1}{t³} \right)-t³\left(- \frac{3}{t²} \right)-t³\left( -\frac{2}{t} \right)+5t³ \\ \\
P(t)=5t³+2t²+3t-1. \quad P'(t)= 15t²+4t+3. \quad P''(t) = 30t+4. \quad P'''(t)=30 \\ \\
\text{si }t=1\Rightarrow P(1)=9>0. \quad P'(1)= 22>0. \quad P''(1)=34>0. \quad P'''(1)=30>0 \Rightarrow \lambda_{2}^-=-1 \\ \\
\text{cambio de variable:}\quad P(-t)= -t³-3t²+2t+5\Rightarrow P(-t) \cdot (-1)=t³+3t²-2t-5 \\ \\
P(t)=t³+3t²-2t-5. \quad P'(t)=3t²+3t-2. \quad P''(t)=6t+3. \quad P'''(t)=6 \\ \\
\text{si }t=2 \Rightarrow P(2)=11>0. \quad P'(2)=16>0. \quad P''(2) = 15>0. \quad P'''(2)=6>0 \Rightarrow \lambda_{1}^-=-2 \\ \\
\therefore \text{las cotas son: }(-2,-1) ~~\cup~~ (1,4) \\ \\
\text{ahora buscamos sub cotas, para eso desde el polinomio encontramos nuevos polinomios:} \\ \\
f_{0}(x)=x³-3x²-2x+5 \quad \quad \quad \text{polinomio original} \\
f_{1}(x)=3x²-6x-2 \quad \quad \quad \quad ~~\text{la derivada de }f_{0} \\
f_{2}(x)= -18x-11 \quad \quad \quad \quad \quad~ resto \left( \frac{f_{0}}{f_{1}}\right)(-1) \\
f_{3}(x)=-297 \quad \quad \quad \quad \quad \quad \quad ~~resto \left(\frac{f_{1}}{f_{2}} \right)(-1)
\end{gather}
$$

|                            | $-2$ | $-1$ | $0$ | $1$ | $2$ | $3$ | $4$ |
| -------------------------- | ---- | ---- | --- | --- | --- | --- | --- |
| $f_{0}$                    | $-$  | $+$  | $+$ | $+$ | $-$ | $-$ | $+$ |
| $f_{1}$                    | $-$  | $+$  | $-$ | $-$ | $-$ | $+$ | $+$ |
| $f_{2}$                    | $+$  | $+$  | $-$ | $-$ | $-$ | $-$ | $-$ |
| $f_{3}$                    | $-$  | $-$  | $-$ | $-$ | $-$ | $-$ | $-$ |
| $\text{cambios de signos}$ | $2$  | $1$  | $1$ | $1$ | $0$ | $2$ | $1$ |
$\text{luego podemos definir sub cotas donde en cada intervalo hay una sola raiz:} (-2,-1)~~\cup~~(1,2)~~\cup~~(3,4).$
---
### Ejercicio Nº 8
Usando el método de Bairstow encontrar todas las raíces del polinomio:
$$P(x) = x^4 + 5x^3 + 15x^2 + 5x - 26$$

Usar $\epsilon = 0.0001$, $r_0 = -1.01$ y $s_0 = 2.01$.

---

### Ejercicio Nº 9
Encontrar todas las raíces de los siguientes polinomios:
- **a)** $P(x) = 6x^3 + x^2 - 29x - 14 = 0$
- **b)** $P(x) = x^3 + x^2 - 4x + 6 = 0$
- **c)** $P(x) = x^3 + 3x^2 + 3x - 10 = 0$
- **d)** $P(x) = x^3 - 19x^2 + 64x - 60 = 0$

---

# Bloque 2 - Programación

Realizar un programa que incorpore procedimientos para:

- **a)** Calcular el valor de un polinomio para un determinado punto.
- **b)** Dividir un polinomio de grado $n$ por otro de la forma $ax \pm b$.
- **c)** Dividir un polinomio de grado $n$ por otro de la forma $x^2 + px + q$.
- **d)** Determinar las posibles raíces enteras.
- **e)** Determinar las posibles raíces racionales.
- **f)** Determinar las cotas de las raíces positivas y negativas por distintos métodos.
- **g)** Encontrar raíces reales por el método de Newton y Halley para polinomios.
- **h)** Encuentre la sucesión de polinomios de Sturm.
- **i)** Realice la separación de raíces por Sturm.
- **j)** Implemente el Método de Bairstow.

> **Nota:** Diseñe casos de pruebas y realice un informe sobre el funcionamiento de los programas.
