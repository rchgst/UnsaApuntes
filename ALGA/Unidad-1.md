## Ecuaciones lineales. Ecuaciones lineales con parámetros. Sistemas de ecuaciones lineales. Método de Gauss. Sistemas con parámetros. Aplicaciones.

###  TP1

*Ejercicio 1:
a) Defina qué es una ecuación lineal y mencione los tipos de soluciones posibles en función de sus coeficientes*

Una ecuación lineal es aquella ecuación que esta dada por la forma: $mx+b$ , donde m es la pendiente y coeficiente principal, x es la incógnita de la ecuación y b es el termino independiente, se la llama ecuación lineal por que su representación gráfica es una linea recta.

```obs-graph
2x+3
```
si prestamos atención a los coeficientes que acompañan a la ecuación ( m y b) dependiendo de sus valores la solución de la misma se ve afectada veamos sus casos:

1. si $m\neq0$ no importa el valor de b que la ecuación va a tener solución y ademas va a ser única.
2. si $a=0\land b=0 \Rightarrow$ la ecuación va a tener infinitas soluciones para cualquier valor de x.
3. si $a=0 \land b\neq0$ la ecuación no va a tener ninguna solución, pues no hay valor de x que satisfaga este resultado.

---

*b) Determine el valor de a para que la ecuación* $a(ax − 1) = 3(3x − 1)$ *tenga infinitas soluciones en* $\mathbb{R}$.
$$
\begin{matrix}
a(ax-1)=3(3x-1) \\
a^2 x-a=9x-3 \\
a^2x-9x-a=-3 \\
(a^2-9)x=-3+a \\
\text{si tomamos a = 3} \\
(3^2-9)x=-3+3 \\
(9-9)x=0 \\
0x=0 \\
0=0 \\
\therefore \text{para que la ecuación tenga $\infty$ soluciones a = 3}
\end{matrix}
$$

---

*c) Proporcione tres pares ordenados (x, y) que satisfagan la ecuación $−x+2y = 10.$ Justifique su elección.*
$$
\begin{matrix}
-x+2y=10 \\
2y=10+x \\
y= \dfrac{x+10}{2} \\
\text{como es una ecuación lineal podemos elegir un x} \\
\text{para que salga un y automaticamente} \\
\text{si $x=0 \Rightarrow y=5$ entonces $-0+2(5)=10$} \\
\text{si $x=2 \Rightarrow y=6$ entonces $-2+2(6)=10$} \\
\text{si $x=-4 \Rightarrow y=3$ entonces $4+2(3)=10$}
\end{matrix}
$$

---

*d) Calcule el valor de c para que el punto $(−2, 3)$ sea solución de la ecuación $2x + y − c = 0$.*
$$
\begin{matrix}
2x+y-c=0 \\
y=-2x+c \\
\text{remplazamos el par y despejamos c:} \\
3=-2(-2)+c \\
3=4+c \\
-1=c \\
\text{remplazamos en la ecuación original:} \\
y=-2x-1 \\
\text{evaluamos el par ordenado:} \\
3=-2(-2)-1 \equiv 3=3 \\
\therefore \text{cuando $c = -1$ el par ordenado es solución de $2x+y-c=0$}
\end{matrix}
$$

---

*Ejercicio 2: Para cada sistema de ecuaciones:*
**a) Determine la solución analíticamente (utilizando el método algebraico de su elección).
b) Clasifique el sistema según su tipo de solución (compatible determinado, compatible indeterminado o incompatible).
c) Verifique gráficamente la clasificación obtenida, representando las rectas en el plano cartesiano.** 
$$
a)\begin{cases}
x+y=1 \\
x+2y=6
\end{cases}
$$
$$
\begin{matrix}
\text{por el metodo de sustitucion:} \\ \\
1)~~x+y=1 \Rightarrow y = 1-x \\
2)~~x+2(1-x)=6 \\
2-x=6 \\
x=-4 \\
1)~~y=1+4=5 \\ \\
cs=\{(-4,5)\} \\ 
\end{matrix}
$$
```obs-system
x+y=1
x+2y=6
```

