## Espacios vectoriales

uno de los principales estudios del álgebra lineal consiste en los espacios vectoriales y en esta unidad veremos como armar uno y estudiarlo.

**Definición:**
	sea $\mathbb{V}$ un conjunto, podemos definir sobre este conjunto dos operaciones, que van a ser la suma ( $+$ ) y el producto ( $\cdot$ ), si cuando definimos estas operaciones sobre el conjunto y ademas cumple con 10 propiedades entonces podemos decir con seguridad que $\mathbb{V}$ es un espacio vectorial.

¿Qué propiedades debe cumplir para afirmar que es un espacio vectorial?

a ver para ser mas específicos la suma y el producto deben cumplir unas condiciones antes de dictar sus propiedades:

* la suma debe ser entre dos elementos de $\mathbb{V}$
* el producto debe realizarse entre un elemento de $\mathbb{V}$ y un elemento de un cuerpo de escalares: $k \in \mathbb{R} \lor \mathbb{C}$ 

**Propiedades:**
	las 10 propiedades se dividen en 2 grupos, son 5 para la suma y 5 para el producto.

1. La suma es cerrada en $\mathbb{V}$ : $\forall u,v \in \mathbb{V} \Rightarrow u+v \in \mathbb{V}$ 
2. La suma es conmutativa: $\forall u,v \in \mathbb{V}: u+v=v+u$ 
3. La suma es asociativa: $\forall u,v,w \in \mathbb{V}: (u+v)+w=u+(v+w)$ 
4. La existencia de un elemento neutro: $\exists \odot \in \mathbb{V},\forall v \in \mathbb{V}: v+\odot=\odot+v=v$ 
5. La existencia del opuesto aditivo: $\forall v \in \mathbb{V},\exists -v \in \mathbb{V}:v+(-v)=-v+v=\odot$

6. El producto por un escalar es una operación cerrada: $\forall v \in \mathbb{V},\forall k \in \mathbb{K} \Rightarrow vk \in \mathbb{V}$ 
7. Distributiva con respecto a la suma de escalares: $\forall v \in \mathbb{V},\forall k,h \in \mathbb{K} : v(k+h)=vk+vh$ 
8. Distributiva con respecto a la suma de vectores: $\forall v,u \in \mathbb{V},\forall k \in \mathbb{K}:k(u+v)=ku+kv$
9. Asociativa mixta: $\forall h,k \in \mathbb{K},\forall v \in \mathbb{V}:h\cdot k\cdot v=h(kv)$
10. Existencia del elemento neutro: $\forall v \in \mathbb{v}, \exists k \in \mathbb{K}:vk=kv=v$ 

**Observación:**
	al referirme yo a un conjunto $\mathbb{V}$ genérico me refiero a que cualquier conjunto ya sea de los reales o complejos o cualquiera que yo pueda inventar que cumpla con esas definiciones ya estoy hablando de un espacio vectorial, cuyos elementos se llaman vectores y el nulo se llama vector nulo. por ejemplo, el cuerpo de las matrices de $M^{n \times m}$ es un espacio vectorial.
**U.N.Sa. Facultad de Ciencias Exactas**  
**Asignatura:** Álgebra Lineal y Geometría Analítica  
**Carreras:** PM, LAS, LF, LER, TEU, TUP, TUES  
**Año:** 2º Cuatrimestre 2026  

---

# Trabajo Práctico Nº 3
### Espacios vectoriales - Subespacios - Combinaciones lineales - Subespacio generado - Dependencia e Independencia Lineal

**Duración:** 3 clases.  

### Objetivos
Que el estudiante sea capaz de:
- Reconocer la estructura de espacio vectorial en los conjuntos más usuales, verificando el cumplimiento de sus propiedades.
- Identificar subespacios vectoriales y distinguirlos de aquellos subconjuntos que no lo son.
- Reconocer e interpretar geométricamente los subespacios de $\mathbb{R}^{2}$ y $\mathbb{R}^{3}$.
- Determinar combinaciones lineales de vectores e interpretar geométricamente este concepto en $\mathbb{R}^{2}$ y $\mathbb{R}^{3}$.
- Reconocer y justificar cuándo un conjunto de vectores es linealmente dependiente o independiente, utilizando las definiciones y propiedades correspondientes.
- Desarrollar razonamientos lógico-deductivos para justificar procedimientos y demostrar propiedades vinculadas con los conceptos trabajados.

**Tecnología sugerida:** Se recomienda utilizar GeoGebra, Matrix Calculator, Symbolab, Wolfram Alpha o cualquier software de álgebra computacional para verificar resultados.

---

### Ejercicio 1
Decide, justificando tu respuesta, en cada uno de los siguientes casos, si el conjunto $\mathbb{V}$ es un espacio vectorial sobre $\mathbb{R}$, con las operaciones de adición ($+$) y producto ($\cdot$) por un escalar dadas:

