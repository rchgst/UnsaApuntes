# Trabajo Práctico Nº 2
## Matrices. Álgebra matricial. Matrices Cuadradas. Simétricas, Antisimétricas e Inversa. Aplicación a sistemas de ecuaciones lineales

> [!info] **U.N.Sa. - Facultad de Ciencias Exactas**
> **Asignatura:** Álgebra Lineal y Geometría Analítica  
> **Carreras:** PM, LAS, LF, LER, TEU, TUP, TUES  
> **Año / Cuatrimestre:** 2º Cuatrimestre 2026  
> **Duración:** 2 clases  

---

### Objetivos
Que el estudiante sea capaz de:
- Conocer y manejar de manera correcta la simbología de sumatoria y sus propiedades.
- Comprender el concepto de matriz y las operaciones básicas entre ellas.
- Reconocer las matrices especiales y sus propiedades.
- Calcular la inversa de una matriz utilizando la definición de inversa y/o las operaciones elementales entre filas.
- Desarrollar y aplicar un pensamiento lógico deductivo en la justificación de procedimientos y demostraciones.

---

### Ejercicio 1:

**a)** Evalúe las siguientes sumatorias:
- i) $$\sum_{k=1}^{4} 2k$$
`solución:`
$$
\sum_{k=1}^42k=2+4+6+8=20
$$
- ii) $$\sum_{k=0}^{5} (2k+1)$$
`solución:`
$$
\sum_{k=0}^5(2k+1)=1+3+5+7+9=25
$$
- iii) $$\sum_{k=0}^{4} \frac{(-1)^k n}{n+1}$$
`solución:`
$$
\sum_{k=0}^4\frac{(-1)^kn}{n+1}= \frac{4}{5}- \frac{4}{5} +\frac{4}{5}- \frac{4}{5}+\frac{4}{5}= \frac{4}{5}
$$
- iv) $$\sum_{k=1}^{4} a_{k2}$$
`solución:`
$$
\sum_{k=1}^4a_{k2}= a_{12} + a_{22} + a_{32} + a_{44}
$$
- v) $$\sum_{k=1}^{4} a_{3k} b_{k2}$$
`solución:`
$$
\sum_{k=1}^4 a_{31}b_{12}+a_{32}b_{22}+a_{33}b_{32}+a_{34}b_{42}
$$
- vi) $$\sum_{i=1}^{2} \sum_{j=1}^{2} (-1)^{i+j} a_{ij} M_{ij}$$
`solución:`
$$
\sum_{i=1}^2\sum_{j=1}^2(-1)^{i+j}a_{ij}M_{ij}=a_{11}M_{11}+a_{12}M_{12}+a_{21}M_{21}+a_{22}M_{22}
$$

**b)** Exprese las siguientes sumas, utilizando la simbología de sumatoria:
- i) $\frac{1}{3} - \frac{1}{12} + \frac{1}{48} - \frac{1}{192}$
- ii) $\beta b_{11} + \beta b_{21} + \beta b_{12} + \beta b_{22} + \beta b_{13} + \beta b_{23}$
- iii) $c_{21}d_{12} + c_{22}d_{22} + c_{23}d_{32} + c_{24}d_{42}$
- iv) $a_{11} + b_{11} + a_{22} + b_{22} + \dots + a_{nn} + b_{nn}$

`solución:`
$$
i)~~~ \frac{1}{3} - \frac{1}{12} + \frac{1}{48} - \frac{1}{192} = \sum_{i=0}^3 \frac{(-1)^i1}{3 \cdot 4^i}
$$
$$
ii)~~~ \beta b_{11} + \beta b_{21} + \beta b_{12} + \beta b_{22} + \beta b_{13} + \beta b_{23} = \sum_{i=1}^3\left( \sum_{j=1}^2 \beta b_{ji} \right)
$$
$$
iii)~~~ c_{21}d_{12} + c_{22}d_{22} + c_{23}d_{32} + c_{24}d_{42} = \sum_{i=1}^4c_{2i}d_{i_{2}}
$$
$$
iv)~~~ a_{11} + b_{11} + a_{22} + b_{22} + \dots + a_{nn} + b_{nn} = \sum_{i=1}^n(a_{ii}+b_{ii})
$$
---