---

$$
b)\begin{cases}
4x+y=3 \\
2x-y=-3
\end{cases}
$$
$$
\begin{matrix}
\text{por el metodo de reducción:} \\
(4x+y=3) +(2x-y=-3)=(6x=0) \\
x=0 \Rightarrow y=3 \\
cs\{(0,3)\}
\end{matrix}
$$
```obs-system
4x+y=3
2x-y=-3
```

---

$$
c) \begin{cases}
x+y-2=0 \\
2x+2y=4
\end{cases}
$$

$$
\begin{matrix}
\text{por metodo de reducción:} \\
-2(x+y=2)+(2x+2y=4)= \\
(-2x-2y=-4)+(2x+2y=4)=(0=0) \\
\text{tiene infinitas soluciones}
\end{matrix}
$$
```obs-system
x+y=2
2x+2y=4
```

---

$$
d) \begin{cases}
x+3y-6=0 \\
-2x+4y+2=0
\end{cases}
$$
$$
\begin{matrix}
2(x+3y-6=0)+(-2x+4y+2=0)= \\
(2x+6y-12=0)+(-2x+4y+2=0)= \\
10(y-1)=0 \\
cs= \{(3,1)\}
\end{matrix}
$$
```obs-system
x+3y=6
4y-2x=-2
```

---

$$
e) \begin{cases}
2x-3y=2 \\
-4x+6y=3
\end{cases}
$$
$$
\begin{matrix}
2(2x-3y=2)+(-4x+6y=3)=  \\
(4x-6y=4) + (-4x+6y=3)= \\
0=7 \\
\text{sin solución}
\end{matrix}
$$
```obs-system
2x-3y=2
-4x+6y=3
```

---

*Ejercicio 3:*
**Para los sistemas de ecuaciones de los incisos i), iv) y v) del ejercicio anterior, determine al menos un sistema de ecuaciones equivalente para cada uno, y justifique brevemente por qué los sistemas propuestos son equivalentes.**

`definición:`
	**2 sistemas de ecuaciones lineales son equivalentes si y solo si tienen el mismo conjunto solución.**

`definición:`
	**existen 3 operaciones que me permiten conseguir sistemas de ecuaciones equivalentes partiendo de un sistema, estas operaciones se denominan operaciones elementales:**

1. operación elemental 1: se pueden intercambiar dos ecuaciones (filas entre si) 
$$
i)\begin{cases}
x+y=1 \\
x+2y=6
\end{cases} \equiv
\begin{cases}
x+2y=6 \\
x+y=1
\end{cases}
$$

---

2. operación elemental 2: se puede multiplicar una ecuación (fila) por un escalar no nulo
$$
iv) \begin{cases}
x+3y-6=0 \\
-2x+4y+2=0
\end{cases} \equiv \begin{cases}
2x+6y-12=0 \\
-2x+4y+2=0
\end{cases}
$$

---

3. operación elemental 3: Sumar una ecuación (fila) el múltiplo escalar de otra ecuación (fila),donde el escalar es no nulo. Esta es la definición del método de reducción.
$$
v) \begin{cases}
2x-3y=2 \\
-4x+6y=3
\end{cases} \equiv \begin{cases}
2x-3y=2 \\
0=\dfrac{3}{2}
\end{cases}
$$
`gracias a estas operaciones elementales y sistemas equivalentes podemos simplificar el sistema hasta que la solucion sea obvia o facil de lograr.`

---

*Ejercicio 4:*
**Resuelva los siguientes sistemas de ecuaciones y determine el conjunto solución para cada uno. Incluya todos los pasos del procedimiento.**
$$
i)\begin{cases}
   x + y + z - t = 1 \\
   2x - y + z = 2 \\
   x - y + z + t = 1
