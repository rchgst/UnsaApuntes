## Determinantes. Definición. Propiedades. Cálculo. Inversa de una matriz.

**Facultad:** U.N.Sa. Facultad de Ciencias Exactas  
**Asignatura:** Álgebra Lineal y Geometría Analítica  
**Carreras:** PM, LAS, LF, LER, TEU, TUP, TUES  
**Año:** 2º Cuatrimestre 2026  
**Duración:** 2 clases.

---

### Objetivos: Que el alumno sea capaz de:
- Incorporar y comprender el concepto de determinante y sus propiedades.
- Calcular el determinante de una matriz, aplicando axiomas y/o propiedades y métodos de cálculo.
- Calcular la inversa de una matriz usando la adjunta.
- Resolver sistemas de ecuaciones lineales usando el concepto de determinante.
- Utilizar su pensamiento lógico deductivo en la justificación de lo que realiza y para demostrar algunas propiedades.

---

### Ejercicio 1.

a) Enuncie las propiedades y axiomas de la función determinante.

b) Demuestra las siguientes igualdades, usando solo axiomas y/o propiedades de la función determinante.

1. 
$$
\begin{vmatrix}
a & b & c \\
a+b & b+c & c+a \\
2a+b & 2b+c & 2c+a
\end{vmatrix} = 0
$$
##### Solución:
$$
\begin{gather}
\underbrace{\begin{vmatrix}
a&b&c \\
a+b&b+c&c+a \\
2a+b&2b+c&2c+a
\end{vmatrix}}_{\text{A}} \xrightarrow[{F_{3}=F_{3}-2F_{1}}]{
F_{2}=F_{2}-F_{1} } \begin{vmatrix}
a&b&c \\
b&c&a \\
b&c&a
\end{vmatrix} \\ \\
\therefore \text{ por propiedad de determinantes, una matriz con dos filas iguales tiene determinante 0}\Rightarrow|A|=0
\end{gather}
$$

2. 
$$
\begin{vmatrix}
\frac{2}{\sqrt{5}} & \frac{1}{\sqrt{5}} & 0 \\
\frac{1}{\sqrt{5}} & -\frac{2}{\sqrt{5}} & 0 \\
0 & 0 & 2
\end{vmatrix} = \frac{6}{5}
$$
##### Solución:
$$
\begin{gather}
\underbrace{\begin{vmatrix}
\frac{2}{\sqrt{5}} & \frac{1}{\sqrt{5}} & 0 \\
\frac{1}{\sqrt{5}} & -\frac{2}{\sqrt{5}} & 0 \\
0 & 0 & 2
\end{vmatrix}}_{A} \xrightarrow[{F_{1},F_{2}}]{\text{Homogeneidad en}} \frac{1}{5}\begin{vmatrix}
2&1&0 \\
1&-2&0 \\
0&0&2
\end{vmatrix} \xrightarrow{F_{1}=F_{1}+ \frac{1}{2}F_{2}} \frac{1}{5}\begin{vmatrix}
\frac{5}{2}&0&0 \\
1&-2&0 \\
0&0&2
\end{vmatrix} \Rightarrow \frac{1}{5} \cdot (-10)=-2 \neq \frac{6}{5} \\ \\
\therefore\text{vemos que el determinante es }-2\text{ lo que es distinto al resultado esperado entonces }|A| \neq \frac{6}{5}
\end{gather}
$$

3. 
$$
\begin{vmatrix}
-3 & 1 & 1 & 1 \\
1 & -3 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{vmatrix} = 0
$$
##### Solución:
$$
\begin{gather}
\underbrace{\begin{vmatrix}
-3 & 1 & 1 & 1 \\
1 & -3 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{vmatrix}}_{A} \xrightarrow[{F_{3}=F_{3}+F_{4}}]{F_{1}=F_{1}+F_{2}} \begin{vmatrix}
-2&-2&2&2 \\
1&-3&1&1 \\
2&2&-2&-2 \\
1&1&1&3
\end{vmatrix} \xrightarrow{F_{1}=F_{1}+F_{3}} \begin{vmatrix}
0&0&0&0 \\
1&-3&1&1 \\
2&2&-2&-2 \\
1&1&1&3
\end{vmatrix} \\ \\
\therefore\text{ por propiedad de determinantes si una fila es nula el determinante es }0 \Rightarrow |A| = 0
\end{gather}
$$

4. 
$$
\begin{vmatrix}
t+3 & -1 & 1 \\
5 & t-3 & 1 \\
6 & -6 & t+4
\end{vmatrix} = (t+2)(t-2)(t+4)
$$
##### Solución:
$$
\begin{gather}
\underbrace{\begin{vmatrix}
t+3 & -1 & 1 \\
5 & t-3 & 1 \\
6 & -6 & t+4
\end{vmatrix}}_{A} \xrightarrow{F_{2}=F_{2}-F_{1}} \begin{vmatrix}
t+3&-1&1 \\
-t+2&t-2&0 \\
6&-6&t+4
\end{vmatrix} \xrightarrow{C_{1}=C_{1}+C_{2}} \begin{vmatrix}
t+2&-1&1 \\
0&t-2&0 \\
0&-6&t+4
\end{vmatrix} \\ \\
\xrightarrow{F_{3}=F_{3}-F_{2}} \begin{vmatrix}
t+2&-1&0 \\
0&t-2&0 \\
0&-t-4&t+4
\end{vmatrix} \xrightarrow{C_{2}=C_{2}+C_{3}} \begin{vmatrix}
t+2&-1&0 \\
0&t-2&0 \\
0&0&t+4
\end{vmatrix} = (t+2)(t-2)(t+4) \\ \\
\therefore \text{ podemos ver que al quedarnos una matriz triangular el determinante es el producto de la diagonal}
\end{gather}
$$