### Ejercicio 2:

Determine y exprese las siguientes matrices:

- **i)** $A_{3 \times 2} = (a_{ij}) \quad / \quad a_{ij} = \begin{cases} 2i - j & \text{si } i \neq j \\ -2 & \text{si } i = j \end{cases}$
- **ii)** $B_{3 \times 3} = (b_{ij}) \quad / \quad b_{ij} = \begin{cases} 0 & \text{si } j > i \\ i - j & \text{si } i \ge j \end{cases}$
- **iii)** $C_{3 \times 3} = (c_{ij}) \quad / \quad c_{ij} = \begin{cases} 3 & \text{si } i = j \\ 0 & \text{si } i \neq j \end{cases}$
- **iv)** $D_{3 \times 3} = (d_{ij}) \quad / \quad d_{ij} = \begin{cases} 0 & \text{si } i = j \\ j - 2i & \text{si } i \neq j \end{cases}$
`solución:`
$$
\begin{matrix}
i)~~~ \begin{pmatrix}
-2& 0\\
3& -2\\
5&4
\end{pmatrix} ~~~ii)~~~\begin{pmatrix}
0&0&0 \\
1&0&0 \\
2&1&0
\end{pmatrix}~~~iii)~~~ \begin{pmatrix}
3&0&0 \\
0&3&0 \\
0&0&3
\end{pmatrix} ~~~ iv)~~~ \begin{pmatrix}
0&0&1 \\
-3&0&-1 \\
-5&-4&0
\end{pmatrix}
\end{matrix}
$$

---

### Ejercicio 3:

Dadas las siguientes matrices:

$$A = \begin{pmatrix} 1 & 3 \\ 3 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 3 \\ 2 & 0 \\ 2 & 1 \end{pmatrix}, \quad C = \begin{pmatrix} 0 & 1 & 2 \\ 1 & 2 & -1 \\ 1 & 0 & 1 \end{pmatrix}$$

$$D = \begin{pmatrix} 1 & 2 & 0 \\ 1 & 2 & -3 \end{pmatrix}, \quad E = \begin{pmatrix} 3 & 2 & 1 \\ 6 & 4 & 2 \\ 3 & 2 & 1 \end{pmatrix}, \quad F = \begin{pmatrix} -1 & 0 & 0 \\ 1 & 2 & 0 \\ 1 & 1 & 1 \end{pmatrix}$$

**a)** Realice, de ser posible, las operaciones que se indican a continuación. En los casos que no sea posible, justifique el por qué:
- i) $A + A^T= \begin{pmatrix} 2&6 \\  6&2\end{pmatrix}$
- ii) $AB^T + D \Rightarrow B^T=\begin{pmatrix} 1&2&2 \\  3&0&1\end{pmatrix}, AB^T=\begin{pmatrix} 10&8&5  \\  6&6&7  \\  \end{pmatrix},AB^T+D=\begin{pmatrix} 11&10&5 \\ 7&8&4  \end{pmatrix}$
- iii) $AD - 2B^T \Rightarrow AD= \begin{pmatrix} 4&8&-9  \\  4&8&-3 \end{pmatrix}, 2B^T=\begin{pmatrix} 2&4&4  \\  6&0&2 \end{pmatrix}, AD-2B^T=\begin{pmatrix} 2&4&-13  \\  -2&8&-5 \end{pmatrix}$
- iv) $F + 2C - B^2 \Rightarrow \text{no se puede realizar pues, }B \in M_{3x2} \text{ y no se puede realizar el producto }B \cdot B$
- v) $\frac{1}{3}C + \frac{2}{3}C - 2C \Rightarrow \frac{1}{3}+\frac{2}{3}-2(C)=-C= \begin{pmatrix} 0&-1&-2 \\  -1&-2&1 \\  -1&0&-1  \end{pmatrix}$
- vi) $(B^T + D)^T - D^T \Rightarrow ((B^T+D)-D)^T=(B^T+(D-D))^T=(B^T)^T=B=\begin{pmatrix} 1&3 \\ 2&0 \\ 2&1 \end{pmatrix}$
- vii) $2DE + FC \Rightarrow \text{no se puede realizar pues, }D \cdot E \in M_{2 x 3} \text{ y }F \cdot C \in M_{3 x 3} \text{ entonces no se puede realizar la suma de }2DE+FC \text{ por que no tienen el mismo orden}$
- viii) $BD - 2C \Rightarrow BD=\begin{pmatrix} 4&8&-9 \\ 2&4&0 \\ 3&6&-3 \end{pmatrix},~BD-2C= \begin{pmatrix} 4&6&-13 \\ 0&0&2 \\ 1&6&-5 \end{pmatrix}$