\end{cases}
\equiv
\begin{cases}
x+y+z-t=1 \\
-3y-z+t=2 \\
-2y+2t=0
\end{cases}
\equiv
\begin{cases}
x+y+z-t=1 \\
-3y-z+t=2 \\
6y-6t=0
\end{cases}
\equiv
\begin{cases}
x+y+z-t=1 \\
-3y-z+t=2 \\
z+2t=0
\end{cases}
$$
`observación:`
	redujimos el sistema usando operaciones elementales, si observamos el resultado tenemos que la primera ecuación tiene 4 incógnitas (x, y, z, t), la segunda ecuación tiene 3 incógnitas por que redujimos "x" y la 3ra ecuación tiene 2 incógnitas por que redujimos "x" e "y", entonces se puede observar como si fueran escaleras por lo que definimos al sistema final como: "sistema de ecuaciones escalonado".

`observación:`
	 un sistema de ecuaciones se puede clasificar de 2 formas: es que sea consistente o inconsistente, si alguna de las ecuaciones es una inconsistencia, es decir, si pasa algo como $2=0$ entonces el sistema en gral no tiene solución, si ninguna presenta una inconsistencia entonces el sistema tiene una o infinita soluciones .

`Observación:`
	para saber si un sistema consistente tiene solución única o infinitas podemos analizar sus incógnitas y ecuaciones.

`teorema:`
	dado un sistema escalonado y sean  $r \land n ~~ \in~~ \mathbb{R}$ $r=\text{cantidad de incognitas} \land n=\text{cantidad de ecuaciones}$.
	si $r=n$ existe una única solución.
	si $n<r$ existen infinitas soluciones.

$\therefore \text{el sistema del inciso i) tiene inifinitas soluciones, pues el sistema escalonado tiene 4 incognitas y 3 ecuaciones.}$

`definición:`
	un sistema de ecuación lineal se puede escribir como una matriz de números reales, donde los números de esta matriz van a ser los coeficientes  de las ecuaciones del sistema, es decir si la ecuación es: $3x+5y$ en una fila de la matriz va a estar: (3  5), esta matriz se denomina: Matriz asociada al sistema.

Ejemplo:
$$
\begin{cases}
4x+5y=0 \\
-2x-y=3
\end{cases} \equiv 

\begin{pmatrix}
4 & 5 \\
-2 & -1
\end{pmatrix}
$$
`definición:`
	se pueden agregar los resultados de la ecuaciones también, esta matriz se denomina matriz ampliada del sistema:
$$
\begin{cases}
4x+5y=0 \\
-2x-y=3
\end{cases}
\equiv
\left(
\begin{array}{cc|c}
4&5&0 \\
-2&-1&3
\end{array}
\right)
$$
`observación:`
	todas las operaciones elementales entre ecuaciones se pueden aplicar a las matrices en sus filas.

**algoritmo de gauss y gauss-jordan**
	Este es un algoritmo que tiene una serie de pasos que garantiza el escalonamiento de una matriz, si lo usamos en una matriz ampliada asociada al sistema, terminamos escalonando el sistema.
	Consiste en elegir un numero pivot, luego multiplicar en diagonal y restar el producto de la diagonal inversa con esto se logra un escalonamiento ya que en el fondo usa operaciones elementales pero en un solo movimiento.
![[Pasted image 20260807192343.png]]

---

$$
\begin{matrix}
ii) \begin{cases}
2x − 5y + 3z = 4 \\
x − 2y + z = 3 \\
5x + y + 7z = 11
\end{cases}
~\sim~
\left(
\begin{array}{ccc|c}
2&-5&3&4 \\
1&-2&1&3 \\
5&1&7&11
\end{array}
\right)
\sim
\left(
\begin{array}{ccc|c}
2&-5&3&4 \\
0&-1&-1&2 \\
0&27&-1&2
\end{array}
\right)
\sim
\left(
\begin{array}{ccc|c}
2&-5&3&4 \\
0&-1&-1&2 \\
0&0&1&-2
\end{array}
\right) \\ \\

\left(
\begin{array}{ccc|c}
2&-5&3&4 \\
0&-1&-1&2 \\
0&0&1&-2
\end{array}
\right) 
\sim 
\left(
\begin{array}{ccc|c}
2&-5&3&4 \\
0&-1&0&0 \\
0&0&1&-2
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
2&0&3&4 \\
0&-1&0&0 \\
0&0&1&-2
\end{array}
\right) \sim \begin{cases}
2x+3z=4 \\
y=0 \\
z=-2
\end{cases} \Rightarrow cs\{(5,0,-2)\}
\end{matrix}
$$