5. 
$$
\begin{vmatrix}
1 & 1 & 1 \\
x & y & z \\
x^2 & y^2 & z^2
\end{vmatrix} = (y-x)(z-x)(z-y)
$$
##### Solución:
$$
\begin{gather}
\underbrace{\begin{vmatrix}
1 & 1 & 1 \\
x & y & z \\
x^2 & y^2 & z^2
\end{vmatrix}}_{A} \xrightarrow{C_{2}=C_{2}-C_{1}} \begin{vmatrix}
1&0&1 \\
x&y-x&z \\
x²&y²-x²&z²
\end{vmatrix} \xrightarrow{C_{3}=C_{3}-C_{1}} \begin{vmatrix}
1&0&0 \\
x&y-x&z-x \\
x²&y²-x²&z²-x²
\end{vmatrix} \\ \\
 \xrightarrow{Homogeneidad}(y-x)(z-x)\begin{vmatrix}
1&0&0 \\
x&1&1 \\
x²&y-x&z-x
\end{vmatrix} \xrightarrow{C_{3}=C_{3}-C_{2}} (y-x)(z-x)\begin{vmatrix}
1&0&0 \\
x&1&0 \\
x²&y-x&z-y
\end{vmatrix} \\ \\
\text{luego el determinante de la matriz al ser triangular inferior es el producto de su diagonal entonces:} \\ \\
\therefore|A| = (y-x)(z-x)(z-y)
\end{gather}
$$

c) Sean las matrices $A, B \in \mathbb{R}^{4 \times 4}$ que se simbolizan como $A = (A_1, A_2, A_3, A_4)$ y $B = (A_1, A_4, A_3, A_2)$, donde $A_i$ corresponde a una fila de la matriz $A$ que ocupa el lugar $i$-ésimo. Si el $\det(A) = -10$, justifique utilizando solamente los axiomas de la función determinante, que el $\det(B) = 10$.

**por propiedad el determinante cambia cuando se intercambian filas o columnas, cambia de signo, entonces:**  $det(A) = -10 \Rightarrow det(B) = 10,$ **pues se esta intercambiando solamente la fila 4 con la fila 2**

---

### Ejercicio 2.

Sea $A = (A_1, A_2, A_3)$ donde $A_i$, $i=1,2,3$ son las filas de $A$ y sabiendo que $\det A = 3$. Calcula:

a) $\det(A_3, A_2, A_1)$  b) $\det(2A_1, A_2, A_2 + 3A_3)$  c) $\det(A_1, A_2 - 2A_3, 2A_3 - A_2)$  
d) $\det(3A)$  e) $\det(A^{-1})$  f) $\det(A^2)$

##### Solución:
###### a)
$$det(A_{3},A_{2},A_{1})=-det(A_{1},A_{2},A_{3})=-3$$
###### b) 
$$det(2A_{1},A_{2},A_{2}+3A_{3})=\underbrace{det(2A_{1},A_{2},A_{2})}_{0}+det(2A_{1},A_{2},3A_{3})=6\cdot det(A_{1},A_{2},A_{3})=18$$
###### c)
$$
\begin{gather}
\det(A_{1},A_{2}-2A_{3},2A_{3}-A_{2})=\det(A_{1},A_{2},2A_{3}-A_{2})+\det(A_{1},-2A_{3},2A_{3}-A_{2})= \\ \\
\det(A_{1},A_{2},2A_{3})+\underbrace{\det(A_{1},A_{2},-A_{2})}_{0}+\underbrace{\det(A_{1},-2A_{3},2A_{3})}_{0}+\det(A_{1},-2A_{3},-A_{2})= \\ \\
2 \cdot \det(A_{1},A_{2},A_{3})-2 \cdot\det(A_{1},A_{2},A_{3})=0
\end{gather}
$$
###### d)
$$
\det(3A) = (3A_{1},3A_{2},3A_{3}) = 9 \cdot (A_{1},A_{2},A_{3})= 27
$$
###### e)
$$
\begin{gather}
A \cdot A^{-1}= I \\
\det(A \cdot A^{-1}) = \underbrace{\det(I)}_{1} \\
\det (A) \det(A^{-1}) = 1 \\ \\
\det(A^{-1})=\frac{1}{\det(A)}
\end{gather}
$$
###### f)
$$
\det(A^2) = \det(A \cdot A)=\det(A) \cdot \det(A) = \det(A)^2=3²=9
$$
---

### Ejercicio 3.

Dadas las siguientes matrices:

$$
A = \begin{pmatrix}
1 & 0 & 1 \\
-2 & 1 & 1 \\
1 & -1 & 0
\end{pmatrix}
\quad
B = \begin{pmatrix}
4 & 2 & -1 \\
-1 & 0 & 0 \\
3 & 4 & 10
\end{pmatrix}
\quad
C = \begin{pmatrix}
9 & 0 & 7 \\
3 & 1 & 2 \\
-1 & 0 & 0
\end{pmatrix}
\quad
D = \begin{pmatrix}
1 & 1 & 1 & 6 \\
2 & 4 & 1 & 6 \\
4 & 1 & 2 & 9 \\
2 & 4 & 2 & 7
\end{pmatrix}
$$