**b)** Encuentre $X$ tal que $B - 2X = D^T$.

`solución:`
$$
\begin{matrix}
B-2X=D^T \\
\begin{pmatrix}
1&3 \\
2&0 \\
2&1
\end{pmatrix}- 2 \begin{pmatrix}
a&b \\
c&d \\
e&f
\end{pmatrix}= \begin{pmatrix}
1&1 \\
2&2 \\
0&-3
\end{pmatrix} \\
\begin{pmatrix}
1-2a&3-2b \\
2-2c&-2d \\
2-2e&1-2f
\end{pmatrix}=\begin{pmatrix}
1&1 \\
2&2 \\
0&-3
\end{pmatrix} \\ \\
1-2a=1 \Rightarrow a=0 \\
3-2b=1 \Rightarrow b=1 \\
2-2c=2 \Rightarrow c=0 \\
-2d=2 \Rightarrow d=-1 \\
2-2e=0 \Rightarrow e=1 \\
1-2f=-3 \Rightarrow f=2 \\ \\
\begin{pmatrix}
1&3 \\
2&0 \\
2&1
\end{pmatrix} -2 \begin{pmatrix}
0&1 \\
0&-1 \\
1&2
\end{pmatrix}=\begin{pmatrix}
1&1 \\
2&2 \\
0&-3
\end{pmatrix} \\
\begin{pmatrix}
1&1 \\
2&2 \\
0&-3
\end{pmatrix}=\begin{pmatrix}
1&1 \\
2&2 \\
0&-3
\end{pmatrix}
\end{matrix}
$$
**c)** Sea $A = \begin{pmatrix} 5 & 0 \\ 2 & \alpha \end{pmatrix}$. Determine el valor de $\alpha$ para el cual $A$ es una raíz del polinomio $p(x) = x^2 - 25$.  
*(Nota: En la última igualdad $-25$ representa la matriz escalar del orden que corresponda).*

---

### Ejercicio 4:

Decida, justificando su respuesta, la verdad o falsedad de las siguientes proposiciones:

**a)** $\forall A, B \in \mathbb{R}^{n \times n}, \quad (A + B)^2 = A^2 + 2AB + B^2$.

`solución:`
$$
\begin{matrix}
(A+B)^2=(A+B)(A+B)=(A+B)A+(A+B)B=A^2+BA+AB+B^2 \\
\text{teniendo AB y BA serian 2AB si y solo si A y B conmutaran} \\
\text{pero eso no esta asegurado para todas las matrices asi que:} \\
\therefore \text{no es verdadera la proposición.}
\end{matrix}
$$
**b)** $\forall A, B, C \in \mathbb{R}^{n \times n}, \quad A \neq \mathbb{O}, \; AB = AC \implies B = C$.

`solución:`
$$

$$
**c)** Si $A \in \mathbb{R}^{m \times n}$ y $B \in \mathbb{R}^{n \times p}$, entonces $(AB)^T = B^T A^T$.

---

### Ejercicio 5:

**a)** Defina: Matriz simétrica, antisimétrica, triangular, diagonal y escalar. Dé un ejemplo de $3 \times 3$ para cada una de ellas.

`aolución:`
$$
\begin{matrix} 
sea ~~A \in M_{n x m} \\ \\
\text{Matriz simetrica es una matriz la cual cumple con la siguiente propiedad:} \\
 A^T=A \\ \\