---

$$
\begin{matrix}
iii) \begin{cases}
x+2y=1 \\
2x+y+3z=2 \\
3x+y+5z=3
\end{cases}~~ \sim ~~ \left( 
 \begin{array}{ccc|c}
 1&2&0&1 \\
 2&1&3&2 \\
 3&1&5&3
\end{array}
\right) \sim \left( 
 \begin{array}{ccc|c}
 1&2&0&1 \\
 0&-3&3&0 \\
 0&-5&5&0
\end{array}
\right) \sim \left( 
 \begin{array}{ccc|c}
 1&2&0&1 \\
 0&-3&3&0 \\
 0&0&0&0
\end{array}
\right) \\ \\
\left( 
 \begin{array}{ccc|c} 
 1&2&0&1 \\
 0&-3&3&0 \\
 0&0&0&0
\end{array}
\right) \sim \begin{cases}
x+2y=1 \\
-3y+3z=0
\end{cases} \\ \\
\text{como hay mas variables que ecuaciones} \\
\text{por teorema las soluciones son infinitas } \\
\therefore cs=\{\infty\}
\end{matrix}
$$

---

$$
\begin{matrix}
iv)\begin{cases}
3x+6y-5z=0 \\
x+y+2z=9 \\
2x+4y-3z=1
\end{cases} ~~ \sim ~~ \left(  
 \begin{array}{ccc|c}
 3&6&-5&0 \\
 1&1&2&9 \\
 2&4&-3&1
\end{array}
\right) \sim \left(  
 \begin{array}{ccc|c}
 3&6&-5&0 \\
 0&-3&11&27 \\
 0&0&1&3
\end{array} 
\right) \sim \begin{cases}
3x+6y-5z=0 \\
-3y+11z=27 \\
z=3
\end{cases} \\ \\
z=3 \Rightarrow y=2 \Rightarrow x=1  \\
\therefore cs=\{(1,2,3)\}
\end{matrix}
$$

---

$$
\begin{matrix}
v) \begin{cases}
x+2y+z=0 \\
y+z=-1 \\
x+2y-z=2
\end{cases}~~ \sim \left(  
 \begin{array}{ccc|c} 
 1&2&1&0 \\
 0&1&1&-1 \\
 1&2&-1&2
\end{array}
\right) \sim \left(  
 \begin{array}{ccc|c} 
 1&2&1&0 \\
 0&1&1&-1 \\
 0&0&0&2
\end{array}
\right) \sim \begin{cases}
x+2y+z=0 \\
y+z=-1 \\
0=2 \Rightarrow ABSURDO!!!
\end{cases} \\ \\
\therefore cs=\emptyset
\end{matrix}
$$

---

$$
\begin{matrix}
vi) \begin{cases}
x+2y+3z=-1 \\
2x+3y+4z=0 \\
3x+4y+6z=1
\end{cases} \sim \left(
\begin{array}{ccc|c} 
1&2&3&-1 \\
2&3&4&0 \\
3&4&6&1
\end{array}
\right) \sim \left(
\begin{array}{ccc|c} 
1&2&3&-1 \\
0&-1&-2&2 \\
0&-2&-3&4
\end{array}
\right) \sim \left(
\begin{array}{ccc|c} 
1&2&3&-1 \\
0&-1&-2&2 \\
0&0&-1&0
\end{array}
\right) \\ \\
\sim \left(
\begin{array}{ccc|c} 
1&2&3&-1 \\
0&-1&0&2 \\
0&0&-1&0
\end{array}
\right) \sim \left(
\begin{array}{ccc|c} 
1&2&0&-1 \\
0&-1&0&2 \\
0&0&-1&0
\end{array}
\right) \sim \left(
\begin{array}{ccc|c} 
1&0&0&3 \\
0&-1&0&2 \\
0&0&-1&0
\end{array}
\right) \sim \begin{cases}
x=3 \\
y=-2 \\
z=0
\end{cases} \\ \\
\therefore cs=\{(3,-2,0)\}
\end{matrix}
$$