a) Calcula su determinante utilizando el método de Laplace y el método de Gauss.  
b) Determina la matriz de Cofactores y la matriz Adjunta.  
c) Verifica que $A \cdot \text{Adj}(A) = (\det A) I$. ¿Ocurre esto para cualquier matriz cuadrada $A$? Intenta justificar tu respuesta.

##### Solución:
#### a) Cálculo de determinantes por Laplace y Gauss

##### Matriz $A$
$$A = \begin{pmatrix} 1 & 0 & 1 \\ -2 & 1 & 1 \\ 1 & -1 & 0 \end{pmatrix}$$

* **Método de Laplace (por columna 2, tras $F_2 \leftarrow F_2 + F_3$):**
$$A = \begin{pmatrix} 1 & 0 & 1 \\ -2 & 1 & 1 \\ 1 & -1 & 0 \end{pmatrix} \xrightarrow{F_2 \leftarrow F_2 + F_3} \begin{pmatrix} 1 & 0 & 1 \\ -1 & 0 & 1 \\ 1 & -1 & 0 \end{pmatrix}$$

$$\det(A) = a_{32} \cdot (-1)^{3+2} \cdot M_{32} = (-1)(-1) \begin{vmatrix} 1 & 1 \\ -1 & 1 \end{vmatrix} = 1 \cdot (1 - (-1)) = 2$$

* **Método de Gauss:**
$$A = \begin{pmatrix} 1 & 0 & 1 \\ -2 & 1 & 1 \\ 1 & -1 & 0 \end{pmatrix} \sim \begin{pmatrix} 1 & 0 & 1 \\ 0 & 1 & 3 \\ 0 & -1 & -1 \end{pmatrix} \sim \begin{pmatrix} 1 & 0 & 1 \\ 0 & 1 & 3 \\ 0 & 0 & 2 \end{pmatrix}$$

$$\det(A) = \frac{1 \cdot 1 \cdot 2}{1^2 \cdot 1^1} = 2$$

##### Matriz $B$
$$B = \begin{pmatrix} 4 & 2 & -1 \\ -1 & 0 & 0 \\ 3 & 4 & 10 \end{pmatrix}$$

* **Método de Laplace (desarrollo directo por fila 2):**
$$\det(B) = (-1) \cdot (-1)^{2+1} \begin{vmatrix} 2 & -1 \\ 4 & 10 \end{vmatrix} = (-1)(-1)(20 - (-4)) = 24$$
* **Método de Gauss:**
$$B = \begin{pmatrix} 4 & 2 & -1 \\ -1 & 0 & 0 \\ 3 & 4 & 10 \end{pmatrix} \sim \begin{pmatrix} 4 & 2 & -1 \\ 0 & 2 & -1 \\ 0 & 10 & 43 \end{pmatrix} \sim \begin{pmatrix} 4 & 2 & -1 \\ 0 & 2 & -1 \\ 0 & 0 & 48 \end{pmatrix}$$
$$\det(B) = \frac{4 \cdot 2 \cdot 48}{4^2 \cdot 2} = \frac{384}{32} = 24$$
##### Matriz $C$
$$C = \begin{pmatrix} 9 & 0 & 7 \\ 3 & 1 & 2 \\ -1 & 0 & 0 \end{pmatrix}$$
* **Método de Laplace (desarrollo directo por fila 3):**
$$\det(C) = (-1) \cdot (-1)^{3+1} \begin{vmatrix} 0 & 7 \\ 1 & 2 \end{vmatrix} = (-1)(1)(0 - 7) = 7$$
* **Método de Gauss:**
$$C = \begin{pmatrix} 9 & 0 & 7 \\ 3 & 1 & 2 \\ -1 & 0 & 0 \end{pmatrix} \sim \begin{pmatrix} 9 & 0 & 7 \\ 0 & 9 & -1 \\ 0 & 0 & 7 \end{pmatrix}$$
$$\det(C) = \frac{9 \cdot 9 \cdot 7}{9^2} = 7$$
##### Matriz $D$
$$D = \begin{pmatrix} 1 & 1 & 1 & 6 \\ 2 & 4 & 1 & 6 \\ 4 & 1 & 2 & 9 \\ 2 & 4 & 2 & 7 \end{pmatrix}$$
* **Método de Laplace (operaciones elementales y desarrollo):**
$$\det(D) = \begin{vmatrix} 1 & 1 & 1 & 6 \\ 2 & 4 & 1 & 6 \\ 4 & 1 & 2 & 9 \\ 2 & 4 & 2 & 7 \end{vmatrix} \xrightarrow{F_1 \leftarrow F_1 - F_2} \begin{vmatrix} -1 & -3 & 0 & 0 \\ 2 & 4 & 1 & 6 \\ 4 & 1 & 2 & 9 \\ 2 & 4 & 2 & 7 \end{vmatrix} \xrightarrow{C_2 \leftarrow C_2 - 3C_1} \begin{vmatrix} -1 & 0 & 0 & 0 \\ 2 & -2 & 1 & 6 \\ 4 & -11 & 2 & 9 \\ 2 & -2 & 2 & 7 \end{vmatrix}$$