| Conjunto $\mathbb{V}$                                                                          | Adición ($+$)                         | Producto por escalar ($\cdot$)       |
| :--------------------------------------------------------------------------------------------- | :------------------------------------ | :----------------------------------- |
| $\mathbb{V} = \{(x,y) \in \mathbb{R}^{2} \mid x - 2y = 1\}$                                    | La usual en $\mathbb{R}^{2}$          | El usual en $\mathbb{R}^{2}$         |
| $\mathbb{V} = \{(x,y) \in \mathbb{R}^{2} \mid x - 2y = 0\}$                                    | La usual en $\mathbb{R}^{2}$          | El usual en $\mathbb{R}^{2}$         |
| $\mathbb{V} = \mathbb{R}^{2}$                                                                  | $(a,b) + (c,d) = (a+c, b+d)$          | $k \cdot (a,b) = (a, kb)$            |
| $\mathbb{V} = \{(x,y,z) \in \mathbb{R}^{3} \mid 2x + y - z = 0\}$                              | La usual en $\mathbb{R}^{3}$          | El usual en $\mathbb{R}^{3}$         |
| $\mathbb{V} = \{x \in \mathbb{R} \mid x > 0\}$                                                 | $a + b = a \cdot b$                   | $k \cdot a = a^{k}$                  |
| $\mathbb{V}= \begin{pmatrix}  x&y  \\  z&w \end{pmatrix} \in \mathbb{R}^{2 \times 2}\| y-3w=0$ | La usual en $\mathbb{R}^{2 \times 2}$ | La usual en $\mathbb{R}^{2\times 2}$ |
| $\mathbb{V} = \{A \in \mathbb{R}^{n\times n} \mid A = -A^{T}\}$                                | La usual en $\mathbb{R}^{n\times n}$  | El usual en $\mathbb{R}^{n\times n}$ |

**Solución:**
$$
\begin{matrix}
i)~~~ \forall u,v \in \mathbb{R} \Rightarrow u+v \in \mathbb{V} \\ \\
sea~~v= x_{1}-2y_{1}=1 \\
sea~~u= x_{2}
-2y_{2}=1  \\ \\
u+v\Rightarrow x_{1}-2y_{1}+x_{2}-2y_{2}=2 \\
\Rightarrow (x_{1}-x_{2})+(2y_{1}-2y_{2})=2 \\
si~x_{3}=(x_{1}-x_{2})~~\land~~y_{3}=2(y_{1}-y_{2}) \\
x_{3}+2y_{3}=2 \\ \\
\therefore \text{no es un espacio vectorial pues la suma no es cerrada en $\mathbb{V}.$}
\end{matrix}
$$
$$
\begin{matrix}
ii)1)~~~\forall u,v \in \mathbb{V} \Rightarrow u+v \in \mathbb{V} \\ \\
sea~~u=x_{1}-2y_{1}=0 \\
sea~~v= x_{2}-2y_{2}=0 \\ \\
u+v \Rightarrow x_{1}-2y_{1}+x_{2}-2y_{2}=0 \\
\Rightarrow (x_{1}-x_{2})+(2y_{1}-2y_{2})=0 \\
\Rightarrow \underbrace{(x_{1}-x_{2})}+ 2\underbrace{(y_{1}-y_{2})}=0 \\
x_{3}~~~~~~~~~~~~~~~~~~2y_{3} \\
x_{3}+2y_{3}=0 \\ \\

\therefore \text{cumple que la suma es cerrada.}  \\ \\
2)~~~ \forall u,v \in \mathbb{V} : u+v=v+u \\ \\
x_{1}-2y_{1}+x_{2}-2y_{2}=x_{2}-2y_{2}+x_{1}-2y_{1}  \\
(x_{1}-x_{2})+(2y_{1}-2y_{2})= ( x_{2}-x_{1})+(2y_{2}-2y_{1}) \\
(x_{1}-x_{2})+2(y_{1}-y_{2})= ( x_{2}-x_{1})+2(y_{2}-y_{1}) \\
2(y_{1}-y_{2})-2(y_{2}-y_{1})=(x_{2}-x_{1})-(x_{1}-x_{2}) \\
2 \left[ (y_{1}-y_{2}-y_{2}+y_{1}) \right]= x_{2}-x_{1}-x_{1}+x_{2} \\
2 \left[ (2y_{1}-2y_{2}) \right]=2x_{2}-2x_{1} \\
2(y_{1}-y_{2})=x_{2}-x_{1} \\
2(y_{1}-y_{2})-(x_{2}-x_{1})=0 \\
-(x_{2}-x_{1})+2(y_{1}-y_{2})=0 \\
(x_{1}-x_{2})+2(y_{1}-y_{2})=0 \\ \\
\therefore \text{cumple la conmutatividad de la suma.} \\ \\
3)~~~ \forall u,v,w \in \mathbb{V} : (u+v)+w=u+(v+w) \\ \\

\end{matrix}
$$
---

### Ejercicio 2
Sea $(\mathbb{V}, +, \mathbb{R}, \cdot)$ un espacio vectorial. Demuestra que:
- **a)** Si $\vec{0}$ es el neutro de la suma en $\mathbb{V}$, entonces $\forall \alpha \in \mathbb{R},\; \alpha \cdot \vec{0} = \vec{0}$.
- **b)** Si $\alpha \in \mathbb{R} \land u \in \mathbb{V} \land \alpha u = \vec{0} \implies \alpha = 0 \lor u = \vec{0}$.

---

### Ejercicio 3
Decide, justificando tu respuesta, si el conjunto $\mathbb{S}$ es o no un subespacio del espacio $\mathbb{V}$ que se indica en cada uno de los siguientes casos, con las operaciones de suma y producto usuales en cada uno de los espacios dados. Cuando se trate de conjuntos de $\mathbb{R}^{2}$ o $\mathbb{R}^{3}$ interpreta geométricamente.

