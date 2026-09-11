# U.N.Sa. - Facultad de Ciencias Exactas
**Asignatura:** Álgebra Lineal y Geometría Analítica  
**Carreras:** PM, LAS, LF, LER, TEU, TUP, TUES  
**Año:** 2º Cuatrimestre 2026  

---

# Trabajo Práctico Nº 4
## Base. Dimensión. Coordenadas de un vector. Espacio fila y espacio columna. Rango. Teorema de Rouché-Frobenius

**Duración:** 3 clases.  

### Objetivos
Que el estudiante sea capaz de:
- Incorporar y comprender el concepto de base de un espacio vectorial y el de coordenadas de un vector.
- Incorporar los conceptos de espacio fila, espacio columna y rango de una matriz.
- Utilizar el teorema de Rouché-Frobenius para decidir si un sistema de ecuaciones lineales tiene o no solución.
- Ejercitar su pensamiento lógico-deductivo en la justificación de lo que realiza y para demostrar distintas propiedades.

---

### Ejercicio 1
Dado un espacio vectorial $V$:
1. Defina base y dimensión de $V$.
2. Escriba la base canónica de $\mathbb{R}^{2}$ y de $\mathbb{R}^{3}$.
3. Muestre un ejemplo de una base de $\mathbb{R}^{2}$ que no sea la base canónica.

### solución:

*El concepto de base de un espacio vectorial es uno de los conceptos centrales de la teoría de espacios vectoriales.*

**Definición:**
	Sea $\mathbb{S}$ un subconjunto de un espacio vectorial  $\mathbb{V}$ diremos que que $\mathbb{S}$ es una base de $\mathbb{S}$ si y solo si:
	$\rightarrow \mathbb{S}$ es linealmente independiente.
	$\rightarrow \mathbb{S}$ es un conjunto generador de $\mathbb{V}$.
	La dimensión de $\mathbb{V}$ es la cantidad de vectores que tiene una base del mismo espacio vectorial.

**Bases canonicas:**
	se le denomina base canonica al conjunto de vectores cuyos elementos son iguales a  las filas de una matriz identidad lo que hace que la sea un conjunto linealmente independiente y por lo tanto constituye una base de $\mathbb{R}^n$ :
	$$
	v_{1}=(1,0,0,\dots,0), v_{2}=(0,1,0,\dots,0), v_{3}=(0,0,1\dots,0),\dots,v_{n}=(0,0,\dots,1)
	$$
	**Base canonica de $\mathbb{R}^2$:**
		B=$\{(0,1),(1,0)\}$
	**Base canonica de $\mathbb{R}^3$:**
		B= $\{ (1,0,0),(0,1,0),(0,0,1) \}$
**Teorema:**
	Todo conjunto de dos vectores es linealmente independiente si y solo si, los vectores no se pueden escribir como combinacion lineal del otro, o también, ningún vector es producto escalar del otro.

**Teorema:**
	todo conjunto de $n$ vectores es base de $\mathbb{R}^n$ si es linealmente independiente.

**Oras bases de $\mathbb{R}^2$ :**
1. $\{(1,2),(2,1)\}$
2. $\{(2,3),(1,5)\}$
3. $\{(1,1),(0,1)\}$
4. etc.
---

### Ejercicio 2
Decida, justificando su respuesta, si los siguientes conjuntos constituyen o no una base del espacio en el cual están incluidos:

a) $\mathbb{B} = \left\{ \begin{pmatrix} -1 \\ 1 \end{pmatrix} \right\} \subset \mathbb{R}^{2}$

b) $\mathbb{B} = \left\{ \begin{pmatrix} -1 \\ 2 \end{pmatrix}, \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \begin{pmatrix} -2 \\ -1 \end{pmatrix} \right\} \subset \mathbb{R}^{2}$

c) $\mathbb{B} = \left\{ \begin{pmatrix} -1 \\ 2 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} -2 \\ 1 \\ -1 \end{pmatrix} \right\} \subset \mathbb{R}^{3}$

d) $\mathbb{B} = \left\{ \begin{pmatrix} 1 & 1 \\ 0 & 2 \end{pmatrix}, \begin{pmatrix} 1 & 0 \\ -1 & 1 \end{pmatrix} \right\} \subset M_{2\times2}(\mathbb{R})$