Extrayendo escalares $(-1)$ de $F_1$ y $(-1)$ de $C_2$:
$$\det(D) = (-1)(-1) \begin{vmatrix} 1 & 0 & 0 & 0 \\ 2 & 2 & 1 & 6 \\ 4 & 11 & 2 & 9 \\ 2 & 2 & 2 & 7 \end{vmatrix} = 1 \cdot (-1)^{1+1} \begin{vmatrix} 2 & 1 & 6 \\ 11 & 2 & 9 \\ 2 & 2 & 7 \end{vmatrix}$$
Reduciendo el menor de $3 \times 3$:
$$\begin{vmatrix} 2 & 1 & 6 \\ 11 & 2 & 9 \\ 2 & 2 & 7 \end{vmatrix} \xrightarrow{F_1 \leftarrow F_1 - F_2} \begin{vmatrix} -9 & -1 & -3 \\ 11 & 2 & 9 \\ 2 & 2 & 7 \end{vmatrix}$$
Aplicando operaciones elementales de columna:
$$\det(D) = \begin{vmatrix} 1 & 1 & 1 & 6 \\ 0 & 2 & -1 & -6 \\ 0 & -3 & -2 & -15 \\ 0 & 2 & 0 & -5 \end{vmatrix} = 1 \cdot (-1)^{1+1} \begin{vmatrix} 2 & -1 & -6 \\ -3 & -2 & -15 \\ 2 & 0 & -5 \end{vmatrix}$$
Desarrollando por fila 3:
$$\det(D) = 2 \cdot (-1)^{3+1} \begin{vmatrix} -1 & -6 \\ -2 & -15 \end{vmatrix} + (-5) \cdot (-1)^{3+3} \begin{vmatrix} 2 & -1 \\ -3 & -2 \end{vmatrix} = 2(3) - 5(-7) = 6 + 35 = 41$$
* **Método de Gauss:**
$$D \sim \begin{pmatrix} 1 & 1 & 1 & 6 \\ 0 & 2 & -1 & -6 \\ 0 & -3 & -2 & -15 \\ 0 & 2 & 0 & -5 \end{pmatrix} \sim \begin{pmatrix} 1 & 1 & 1 & 6 \\ 0 & 2 & -1 & -6 \\ 0 & 0 & -7 & -48 \\ 0 & 0 & 2 & 7 \end{pmatrix} \sim \begin{pmatrix} 1 & 1 & 1 & 6 \\ 0 & 2 & -1 & -6 \\ 0 & 0 & -7 & -48 \\ 0 & 0 & 0 & -47 \end{pmatrix}$$
$$\det(D) = \frac{1 \cdot 2 \cdot (-7) \cdot (-47)}{1^3 \cdot 2^2 \cdot (-7)} = 41$$
#### b) Matrices de Cofactores y Matrices Adjuntas
$$\text{Recordatorio: } C_{ij} = (-1)^{i+j} M_{ij} \qquad \text{Adj}(M) = [\text{Cof}(M)]^T$$
##### Para la Matriz $A$
* **Menores complementarios:**
  * $M_{11} = \begin{vmatrix} 1 & 1 \\ -1 & 0 \end{vmatrix} = 1 \qquad M_{12} = \begin{vmatrix} -2 & 1 \\ 1 & 0 \end{vmatrix} = -1 \qquad M_{13} = \begin{vmatrix} -2 & 1 \\ 1 & -1 \end{vmatrix} = 1$
  * $M_{21} = \begin{vmatrix} 0 & 1 \\ -1 & 0 \end{vmatrix} = 1 \qquad M_{22} = \begin{vmatrix} 1 & 1 \\ 1 & 0 \end{vmatrix} = -1 \qquad M_{23} = \begin{vmatrix} 1 & 0 \\ 1 & -1 \end{vmatrix} = -1$
  * $M_{31} = \begin{vmatrix} 0 & 1 \\ 1 & 1 \end{vmatrix} = -1 \qquad M_{32} = \begin{vmatrix} 1 & 1 \\ -2 & 1 \end{vmatrix} = 3 \qquad M_{33} = \begin{vmatrix} 1 & 0 \\ -2 & 1 \end{vmatrix} = 1$
 
* **Cofactores y Adjunta:**
$$\text{Cof}(A) = \begin{pmatrix} 1 & 1 & 1 \\ -1 & -1 & 1 \\ -1 & -3 & 1 \end{pmatrix} \qquad \text{Adj}(A) = \begin{pmatrix} 1 & -1 & -1 \\ 1 & -1 & -3 \\ 1 & 1 & 1 \end{pmatrix}$$
##### Para la Matriz $B$
* **Menores complementarios:**
  * $M_{11} = \begin{vmatrix} 0 & 0 \\ 4 & 10 \end{vmatrix} = 0 \qquad M_{12} = \begin{vmatrix} -1 & 0 \\ 3 & 10 \end{vmatrix} = -10 \qquad M_{13} = \begin{vmatrix} -1 & 0 \\ 3 & 4 \end{vmatrix} = -4$
  * $M_{21} = \begin{vmatrix} 2 & -1 \\ 4 & 10 \end{vmatrix} = 24 \qquad M_{22} = \begin{vmatrix} 4 & -1 \\ 3 & 10 \end{vmatrix} = 43 \qquad M_{23} = \begin{vmatrix} 4 & 2 \\ 3 & 4 \end{vmatrix} = 10$
  * $M_{31} = \begin{vmatrix} 2 & -1 \\ 0 & 0 \end{vmatrix} = 0 \qquad M_{32} = \begin{vmatrix} 4 & -1 \\ -1 & 0 \end{vmatrix} = -1 \qquad M_{33} = \begin{vmatrix} 4 & 2 \\ -1 & 0 \end{vmatrix} = 2$