- **a)** $\mathbb{S} = \{(x,y) \in \mathbb{R}^{2} \mid y - x = 0\}$
- **b)** $\mathbb{S} = \{(x,y) \in \mathbb{R}^{2} \mid y - x = 0 \land 2x + 3y = 0\}$
- **c)** $\mathbb{S} = \{(x,y) \in \mathbb{R}^{2} \mid x \ge 0\}$
- **d)** $\mathbb{S} = \{(x,y) \in \mathbb{R}^{2} \mid y = x^{2}\}$
- **e)** $\mathbb{S} = \{(x,y,z) \in \mathbb{R}^{3} \mid 2x + y - z = 1\}$
- **f)** $\mathbb{S} = \{(x,y,z) \in \mathbb{R}^{3} \mid x - y + 2z = 0 \land 2x - y + z = 0\}$
- **g)** $\mathbb{S} = \{X \in \mathbb{R}^{2\times 2} \mid X \text{ es diagonal}\}$
- **h)** $\mathbb{S} = \{X \in \mathbb{R}^{n\times n} \mid X - X^{T} = \mathcal{O}\}$

---

### Ejercicio 4
Demuestra que:
- **a)** El conjunto solución de un sistema homogéneo de $m$ ecuaciones lineales con $n$ incógnitas es un subespacio del espacio $\mathbb{R}^{n}$ sobre el cuerpo de los reales y con las operaciones de suma y producto por un escalar usuales en $\mathbb{R}^{n}$.

- **b)** Si $\mathbb{S}_{1}$ y $\mathbb{S}_{2}$ son subespacios de un espacio vectorial $\mathbb{V}$, entonces $\mathbb{S} = \mathbb{S}_{1} \cap \mathbb{S}_{2}$ también es un subespacio de $\mathbb{V}$.

---

### Ejercicio 5
Dados los vectores $u = (1,3)$, $v = (2,4)$, $w = (-3,1)$ de $\mathbb{R}^{2}$ y $r = (1,2,3)$, $s = (-1,1,-1)$, $t = (0,3,2)$ de $\mathbb{R}^{3}$.  
Calcula:
- **i)** $2u - v$
- **ii)** $u + 3v - w$
- **iii)** $3r - s$
- **iv)** $\frac{3}{4}s + t$
- **v)** $3r + s - t$

**Solución:**
$$
\begin{matrix}
i)~~~2u-v= (1,3)-(2,4)& \text{por hipotesis} \\
a=(-1,-1)& \text{por definición de suma de vectores} \\ \\ \\
ii)~~~ u+3v-w=(1,3)+3(2,4)-(-3,1) & \text{por hipotesis} \\
(1,3)+(6,12)+(3,-1)& \text{por definición de producto de un escalar por un vector} \\
b=(10,14) & \text{por definición de suma de vectores} \\ \\ \\
iii)~~~ 3r-s=3(1,2,3)-(-1,1,-1) & \text{por hipotesis} \\
(3,6,9)+(1,-1,1)& \text{por definición de producto de un escalar por un vector} \\
c=(4,5,10) & \text{por definicón de suma de vectores} \\ \\ \\
iv)~~~ \frac{3}{4}s+t= \frac{3}{4}(-1,1,-1)+(0,3,2)& \text{por hipotesis} \\
\left( -\frac{3}{4}, \frac{3}{4} , -\frac{3}{4} \right)+(0,3,2) & \text{por definición de producto de un escalar por un vector} \\
d=\left( -\frac{3}{4} , \frac{15}{4} , \frac{5}{4} \right) & \text{por definición de suma de vectores} \\ \\ \\
v)~~~3r+s-t = (3,6,9)+(-1,1,-1)-(0,3,2) & \text{por hipotesis} \\
()
\end{matrix}
$$
*Interpreta geométricamente cuando se trate de vectores de $\mathbb{R}^{2}$.*

![[Pasted image 20260829013845.png]]

---

### Ejercicio 6
Dados los vectores $r$, $s$ y $t$ del ejercicio anterior:
- **a)** Determina una combinación lineal de ellos.
- **b)** Determina todas las combinaciones lineales de ellos.
- **c)** Expresa a $\vec{0}$ como combinación lineal de $r$, $s$ y $t$.
- **d)** Justifique conceptualmente si $v_{1} = (1,8,7)$ y $v_{2} = (1,4,6)$ son combinaciones lineales de $r$, $s$ y $t$.

