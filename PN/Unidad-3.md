# Universidad Nacional de Salta
## Facultad de Ciencias Exactas - Departamento de Informática
### Programación Numérica / Cálculo Numérico

---

# Trabajo Práctico Nº 3
## Resolución de Ecuaciones No Lineales

---

## Bloque 1

### Ejercicio Nº 1
a) Enunciar las condiciones de unicidad y existencia para que haya una única raíz en $[a, b]$.  
b) Enunciar las condiciones suficientes para la aplicación de los métodos de Bisección, Regula Falsi y Regula Falsi Modificada.

**Definiciones:**
* Sea el intervalo $[a,b]$ puedo garantizar que hay al menos una raiz si se cumple el teorema de Bolzano:
$$
\text{sea $f$ una función continua en el intervalo $[a,b]$ y }f(a)f(b)<0 \Rightarrow \exists c \in (a,b) : f(c)=0
$$
* Puedo garantizar que la raiz que encontre en el intervalo $[a,b]$ es única si ademas de lo anterior tambien se cumple el teorema de Rolle:
$$
\text{sea $f$ una función continua en el intervalo $[a,b]$ y derivable en $(a,b)$ } \Rightarrow \exists c \in (a,b)| f'(c)=0
$$
* Las condiciones suficientes para la aplicación de los métodos de Bisección, Regula Falsi y Regula Falsi modificada son los siguientes:
	1. La función debe ser monotona.
	2. Se cumple la hipotesis de Bolzano es decir: $f(a)f(b)<0$
	3. Se cumple la hipotesis de Rolle es decir que $f$ es continua y derivable en $(a,b)$ 

---

### Ejercicio Nº 2
Dada $f(x) = e^{x} - x^{2} + 1$

Hallar una raíz aproximada con seis cifras de precisión, calculándola por el método:
- **i)** Bisección
- **ii)** Regula Falsi
- **iii)** Regula Falsi Modificada
> **Comparar los resultados obtenidos.**

**Solución:**

*Bisección:*

| $i$  | $a$          | $b$            | $c$             | $f(a)$            | $f(c)$            |
| ---- | ------------ | -------------- | --------------- | ----------------- | ----------------- |
| $1$  | $-2$         | $-1$           | $-1.5$          | $-2.86466471676$  | $-1.02686984$     |
| $2$  | $-1.5$       | $-1$           | $-1.25$         | $-1.02686984$     | $-0.2759952031$   |
| $3$  | $-1.25$      | $-1$           | $-1.125$        | $-0.2759952031$   | $0.05902746736$   |
| $4$  | $-1.25$      | $-1.125$       | $-1.1875$       | $-0.2759952031$   | $-0.1051734813$   |
| $5$  | $-1.1875$    | $-1.125$       | $-1.15625$      | $-0.1051734813$   | $-0.02225010148$  |
| $6$  | $-1.15625$   | $-1.125$       | $-1.140625$     | $-0.02225010148$  | $0.01859380675$   |
| $7$  | $-1.15625$   | $-1.140625$    | $-1.1484375$    | $-0.02225010148$  | $-0.001776790354$ |
| $8$  | $-1.1484375$ | $-1.140625$    | $-1.14453125$   | $-0.001776790354$ | $0.008172706126$  |
| $9$  | $-1.1484375$ | $-1.14453125$  | $-1.146484375$  | $-0.001776790354$ | $0.003325482452$  |
| $10$ | $-1.1484375$ | $-1.146484375$ | $-1.1474609375$ | $-0.001776790354$ | $0.000775148355$  |
*Regula Falsi:*

| $i$  | $a$  | $b$            | $c$            | $f(a)$             | $f(c)$              |
| ---- | ---- | -------------- | -------------- | ------------------ | ------------------- |
| $1$  | $-2$ | $-1$           | $-1.113804924$ | $-2.864664717$     | $0.08774598811$     |
| $2$  | $-2$ | $-1.113804924$ | $-1.140142744$ | $-2.864664717$     | $0.01984789613$     |
| $3$  | $-2$ | $-1.140142744$ | $-1.146059292$ | $-2.864664717$     | $0.004435103437$    |
| $4$  | $-2$ | $-1.146059292$ | $-1.147379328$ | $-2.864664717$     | $0.000988336442$    |
| $5$  | $-2$ | $-1.147379328$ | $-1.147673389$ | $-2.864664717$     | $0.000220109812$    |
| $6$  | $-2$ | $-1.147673389$ | $-1.147738873$ | $-2.864664717$     | $0.0000490147763$   |
| $7$  | $-2$ | $-1.147738873$ | $-1.147753455$ | $-2.864664717$     | $0.0000109142916$   |
| $8$  | $-2$ | $-1.147753455$ | $-1.147756702$ | $-2.864664717$     | $0.00000243033991$  |
| $9$  | $-2$ | $-1.147756702$ | $-1.147757425$ | $-2.864664717$<br> | $0.000000541240768$ |
| $10$ | $-2$ | $-1.147757425$ | $-1.147757586$ | $-2.864664717$<br> | $0.000000120569884$ |
*Regula Falsi Modificada:*