\text{matriz antisimétrica es la matriz que cumple lo siguiente:} \\
A^T=-A \\ \\
\text{matriz triangular es la matriz que tiene 0 por arriba} \\
\text{o por debajo de la diagonal principal, si es por arriba:} \\
A=\begin{pmatrix}
x&0&0 \\
a&y&0 \\
b&c&z
\end{pmatrix}\Rightarrow triangular~~superior. \\
A=\begin{pmatrix}
x&a&b \\
0&y&c \\
0&0&z
\end{pmatrix} \Rightarrow triangular~~inferior. \\ \\
\text{La matriz diagonal es la matriz que solo tiene valores} \\
\text{en su diagonal y en el resto solo ceros: } \\
A=\begin{pmatrix}
a&0&0 \\
0&b&0 \\
0&0&c
\end{pmatrix} \\ \\
\text{una matriz escalar es una matriz que esta siendo multiplicada por un escalar no nulo:} \\
A=\begin{pmatrix}
a&b&c \\
d&e&f \\
g&h&i
\end{pmatrix} \Rightarrow kA=\begin{pmatrix}
ka&kb&kc \\
kd&ke&kf \\
kg&kh&ki
\end{pmatrix}
\end{matrix}
$$

**b)** Siendo $A$ y $B$ matrices cuadradas, demuestre que:
- i) Si $A$ y $B$ son matrices antisimétricas, entonces $(A + B)$ es antisimétrica.
- ii) $AA^T$ es simétrica.
- iii) Cualquier matriz $A$ se puede expresar de forma única como la suma de una matriz simétrica y una matriz antisimétrica.

---

### Ejercicio 6:

Siendo $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$ y $B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, encuentre las condiciones para $a, b, c$ y $d$ para que $A$ y $B$ conmuten.

`solución:`
$$
\begin{matrix}
\begin{pmatrix}
1&1 \\
0&1
\end{pmatrix}\begin{pmatrix}
a&b \\
c&d
\end{pmatrix}=\begin{pmatrix}
a&b \\
c&d
\end{pmatrix}\begin{pmatrix}
1&1 \\
0&1
\end{pmatrix} \\ \\
\begin{pmatrix}
a+c&b+d \\
c&d
\end{pmatrix}=\begin{pmatrix}
a&a+b \\
c&c+d
\end{pmatrix} \\ \\
\begin{cases}
a+c=a \\
b+d=a+b \\
c=c \\
d=c+d
\end{cases} \sim \begin{cases}
c=0 \\
d=a \\
0=0 \\
c=0
\end{cases} \\ \\
B=\begin{pmatrix}
a&b \\
0&a
\end{pmatrix}
\end{matrix}
$$
---

### Ejercicio 7:

Si $A = \begin{pmatrix} a & 1 \\ 0 & a \end{pmatrix}$:

**a)** Determine si existen valores de $a$ para los que la ecuación $AX = X$ tenga solución para una matriz $X_{2 \times 2}$ no nula.

`solución:`
$$

$$
**b)** Demuestre que $\forall n \in \mathbb{N}, \quad A^n = \begin{pmatrix} a^n & n a^{n-1} \\ 0 & a^n \end{pmatrix}$ con $a \neq 0$.

---

### Ejercicio 8:

Dadas las siguientes matrices:

$$A = \begin{pmatrix} 2 & 2 \\ 1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix}, \quad C = \begin{pmatrix} 3 & 0 \\ 2 & 1 \end{pmatrix}$$

$$D = \begin{pmatrix} -1 & 2 & 1 \\ 1 & 0 & 1 \\ 0 & 1 & 2 \end{pmatrix}, \quad E = \begin{pmatrix} -1 & 0 & 0 \\ 1 & 2 & 0 \\ 1 & 1 & -1 \end{pmatrix}, \quad F = \begin{pmatrix} 1 & 3 & 1 \\ -1 & 1 & -3 \\ 1 & 1 & 2 \end{pmatrix}$$

**a)** Determine, de ser posible, su inversa utilizando la definición. En caso de no ser posible justifique por qué no es posible.

**b)** Ídem al inciso anterior pero utilizando la matriz aumentada $(A \mid I)$ reducida por filas.

