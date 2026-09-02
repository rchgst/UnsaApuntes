# Trabajo Práctico Nº 1
## Ecuaciones lineales. Ecuaciones lineales con parámetros. Sistemas de ecuaciones lineales. Método de Gauss. Sistemas con parámetros. Aplicaciones.

> [!info] **U.N.Sa. - Facultad de Ciencias Exactas**
> **Asignatura:** Álgebra Lineal y Geometría Analítica  
> **Carreras:** PM, LAS, LF, LER, TEU, TUP, TUES  
> **Año / Cuatrimestre:** 2º Cuatrimestre 2026  
> **Duración:** 2 clases  

---

### Objetivos
Que el estudiante sea capaz de:
- Resolver ecuaciones lineales y analizar las distintas posibilidades de solución en ecuaciones con parámetros.
- Emplear el algoritmo de Gauss para resolver sistemas de ecuaciones lineales.
- Analizar las distintas posibilidades de solución en sistemas con parámetros y expresarlas paramétricamente.
- Modelizar situaciones problemáticas de otras áreas mediante sistemas lineales.

---

### Ejercicio 1.

**a)** Defina qué es una ecuación lineal y explique qué se entiende por solución de una ecuación.

`una ecuación lineal es aquella ecuación que tiene la forma: ax=b donde los parametros "a" y "b" son numeros reales y la incognita "x" esta elevada a la potencia 1.` 

**b)** Identifique cuáles de las siguientes ecuaciones dadas son lineales:
- i) $2x - y = 4z$ 
	- no es una ecuación lineal pues, no respeta la forma: $ax+b$
- ii) $3x - \pi y = \sqrt{2}$
	- es una ecuación lineal
- iii) $xy - z = 3$
	- no es una ecuación lineal
- iv) $\frac{1}{x} + y = 1$
	- no es una ecuación lineal
- v) $y^2 - z = 4$
	- no es una ecuación lineal

**c)** Determine el valor de $c$ para que la ecuación $c(cx+5) = 2(2x+5)$ tenga infinitas soluciones en $\mathbb{R}$. Justifique su respuesta.

`solución:`
$$
\begin{matrix}
c(cx+5)=2(\text{x+5}) \\
c^2x+5c=2x+10 \\
c^2x-2x=10-5c  \\
x(c^2-2)=5(2-c) \\ \\
\text{para que tenga infinitas soluciones se tiene que dar lo siguiente: } 0x=0 \\
\text{entonces tiene que pasar que }c^2-2=0 ~~\land~~ 2-c=0 \\ \\
c^2-2= 0\Rightarrow c^2=2 \Rightarrow c=\pm ~2 \\
2-c=0 \Rightarrow c=2 \\
\therefore c=2 
\end{matrix}
$$

**d)** Proponga tres pares ordenados $(x, y)$ que satisfagan la ecuación $3x - 2y = 12$. Justifique su elección.

`solución:`
$$
\begin{matrix}
\text{para lograr esto lo que hacemos es buscar soluciones particulares} \\
\text{que se consiguen cuando evaluamos una inncognita con algun valor:} \\ \\
\text{si  } x=0 \Rightarrow 3(0)-2y=12 \Rightarrow y=-6 \Rightarrow (0,-6) \text{  es una solución} \\
\text{si  } x=1 \Rightarrow 3(2)-2y=12 \Rightarrow -2y=6 \Rightarrow y=-3\Rightarrow (2,-3) \text{  es solución} \\
\text{si  }x=4 \Rightarrow 3(4)-2y=12 \Rightarrow -2y=0 \Rightarrow y=0 \Rightarrow (4,0) \text{ es solución}
\end{matrix}
$$


**e)** Calcule el valor de $m$ para que el punto $(-2, 3)$ sea solución de la ecuación $2x + y - m = 0$.

`solución:`
$$
\begin{matrix}
\text{para lograr esto lo unico que se necesita es remplazar el valor de x e y para despejar m:} \\ \\
2(-2)+3-m=0 \\
-4+3-m=0 \\
-1-m=0 \\
m=-1 \\
\therefore 2x+y+1=0 \text{ es la ecuación que tiene de solución al par $(-2,3)$}
\end{matrix}
$$


---

### Ejercicio 2.

**a)** Parametrice el conjunto solución de $3x - 2y = 12$. Verifique que los tres pares ordenados obtenidos en el Ejercicio 1 d) se corresponden con valores particulares del parámetro hallado.