### Solución:
$$
\begin{matrix}
\text{los incisos a y b no son una base de }\mathbb{R}^2 \text{ pues todas sus bases tienen que tener solamente 2 elementos.} \\ \\
c)~~~ \text{para decidir si es una base empezamos verificando su independencia lineal} \\ \\
\alpha_{1}\begin{pmatrix}
-1 \\
2 \\
1
\end{pmatrix}+ \alpha_{2} \begin{pmatrix}
0 \\
1 \\
1
\end{pmatrix} + \alpha_{3} \begin{pmatrix}
-2 \\
1 \\
-1
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\ \\
\begin{pmatrix}
-\alpha_{1} \\
2\alpha_{1} \\
\alpha_{1}
\end{pmatrix}+ \begin{pmatrix}
0 \\
\alpha_{2} \\
\alpha_{2}
\end{pmatrix} + \begin{pmatrix}
-2\alpha_{3} \\
\alpha_{3} \\
-\alpha_{3}
\end{pmatrix}= \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\ \\
\begin{pmatrix}
-\alpha_{1}-2\alpha_{3} \\
2\alpha_{1}+\alpha_{2}+3\alpha_{3} \\
\alpha_{1}+\alpha_{2}-\alpha_{3}
\end{pmatrix}= \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \xrightarrow{\text{por igualdad de vectores}} \begin{cases}
-\alpha_{1}-2\alpha_{3}=0 \\
2\alpha_{1}+\alpha_{2}+\alpha_{3}=0 \\
\alpha_{1}+\alpha_{2}-\alpha_{3}=0
\end{cases} \\ \\
\overbrace{ \begin{pmatrix}
-1&0&-2 \\
2&1&1 \\
1&1&-1
\end{pmatrix} }^{\text{matriz asociada al sistema}} \xrightarrow{\text{Gauss}} \begin{pmatrix}
-1&0&-2 \\
0&-1&1 \\
0&-1&3
\end{pmatrix} \sim \begin{pmatrix}
-1&0&2 \\
0&-1&1 \\
0&0&-2
\end{pmatrix} \xrightarrow[\text{ecuaciones asociado}]{\text{sistema de}} \begin{cases}
-\alpha_{1}-2\alpha_{3}=0 \\
-\alpha_{2}+\alpha_{3}=0 \\
-2\alpha_{3}=0
\end{cases} \\ \\
\text{luego, por teorema como el sistema escalonado tiene 3 ecuaciones y 3 incognitas }= 0 \text{ variables libres} \\
\text{significa que el sistema tiene solución única y como es un sistema homogeneo la solucón es la trivial,} \\
\text{es decir: }\alpha_{1}=\alpha_{2}=\alpha_{3}=0 \text{ por lo tanto el conjunto es linealmente independiente} \\ \\
\text{ por teorema todo conjunto de }n \text{ vectores linealmente independiente es base de }\mathbb{R}^n \\
\therefore \text{ en este caso el conjunto } \underbrace{\left\{ \begin{pmatrix} -1 \\ 2 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} -2 \\ 1 \\ -1 \end{pmatrix} \right\}}_{\text{3 vectores}} \text{ y es }LI \Rightarrow \text{ es base de }\mathbb{R}^3 \\ \\ \\
d)~~~\text{consultar si puedo aplicar teorema de 2 vectores.}
\end{matrix}
$$
---

### Ejercicio 3
Determine, justificando su respuesta, una base y la dimensión de los siguientes subespacios:

a) $\mathbb{S}_{1} = \left\{ \begin{pmatrix} x \\ y \\ z \end{pmatrix} \in \mathbb{R}^{3} : x - y + 2z = 0 \right\}$

b) $\mathbb{S}_{2} = \operatorname{gen}\left\{ \begin{pmatrix} -1 \\ 2 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} -2 \\ 1 \\ -1 \end{pmatrix} \right\}$

c) $\mathbb{S}_{3} = \mathbb{S}_{1} \cap \mathbb{S}_{2}$

d) $\mathbb{S}_{4} = \{X \in M_{3\times3}(\mathbb{R}) : X = X^{T}\}$

e) $\mathbb{S}_{5} = \{X \in M_{3\times3}(\mathbb{R}) : X = 2X^{T} \wedge X = -X^{T}\}$

f) $\mathbb{S}_{6} = \left\{ \begin{pmatrix} x \\ y \end{pmatrix} \in \mathbb{R}^{2} : x + y = 0 \wedge 3x + 2y = 0 \right\}$