**soluciones:**
$$
\begin{matrix}
\text{sea } \vec{x} = \alpha_{1}v_{1}+\alpha_{2}v_{2}+\dots+\alpha_{n}v_{n} \\
\vec{x}=\alpha_{1}(1,2,3)+ \alpha_{2}(-1,1,-1)+ \alpha_{3}(0,3,2) \\
\vec{x} = (\alpha_{1},2\alpha_{1}, 3\alpha_{1} ) + (-\alpha_{2}, \alpha_{2}, -\alpha_{2} ) + (0, 3\alpha_{3}, 2\alpha_{3} ) \\
\vec{x} = (x,y,z) \Rightarrow (x,y,z)=(\alpha_{1}-\alpha_{2}, 2\alpha_{1}+ \alpha_{2} + 3\alpha_{3}, 3\alpha_{1}-\alpha_{2}+ 2\alpha_{3} ) \\
\begin{cases}
\alpha_{1}-\alpha_{2}=x \\
2\alpha_{1}+ \alpha_{2} + 3\alpha_{3}=y \\
3\alpha_{1}-\alpha_{2}+ 2\alpha_{3}
\end{cases} \\  \\
\left( \begin{array}{ccc|c}
1&-1&0&x \\
2&1&3&y \\
3&-1&2&z
\end{array} \right) \sim \left( \begin{array}{ccc|c}
1&-1&0&x \\
0&3&3&y-2x \\
0&2&2&z-3x
\end{array} \right) \sim \left( \begin{array}{ccc|c}
1&-1&0&x \\
0&3&3&y-2z \\
0&0&0&3z-5x-2y
\end{array} \right) \\ \\
\sim \begin{cases}
\alpha_{1}-\alpha_{2}=x \\
3\alpha_{2}+3\alpha_{3}=y-2z \\
0=5x+2y-3z
\end{cases}  \\ \\
\text{la condición para que el sistem tenga solución es:} \\ \\
5x+2y-3z=0 \\ \\
\therefore \text{ para que el sistema tenga solución lo cual me indica que existen los escalares} \\
\text{y por ende el vector $\vec{x}$ es combinación lineal de r,s y t es todo aquel vector de $\mathbb{R}^3$} \\
\text{que cumple con la condicón o dicho en simbolos:} \\
\forall \vec{x} \in \mathbb{R}^3 : 5x+2y-3z=0 \\ \\
\text{una solución particular: } (1,2,3) \\ \\ \\
si~~\vec{0} \text{ es combinacion lineal de r,s y t entonces:} \\ \\
(0,0,0)=\alpha_{1}(1,2,3)+\alpha_{2}(-1,1,-1)+\alpha_{3}(0,3,2) \\
(0,0,0)= (\alpha_{1}-\alpha_{2}, 2\alpha_{1}+ \alpha_{2} + 3\alpha_{3}, 3\alpha_{1}-\alpha_{2}+ 2\alpha_{3} ) \\
\begin{cases}
\alpha_{1}-\alpha_{2}=0 \\
2\alpha_{1}+ \alpha_{2} + 3\alpha_{3}=0 \\
3\alpha_{1}-\alpha_{2}+ 2\alpha_{3}=0
\end{cases} \\ \\
\begin{pmatrix}
1&-1&0 \\
2&1&3 \\
3&-1&2
\end{pmatrix} \sim \begin{pmatrix}
1&-1&0 \\
0&3&3 \\
0&2&2
\end{pmatrix} \sim \begin{pmatrix}
1&-1&0 \\
0&3&3 \\
0&0&0
\end{pmatrix} \sim \begin{cases}
\alpha_{1}-\alpha_{2}=0 \\
3\alpha_{2}+3\alpha_{3}=0 
\end{cases} \\ \\
\therefore \text{podemos ver que el vector: $\vec{0}$ es combinación lineal de r,s y t para cualquier escalar de $\mathbb{R}^3$}
\end{matrix}
$$
---
### Ejercicio 7
En cada caso, decide, justificando tu respuesta:

- **a)** ¿$w$ es combinación lineal de $u$ y $v$? En caso afirmativo, expresa a $w$ como combinación lineal de $u$ y $v$.
  - **i)** $u = (1,2,-3)$, $v = (1,-1,1)$ y $w = (0,0,0)$
  - **ii)** $u = (1,-1,2)$, $v = (0,1,1)$ y $w = (1,2,-1)$
  - **iii)** $u = x^{2} - x$, $v = 2x^{2} + x - 1$ y $w = -x^{2} + 4x - 2$

- **b)** ¿Existen valor/es del parámetro $k$ tal que el vector $t$ sea combinación lineal de $u$, $v$ y $w$?
  - **i)** $u = (1,-1,1)$, $v = (2,1,1)$, $w = (0,-1,1)$ y $t = (1,k,k-1)$

- **ii)** $u = \begin{pmatrix} 1 & 2 \\ -1 & 0 \end{pmatrix}$, $v = \begin{pmatrix} 2 & 1 \\ -1 & 4 \end{pmatrix}$, $w = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$ y $t = \begin{pmatrix} 0 & -1 \\ 2 & -1 \end{pmatrix}$

**Solución:**
$$
\begin{matrix}
b)i)~~~ (1,k,k-1)=\alpha_{1} u+ \alpha_{2}v+\alpha_{3}w \\
(1,k,k-1)=(\alpha,-\alpha,\alpha)+(2\alpha_{2},\alpha_{2},\alpha_{2})+(0,-\alpha_{3},\alpha_{3}) \\
(1,k,-1)=(\alpha_{1}+2\alpha_{2}~,~ -\alpha_{1}+ \alpha_{2}- \alpha_{3}~,~ \alpha_{1}+\alpha_{2}+\alpha_{3} ) \\ \\
\begin{cases}
\alpha_{1}+2\alpha_{2} =1\\
-\alpha_{1}+ \alpha_{2}- \alpha_{3}=k \\
\alpha_{1}+\alpha_{2}+\alpha_{3}=k-1
\end{cases} \sim \left( \begin{array}{ccc|c}
1&2&0&1 \\
-1&1&-1&k \\
1&1&1&k-1
\end{array} \right) \\ \\
\left( \begin{array}{ccc|c}
1&2&0&1 \\
0&3&-1&k+1 \\
0&-1&1&k-2
\end{array} \right) \sim \left( \begin{array}{ccc|c}
1&2&0&1 \\
0&3&-1&k+1 \\
0&0&2&4k-5
\end{array} \right) \sim \begin{cases}
\alpha_{1}+2\alpha_{2}=1 \\
3\alpha_{2}-\alpha_{3}=k+1 \\
2\alpha_{3}=4k-5
\end{cases} \\
 \\