* **Cofactores y Adjunta:**
$$\text{Cof}(B) = \begin{pmatrix} 0 & 10 & -4 \\ -24 & 43 & -10 \\ 0 & 1 & 2 \end{pmatrix} \qquad \text{Adj}(B) = \begin{pmatrix} 0 & -24 & 0 \\ 10 & 43 & 1 \\ -4 & -10 & 2 \end{pmatrix}$$

##### Para la Matriz $C$
* **Menores complementarios:**
  * $M_{11} = \begin{vmatrix} 1 & 2 \\ 0 & 0 \end{vmatrix} = 0 \qquad M_{12} = \begin{vmatrix} 3 & 2 \\ -1 & 0 \end{vmatrix} = 2 \qquad M_{13} = \begin{vmatrix} 3 & 1 \\ -1 & 0 \end{vmatrix} = 1$
  * $M_{21} = \begin{vmatrix} 0 & 7 \\ 0 & 0 \end{vmatrix} = 0 \qquad M_{22} = \begin{vmatrix} 9 & 7 \\ -1 & 0 \end{vmatrix} = 7 \qquad M_{23} = \begin{vmatrix} 9 & 0 \\ -1 & 0 \end{vmatrix} = 0$
  * $M_{31} = \begin{vmatrix} 0 & 7 \\ 1 & 2 \end{vmatrix} = -7 \qquad M_{32} = \begin{vmatrix} 9 & 7 \\ 3 & 2 \end{vmatrix} = -3 \qquad M_{33} = \begin{vmatrix} 9 & 0 \\ 3 & 1 \end{vmatrix} = 9$

* **Cofactores y Adjunta:**
$$\text{Cof}(C) = \begin{pmatrix} 0 & -2 & 1 \\ 0 & 7 & 0 \\ -7 & 3 & 9 \end{pmatrix} \qquad \text{Adj}(C) = \begin{pmatrix} 0 & 0 & -7 \\ -2 & 7 & 3 \\ 1 & 0 & 9 \end{pmatrix}$$

#### c) Verificación de la identidad $A \cdot \text{Adj}(A) = (\det A) I$

Calculamos el producto entre $A$ y su matriz adjunta $\text{Adj}(A)$[cite: 1]:

$$
\begin{gather}
A \cdot \text{Adj}(A) = \begin{pmatrix} 1 & 0 & 1 \\ -2 & 1 & 1 \\ 1 & -1 & 0 \end{pmatrix} \begin{pmatrix} 1 & -1 & -1 \\ 1 & -1 & -3 \\ 1 & 1 & 1 \end{pmatrix} = \begin{pmatrix}
2&0&0 \\
0&2&0 \\
0&0&2
\end{pmatrix}
\end{gather}
$$
$$A \cdot \text{Adj}(A) = \begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{pmatrix} = 2 \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = (\det A) I$$

---

##### ¿Ocurre esto para cualquier matriz cuadrada $A$?

**Sí, es una propiedad general válida para toda matriz cuadrada $A \in \mathbb{R}^{n \times n}$**

**Justificación teórica:**
$$
\begin{gather}
A^{-1}= Adj(A)\frac{1}{\det(A)} &,& \text{aplicación de determinante} \\ \\
\det(A)A^{-1} = Adj(A) &,& \text{ley uniforme del producto} \\ \\
\det(A)A^{-1}A = Adj(A)A &,& \text{multiplico A en ambos mienmbros} \\ \\
\det(A)(A^{-1}A)=Adj(A)A &,& \text{asociativa de matrices} \\ \\
\det(A)I=Adj(A)A &,& \text{definición de inversa de una matriz} \\ \\
&cqd
\end{gather}
$$
---
### Ejercicio 4.

a) Decide, justificando tu respuesta, si cada una de las matrices del Ejercicio 3 son o no inversibles.  
b) Para aquellas que sean inversibles, calcula su inversa utilizando el método de la adjunta.

##### Solución:
###### a)  
$\text{como todos los determinantes de las matrices son }\neq 0\text{ entonces todas admiten inversa}$
###### b) 
$$
\begin{gather}
A^{-1}= \frac{1}{|A|}Adj(A) = \frac{1}{2} \begin{pmatrix}
1&-1&-1 \\
1&-1&-3 \\
1&1&1
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2}&-\frac{1}{2}&-\frac{1}{2} \\
\frac{1}{2}&-\frac{1}{2}&-\frac{3}{2} \\
\frac{1}{2}& \frac{1}{2} & \frac{1}{2}
\end{pmatrix} \\ \\ \\
B^{-1} = \frac{1}{|B|} Adj(B)= \frac{1}{24} \begin{pmatrix}
0&-24&0 \\
10&43&1 \\
-4&-10&2
\end{pmatrix} = \begin{pmatrix}
0&-1&0 \\
\frac{5}{12}& \frac{43}{24} & \frac{1}{24} \\
-\frac{1}{6}& -\frac{5}{12} & \frac{1}{12}
\end{pmatrix} \\ \\ \\
C^{-1} = \frac{1}{|C|} Adj(C) = \frac{1}{7} \begin{pmatrix}
0&0&-7 \\
-2&7&3 \\
1&0&9
\end{pmatrix} = \begin{pmatrix}
0&0&-1 \\
-\frac{2}{7}&1& \frac{3}{7} \\
\frac{1}{7}& 0 & \frac{9}{7}
\end{pmatrix}
\end{gather}
$$