### Solución:
**a)**
$$
\begin{matrix}
\text{por teorema la dimención de un espacio es la cantidad de variables libres de su ecuación general} \\ \\
y=x+2z \Rightarrow 2VL \therefore dim~ \mathbb{S}_{1}=2 \\ \\
\text{ahora buscamos una base, ya nos dieron las condiciones que cumple cualquier vector del conjunto }\mathbb{S}_{1} \\
\text{sabemos que los vectores tienen la forma: }v=(x,x+2z,z)\text{ es decir cualquier vector que cumpla eso} \\
\text{va a ser generador de } \mathbb{S}\text{ faltaria encontrar un conjunto con dos vectores asi y que sean LI para ser base} \\ \\
\text{si }x=1\text{ y }z=1 \rightarrow y=3 \Rightarrow \vec{v} \in \mathbb{S}:v=(1,3,1) \\
\text{si }x=1 \text{ y }z=0 \rightarrow y= 1 \Rightarrow \vec{u} \in \mathbb{S}: u=(1,1,0) \\ \\
\text{sea }\mathbb{B}= \{ v,u \} \text{ por teorema este conjunto es linealmente independiente pues, es un conjunto} \\
\text{de dos vectores que no son multiplo escalar uno del otro por lo tanto son }LI \text{ entonces es una base de }\mathbb{S}_{1}
\end{matrix}
$$
**b)**
$$
\begin{matrix}
\text{ como ya tenemos el conjunto generador comprobamos si es }LI \\ \\
\alpha_{1} \begin{pmatrix}
-1 \\
2 \\
1
\end{pmatrix} + \alpha_{2} \begin{pmatrix}
0 \\
1 \\
1 
\end{pmatrix} + \alpha_{3}\begin{pmatrix}
-2 \\
1 \\
-1
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\ \\
\begin{pmatrix}
-\alpha_{1} \\
2\alpha_{1} \\
\alpha_{1}
\end{pmatrix} + \begin{pmatrix}
0 \\
\alpha_{2} \\
\alpha_{2}
\end{pmatrix} + \begin{pmatrix}
-2\alpha_{3} \\
\alpha_{3} \\
-\alpha_{3}
\end{pmatrix}=\begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\ \\
\begin{pmatrix}
-\alpha_{1}-2\alpha_{3} \\
2\alpha_{1}+\alpha_{2}+\alpha_{3} \\
\alpha_{1}+\alpha_{2}-\alpha_{3}
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \xrightarrow[{\text{de vectores}}]{\text{por igualdad}} \begin{cases}
-\alpha_{1}-2\alpha_{3}=0 \\
2\alpha_{1}+\alpha_{2}+3\alpha_{3}=0 \\
\alpha_{1}+\alpha_{2}-\alpha_{3}=0
\end{cases} \\ \\
\overbrace{\begin{pmatrix}
-1&0&-2 \\
2&1&1 \\
1&1&-1
\end{pmatrix}}^{\text{matriz asociada al sistema}} \xrightarrow{Gauss} \begin{pmatrix}
-1&0&-2 \\
0&-1&3 \\
0&-1&3
\end{pmatrix} \sim \begin{pmatrix}
-1&0&2 \\
0&-1&3 \\
0&0&0
\end{pmatrix} \xrightarrow[{\text{ecuaciones asociado}}]{\text{sistema de}} \begin{cases}
-\alpha_{1}-2\alpha_{3}=0 \\
-\alpha_{2}+3\alpha_{3}=0 \\
\end{cases} \\ \\
\text{luego el sistema tiene 2 ecuaciones y 3 incognitas}= 1 VL\text{ lo que me indica que tiene infinitas soluciones} \\
\text{y eso significa que el conjunto es linealmente dependiente pero por teorema todo conjunto generador} \\
\text{linealmente dependiente contiene una base, por el escalonamiento de gauss eliminamos la columna} \\
\text{dependiente lo que termina indicandome que los vectores: }\begin{pmatrix}
-1 \\
2 \\
1
\end{pmatrix},\begin{pmatrix}
0 \\
1 \\
1
\end{pmatrix} \text{ son }LI \\ \\
\therefore \text{ el conjunto: } \left\{\begin{pmatrix}
-1 \\
2 \\
1
\end{pmatrix} , \begin{pmatrix}
0 \\
1 \\
1
\end{pmatrix} \right\} \text{ conforman una base de }\mathbb{S_{2}}
\end{matrix}
$$
**c)**
$$
\begin{matrix}
\text{me va a interesar saber cual es la ecuación de formación del conjunto }\mathbb{S}_{2}: \\ \\
\alpha_{1} \begin{pmatrix}
-1 \\
2 \\
1
\end{pmatrix}+\alpha_{2}\begin{pmatrix}
0 \\
1 \\
1
\end{pmatrix} + \alpha_{3} \begin{pmatrix}
-2 \\
1 \\
-1
\end{pmatrix} = \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} \\ \\
\text{usando las propiedades del ejercicio anterior tenemos el siguiente sistema:} \\ \\
\begin{cases}
-\alpha_{1}-2\alpha_{3}=x \\
2\alpha_{1}+\alpha_{2}+\alpha_{3}=y \\
\alpha_{1}+\alpha_{2}-\alpha_{3}=z
\end{cases} \xrightarrow[{\text{asociada al sistema}}]{\text{matiz ampleada}} \left( \begin{array}{ccc|c}
-1&0&-2&x \\
2&1&1&y \\
1&1&-1&z
\end{array} \right) \\ \\
\left( \begin{array}{ccc|c}
-1&0&-2&x \\
0&-1&3&-2x-y \\
0&-1&3&-x-z
\end{array} \right) \sim \left( \begin{array}{ccc|c}
-1&0&-2&x \\
0&-1&3&-2x-y \\
0&0&0&-x-y+z
\end{array} \right) \sim \begin{cases}
-\alpha_{1}-2\alpha_{3}=x \\
-\alpha_{2}+3\alpha_{3}=y \\
0=-x-y+z
\end{cases} \\ \\
\text{para que el sistema sea concistente se debe cumplir que }-x-y+z=0\text{ para que no se anule} \\
\text{esta es mi ecuación de formaciń que me genera al espacio }\mathbb{S}_{2} \text{ luego para la intersección: } \mathbb{S}_{1} \cap \mathbb{S}_{2}: \\ \\
\mathbb{S}_{3}=\left\{ \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} \in \mathbb{R}^3 : x-y+2z=0 ~~\land~~ -x-y+z=0\right\} \\ \\
\text{ahora resolvemos para buscar una base y dimension, para obtener la dimension vemos la} \\
\text{cantidad de variables libres al despejar en la ecuacion general, como son 2 tenemos un sistema:} \\ \\
\begin{cases}
x-y+2z=0 \\
-x-y+z=0
\end{cases} \xrightarrow{F_{2}=F_{1}+F_{2}} \begin{cases}
x-y+2z=0 \\
-2y+3z=0
\end{cases} \\ \\
\text{despejando la variable y obtenemos de la segunda ecuación: } \\ \\
y=\frac{3}{2}z \Rightarrow x=-\frac{1}{2}z \\ \\
SG= \left( -\frac{1}{2}z , \frac{3}{2}z, z \right) \Rightarrow 1VL \Rightarrow dim(\mathbb{S})=1 \\ \\
\text{luego por teorema cualquier conjunto unitario distinto del nulo es }LI: \\ \\
\text{si }z=2 \Rightarrow x=-1 ~~ \land~~y=3 \\
\text{sea }\vec{v}= \begin{pmatrix}
-1 \\
3 \\
2
\end{pmatrix} \in \mathbb{S}_{3} \Rightarrow \{\vec{v}\} \text{ es una base de }\mathbb{S}_{3} \text{ por que es }LI \text{ y es generador.}
\end{matrix}
$$
**d)**
$$
\begin{matrix}
\text{sabemos que una matriz simetrica tiene la forma: }\begin{pmatrix}
x&a&b \\
a&y&c \\
b&c&z
\end{pmatrix} \text{ descomponiendo las variables: } \\ \\
x \begin{pmatrix}
1&0&0 \\
0&0&0 \\
0&0&0
\end{pmatrix}+ y \begin{pmatrix}
0&0&0 \\
0&1&0 \\
0&0&0
\end{pmatrix}+ z \begin{pmatrix}
0&0&0 \\
0&0&0 \\
0&0&1
\end{pmatrix} + a \begin{pmatrix}
0&1&0 \\
1&0&0 \\
0&0&0
\end{pmatrix} + b \begin{pmatrix}
0&0&1 \\
0&0&0 \\
1&0&0
\end{pmatrix} + c \begin{pmatrix}
0&0&0 \\
0&0&1 \\
0&1&0
\end{pmatrix} \\ \\
\text{luego, las matrices que se multiplican a las variables son las que me generan el conjunto }\mathbb{S}_{4}: \\ \\
\mathbb{S}_{4}= gen\left\{ \begin{pmatrix}
1&0&0 \\
0&0&0 \\
0&0&0
\end{pmatrix}, \begin{pmatrix}
0&0&0 \\
0&1&0 \\
0&0&0
\end{pmatrix}, \begin{pmatrix}
0&0&0 \\
0&0&0 \\
0&0&1
\end{pmatrix}, \begin{pmatrix}
0&1&0 \\
1&0&0 \\
0&0&0
\end{pmatrix}, \begin{pmatrix}
0&0&1 \\
0&0&0 \\
1&0&0
\end{pmatrix}, \begin{pmatrix}
0&0&0 \\
0&0&1 \\
0&1&0
\end{pmatrix}  \right\} \\ \\
\text{el conjunto generador es linealmente independiente pues no se pueden expresar a sus vectores} \\
\text{como combinacion lineal del resto de los vectores por lo tanto es }LI\text{ y por consecuencia es una base} \\ \\
dim(\mathbb{S})=6
\end{matrix}
$$
**e)**
$$
\text{consultar como demostrar que es matriz nula}
$$
**f)**
$$
\begin{matrix}
\text{de la solución general obtenemos que los vectores generadores del subespacio son los que cumplen:} \\ \\
\begin{cases}
x+y=0 \\
3x+2y=0
\end{cases} \xrightarrow{F_{2}=-3F_{1}+F_{2}} \begin{cases}
x+y=0 \\
-y=0
\end{cases} \Rightarrow y=0 ~~ \land~~ x=0 \\ \\
\text{luego el unico vector que cumple es el nulo, por lo que cumple la siguientes propiedades:} \\ \\
1)~~~dim(\odot)=0 \\
2)~~~\beta(\odot)= \emptyset
\end{matrix}
$$