**b)** Parametrice el conjunto solución de $x + y + z + 3 = 0$.

**c)** Explique cuál es la diferencia entre: una solución particular; la solución general y el conjunto solución.

---

### Ejercicio 3.

Las operaciones elementales sobre las ecuaciones de un sistema permiten obtener otros sistemas equivalentes, es decir, con el mismo conjunto solución.

**a)** Considere el sistema:
$$\begin{cases} 2x + 2y = 2 \\ x + 2y = 6 \end{cases}$$
Transfórmelo en un sistema equivalente de resolución inmediata aplicando operaciones elementales. Indique en cada paso la operación realizada y verifique la solución obtenida en el sistema original.

`solución:`
$$
\begin{cases}
2x+2y=2 \\
x+2y=6
\end{cases} \sim \begin{cases}
x+y=1 \\
x+2y=6
\end{cases} \sim \begin{cases}
x+y=1 \\
y=6
\end{cases} \sim \begin{cases}
x=-5 \\
y=6
\end{cases}
$$

**b)** Repita el procedimiento para:
$$\begin{cases} 2x - y + z = 3 \\ x + y + z = 6 \\ x + 2y - z = 2 \end{cases}$$

`solución:`
$$
\begin{matrix}
\begin{cases}
x+y+z=6 \\
x+2y-z=2 \\
2x-y+z=3
\end{cases} \sim \begin{cases}
x+y+z=6 \\
-y+2z=4 \\
2x-y+z=3
\end{cases} \sim \begin{cases}
x+y+z=6 \\
-y+2z=4 \\
3y+z=9
\end{cases} \sim \begin{cases}
x+y+z=6 \\
-y+2z=4 \\
7z=21
\end{cases} \\ \\
z=3 \Rightarrow y=2 \Rightarrow x=1 \\
cs=\{(1,2,3)\}
\end{matrix}
$$
**c)** ¿Qué característica tuvo el sistema final que le permitió resolverlo de inmediato, en ambos casos?

`Lo que permite resolver de manera inmediata el sistema en ambos casos, es el escalonamiento del sistema, una de las variables por lo general la última, tiene asignado un valor automaticamente y con remplazar de abajo hacia arriba el sistema se resuelve.`

---

### Ejercicio 4.

Las operaciones elementales estudiadas en el ejercicio anterior pueden realizarse de manera más organizada utilizando la matriz ampliada del sistema.

Considere el siguiente sistema:
$$\begin{cases} x - 2y + 2z = 2 \\ 2x + y + 2z = 8 \\ -x + 3y - 2z = -1 \end{cases}$$

**a)** Escriba la matriz ampliada asociada al sistema.

**b)** Aplique el algoritmo de Gauss para llevar la matriz a su forma escalonada, indicando en cada paso la operación elemental utilizada.

**c)** Determine el conjunto solución.

`solución:`
$$
\begin{matrix} 
\text{matriz ampliada asociada al sistema: } \\ \\
\left(
\begin{array}{ccc|c}
1&-2&2&2 \\
2&1&2&8 \\
-1&3&-2&-1
\end{array}
\right) \\ \\
\text{escalonamiento por gauss: }  \\ \\
\left(
\begin{array}{ccc|c}
1&-2&2&2 \\
2&1&2&8 \\
-1&3&-2&-1
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&-2&2&2 \\
0&5&-2&4 \\
0&1&0&1
\end{array}
\right) \sim \left(
\begin{array}{ccc|c}
1&-2&2&2 \\
0&5&-2&4 \\
0&0&2&1
\end{array}
\right) \\ \\
\left(
\begin{array}{ccc|c}
1&-2&2&2 \\
0&5&-2&4 \\
0&0&2&1
\end{array}
\right) \sim \begin{cases}
x-2y+2z=2 \\
5y-2z=4 \\
2z=1
\end{cases}  \\ \\
cs=\left\{ \left(3, 1,\frac{1}{2} \right) \right\}
\end{matrix}
$$
---

### Ejercicio 5.

Resuelva cada uno de los siguientes sistemas mediante el algoritmo de eliminación de Gauss. Clasifique el sistema indicando si es consistente o inconsistente; en caso de ser consistente, determine si posee una única solución o infinitas soluciones. Exprese el conjunto solución de forma paramétrica cuando corresponda.

