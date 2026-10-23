---
materia: Programación Numérica / Cálculo Numérico
facultad: Facultad de Ciencias Exactas - UNSa
departamento: Departamento de Informática
año: 2026
tipo: Trabajo Práctico
numero: 5
tema: Sistema de Ecuaciones Lineales
---
### Ejercicio N° 1
Sea la resolución de $A \cdot x = b$, con $|A| \ne 0$. Expresar el modelo matemático y determinar el número de operaciones para los siguientes casos, en donde $A$ es:
- **a)** Diagonal
- **b)** Triangular Superior
- **c)** Triangular Inferior

---

### Ejercicio N° 2
Investigar la demostración del teorema de la descomposición $LU$ para una matriz cuadrada de orden $n$.

---

### Ejercicio N° 3
Descomponer mediante operaciones elementales las siguientes matrices en $L-U$, tal que $A = L \cdot U$ o $PA = L \cdot U$:

**i)**
$$A = \begin{pmatrix} 1 & 2 & 6 \\ 4 & 8 & -1 \\ -2 & 3 & 5 \end{pmatrix}$$

**ii)**
$$A = \begin{pmatrix} 6 & -2 & 2 & 4 \\ 12 & -8 & 6 & 10 \\ 3 & -13 & 9 & 3 \\ -6 & 4 & 1 & -18 \end{pmatrix}$$

---

### Ejercicio N° 4
Se quiere resolver $A \cdot x = b$, con $|A| \ne 0$. Utilice el método de Gauss y Gauss-Jordan para encontrar la solución. Utilícese la matriz del inciso **ii)** del Ejercicio 3 y:

$$b^T = (12, 34, 27, -38)$$

---

### Ejercicio N° 5
Determine el modelo matemático y el número de operaciones de los métodos de Gauss, Crout y Cholesky.

---

### Ejercicio N° 6
Resolver los siguientes sistemas lineales mediante los siguientes métodos:
1. Gauss con pivoteo parcial.
2. Gauss con pivoteo completo.
3. Crout.
4. Cholesky.

**a)**
$$\begin{cases}
2x_1 + x_2 - 5x_3 + x_4 = 8 \\
x_1 - 3x_2 - x_4 = 9 \\
-x_1 + 2x_2 + 2x_4 = -5 \\
x_1 + 4x_2 - 7x_3 + 6x_4 = 0
\end{cases}$$

**b)**
$$\begin{cases}
0.05x_1 + 0.07x_2 + 0.06x_3 + 0.08x_4 = 0.30 \\
0.07x_1 + 0.10x_2 + 0.08x_3 + 0.07x_4 = 0.32 \\
0.06x_1 + 0.08x_2 + 0.10x_3 + 0.09x_4 = 0.33 \\
0.05x_1 + 0.07x_2 + 0.09x_3 + 0.10x_4 = 0.31
\end{cases}$$

---

### Ejercicio N° 7
Sean los siguientes problemas:

**a)**
$$\begin{pmatrix} 10 & 7 & 8 & 7 \\ 7 & 5 & 6 & 5 \\ 8 & 6 & 10 & 9 \\ 7 & 5 & 9 & 10 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = \begin{pmatrix} 32 \\ 23 \\ 33 \\ 31 \end{pmatrix}$$

**b)**
$$\begin{pmatrix} 10 & 7 & 8 & 7 \\ 7 & 5 & 6 & 5 \\ 8 & 6 & 10 & 9 \\ 7 & 5 & 9 & 10 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = \begin{pmatrix} 32.1 \\ 22.9 \\ 33.1 \\ 30.9 \end{pmatrix}$$

- ¿Son problemas equivalentes?
- ¿Las soluciones son aproximadamente iguales? Justifique.

---

### Ejercicio N° 8
Utilice el método de Mejoramiento Iterativo para encontrar una solución mejorada al siguiente caso:

$$\begin{pmatrix} 2 & 1 & 1 \\ 4 & 3 & 3 \\ 8 & 7 & 9 \end{pmatrix} \cdot \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 3 \end{pmatrix}$$

Sabiendo que:
$$x^{(0)} = \begin{pmatrix} 0.9 \\ -2.5 \\ 1.5 \end{pmatrix}$$

---

### Ejercicio N° 9
Dado el siguiente sistema lineal, obtener la solución aproximada mediante los métodos que se indica, usando $\bar{x}^{(0)} = (0, 0, 0, 0)^T$ y $\|\bar{x}^{(k+1)} - \bar{x}^{(k)}\| < 0.001$:
- Jacobi
- Gauss-Seidel
- Relajamiento

$$\begin{cases}
10x_1 - x_2 + 2x_3 = 6 \\
-x_1 + 11x_2 - x_3 + 3x_4 = 25 \\
2x_1 - x_2 + 10x_3 - x_4 = -11 \\
3x_2 - x_3 + 8x_4 = 15
\end{cases}$$

---

# Bloque 2 — Programación

Diseñar un programa que implemente los siguientes algoritmos:
- **Normas de VECTORES**: Distintos tipos.
- **Normas de MATRICES**: Distintos tipos.
- **Factorización de matrices cuadradas** en $L \cdot U$.
- **Resolver SISTEMAS LINEALES** mediante los métodos de:
  - Gauss
  - Gauss-Jordan
  - Crout
  - Cholesky
  - Jacobi
  - Gauss-Seidel
  - Relajamiento
  - SOR
  - Mejoramiento Iterativo

> **Nota:** Para los métodos directos programar estrategias de pivoteo:
> - Pivoteo Simple
> - Pivoteo Parcial
> - Pivoteo Total