consultar!!!!!
\end{matrix}
$$
---

### Ejercicio 8
En cada caso determina $\mathcal{L}(\mathbb{G})$. Interpreta geométricamente los casos de $\mathbb{R}^{2}$:
- **a)** $\mathbb{G} = \{(1,3)\}$
$$
\begin{matrix}
\vec{x}=\alpha(1,3) \\
(x,y)=\alpha(1,3) \\
(x,y)=(\alpha,3\alpha) \\ \\
\begin{cases}
\alpha=x \\
3\alpha=y
\end{cases} \sim \left ( \begin{array}{c|c}
1&x \\
3&y
\end{array} \right) \sim \left ( \begin{array}{c|c}
1&x \\
0&y-3x
\end{array} \right) \sim \begin{cases}
\alpha=x \\
0=-2y
\end{cases} \\ \\
gen\{(1,3)\}=\{\forall (x,y) \in \mathbb{R}^2 : -3x+y=0\}
\end{matrix}
$$
- **b)** $\mathbb{G} = \{(1,3), (2,4)\}$
$$
\begin{matrix}
\vec{x}=\alpha_{1}(1,3)+\alpha_{2}(2,4) \\
\vec{x}=(\alpha_{1},3\alpha_{1})+(2\alpha_{2},4\alpha_{2}) \\
\vec{x}=(\alpha_{1}+2\alpha_{2},3\alpha_{1}+4\alpha_{2}) \\
(x,y)=(\alpha_{1}+2\alpha_{2},3\alpha_{1}+4\alpha_{2}) \\ \\
\begin{cases}
\alpha_{1}+2\alpha_{2}=x \\
3\alpha_{1}+4\alpha_{2}=y
\end{cases} \sim \left ( \begin{array}{cc|c}
1&2&x \\
3&4&y
\end{array} \right) \sim \left ( \begin{array}{cc|c}
1&2& x\\
0&-2&y-3x
\end{array} \right) \sim \begin{cases}
\alpha_{1}+2\alpha_{2}=x \\
-2\alpha_{2}=-3x+y 
\end{cases} \\ \\
\therefore \text{como no es necesario aplicar ninguna condición podemos afirmar que todo } \mathbb{R}^2 \text{ genera el subespacio} 
\end{matrix}
$$
- **c)** $\mathbb{G} = \{(-1,1,-1), (0,3,2)\}$
$$
\begin{matrix}
\vec{x}=\alpha_{1}(-1,1,-1)+\alpha_{2}(0,3,2) \\
\vec{x}=(-\alpha_{1},\alpha_{1},-\alpha_{1})+(0,3\alpha_{2},2\alpha_{2}) \\
\vec{x}=(-\alpha_{1},\alpha_{1}+3\alpha_{2},-\alpha_{1}+2\alpha_{2}) \\
(x,y,z)=(-\alpha_{1},\alpha_{1}+3\alpha_{2},-\alpha_{1}+2\alpha_{2}) \\ \\
\begin{cases} 
-\alpha_{1}=x \\
\alpha_{1}+3\alpha_{2} =y\\
-\alpha_{1}+2\alpha_{2}=z
\end{cases} \sim \left( \begin{array}{cc|c} 
-1&0&x \\
1&3&y \\
-1&2&z
\end{array} \right) \sim \left( \begin{array}{cc|c} 
-1&0&x \\
0&-3&-y-x \\
0&-2&-z+x
\end{array} \right) \sim \left( \begin{array}{cc|c} 
-1&0&x \\
0&-3&-y-x \\
0&0&3z-x-2y
\end{array} \right) \\  \\
\begin{cases}
-\alpha_{1}=x \\
3\alpha_{2}=y+x \\
0=x+2y-3z
\end{cases} \Rightarrow cond: x+2y-3z=0 \\ \\
\therefore gen\{(-1,1,-1),(0,3,2)\}=\{\forall (x,y,z) \in \mathbb{R}^3:x+2y-3z=0\}
\end{matrix}
$$
- **d)** $\mathbb{G} = \left\{ \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \begin{pmatrix} -1 & 0 \\ 0 & 2 \end{pmatrix} \right\}$
$$
\begin{matrix}
\vec{x}= \alpha_{1} \begin{pmatrix}
1&0 \\
0&1
\end{pmatrix} + \alpha_{2} \begin{pmatrix}
-1&0 \\
0&2
\end{pmatrix} \\ \\
\vec{x}=  \begin{pmatrix}
\alpha_{1}&0 \\
0&\alpha_{1}
\end{pmatrix} + \begin{pmatrix}
-\alpha_{2}&0 \\
0&2\alpha_{2}
\end{pmatrix} \\ \\
\vec{x}= \begin{pmatrix}
\alpha_{1}-\alpha_{2}& 0\\
0& \alpha_{1}+2\alpha_{2}
\end{pmatrix} \\ \\
\begin{pmatrix}
a&b \\
c&d
\end{pmatrix} = \begin{pmatrix}
\alpha_{1}-\alpha_{2}& 0\\
0& \alpha_{1}+2\alpha_{2}
\end{pmatrix} \\ \\
\begin{cases}
\alpha_{1}-\alpha_{2}
= a \\
0=b \\
0=c \\
\alpha_{1}+2\alpha_{2}=d
\end{cases}
\end{matrix}
$$