- **i)** 
  $$\begin{cases} x + y = 3 \\ 2x - y = 0 \\ 3x + y = 4 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left( 
\begin{array}{cc|c}
1&1&3 \\
2&-1&0 \\
3&1&4
\end{array}
\right)  \sim \left( 
\begin{array}{cc|c}
1&1&3 \\
0&-3&-6 \\
0&-2&-5
\end{array}
\right) \sim \left( 
\begin{array}{cc|c}
1&1&3 \\
0&-3&-6 \\
0&0&3
\end{array}
\right) \sim \begin{cases}
x+y=3 \\
3y=6 \\
0=3 \Rightarrow ABSURDOOO!!!
\end{cases} \\ \\
\therefore cs = \emptyset
\end{matrix}
$$
- **ii)** 
  $$\begin{cases} x + 2y = 1 \\ 2x + y + 3z = 2 \\ 3x + y + 5z = 3 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left( \begin{array}{ccc|c}
1&2&0&1 \\
2&1&3&2 \\
3&1&5&3
\end{array}\right) \sim \left( \begin{array}{ccc|c}
1&2&0&1 \\
0&-3&3&0 \\
0&-5&5&0
\end{array}\right) \sim \left( \begin{array}{ccc|c}
1&2&0&1 \\
0&-3&3&0 \\
0&0&0&0
\end{array}\right) \sim \begin{cases}
x+2y=1 \\
-3y+3z=0
\end{cases} \\ \\
\text{por teorema como hay más ecuaciones que incognitas, el sistema tiene infinitas soluciones.} \\ \\
\therefore cs = \infty
\end{matrix}
$$
- **iii)** 
  $$\begin{cases} x + 2y - z = 1 \\ -3x + y - 2z = 2 \\ -x + 5y - 4z = -2 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left( \begin{array}{ccc|c}
1&2&-1&1 \\
-3&1&-2&2 \\
-1&5&-4&-2
\end{array}
\right) \sim \left( \begin{array}{ccc|c}
1&2&-1&1 \\
0&7&-5&5 \\
0&7&-5&-1
\end{array}
\right) \sim \left( \begin{array}{ccc|c}
1&2&-1&1 \\
0&7&-5&5 \\
0&0&0&-42
\end{array}
\right) \sim \begin{cases}
x+2y-z=1 \\
7y-5z=5 \\
0=-42 \Rightarrow ABSURDO!!!
\end{cases} \\ \\
\therefore cs= \emptyset
\end{matrix}
$$
- **iv)** 
  $$\begin{cases} 2x - 5y + 3z = 4 \\ x - 2y + z = 3 \\ 5x + y + 7z = 11 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left( \begin{array}{ccc|c}
2&-5&3&4 \\
1&-2&1&3 \\
5&1&7&11
\end{array}
\right) \sim \left( \begin{array}{ccc|c}
2&-5&3&4 \\
0&1&-1&2 \\
0&27&-1&2
\end{array}
\right) \sim \left( \begin{array}{ccc|c}
2&-5&3&4 \\
0&1&-1&2 \\
0&0&1&-2
\end{array}
\right) \sim \begin{cases}
2x-5y+3z=4 \\
y-z=2 \\
z=-2
\end{cases} \\ \\
\therefore cs=\{(5,0,-2)\}
\end{matrix}
$$
- **v)** 
  $$\begin{cases} -x - 2y + 2z - w = -5 \\ x + 2y - z + w = 5 \\ 2x + 4y - 3z + w = 8 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left( \begin{array}{cccc|c}
-1&-2&2&-1&-5 \\
1&2&-1&1&5 \\
2&4&-3&1&8
\end{array}\right) \sim \left( \begin{array}{cccc|c}
-1&-2&2&-1&-5 \\
0&0&-1&0&0 \\
0&0&-1&1&2
\end{array}\right) \sim \begin{cases}
-x-2y+2z-w=-5 \\
z=0 \\
-z+w=2
\end{cases} \\ \\
incognitas-ecuaciones>0\Rightarrow cs=\infty
\end{matrix}
$$
- **vi)** 
  $$\begin{cases} 2x + y - 2z + t = -3 \\ x - y + z + t = 4 \\ -3x - 2y + 2z - 2t = 3 \\ 2x - y + 3z - t = 9 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left(\begin{array}{cccc|c}
2&1&-2&1&-3 \\
1&-1&1&1&4 \\
-3&-2&2&-2&3 \\
2&-1&3&-1&9
\end{array} \right)
\end{matrix}
$$
- **vii)** 
  $$\begin{cases} 2x + y - 3 = z \\ x - 2y + 2z = 4 \\ 3x - 4y + 4z = 10 \end{cases}$$