---

### Ejercicio 4
1. Determine una base del espacio solución del siguiente sistema homogéneo de 2 ecuaciones lineales con 4 incógnitas:
   $$\begin{cases} x + y - 2z + t = 0 \\ x - y - z + 4t = 0 \end{cases}$$
**Solución:**
$$
\begin{matrix}
\overbrace{\begin{pmatrix}
1&1&-2&1 \\
1&-1&-1&4
\end{pmatrix}}^{\text{matriz asociada al sistema}} \xrightarrow{Gauss} \begin{pmatrix}
1&1&-2&1 \\
0&-2&1&3
\end{pmatrix} \xrightarrow[{\text{ecuaciones asociado}}]{\text{sistema de }} \begin{cases}
x+y-2z+t=0 \\
-2y+z+3t=0
\end{cases} \\ \\
\text{despejando }z: ~\rightarrow z=2y-3t \\
\text{despejando }x: ~ \rightarrow x+y-2(2y-3t)+t=0 \Rightarrow x=3y-7t \\ \\
SG= \{ (3y-7t, y, 2y-3t,t) \} \\ \\
\text{si descomponemos la solución general conseguimos una base del espacio solución:} \\ \\
(3y-7t, y, 2y-3t,t)=y(3,1,2,0)+t(-7,0,-3,1) \\ \\
\text{luego una base del espacio solución: } \left\{ (3,1,2,0),(-7,0,-3,1) \right\} \text{ y la dimencion es }2.
\end{matrix}
$$
2. Extienda la base del espacio solución anterior a una base de $\mathbb{R}^{4}$.