---

### Ejercicio Nº 3
Dada la función $f(x) = x - \cos(x)$ definida en $[0, 1]$:
- **a)** Demuestre que tiene solución única en $[0, 1]$.
- **b)** Determinar el número de iteraciones necesarias para asegurar 4 decimales exactos mediante iteración de punto fijo.
- **c)** Calcule las 5 primeras iteraciones a partir de $x_0 = 0.5$.

---

### Ejercicio Nº 4
**Método de iteración de Punto Fijo:** Elija la función de iteración adecuada, exprese los criterios de convergencia y determine las raíces de las siguientes ecuaciones:

- **i)** $f(x) = x^{2} - \sin(x) - 1 = 0$
- **ii)** $f(x) = \ln(x) - 1 - \frac{1}{x} = 0$
- **iii)** $f(x) = x + \frac{1}{x} - e^{x} = 0$
- **iv)** $f(x) = x^{2} - 5x + 3 = 0$
- **v)** $f(x) = \cos(x) - 3x = 0$
- **vi)** $f(x) = x \, e^{x} - 1 = 0$

---

### Ejercicio Nº 5
Encontrar la raíz de $f(x) = e^{x} - x^{2} + 1$ con 6 cifras de precisión decimal usando el algoritmo de **Newton** y **Secante**. Obtener conclusiones.

---

### Ejercicio Nº 7
Encontrar la raíz de $f(x) = (x - 1)^{2}$ con 4 cifras de precisión decimal usando el algoritmo de **Newton** y **Newton Extendido**. Obtener conclusiones.

---

### Ejercicio Nº 8
Justificar que la fórmula de Newton corresponde a un proceso iterativo de segundo orden.

---

### Ejercicio Nº 9
Dada la ecuación $f(x) = 0$ y la fórmula de Halley:

$$x_{n+1} = x_{n} - \frac{2f(x_{n})f'(x_{n})}{2(f'(x_{n}))^{2} - f(x_{n})f''(x_{n})}$$

Mostrar que da lugar a un proceso iterativo de tercer orden. Use este modelo para encontrar una raíz aproximada con seis dígitos de precisión usando la función del ejercicio 2.

---

### Ejercicio Nº 10
Estudiar la convergencia del método de Bisección y determine la cantidad necesaria de iteraciones para asegurar una precisión de $t$ dígitos decimales. Use el resultado para calcular la cantidad de iteraciones necesarias para aproximar la solución de $f(x) = x - \cos(x)$ en $[0,1]$ con 4 dígitos de precisión decimal, luego encuentre la raíz con bisección. ¿Cuántas iteraciones realizó el método?

---

### Ejercicio Nº 11
Utilizar el método de **Aitken** para acelerar la convergencia en la aproximación de la solución para:

$$f(x) = x \, e^{x} - 1$$

---

### Ejercicio Nº 12
Ídem al ejercicio 11, pero con el método de **Steffensen**.

---

## Bloque 2 - Programación

Diseñar un programa que permita calcular la raíz simple de una función a través de los siguientes métodos:

| Nº | Método | Nº | Método |
| :---: | :--- | :---: | :--- |
| **i** | Bisección | **ii** | Regula Falsi |
| **iii** | Regula Falsi Modificada | **iv** | Método de Newton |
| **v** | Secante | **vi** | Método de Halley |
| **vii** | Punto Fijo | **viii** | Newton para raíces múltiples |
| **ix** | PF con Aitken | **x** | PF con Steffensen |

- Implemente un módulo que permita realizar comparaciones de dos métodos a elección.
- Diseñe casos de pruebas y realice un informe sobre el funcionamiento de los programas.