`solución:`
$$
\begin{matrix}
\left( \begin{array}{ccc|c}
2&1&-1&3 \\
1&-2&2&4 \\
3&-4&4&10
\end{array} \right) \sim \left( \begin{array}{ccc|c}
2&1&-1&3 \\
0&-5&5&5 \\
0&-11&11&11
\end{array} \right) \sim \left( \begin{array}{ccc|c}
2&1&-1&3 \\
0&-1&1&1 \\
0&-1&1&1
\end{array} \right) \sim \left( \begin{array}{ccc|c}
2&1&-1&3 \\
0&-1&1&1 \\
0&0&0&0
\end{array} \right) \\ \\
\sim \begin{cases}
2x+y-z=3 \\
-y+z=1 \\
\end{cases} \Rightarrow cs = \infty
\end{matrix}
$$
- **viii)** 
  $$\begin{cases} 2x + y - z = 0 \\ x - 2y + 2z = 0 \\ 3x - 4y + 4z = 0 \end{cases}$$
`solución:`
$$
\begin{matrix}
\begin{pmatrix}
2&1&-1 \\
1&-2&2 \\
3&-4&4
\end{pmatrix} \sim \begin{pmatrix}
2&1&-1 \\
0&-5&5 \\
0&-11&11
\end{pmatrix} \sim \begin{pmatrix}
2&1&-1 \\
0&-1&1 \\
0&-1&1
\end{pmatrix} \sim \begin{pmatrix}
2&1&-1 \\
0&-1&1 \\
0&0&0
\end{pmatrix} \\ \\
\sim \begin{cases}
2x+y-z=0 \\
-y+z=0 
\end{cases} \Rightarrow cs=  \infty
\end{matrix}
$$
- **ix)** 
  $$\begin{cases} x + z = y \\ 2x - 3y + z = 0 \\ x - 2y + z = 0 \end{cases}$$
`solución:`
$$
\begin{matrix}
\begin{pmatrix}
1&-1&1 \\
2&-3&1 \\
1&-2&1
\end{pmatrix} \sim \begin{pmatrix}
1&-1&1 \\
0&-1&-1 \\
0&-1&0
\end{pmatrix} \sim \begin{pmatrix}
1&-1&1 \\
0&-1&-1 \\
0&0&-1
\end{pmatrix} \sim \begin{cases}
x-y+z=0 \\
-y-z=0 \\
-z=0
\end{cases} \\ \\
cs=\{(0,0,0)\}
\end{matrix}
$$


Para cada uno de los sistemas de dos o tres incógnitas, interprete geométricamente la solución obtenida. Responda:

**a)** ¿Es posible que un sistema homogéneo sea inconsistente? Justifique su respuesta.

**b)** Si un sistema homogéneo tiene menos ecuaciones que incógnitas, ¿puede tener solución única? Justifique su respuesta.

**c)** Escriba tres soluciones particulares distintas del sistema homogéneo que admita infinitas soluciones.

---

### Ejercicio 6.

Aplique el algoritmo de Gauss - Jordan para encontrar la solución de los sistemas con única solución del Ejercicio 5.

---

### Ejercicio 7.

Considere los siguientes sistemas lineales con parámetros:

- **i)** 
  $$\begin{cases} kx + y = m \\ mx + y = k \end{cases}$$

- **ii)** 
  $$\begin{cases} x + ky + z = k \\ 2x + (k+1)y + 2z = 1 \\ x + y + kz = 1 \end{cases}$$

- **iii)** 
  $$\begin{cases} mx + y + z = 1 \\ x + my + z = 1 \\ x + y + mz = 1 \end{cases}$$

**a)** Determine los valores del parámetro para los cuales el sistema posee una única solución, infinitas soluciones o ninguna solución.

**b)** Para los valores del parámetro que dan única solución o infinitas soluciones, determine el conjunto solución correspondiente.

---

### Ejercicio 8.

Resuelva los siguientes problemas mediante el algoritmo de Gauss, definiendo en cada caso las incógnitas necesarias e interpretando el resultado obtenido en el contexto del problema.