---

$$
\begin{matrix}
vii) \begin{cases}
x+2y+2z+t=-1 \\
-2y+z-2t=1 \\
-z-2t=1 \\
2t=2
\end{cases} \sim \left(
\begin{array}{cccc|c}
1&2&2&1&-1 \\
0&-2&1&-2&1 \\
0&0&-1&-2&1 \\
0&0&0&2&2
\end{array}
\right) \sim \left(
\begin{array}{cccc|c}
1&2&2&1&-1 \\
0&-2&1&-2&1 \\
0&0&-1&0&3 \\
0&0&0&2&2
\end{array}
\right) \\ \\
\sim \left(
\begin{array}{cccc|c}
1&2&2&1&-1 \\
0&-1&0&0&3 \\
0&0&-1&0&3 \\
0&0&0&1&1
\end{array}
\right) \sim \left(
\begin{array}{cccc|c}
1&0&0&0&10 \\
0&-1&0&0&3 \\
0&0&-1&0&3 \\
0&0&0&1&1
\end{array}
\right) \sim \begin{cases}
x=10 \\
y=-3 \\
z=-3 \\
t=1
\end{cases} \\ \\
\therefore cs = \{(10,-3,-3,1)\}
\end{matrix}
$$

---

$$
\begin{matrix}
viii) \begin{cases}
x+2y-z=1 \\
-3x+y-2z=2 \\
-x+5y-4z=-2
\end{cases} \sim \left(
\begin{array}{ccc|c}
1&2&-1&1 \\
-3&1&-2&2\\
-1&5&-4&-2
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&2&-1&1 \\
0&7&-5&5\\
0&7&-5&-1
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&2&-1&1 \\
0&7&-5&5\\
0&0&0&-6
\end{array}
\right) \\ \\
\sim \begin{cases}
x+2y-z=1 \\
7y-5z=5 \\
0=-6 \Rightarrow ABSURDO!!!
\end{cases} \\ \\
\therefore cs = \emptyset
\end{matrix}
$$

---

$$
\begin{matrix}
ix) \begin{cases}
x+2y+2z+t=-1 \\
2x-2y+2z-2t=1 \\
2x+y-2z=1
\end{cases} \sim \left(  
\begin{array}{cccc|c} 
1&2&2&1&-1 \\
2&-2&2&-2&1 \\
2&1&-2&0&1
\end{array}
\right) \sim \left(  
\begin{array}{cccc|c} 
1&2&2&1&-1 \\
0&-6&-2&4&3 \\
0&-1&-6&-2&3
\end{array}
\right) \\ \\
\sim \left(  
\begin{array}{cccc|c} 
1&2&2&1&-1 \\
0&-6&-2&4&3 \\
0&0&34&8&-15
\end{array}
\right) \sim \begin{cases}
x+2y+2z+t=-1 \\
-6y-2z+4t=3 \\
34z+8t=-15 
\end{cases} \\ \\
n>r \Rightarrow cs=\infty
\end{matrix}
$$

---

`definición:`
	un sistema de ecuaciones es homogéneo si todas los resultados son 0, en caso contrario son no homogéneos. 

`observación:`
	si al escalonar un sistema homogéneo no se anula ninguna fila-ecuación entonces el sistema tiene una única solución y de echo es trivial pues se sabe que es 0, en caso de que se anule alguna fila-ecuación entonces el sistema tiene infinitas soluciones.

*resuelva los siguientes sistemas homogéneos:*
$$
\begin{matrix}
i) \begin{cases}
 x+3y+2z=0 \\
 2x-3y+z=0 \\
 3x-2y+z=0
\end{cases} \sim \begin{pmatrix}
1&3&2 \\
2&-3&1 \\
3&-2&1
\end{pmatrix} \sim \begin{pmatrix}
1&3&2 \\
0&-9&-3 \\
0&-11&-5
\end{pmatrix} \sim \begin{pmatrix}
1&3&2 \\
0&-9&-3 \\
0&0&12
\end{pmatrix} \\ \\
\therefore cs=\{(0,0,0)\} 
\end{matrix}
$$