`solución:`
$$
\begin{matrix}
A \cdot A^{-1}=I \Rightarrow \begin{pmatrix}
2&2 \\
1&3
\end{pmatrix}\begin{pmatrix}
a&b \\
c&d
\end{pmatrix}=\begin{pmatrix}
1&0 \\
0&1
\end{pmatrix} \\ \\
\begin{pmatrix}
2a+2c&2b+2d \\
a+3c&b+3d
\end{pmatrix}= \begin{pmatrix}
1&0 \\
0&1
\end{pmatrix} \\ \\
\begin{cases}
2a+2c=1 \\
2b+2d=0 \\
a+3c=0 \\
b+3d=1
\end{cases}~\sim~\begin{cases}
2a+2c=1 \\
a+3c=0
\end{cases}~~\land~~\begin{cases}
2b+2d=0 \\
b+3d=1
\end{cases} \\ \\
1)~~ \left( \begin{array}{cc|c}
2&2&1 \\
1&3&0
\end{array} \right)\sim \left( \begin{array}{cc|c}
2&2&1 \\
0&4&-1
\end{array} \right) \sim \begin{cases}
2a+2c=1 \\
4c=-1
\end{cases} \Rightarrow Cs=\left\{ \left(\frac{3}{4}, -\frac{1}{4} \right) \right\} \\ \\
2)~~ \left( \begin{array}{cc|c}
2&2&0 \\
1&3&1
\end{array} \right) \sim \left( \begin{array}{cc|c}
2&2&0 \\
0&2&1
\end{array} \right)\sim \begin{cases}
2b+2d=0 \\
2d=1
\end{cases} \Rightarrow Cs=\left\{ \left(-\frac{1}{\text{2}} ,\frac{1}{\text{2}} \right) \right\} \\ \\
\therefore \text{la matriz inversa de A es: } A^{-1}=\begin{pmatrix}
\frac{3}{4}&-\frac{-1}{2} \\
-\frac{1}{4}& \frac{1}{2}
\end{pmatrix}\sim \begin{pmatrix}
3&-2 \\
-1&2
\end{pmatrix}
\end{matrix}
$$
$$
\begin{matrix}
(A|I)= \left( \begin{array}{cc|cc}
2&2&1&0 \\
1&3&0&1
\end{array} \right) \sim \left( \begin{array}{cc|cc}
2&2&1&0 \\
0&4&-1&2
\end{array} \right) \sim \frac{1}{2}F_{1}, \frac{1}{4}F_{2} \left( \begin{array}{cc|cc}
1&1& \frac{1}{2} &0 \\
0&1& -\frac{1}{4} & \frac{1}{2}
\end{array} \right) \\ \\
F_{1}=F_{1}-F_{2} \left( \begin{array}{cc|cc}
1&0& \frac{3}{4} & -\frac{1}{2} \\
0&1& -\frac{1}{4} & \frac{1}{2}
\end{array} \right) \Rightarrow A^{-1}= \begin{pmatrix}
\frac{3}{4}& -\frac{1}{2} \\
-\frac{1}{4}& \frac{1}{2}
\end{pmatrix}\sim \begin{pmatrix}
3&-2 \\
-1&2
\end{pmatrix}
\end{matrix}
$$
1
---

### Ejercicio 9:

Dadas las siguientes matrices con parámetro $k$:

$$A = \begin{pmatrix} k & 2 \\ 2 & k \end{pmatrix}, \quad B = \begin{pmatrix} 1 & k+1 \\ 2 & 2k+2 \end{pmatrix}, \quad C = \begin{pmatrix} k & 1 & 1 \\ 1 & k & 1 \\ 0 & 1 & k-1 \end{pmatrix}$$

**a)** Determine, si existen, valores de $k$ tal que la matriz sea invertible. En caso afirmativo encuentre su inversa en función del parámetro $k$.

**b)** Para algún valor del parámetro, de los determinados en a), encuentre la inversa de la matriz.

---

### Ejercicio 10:

**a)** Demuestre que si $A_{n \times n}$ es inversible, entonces el sistema de ecuaciones lineales $AX = B$ tiene solución única.

**b)** Para cada uno de los sistemas de ecuaciones lineales dados:

$$\begin{cases} x + y = 1 \\ -x + 2y = 1 \end{cases} \qquad \begin{cases} u + v + w = 1 \\ u + 2v + 3w = 0 \\ -u + v - 2w = -1 \end{cases} \qquad \begin{cases} x - y + 2z = 2 \\ 3x - 2y + z = 3 \\ 2x - y - z = 1 \end{cases}$$

- **i)** Expréselos en forma matricial (de la forma $AX = B$).
- **ii)** Aplique lo demostrado en a) para determinar si tienen o no solución única. En caso afirmativo determine la misma resolviendo el sistema matricialmente.