**a) (Interpolación polinómica)**  
Se busca un polinomio de segundo grado $p(x) = ax^2 + bx + c$ que pase por los puntos $(-1, 3)$, $(0, 1)$, $(1, 5)$ y $(2, 10)$.  
¿Qué tipo de sistema obtiene al plantear las cuatro ecuaciones correspondientes? ¿Qué significa esto respecto de la posibilidad de encontrar un polinomio de grado 2 que pase exactamente por los cuatro puntos? Si utiliza solo los tres primeros puntos, ¿qué ocurre?

**b) (Tiempos de ejecución de un proceso de IA)**  
Durante la ejecución de un proceso de inferencia, un modelo de inteligencia artificial realiza tres tipos de operaciones básicas: lectura de datos ($L$), procesamiento ($P$) y escritura de resultados ($E$). Al registrar los tiempos de distintas tareas, se observó que la primera realizó una lectura, cuatro procesamientos y una escritura empleando en total 25 segundos; la segunda realizó cuatro lecturas, dos procesamientos y seis escrituras con un tiempo total de 36 segundos; mientras que la tercera realizó una lectura, dos procesamientos y una escritura en 15 segundos. ¿Cuánto tiempo consume cada operación?

**c) (Planificación de un viaje)**  
Tres amigos registraron los gastos de un viaje. El primer día pagaron una carga de combustible, dos peajes y una comida, gastando $\$34000$; el segundo día pagaron dos cargas de combustible, un peaje y tres comidas, gastando $\$56000$. Se supone que el costo de cada tipo de gasto se mantuvo constante. ¿Es posible determinar con estos datos el costo exacto de cada carga de combustible, cada peaje y cada comida? Justifique, y en caso de no ser posible, exprese la relación que deben cumplir esos costos.

**d) (Análisis de redes eléctricas)**  
Las Leyes de Kirchhoff permiten modelizar circuitos eléctricos mediante sistemas de ecuaciones lineales.
- **Ley de los nodos:** la suma de las corrientes que ingresan a un nodo es igual a la suma de las corrientes que egresan.
- **Ley de las mallas:** en toda trayectoria cerrada, la suma de las caídas de tensión es igual al voltaje suministrado.

Considerando el circuito con valores: $V_1 = 7\text{ V}$, $V_2 = 8\text{ V}$, $R_1 = 3\,\Omega$, $R_2 = 2\,\Omega$, $R_3 = 4\,\Omega$:
- Ley de nodos: $I_1 + I_3 = I_2$
- Trayectoria 1: $R_1 I_1 + R_2 I_2 = 3I_1 + 2I_2 = 7$
- Trayectoria 2: $R_2 I_2 + R_3 I_3 = 2I_2 + 4I_3 = 8$

- **i)** Arme el sistema de ecuaciones a partir de las expresiones obtenidas y resuélvalo para hallar las corrientes $I_1$, $I_2$ e $I_3$ del circuito eléctrico.
- **ii)** Plantee y resuelva el sistema asociado al siguiente circuito:
  - $A: 5\text{ V}$, $B: 8\text{ V}$
  - $R_1 = 1\,\Omega$, $R_2 = 2\,\Omega$, $R_3 = 4\,\Omega$
  - ¿Cómo se afecta el resultado cuando $A$ cambia a $2\text{ volts}$ y $B$ a $6\text{ volts}$? Calcule las nuevas corrientes y compare con las obtenidas anteriormente.

> *Nota: Justifique todos sus pasos y verifique que las soluciones obtenidas satisfacen las condiciones originales del problema.*

---

### Ejercicio 9.

Decida, justificando su respuesta, la verdad o falsedad de las siguientes proposiciones:

**a)** Si un sistema de ecuaciones lineales tiene menos ecuaciones que incógnitas, entonces tiene infinitas soluciones.

**b)** Todo sistema de ecuaciones lineales homogéneo con más ecuaciones que incógnitas tiene infinitas soluciones.

**c)** Si en un sistema de ecuaciones lineales una ecuación es múltiplo de otra, entonces el sistema tiene infinitas soluciones.

**d)** Existe un sistema de ecuaciones lineales que tiene exactamente 2 soluciones distintas.

**e)** Todo sistema de ecuaciones lineales con igual número de ecuaciones que de incógnitas tiene solución.

**f)** Si al aplicar el algoritmo de Gauss a un sistema aparece una fila de ceros, entonces el sistema tiene infinitas soluciones.

---

### Bibliografía
- **[1]** Grossman, S. (2012). *Álgebra lineal - Séptima Edición*. McGraw Hill, México.
- **[2]** Anton, H. (2013). *Introducción al álgebra lineal* (5ª ed.). Limusa Wiley, México.