**Solución:**
$$
\begin{matrix}
\text{para extender esta base a una de }\mathbb{R}^4 \text{ lo que haremos es agregar vectores combenientemente para que} \\
\text{siga siendo linealmente independiente, al tener 4 vectores y ser }LI\text{ seguro que es base de }\mathbb{R}^4\text{ para eso} \\
\text{usaremos la base canonica, sabemos que esta base es }LI\text{ como ya tenemos 2 vectores completamos: } \\ \\
B=\left\{ (3,1,2,0),(-7,0,-3,1),(1,0,0,0),(0,1,0,0) \right\} \\ \\
\text{usamos los primeros elementos de la base canonica de }\mathbb{R}^4 \text{ en este caso, luego probamos que es}LI: \\ \\
\alpha_{1}(3,1,2,0)+\alpha_{2}(-7,0,-3,1)+\alpha_{3}(1,0,0,0)+\alpha_{4}(0,1,0,0) = (0,0,0,0)  \\
(3\alpha_{1},\alpha_{1},2\alpha_{1},0)+(-7\alpha_{2},0,-3\alpha_{2},\alpha_{2})+(\alpha_{3},0,0,0)+(0,\alpha_{4},0,0)=(0,0,0,0) \\
(3\alpha_{1}-7\alpha_{2}+\alpha_{3},\alpha_{1}+\alpha_{4},2\alpha_{1}-3\alpha_{2},\alpha_{2})=(0,0,0,0) \\ \\
\begin{cases}
3\alpha_{1}-7\alpha_{2}+\alpha_{3}=0 \\
\alpha_{1}+\alpha_{4}=0 \\
2\alpha_{1}-3\alpha_{2}=0 \\
\alpha_{2}=0
\end{cases} \xrightarrow{\text{matriz asociada}} \begin{pmatrix}
3&-7&1&0 \\
1&0&0&1 \\
2&-3&0&0 \\
0&1&0&0
\end{pmatrix} \xrightarrow{Gauss} \begin{pmatrix}
3&-7&1&0 \\
0&7&-1&3 \\
0&5&-2&0 \\
0&1&0&0
\end{pmatrix} \\ \\
\begin{pmatrix}
3&-7&1&0 \\
0&7&-1&3 \\
0&0&-9&-15 \\
0&0&1&-3
\end{pmatrix} \sim \begin{pmatrix}
3&-7&1&0 \\
0&7&-1&3 \\
0&0&-3&-5 \\
0&0&0&42
\end{pmatrix} \sim \begin{cases}
3\alpha_{1}-7\alpha_{2}+\alpha_{3}=0 \\
7\alpha_{2}-\alpha_{3}+3\alpha_{4}=0 \\
-3\alpha_{3}-5\alpha_{4}=0 \\
42\alpha_{4}=0
\end{cases} \\ \\
\text{nos queda un sistema de 4 ecuaciones con 4 incognitas, es decir, }0VL\text{ lo que indica que} \\
\text{existen escalares cuya solución no es la trivial por ende el conjunto es }LI \text{ en consecuencia} \\
B \text{ es una base de }\mathbb{R}⁴
\end{matrix}
$$
---