---

### Ejercicio 9
Para los subespacios del Ejercicio 3, encuentra un conjunto generador. ¿Es único?

---

### Ejercicio 10
Decide, justificando tu respuesta, si los siguientes conjuntos dados son linealmente independientes o dependientes:
- **i)** $\mathbb{S} = \{(1,-1)\}$
$$
\begin{matrix}
\text{al ser $\mathbb{S}$ un conjunto unitario cuyo unico elemento es distinto del vector nulo} \\
\text{podemos afirmar por teorema que el conjunto $\mathbb{S}$ es linealmente independiente.}
\end{matrix}
$$
- **ii)** $\mathbb{S} = \{(1,-1), (-1,1), (2,2)\}$
$$
\begin{matrix}
\text{usando la definicion de dependencia lineal puedo expresar} \\
\text{a uno de los vectores como combinación lineal del resto:} \\ \\
(1,-1)=-1(-1,1)+0(2,2) \\ \\
\therefore \text{el conjunto es linealmente dependiente.}
\end{matrix}
$$
- **iii)** $\mathbb{S} = \{(0,0,0), (1,-1,1), (1,1,0)\}$
$$
\text{el comjunto $\mathbb{S}$ contiene al vector nulo y sabemos por teorema que es linealmente dependiente.}
$$

- **iv)** $\mathbb{S} = \{(1,1,2), (1,-1,1), (1,1,0)\}$
$$
\begin{matrix}
\alpha_{1}(1,1,2)+\alpha_{2}(1,-1,1)+\alpha_{3}(1,1,0)=(0,0,0) \\
(\alpha_{1},\alpha_{1},2\alpha_{1})+(\alpha_{2},-\alpha_{2},\alpha_{2})+(\alpha_{3},\alpha_{3},0)=(0,0,0) \\
(\alpha_{1}+\alpha_{2}+\alpha_{3},\alpha_{1}-\alpha_{2}+\alpha_{3},2\alpha_{1}+\alpha_{2})=(0,0,0) \\ \\
\begin{cases}
\alpha_{1}+\alpha_{2}+\alpha_{3} =0\\
\alpha_{1}-\alpha_{2}+\alpha_{3} =0\\
2\alpha_{1}+\alpha_{2}=0
\end{cases} \sim \begin{pmatrix}
1&1&1 \\
1&-1&1 \\
2&1&0
\end{pmatrix} \\  \\
\sim \begin{pmatrix}
1&1&1 \\
0&-2&0 \\
0&-1&-2
\end{pmatrix} \sim \begin{pmatrix}
1&1&1 \\
0&-2&0 \\
0&0&-4
\end{pmatrix} \sim \begin{cases}
\alpha_{1}+\alpha_{2}+\alpha_{3}=0 \\
-2\alpha_{2}=0 \\
-4\alpha_{3}=0
\end{cases} \\ \\
\text{tenemos el sistema escalonado con 3 incognitas y 3 ecuaciones por lo que no hay variables libres} \\
\text{lo que significa que el sistema tiene solución unica y al ser un sistema homogeneo la solución es} \\
\text{la trivial por lo tanto } \alpha_{1}=\alpha_{2}=\alpha_{3}=0 \text{ por lo tanto el conjunto es linealmente independiente.}
\end{matrix}
$$

- **v)** $\mathbb{S} = \left\{ \begin{pmatrix} 1 & 0 \\ -1 & -1 \end{pmatrix}, \begin{pmatrix} 1 & 0 \\ 1 & 2 \end{pmatrix}, \begin{pmatrix} -1 & 1 \\ 0 & 2 \end{pmatrix} \right\}$
$$
\begin{matrix}
\alpha_{1} \begin{pmatrix}
1&0 \\
-1&-1
\end{pmatrix} + \alpha_{2}\begin{pmatrix}
1&0 \\
1&2
\end{pmatrix} + \alpha_{3} \begin{pmatrix}
-1&1 \\
0&2
\end{pmatrix}= \begin{pmatrix}
0&0 \\
0&0\end{pmatrix} \\ \\
\begin{pmatrix}
\alpha_{1}&0 \\
-\alpha_{1}&-\alpha_{1}
\end{pmatrix} + \begin{pmatrix}
\alpha_{2}&0 \\
\alpha_{2}&2\alpha_{2}
\end{pmatrix}+\begin{pmatrix}
-\alpha_{3}&\alpha_{3} \\
0&2\alpha_{3}
\end{pmatrix}= \begin{pmatrix}
0&0 \\
0&0\end{pmatrix} \\ \\
\begin{pmatrix}
\alpha_{1}+\alpha_{2}-\alpha_{3}&\alpha_{3} \\
-\alpha_{1}+\alpha_{2}&-\alpha_{1}+2\alpha_{2}+2\alpha_{3}
\end{pmatrix} = \begin{pmatrix}
0&0 \\
0&0\end{pmatrix} \\ \\
\begin{cases}
\alpha_{1}+2\alpha_{2}-\alpha_{3}=0 \\
\alpha_{3}=0 \\
-\alpha_{1}+\alpha_{2}=0 \\
-\alpha_{1}+2\alpha_{2}+2\alpha_{3}=0
\end{cases} \sim \begin{pmatrix}
1&2&-1 \\
0&0&1 \\
-1&1&0 \\
-1&2&2
\end{pmatrix} \\ \\
 \sim \begin{pmatrix}