---

$$
\begin{matrix}
ii) \begin{cases}
x-y+z=0 \\
2x-y+z=0 \\
x-2y+z=0
\end{cases} \sim \begin{pmatrix}
1&-1&1 \\
2&-1&1 \\
1&-2&1
\end{pmatrix} \sim \begin{pmatrix}
1&-1&1 \\
0&1&-1 \\
0&-1&0
\end{pmatrix} \sim \begin{pmatrix}
1&-1&1 \\
0&1&-1 \\
0&0&-1
\end{pmatrix} \\ \\
\therefore cs= \{(0,0,0)\}
\end{matrix}
$$

---

$$
\begin{matrix}
iii) \begin{cases}
x-y+z=0 \\
2x-3y+z=0 \\
2x-2y+2z=0
\end{cases} \sim \begin{pmatrix}
1&-1&1 \\
2&-3&1 \\
2&-2&2
\end{pmatrix} \sim \begin{pmatrix}
1&-1&1 \\
0&1&-1 \\
0&0&0
\end{pmatrix} \\ \\
\therefore cs = \infty
\end{matrix}
$$

---

*Ejercicio 5: Para cada uno de los siguientes sistemas de ecuaciones:*
**a) Determine los valores de los parámetros para que el sistema: 
	i) Tenga solución única     ii) Tenga infinitas soluciones     iii) No tenga solución 
b) Justifique algebraicamente cada caso analizado.**
$$
\begin{matrix}
i) \begin{cases}
x+y+z=-1 \\
2x-3y+z=4 \\
3x-ky+kz=5
\end{cases} \sim \left(
\begin{array}{ccc|c}
1&1&1&-1 \\
2&-3&1&4 \\
3&-k&k&5
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&1&1&-1 \\
0&-5&-1&6 \\
0&-k-3&k-3&8
\end{array}
\right)  \\ \\
\sim \left(
\begin{array}{ccc|c}
1&1&1&-1 \\
0&-5&-1&6 \\
0&0&12-6k&22-6k
\end{array}
\right) \sim \begin{cases}
 x+y+z=-1 \\
 -5y-z=6 \\
 z(-6k+12)=22-6k
\end{cases} \\ \\
1. ~~~ -6k+12 \neq 0 \\
-6k \neq -12  \\
k \neq 2  \\
\therefore \text{cuando $k \neq 2$ el sistema tiene solución única.} \\
2. ~~~ -6k+12=0 ~~\land ~~ 22-6k=0 \\
-6k=-22 \\
k=\dfrac{11}{3} \\
\therefore \text{no existen valores de k que sastifagan ambas ecuaciones.} \\
3. ~~~ -6k+12 = 0 ~~\land ~~ 22-6k \neq 0 \\
\text{ya lo habiamos analizado pues 2 hacec 0 la primera ecuación} \\
\text{y solo $\dfrac{11}{3}$ hace 0 a la segunda ecuación} \\
\therefore k=2
\end{matrix}
$$

---

$$
\begin{matrix}
ii) \begin{cases}
mx+y+z=1 \\
x+my+z=1 \\
x+y+mz=1
\end{cases} \sim \left(
\begin{array}{ccc|c}
m&1&1&1 \\
1&m&1&1 \\
1&1&m&1
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
m&1&1&1 \\
0&m^2-1&m-1&m-1 \\
0&m-1&m^2-1&m-1
\end{array}
\right) \\ \\
\sim \dfrac{1}{m-1}F_{2},F_{3} \left(
\begin{array}{ccc|c}
m&1&1&1 \\
0&m-1&1&1 \\
0&1&m-1&1
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
m&1&1&1 \\
0&m-1&1&1 \\
0&0&(m-1)^2&m-2
\end{array}
\right) \\ \\
\sim \begin{cases}
mx+y+z=1 \\
(m-1)y+z=1 \\
(m-1)^2z=m-2
\end{cases} \\ \\
|1) ~~~ (m-1)^2 \neq 0 \Rightarrow m\neq 1 \\
|2) ~~~ m=1 ~~\land~~ m-2=0 \Rightarrow m = 2 \\
\therefore \nexists m \in \mathbb{R} | m=1 \land m=2 \\
|3) ~~~ m=1
\end{matrix}
$$