---

### Ejercicio 5.

Dado el siguiente sistema de ecuaciones lineales:

$$
\begin{pmatrix}
-1 & 1 & 1 \\
1 & 0 & -3 \\
2 & -5 & 3
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
=
\begin{pmatrix}
-1 \\
-18 \\
52
\end{pmatrix}
$$

a) Justifica sin resolverlo que es consistente con única solución.  
b) Encuentra su solución resolviéndolo como una ecuación matricial.

##### Solución:
$$
\begin{gather}
\text{sea el sistema de ecuaciones: } \underbrace{\begin{pmatrix}
-1&1&1 \\
1&0&-3 \\
2&-5&3
\end{pmatrix}}_{A} \cdot \underbrace{\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}}_{X} = \underbrace{\begin{pmatrix}
-1 \\
-18 \\
52
\end{pmatrix}}_{B} \Rightarrow AX=B \\ \\
\text{si el }|A| \text{ es } \neq 0 \text{ entonces admite inversa, lo que indica que puedo hacer: } X=A^{-1}B \\
\text{en consecuencia el sistema seria inconcistente y admitiria solución única.} \\ \\
\text{sin resolver el sistema aplicamos propiedades de determinante para ver si es }\neq 0: \\ \\
\underbrace{\begin{vmatrix}
-1&1&1 \\
1&0&1 \\
2&-5&3
\end{vmatrix}}_{|A|} \xrightarrow[{C_{2}=C_{2}+C_{1}}]{C_{3}=C_{3}+C_{1}} \begin{vmatrix}
-1&0&0 \\
1&1&-2 \\
2&-3&5
\end{vmatrix} \xrightarrow{C_{3}=C_{3}+2C_{2}} \begin{vmatrix}
-1&0&0 \\
1&1&0 \\
2&-3&-1
\end{vmatrix} = 1 \Rightarrow |A|\neq 0 \\ \\
\therefore\text{como el determinante de A es distinto de 0 entonces el sistema es consistente determinado.} \\ \\
\text{encontrando la inversa de A por el metodo de la adjunta, encontramos los Cofactores:} \\ \\
C_{11}= (-1)^{1+1} \begin{vmatrix}
0&-3 \\
-5&3
\end{vmatrix}=-15 \quad C_{12}= (-1)^{1+2}\begin{vmatrix}
1&-3 \\
2&3
\end{vmatrix}=-9 \quad C_{13}= (-1)^{1+3} \begin{vmatrix}
1&0 \\
2&5
\end{vmatrix}=5 \\ \\
C_{21}=(-1)^{2+1}\begin{vmatrix}
1&1 \\
-5&3
\end{vmatrix}=-8 \quad C_{22}=(-1)^{2+2}\begin{vmatrix}
-1&1 \\
2&3
\end{vmatrix}=-5 \quad C_{23} = (-1)^{2+3} \begin{vmatrix}
-1&1 \\
2&-5
\end{vmatrix}=-3 \\ \\
C_{31} = (-1)^{3+1}\begin{vmatrix}
1&1 \\
0&-3
\end{vmatrix}=-3 \quad C_{32} = (-1)^{3+2}\begin{vmatrix}
-1&1 \\
1&-3
\end{vmatrix}=-2 \quad C_{33}=(-1)^{3+3}\begin{vmatrix}
-1&1 \\
1&0
\end{vmatrix}=-1 \\ \\
Cof(A)= \begin{pmatrix}
-15&-9&5 \\
-8&-5&-3 \\
-3&-2&-1
\end{pmatrix} \quad \quad Adj(A)= \begin{pmatrix}
-15&-8&-3 \\
-9&-5&-2 \\
5&-3&-1
\end{pmatrix} \\ \\
A^{-1}=\frac{1}{|A|}Adj(A) = \frac{1}{1} Adj(A) \Rightarrow A^{-1}=Adj(A) \\ \\
\text{resolvemos el sistema: } AX=B \Rightarrow X=B \cdot A^{-1} \\ \\
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix} = \begin{pmatrix}
-15&-8&-3 \\
-9&-5&-2 \\
-5&-3&-1
\end{pmatrix}\begin{pmatrix}
-1 \\
-18 \\
52
\end{pmatrix} \Rightarrow
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix} = \begin{pmatrix}
3 \\
-5 \\
7
\end{pmatrix}
\end{gather}
$$
---

### Ejercicio 6.

Dadas las siguientes matrices:

$$
A = \begin{pmatrix}
1 & 1 \\
1+k & k
\end{pmatrix}
\quad
B = \begin{pmatrix}
1 & 1 & 0 \\
k & 0 & 0 \\
1 & -1 & k+1
\end{pmatrix}
\quad
C = \begin{pmatrix}
1 & 1 & 1 \\
k & 2 & 0 \\
k-1 & 1 & -1
\end{pmatrix}
$$

a) Decide, justificando tu respuesta, si existen valores del parámetro $k$ tales que sean inversibles. En los casos en los que tu respuesta sea afirmativa, expresa la inversa en función del parámetro $k$.  
b) Para alguno de los valores de $k$ determinados en el anterior inciso, determina la inversa de la matriz.