1&2&-1 \\
0&0&1 \\
0&3&-1 \\
0&4&1
\end{pmatrix}  \sim \begin{pmatrix}
1&2&-1 \\
0&3&-1 \\
0&4&1 \\
0&0&1
\end{pmatrix}  \sim \begin{pmatrix}
1&2&-1 \\
0&3&-1 \\
0&0&7 \\
0&0&1
\end{pmatrix} \sim \begin{cases}
\alpha_{1}+2\alpha_{2}-\alpha_{3}=0 \\
3\alpha_{2}-\alpha_{3}=0 \\
7\alpha_{3}=0 
\end{cases} \\ \\
\text{tenemos el sistema escalonado con 3 incognitas y 3 ecuaciones por lo que no hay variables libres} \\
\text{lo que significa que el sistema tiene solución unica y al ser un sistema homogeneo la solución es} \\
\text{la trivial por lo tanto } \alpha_{1}=\alpha_{2}=\alpha_{3}=0 \text{ por lo tanto el conjunto es linealmente independiente.}
\end{matrix}
$$

- **vi)** $\mathbb{S} = \{x^{2} + 2x - 1,\; x - 1,\; 2x^{2} - x + 2\}$
$$
consultar!!!!!
$$

---

### Ejercicio 11
Dado el conjunto $\mathbb{S} = \{(1,1,1), (0,1,1+k), (0,1,k^{2}+2k+1)\}$, determina, justificando tu respuesta, si existe/n valor/es del parámetro $k$ para los que el conjunto sea:
- **i)** Linealmente independiente
- **ii)** Linealmente dependiente

**Solución:**
$$
\begin{matrix}
\alpha_{1}(1,1,1)+\alpha_{2}(0,1,1+k)+\alpha_{3}(0,1,k^2+2k+1)=(0,0,0) \\
(\alpha_{1},\alpha_{1},\alpha_{1})+(0,\alpha_{2},\alpha(1+k))+(0,\alpha_{3},\alpha_{3}(k^2+2k+1))=(0,0,0) \\
(\alpha_{1}, \alpha_{1}+\alpha_{2}+\alpha_{3},\alpha_{1}+\alpha_{2}(1+k)+\alpha_{3}(k^2+2k+1))=(0,0,0) \\ \\
\begin{cases}
\alpha_{1}=0 \\
\alpha_{1}+\alpha_{2}+\alpha_{3}=0 \\
\alpha_{1}+\alpha_{2}(1+k)+\alpha_{3}(k^2+2k+1)=0
\end{cases} \sim \begin{pmatrix}
1&0&0 \\
1&1&1 \\
1&1+k&k²+2k+1
\end{pmatrix} \\ \\
\begin{pmatrix}
1&0&0 \\
1&1&1 \\
1&1+k&k²+2k+1
\end{pmatrix} \sim \begin{pmatrix}
1&0&0 \\
0&1&1 \\
0&1+k&k²+2k+1
\end{pmatrix} \sim \begin{pmatrix}
1&0&0 \\
0&1&1 \\
0&0&k²+k
\end{pmatrix} \sim \begin{cases}
\alpha_{1}=0 \\
\alpha_{2}+\alpha_{3}=0 \\
\alpha_{3}(k²+k)=0
\end{cases}\\ \\
\text{vemos en el sistema escalonado que la ultima ecuacion depende de k para ambos casos} \\
\text{si }k²+k=0 \text{ tenemos los valores que anulan al }\alpha_{3} \text{ por lo que quedaria un sistema con } \\
\text{2 ecuaciones y 3 incognitas lo que significa que tiene infinitas soluciones y entonces} \\
\text{el sistema seria linealmente dependiente por teorema, para eso :} \\ \\
k²+k=0 \Rightarrow k(k+1)=0 \Rightarrow k=0 ~~\lor  ~~ k=-1 \\
 \\
\therefore \text{si $k=0 ~~ \lor~~ k=-1$ el sistema es LD y si es distinto a esos valores es LI.}
\end{matrix}
$$
---

### Ejercicio 12
Si un conjunto $\mathbb{A} = \{u, v, w\}$ es linealmente independiente, decide, justificando tu respuesta:
- **a)** ¿Cómo es el conjunto $\mathbb{B} = \{3u + w, 2u - v, v + 3w\}$?
- **b)** ¿Existe, al menos, un valor de $k$ para que $\mathbb{C} = \{u + v, 2ku - v, v + kw\}$ sea linealmente dependiente?