### Ejercicio 5
Encuentre, justificando su respuesta, una base de $\mathbb{R}^{4}$ que contenga a los vectores:
$$u = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 1 \end{pmatrix}, \quad v = \begin{pmatrix} 1 \\ 2 \\ -1 \\ 1 \end{pmatrix}$$
¿Es única? Justifique su respuesta.

**Solución:**
$$
\begin{matrix}
\text{al igual que en el inciso anterior armamos una base con los vectores que tenemos y la extendemos} \\
\text{aprovechando a la base canonica, vemos que los vecotores }u,v\text{ son linealmente independientes luego:} \\ \\
B=\left\{ \begin{pmatrix}
1 \\
0 \\
1 \\
1
\end{pmatrix}, \begin{pmatrix}
1 \\
2 \\
-1 \\
1
\end{pmatrix} , \begin{pmatrix}
1 \\
0 \\
0 \\
0
\end{pmatrix}, \begin{pmatrix}
0 \\
1 \\
0 \\
0
\end{pmatrix} \right\}  \\ \\
\text{ahora que tenemos una supuesta base de 4 elementos basta con demostrar que es }LI\text{ para que sea base} \\ \\
\alpha_{1}\begin{pmatrix}
1 \\
0 \\
1 \\
1
\end{pmatrix}+\alpha_{2} \begin{pmatrix}
1 \\
2 \\
-1 \\
1
\end{pmatrix}+\alpha_{3} \begin{pmatrix}
1 \\
0 \\
0 \\
0
\end{pmatrix}+\alpha_{4} \begin{pmatrix}
0 \\
1 \\
0 \\
0
\end{pmatrix}= \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\ \\
\begin{pmatrix}
\alpha_{1} \\
0 \\
\alpha_{1} \\
\alpha_{1}
\end{pmatrix}+ \begin{pmatrix}
\alpha_{2} \\
2\alpha_{2} \\
-\alpha_{2} \\
\alpha_{2}
\end{pmatrix}+\begin{pmatrix}
\alpha_{3} \\
0 \\
0 \\
0
\end{pmatrix}+\begin{pmatrix}
0 \\
\alpha_{4} \\
0 \\
0
\end{pmatrix}= \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\ \\
\begin{pmatrix}
\alpha_{1}+\alpha_{2}+\alpha_{3} \\
2\alpha_{2}+\alpha_{4} \\
\alpha_{1}-\alpha_{2} \\
\alpha_{1}+\alpha_{2}
\end{pmatrix}=\begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \xrightarrow[{\text{de vectores}}]{\text{por igualdad}}\begin{cases}
\alpha_{1}+\alpha_{2}+\alpha_{3}=0 \\
2\alpha_{2}+\alpha_{4}=0 \\
\alpha_{1}-\alpha_{2}=0 \\
\alpha_{1}+\alpha_{2}=0
\end{cases}\\  \\
\overbrace{\begin{pmatrix}
1&1&1&0 \\
0&2&0&1 \\
1&-1&0&0 \\
1&1&0&0
\end{pmatrix}}^{\text{matriz asociada al sistema}} \xrightarrow{Gauss} \begin{pmatrix}
1&1&1&0 \\
0&2&0&1 \\
0&-2&-1&0 \\
0&0&-1&0
\end{pmatrix} \sim \begin{pmatrix}
1&1&1&0 \\
0&2&0&1 \\
0&0&-2&2 \\
0&0&-1&0
\end{pmatrix}\sim \begin{cases}
\alpha_{1}+\alpha_{2}+\alpha_{3}=0 \\
2\alpha_{2}+\alpha_{4}=0 \\
\alpha_{3}-\alpha_{4}=0 \\
-\alpha_{4}=0
\end{cases} \\ \\
\text{luego, vemos que tenemos un sistema con 4 ecuaciones y 4 incognitas lo que me indica que tiene} \\
\text{solución única, es decir, existen los escalares y resultan: }\alpha_{1}=\alpha_{2}=\alpha_{3}=\alpha_{4}=0 \text{ en consecuencia} \\
\text{el conjunto es linealmente dependiente y por lo tanto }B \text{ es una base de }\mathbb{R}⁴, \text{no es la unica.}
\end{matrix}
$$
---