##### Solución:
$$
\begin{gather}
\underbrace{\begin{vmatrix}
1&1 \\
1+k&k
\end{vmatrix}}_{|A|} = (1 \cdot k) - (1+k \cdot 1)=k-1-k=-1\text{ luego tenemos que } |A| \neq 0 \forall k \in \mathbb{R} \\ \\
\underbrace{\begin{vmatrix}
1&1&0 \\
k&0&0 \\
1&-1&k+1
\end{vmatrix}}_{|B|} \xrightarrow{C_{2}=C_{2}-C_{1}} \begin{vmatrix}
1&0&0 \\
k&-k&0 \\
1&-2&k+1
\end{vmatrix} = (1)(-k)(k+1)=-k²-k \\ \\
\text{para que B sea inversible el determinante debe ser distinto de 0 o lo que es igual: } k\neq 0 ~~\lor ~~k\neq -1 \\ \\
\underbrace{\begin{vmatrix}
1&1&1 \\
k&2&0 \\
k-1&1&-1
\end{vmatrix}}_{|C|} \xrightarrow{F_{1}=F_{1}+F_{3}} \begin{vmatrix}
k&2&0 \\
k&2&0 \\
k-1&1&-1
\end{vmatrix}  \\ \\
\text{ luego por teorema, al tener dos filas iguales: } |C| = 0~~ \forall k \in \mathbb{R} \\ \\ \\
\text{si }k=1\text{ podemos calcular una inversa de A y B:} \\
A= \begin{pmatrix}
1&1 \\
2&1
\end{pmatrix} \Rightarrow A^{-1}= \begin{pmatrix}
-1&1 \\
2&-1
\end{pmatrix} \\ \\
B = \begin{pmatrix}
1&1&0 \\
1&0&0 \\
1&-1&2 
\end{pmatrix} \Rightarrow B^{-1}=\begin{pmatrix}
0&1&0 \\
1&-1&0 \\
\frac{1}{2}&-1& \frac{1}{2}
\end{pmatrix}
\end{gather}
$$
---

### Ejercicio 7. Demuestra que:

a) Si $A^2 = A$ entonces $\det A = 0$ o $\det A = 1$.  
b) Si $A$ es antisimétrica de orden $n$, entonces $\det(A^T) = (-1)^n \det A$.  
c) Si $A$ es antisimétrica de orden $n$ y $n$ es impar, entonces $\det A = 0$.  
d) Si 
$$
A = \begin{pmatrix}
k & 0 & 0 \\
1 & k & 0 \\
1 & -1 & k+1
\end{pmatrix}
$$
entonces $\det(A^n) = k^{2n}(k+1)^n$.  
e) Si $A$ es ortogonal, entonces $\det A = \pm 1$.
##### consultar!!!!!!!!
---

### Ejercicio 8.

Dados los siguientes sistemas de ecuaciones lineales:

i)
$$
\begin{cases}
2x - y = 3 \\
-x + y = 1
\end{cases}
$$

ii)
$$
\begin{cases}
x - 2y + z = 0 \\
-x + y + 2z = -2 \\
2x - 3y - z = 2
\end{cases}
$$

iii)
$$
\begin{cases}
2x_1 + 2x_2 + x_3 = 1 \\
x_1 - x_2 - x_3 = 0 \\
3x_1 + x_2 - x_3 = 1 \\
x_1 + 3x_2 + 2x_3 = 2
\end{cases}
$$

Decide, justificando tu respuesta, si son o no Cramerianos (se pueden resolver usando la regla de Cramer). En los casos en los que tu respuesta sea afirmativa, determina su solución, utilizando la regla de Cramer.

##### Solución:
$$
\begin{gather}
\text{i)  el sistema es crameriano, pues su determinante es 1, por lo que puede ser resuelto por su regla:} \\ \\
x= \frac{\begin{vmatrix}
3&-1 \\
1&1
\end{vmatrix}}{1}=4  \quad \quad \quad \quad y= \frac{ \begin{vmatrix}
2&3 \\
-1&1
\end{vmatrix} }{1} =5 \quad \quad \Rightarrow cs=\{(4,5)\} \\ \\ \\
\text{el sistema del inciso ii, tiene determinante 0 y el sistema del inciso iii, no es cuadrado} \\
\text{por lo que ninguno es crameriano y no se puede resolver por su regla.}
\end{gather}
$$
---

### Ejercicio 9.

Decide, justificando tu respuesta, la verdad o falsedad de las siguientes proposiciones:

a) Si $A, B \in \mathbb{R}^{n \times n} \implies \det(A+B) = \det A + \det B$.  
b) $[\det A + \det B]^2 = (\det A)^2 + 2\det A \det B + (\det B)^2$.  
c) $\det(-A) = -\det(A)$.  
d) Si $A$ es antisimétrica, entonces $\det A = 0$.  
e) Si $\det(A) = 0$ entonces $A = \mathcal{O}$ (matriz nula).  
f) Si $A \in \mathbb{R}^{n \times n}$ y $\det A = 0 \implies AX = B$ no tiene solución cualquiera sea $B$.

##### Solución:
#### a) Si $A, B \in \mathbb{R}^{n \times n} \implies \det(A + B) = \det A + \det B$

* **Valor de verdad:** **Falso**
* **Justificación (por contraejemplo):**  
  Sean las matrices de orden $2 \times 2$:
  $$A = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}, \quad B = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$$
  Calculamos sus determinantes individuales:
  $$\det(A) = 0, \quad \det(B) = 0 \implies \det(A) + \det(B) = 0$$
  Sumamos ambas matrices:
  $$A + B = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2 \implies \det(A + B) = 1$$
  Como $1 \neq 0$, la igualdad no se cumple. La función determinante **no es distributiva** respecto a la suma de matrices.