---

$$
\begin{matrix}
iii)\begin{cases}
x+y+z=a \\
x+y+za=1 \\
x+y+z=a^2
\end{cases} \sim \left(
\begin{array}{ccc|c}
1&1&1&a \\
1&1&a&1 \\
1&1&1&a^2
\end{array}
  \right) \sim \left(
\begin{array}{ccc|c}
1&1&1&a \\
0&0&a-1&1-a \\
0&0&0&a^2-a
\end{array}
  \right) \sim \begin{cases}
  x+y+z=a \\
  (a-1)z=1-a \\
  0=a^2-a
  \end{cases} \\ \\
\text{de la ultima ecuación tenemos que} \\
0=a(a-1) \\
a=0 ~~\lor~~ a=1 \\
\text{si a es 1 se anulan 2 ecuaciones dejando infinitas soluciones si a es 1 o 0} \\
\text{si a es distinto a estos numeros el sistema no tiene solución por lo que no} \\
\text{exite el caso de que pueda haber una única solución}
\end{matrix}
$$

---

$$
\begin{matrix}
iv) \begin{cases}
x-z=0 \\
2x-3y+z=0 \\
x+2ny+z=0
\end{cases} \sim \left(
\begin{array}{ccc|c}
1&0&-1&0 \\
2&-3&1&0 \\
1&2n&1&0
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&0&-1&0 \\
0&-3&3&0 \\
0&2n&2&0
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&0&-1&0 \\
0&-3&3&0 \\
0&0&-6(1+n)&0
\end{array}
\right) \\ \\
-6(1+n)=0 \\
-6n=6 \\
n=-1 \\
\therefore n=-1 \Rightarrow cs= \infty ~~ \land ~~ n\neq 1 \Rightarrow cs=\{(0,0,0)\}
\end{matrix}
$$

---

$$
\begin{matrix}
v) \begin{cases}
x+y-z=0 \\
2x+3y-z=0 \\
x+2ny+2z=0
\end{cases} \sim \begin{pmatrix}
1&1&-1 \\
2&3&-1 \\
1&2n&2
\end{pmatrix} \sim \begin{pmatrix}
1&1&-1 \\
0&1&1 \\
0&2n-1&3
\end{pmatrix} \sim \begin{pmatrix}
1&1&-1 \\
0&1&1 \\
0&0&4-2n
\end{pmatrix} \\ \\
4-2n=0 \\
-2n=-4 \\
n=2 \\
\therefore si~~n=2 \Rightarrow cs=\infty ~~\land ~~ si~~n\neq 2 \Rightarrow cs=\{(0,0,0)\}
\end{matrix}
$$

---

$$
\begin{matrix}
vi) \begin{cases}
3x -2y+ kz = 0 \\
2x + ky-z = 0 \\
-x+y + z =0
\end{cases} \sim \begin{pmatrix}
3&-2&k \\
2&k&-1 \\
-1&1&1
\end{pmatrix} \sim \begin{pmatrix}
3&-2&k \\
0&3k+4&-3-2k \\
0&1&3+k
\end{pmatrix} \sim \begin{pmatrix}
3&-2&k \\
0&3k+4&-3-2k  \\
0&0&k^2+5k+5
\end{pmatrix} \\ \\
k^2+5k+5=0 \\
-5\pm \dfrac{\sqrt{ 25-20 }}{2} \\
k_{1}=\dfrac{-5+\sqrt{ 5 }}{2} ~~ \land ~~ k_{1}=\dfrac{-5-\sqrt{ 5 }}{2} \\
\therefore si ~~ k\neq k_{1} ~~ \land ~~ k_{2} \Rightarrow cs=\{(0,0,0)\} \text{de caso contrario: } cs=\infty
\end{matrix}
$$