### Ejercicio 6
Determine si existen valores del parámetro $k$ para que los siguientes conjuntos:
$$\mathcal{S}_{1} = \left\{ \begin{pmatrix} k \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 1 \\ k \\ 1 \end{pmatrix}, \begin{pmatrix} 2 \\ k+1 \\ 1 \end{pmatrix} \right\}, \qquad \mathcal{S}_{2} = \left\{ \begin{pmatrix} k \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 1 \\ k \\ 1 \end{pmatrix}, \begin{pmatrix} 2 \\ 1 \\ k-1 \end{pmatrix} \right\}$$

1. Generen un subespacio de dimensión 2.
2. Constituyan una base de $\mathbb{R}^{3}$.

*consultar!!!!!!!!*

---

### Ejercicio 7
Sea $V$ un espacio vectorial de dimensión finita $n$. Demuestre que:
1. Si $\mathbb{B} = \{v_{1}, v_{2}, \dots, v_{m}\}$ y $m < n$, entonces $\mathbb{B}$ no es una base de $V$.
2. Si $\mathbb{S}$ es un subespacio no nulo de $V$, entonces $\mathbb{S}$ tiene una base finita y $\dim(\mathbb{S}) \le n$.
3. Si $\mathbb{B} = \{v_{1}, v_{2}, \dots, v_{n}\}$ es una base de $V$, y $k \ne 0$, entonces $\mathbb{B}' = \{kv_{1}, v_{2}, \dots, v_{n}\}$ también es una base de $V$.
4. Dado un vector $v \in V$ y $\mathbb{B} = \{v_{1}, v_{2}, \dots, v_{n}\}$ una base de $V$, entonces sus coordenadas en dicha base son únicas.

---

### Ejercicio 8
Dado el vector $v = \begin{pmatrix} -1 \\ 4 \end{pmatrix}$ y el conjunto $\mathbb{B} = \left\{ \begin{pmatrix} 3 \\ 2 \end{pmatrix}, \begin{pmatrix} -1 \\ 2 \end{pmatrix} \right\}$ una base de $\mathbb{R}^{2}$:
1. Determine, justificando su respuesta, las coordenadas del vector $v$ en la base $\mathbb{B}$.
2. Interprete geométricamente los resultados anteriores.
3. Si las coordenadas de un vector son $(u)_{\mathbb{B}} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$, ¿cuáles son las coordenadas del vector $u$ en la base canónica de $\mathbb{R}^{2}$? Justifique su respuesta.

**Solución:**
$$
\begin{matrix}
\alpha_{1}\begin{pmatrix} 3 \\ 2 \end{pmatrix}+\alpha_{2} \begin{pmatrix} -1 \\ 2 \end{pmatrix}= \begin{pmatrix}
-1 \\
4
\end{pmatrix} \\ \\
\begin{pmatrix}
3\alpha_{1} \\
2\alpha_{1}
\end{pmatrix}+\begin{pmatrix}
-\alpha_{2} \\
2\alpha_{2}
\end{pmatrix}=\begin{pmatrix}
-1 \\
4
\end{pmatrix} \\ \\
\begin{pmatrix}
3\alpha_{1}-\alpha_{2} \\
2\alpha_{1}+2\alpha_{2}
\end{pmatrix}=\begin{pmatrix}
-1 \\
4
\end{pmatrix} \\ \\
\begin{cases}
3\alpha_{1}-\alpha_{2}=-1 \\
2\alpha_{1}+2\alpha_{2}=4
\end{cases} \xrightarrow[{\text{asociada al sistema}}]{\text{matriz ampliada}} \left ( \begin{array}{cc|c} 
3&-1&-1 \\
2&2&4
\end{array} \right) \xrightarrow{Gauss} \left ( \begin{array}{cc|c} 
3&-1&-1 \\
0&2&7
\end{array} \right) \xrightarrow[{\text{de vectores}}]{\text{por igualdad}} \begin{cases}
3\alpha_{1}-\alpha_{2}=-1 \\
4\alpha_{2}=7
\end{cases} \\ \\
\alpha_{2}=\frac{7}{2} \Rightarrow \alpha_{1}=\frac{5}{6} \\ \\
(v)_{\mathbb{B}}=\begin{pmatrix}
\frac{1}{4} \\
\frac{7}{4}
\end{pmatrix}
\end{matrix}
$$
![[Pasted image 20260909202105.png]]