#### b) $[\det A + \det B]^2 = (\det A)^2 + 2\det A \det B + (\det B)^2$

* **Valor de verdad:** **Verdadero**
* **Justificación:**  
  Para cualquier par de matrices $A, B \in \mathbb{R}^{n \times n}$, sus determinantes son **números reales** (escalares):
  $$x = \det(A) \in \mathbb{R}, \quad y = \det(B) \in \mathbb{R}$$
  La expresión corresponde al desarrollo algebraico del cuadrado de un binomio en $\mathbb{R}$:
  $$(x + y)^2 = (x + y)(x + y) = x^2 + xy + yx + y^2$$
  Dado que el producto en el cuerpo de los números reales es conmutativo ($xy = yx$):
  $$(x + y)^2 = x^2 + 2xy + y^2$$
  Reemplazando los escalares:
  $$[\det A + \det B]^2 = (\det A)^2 + 2\det A \det B + (\det B)^2$$
#### c) $\det(-A) = -\det(A)$

* **Valor de verdad:** **Falso** (no se cumple para todo $n$)
* **Justificación:**  
  Por la propiedad de homogeneidad del determinante respecto a cada una de las $n$ filas de $A \in \mathbb{R}^{n \times n}$:
  $$\det(-A) = \det((-1) \cdot A) = (-1)^n \det(A)$$
  * Si $n$ es impar: $(-1)^n = -1 \implies \det(-A) = -\det(A)$.
  * Si $n$ es **par**: $(-1)^n = 1 \implies \det(-A) = \det(A)$.

  **Contraejemplo:** Sea $A = I_2 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \in \mathbb{R}^{2 \times 2}$ ($n=2$):
  $$\det(A) = 1 \implies -\det(A) = -1$$
  $$-A = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} \implies \det(-A) = (-1)(-1) - 0 = 1$$
  Como $1 \neq -1$, la proposición es falsa en general.

#### d) Si $A$ es antisimétrica, entonces $\det A = 0$

* **Valor de verdad:** **Falso** (no se cumple para todo $n$)
* **Justificación:**  
  Por definición, una matriz es antisimétrica si $A^T = -A$. Aplicando determinante a ambos miembros:
  $$\det(A^T) = \det(-A)$$
  Usando que $\det(A^T) = \det(A)$ y $\det(-A) = (-1)^n \det(A)$:
  $$\det(A) = (-1)^n \det(A)$$
  * Si el orden $n$ es **impar**: $(-1)^n = -1 \implies \det(A) = -\det(A) \implies 2\det(A) = 0 \implies \det(A) = 0$.
  * Si el orden $n$ es **par**: $(-1)^n = 1 \implies \det(A) = \det(A)$, por lo que $\det(A)$ puede ser no nulo.

  **Contraejemplo:** Sea la matriz antisimétrica de orden $n=2$:
  $$A = \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix} \quad (A^T = -A)$$
  $$\det(A) = (0)(0) - (1)(-1) = 1 \neq 0$$
#### e) Si $\det(A) = 0$ entonces $A = \mathcal{O}$ (matriz nula)

* **Valor de verdad:** **Falso**
* **Justificación:**  
  Que $\det(A) = 0$ únicamente indica que la matriz es singular (sus filas o columnas son linealmente dependientes), pero no implica que todos sus elementos sean nulos.

  **Contraejemplo:** Sea la matriz de orden $2 \times 2$:
  $$A = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$$
  $$\det(A) = (1)(0) - (0)(0) = 0$$
  Sin embargo, $A \neq \mathcal{O}$ dado que $a_{11} = 1 \neq 0$.
#### f) Si $A \in \mathbb{R}^{n \times n}$ y $\det A = 0 \implies AX = B$ no tiene solución cualquiera sea $B$

* **Valor de verdad:** **Falso**
* **Justificación:**  
  Si $\det A = 0$, el sistema no admite solución única (no es crameriano), pero según el Teorema de Rouché-Frobenius puede ser:
  1. **Incompatible:** No tiene solución.
  2. **Compatible indeterminado:** Tiene **infinitas soluciones** (cuando el rango de $A$ coincide con el rango de la matriz ampliada).

  En particular, para cualquier sistema lineal homogéneo ($B = \mathcal{O}$), siempre existe al menos la solución trivial $X = \mathcal{O}$ (y si $\det A = 0$, existen infinitas soluciones).

  **Contraejemplo:** Consideremos $A = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$ con $\det(A) = 0$, y el vector $B = \begin{pmatrix} 2 \\ 0 \end{pmatrix}$:
  $$\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \end{pmatrix} \implies \begin{cases} 1x + 0y = 2 \implies x = 2 \\ 0x + 0y = 0 \quad (\text{se satisface } \forall y \in \mathbb{R}) \end{cases}$$
  El conjunto solución es:
  $$S = \left\{ \begin{pmatrix} 2 \\ y \end{pmatrix} : y \in \mathbb{R} \right\}$$
  Por lo tanto, el sistema posee infinitas soluciones y no es incompatible para todo $B$.

### Bibliografía
- [1] Grossman, S. (2019). *Álgebra lineal con Connect*. McGraw-Hill Latinoamérica.  
- [2] Anton, H. (2004). *Introducción al álgebra lineal* (3ª ed.). Limusa.