$$
\begin{matrix}
\text{sabemos que el conjunto }\mathbb{A} \text{ es linealmente independiente o lo que quiere decir:} \\
\alpha_{1}u+\alpha_{2}v+\alpha_{3}w= \odot \Rightarrow \alpha_{1}=\alpha_{2}=\alpha_{3}=0 \\ \\
\text{veamos ahora la depndencia lieal de }\mathbb{B}: \\ \\
\beta_{1} (3u+w) + \beta_{2}(2u-v)+\beta_{3}(v+3w)= \odot \\
(3\beta_{1}u+\beta_{1}w)+(2\beta_{2}u-\beta_{2}v)+(\beta_{3}v+3\beta_{3}w)= \odot \\
(3\beta_{1}u+2\beta_{2}u)+(-\beta_{2}v+\beta_{3}v)+(\beta_{1}w+3\beta_{3}w)= \odot \\
(3\beta_{1}+2\beta_{2})u+(\beta_{3}-\beta_{2})v+(\beta_{1}+3\beta_{3})w= \odot \\ \\
\text{como }u,v ~~y~~w \text{ son linealmente independiente entonces} \\ \\
\begin{cases}
3\beta_{1}+2\beta_{2}=0 \\
-\beta_{2}+\beta_{3}=0 \\
\beta_{1}+3\beta_{3}=0
\end{cases} \sim \begin{pmatrix}
3&2&0 \\
0&-1&1 \\
1&0&1
\end{pmatrix} \sim \begin{pmatrix}
3&2&0 \\
1&0&1 \\
0&-1&1
\end{pmatrix} \\ \\
\sim \begin{pmatrix}
3&2&0 \\
0&-2&3 \\
0&-1&1
\end{pmatrix} \sim \begin{pmatrix}
3&2&0 \\
0&-2&3 \\
0&0&1
\end{pmatrix} \sim \begin{cases}
3\beta_{1}+2\beta_{2}=0 \\
-2\beta_{2}+3\beta_{3}=0 \\
\beta_{3}=0
\end{cases} \\ \\
\text{como me quedo un sistema escalonado con 3 ecuaciones y 3 incognitas puedo asegurar por teorema} \\
\text{que el sistema tiene solución única y ademas al ser un sistema homogeneo la soluciónes la trivial} \\
\text{por ende el existe una unica combinacion de escalares que lo resuelve la cual es } \beta_{1}=\beta_{2}=\beta_{3}=0 \\
\text{lo que significa que el conjunto }\mathbb{B} \text{ es linealmente independiente.} 
\end{matrix}
$$

---

### Ejercicio 13
Sean $\mathbb{S}_{1}, \mathbb{S}_{2}$ subconjuntos de un mismo espacio vectorial $\mathbb{V}$. Demuestra que:
- **a)** Si $\mathbb{S}_{1} \subset \mathbb{S}_{2}$ y $\mathbb{S}_{1}$ es linealmente dependiente, entonces $\mathbb{S}_{2}$ también lo es.
- **b)** Si $\mathbb{S}_{1} = \{u\}$ y $u \ne \vec{0}$, entonces $\mathbb{S}_{1}$ es linealmente independiente.
- **c)** Si $u, v, w \in \mathbb{V}$ son tales que $u = av + bw$, entonces $\mathbb{S} = \{u, v, w\}$ es linealmente dependiente.

---

### Ejercicio 14
Decide, justificando tu respuesta, la verdad o falsedad de las siguientes proposiciones:
- **a)** Dado un espacio vectorial $(\mathbb{V}, +, \mathbb{R}, \cdot)$, $\forall u \in \mathbb{V}, \forall \alpha, \beta \in \mathbb{R} : \alpha u = \beta u \land u \ne \vec{0} \implies \alpha = \beta$.
- **b)** Dado un espacio vectorial $(\mathbb{V}, +, \mathbb{R}, \cdot)$, $\forall u, v \in \mathbb{V}, \forall \alpha \in \mathbb{R} : \alpha u = \alpha v \land \alpha \ne 0 \implies u = v$.
- **c)** La suma de dos subespacios de un espacio vectorial, sobre un mismo cuerpo y con las mismas operaciones de suma y producto por un escalar, es también un subespacio sobre el mismo cuerpo y con las mismas operaciones.
- **d)** El conjunto $\mathbb{S} = \{(1,0,1), (0,2,-1), (0,-2,1)\}$ genera a $\mathbb{R}^{3}$.
- **e)** Si $u \in \mathcal{L}(\{v, w\})$ entonces $u$ es combinación lineal de $v$ y $w$.
- **f)** Si un conjunto es linealmente dependiente entonces contiene al vector nulo.
- **g)** Si un conjunto genera a $\mathbb{R}^{3}$ entonces contiene exactamente tres vectores de $\mathbb{R}^{3}$.
- **h)** Cualquier conjunto unitario es linealmente independiente.
- **i)** $\mathbb{S} = \{u_{1}, u_{2}, \dots, u_{k}\} \subset \mathbb{R}^{n} \land k > n \implies \mathbb{S}$ es linealmente independiente.

---

### Bibliografía
1. Grossman S. - *Álgebra Lineal con Aplicaciones* - McGraw-Hill[cite: 1]
2. Lipschutz S. - *Álgebra Lineal* - McGraw-Hill[cite: 1]
3. Anton H. - *Introducción al Álgebra Lineal* - Noriega Editores[cite: 1]
4. Kolman B., Hill D. - *Álgebra Lineal* - Pearson / Prentice Hall[cite: 1]
5. David Poole - *Álgebra Lineal* - Cengage Learning[cite: 1]
6. Augusto Estrada - *Álgebra Lineal. Tutoriales: Una Estrategia de Enseñanza para su Aprendizaje Comprensivo* - Milor Talleres Gráficos[cite: 1]