---

### Ejercicio 11: Flujo de información en una red de sensores

Una empresa de monitoreo ambiental cuenta con 5 sensores, cada uno representado por un vértice (nodo) $S_i$ en un grafo dirigido. Si existe una flecha (arista) de $S_i$ hacia $S_j$, es porque el sensor $S_i$ transmite directamente una alerta al sensor $S_j$. La red de comunicaciones observada incluye las siguientes relaciones:

$$S_1 \rightarrow S_2, \quad S_1 \rightarrow S_3, \quad S_2 \rightarrow S_4, \quad S_3 \rightarrow S_5, \quad S_4 \rightarrow S_5$$

Considere las siguientes definiciones:
- Una arista es una flecha entre dos sensores.
- Una cadena es un camino indirecto (de longitud mayor que 1) que une a dos sensores a través de otros.
- Una alerta directa o de primer orden es una arista.
- Una alerta indirecta de segundo orden ocurre cuando $S_i$ alerta a $S_j$ a través de otro sensor.
- Una alerta indirecta de tercer orden ocurre cuando intervienen dos sensores intermediarios, y así sucesivamente.

**a)** Represente el grafo dirigido que describe las relaciones de la red de comunicaciones brindada.

**b)** Escriba la matriz de adyacencia $A = (a_{ij})$ correspondiente al grafo, siendo $a_{ij} = 1$ si hay arista de $S_i$ hacia $S_j$ y $a_{ij} = 0$ en caso contrario.

**c)** Determine si existe algún sensor que reciba alerta de todos los demás sensores, ya sea de forma directa o indirecta. Justifique su respuesta.

**d)** ¿Cuál es el orden mínimo mediante el cual el sensor $S_1$ logra alertar al sensor $S_5$? Describa el camino.

---

### Ejercicio 12: Compra de insumos de librería

Tres sectores de una empresa deben adquirir insumos de librería para sus oficinas. Solicitan presupuesto a dos proveedores, que ofrecen diferentes precios según el tipo de insumo: papel, tinta y carpetas. El primer proveedor ofrece los siguientes precios: una resma de papel a 5 €, un cartucho de tinta a 45 € y una carpeta a 3 €. El segundo proveedor ofrece la resma de papel a 6 €, el cartucho de tinta a 40 € y la carpeta a 4 €. Las necesidades de los sectores son:

| Sector | Papel (resma) | Tinta (cartuchos) | Carpetas |
| :--- | :---: | :---: | :---: |
| **Ventas** | 10 | 4 | 20 |
| **Marketing** | 15 | 6 | 10 |
| **Legales** | 8 | 2 | 30 |

**a)** Represente los datos mediante una matriz $P \in \mathbb{R}^{2 \times 3}$ con el precio de los insumos por proveedor, y con otra matriz $S \in \mathbb{R}^{3 \times 3}$ las necesidades por sector.

**b)** Calcule el costo total de cada proveedor para cada sector.

**c)** Responda:
- i) ¿Qué vendedor resulta más económico para cada sector?
- ii) ¿Cuál sería el gasto total si cada sector elige al proveedor más barato?

---

### Ejercicio 13:

Decida, justificando su respuesta, la verdad o falsedad de las siguientes proposiciones:

**a)** Si una matriz es escalar, entonces es diagonal.

**b)** Si $A$ es antisimétrica, entonces $\forall n \in \mathbb{N}$, $A^n$ es también antisimétrica.

**c)** La suma de dos matrices inversibles es también una matriz inversible.

**d)** Si $A, B, C \in \mathbb{R}^{n \times n}$ son inversibles y tales que $A$ conmuta con $B$ y con $C$, entonces:
$$(ABC)^{-1} = A^{-1} B^{-1} C^{-1}$$

**e)** Si $A^2 + 3A = kI$ y $k \neq 0$, entonces $\frac{1}{k}(A + 3I) = A^{-1}$.

---

### Bibliografía
- **[1]** Grossman, Stanley (2012). *Álgebra Lineal - Séptima Edición*. McGraw-Hill, México.
- **[2]** Anton, Howard (1994). *Introducción al Álgebra Lineal - Tercera Edición*. Limusa Noriega Editores, México.