**3)**
$$
\begin{matrix}
\text{por definicion de base: } \\ \\
2\begin{pmatrix}
3 \\
2
\end{pmatrix}+1\begin{pmatrix}
-1 \\
2
\end{pmatrix}=u \Rightarrow u= \begin{pmatrix}
5 \\
6
\end{pmatrix} \text{ luego en la base canonica por propiedad:} (u)_{c}=\begin{pmatrix}
5 \\
6
\end{pmatrix}
\end{matrix}
$$
---

### Ejercicio 9
1. Dada una matriz $A \in M_{m\times n}(\mathbb{R})$, defina $R_{A}$, $C_{A}$, $N_{A}$.
2. Para cada una de las siguientes matrices:
   $$A = \begin{pmatrix} 1 & 1 & -1 & 0 \\ 2 & 2 & -2 & 0 \\ 0 & 1 & 2 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 2 & -2 & 0 \\ -1 & -1 & 1 & 0 \\ 1 & 0 & 1 & 1 \\ 1 & 0 & 1 & 0 \end{pmatrix}$$
   determine:  
   a) $R_{A}$, $R_{B}$, $C_{A}$, $C_{B}$, $N_{A}$ y $N_{B}$.  
   b) Una base y la dimensión de los espacios anteriores.  
   c) Exprese a las filas (columnas) linealmente dependientes como combinación lineal de las filas (columnas) que constituyen la respectiva base hallada en el inciso anterior, para los espacios filas (columnas).  
   d) Decida, justificando su respuesta, la verdad o falsedad de las siguientes afirmaciones:
      - $R_{A} = R_{B}$
      - $C_{A} = C_{B}$
      - $\rho(A) = \rho(B)$
   e) Determine si existe el valor del parámetro $k$ para que el vector $\begin{pmatrix} 1 \\ k \\ 1 \\ k+1 \end{pmatrix}$ pertenezca simultáneamente a los espacios fila de $A$ y columna de $B$.

---

### Ejercicio 10
1. Enuncie el teorema de Rouché-Frobenius y muestre a través de 3 ejemplos cómo aplicarlo para determinar si un sistema de ecuaciones lineales tiene solución única, ninguna solución o infinitas soluciones.
2. Dados los siguientes sistemas de ecuaciones lineales, aplique el teorema de Rouché-Frobenius para determinar si tienen o no solución. En caso de tener solución, decida (justificando su respuesta) si tiene solución única o infinitas soluciones:

   a) $\begin{cases} x + y + z = 2 \\ x + 2y - z = 0 \\ x + 3z = 4 \end{cases}$

   b) $\begin{cases} x + y - z = 2 \\ 2x + 2y - 2z = 0 \\ y + 2z = 3 \end{cases}$

   c) $\begin{cases} x + y + z + t = 2 \\ x + 2y - z = 0 \\ 2x + 3y + t = 4 \end{cases}$

---

### Ejercicio 11
Aplique el teorema de Rouché-Frobenius para determinar si existen valores del parámetro $k$ de manera que el sistema:
$$\begin{cases} x - y + 2z = k \\ 3x - 2y + kz = 1 \\ 2x - y + z = 1 + k \end{cases}$$

a) Tenga solución única.  
b) Tenga infinitas soluciones.  
c) No tenga solución.  

---

### Ejercicio 12
Decida, justificando su respuesta, la verdad o falsedad de las siguientes proposiciones:
1. Si un conjunto genera a $\mathbb{R}^{3}$, entonces dicho conjunto contiene exactamente 3 vectores de $\mathbb{R}^{3}$.
2. Si $\mathbb{B} = \{v_{1}, v_{2}, v_{3}\}$ es una base para un espacio vectorial $V$, entonces $\mathbb{B}' = \{w_{1}, w_{2}, w_{3}\}$ también es una base de $V$, con:
   $$w_{1} = v_{1} + v_{2} + v_{3}, \quad w_{2} = v_{2} + v_{3}, \quad w_{3} = v_{3}$$
3. Si $A \in M_{3\times5}(\mathbb{R})$, entonces $\rho(A) = 3$.
4. Si $A \in M_{n\times n}(\mathbb{R})$, entonces $R_{A} = C_{A}$.
5. Si $A \in M_{m\times n}(\mathbb{R})$ y $\rho(A) = n$, entonces el sistema $AX = B$ tiene solución única.

---

### Bibliografía
- [ ] Grossman, S. (2019). *Álgebra lineal con Connect*. McGraw-Hill Latinoamérica.
- [[Anton, H. (2004). Introducción al álgebra lineal (3ª ed.). Limusa]]