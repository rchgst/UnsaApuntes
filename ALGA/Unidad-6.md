### Vectores, producto interno, producto vectorial, norma, proyecciones.

**Vector desde el punto de vista geométrico:**

en capítulos anteriores definimos a los vectores y el espacio en el que habitan, todos los vectores que vimos tenían dos puntos para crearse, el punto de origen y el punto final, hasta el  momento solo vimos vectores que tenían como origen el punto $(0,0)$ para $\mathbb{R}^2$ y el $(0,0,0)$ para $\mathbb{R}^3$, ahora definiremos vectores que tienen origen en otros lados (en otros puntos) y para entenderlo mejor lo veremos desde el punto de vista geométrico.

bueno entendemos que un vector esta formado por dos o tres puntos si estamos hablando de los espacios vectoriales $\mathbb{R}²,\mathbb{R}³$ que es en ellos donde trabajaremos en esta unidad, pero acá hay un gráfico que lo explica visualmente:

![[vectoresGeometricos.excalidraw]]

podemos ver que el vector que esta cómo "flotando" tiene como origen al punto $P$ ya que es ahí donde nace la flecha y donde esta termina es el punto final $Q$.

por otra parte el segundo vector tiene también un punto final que se llama $R$ pero este tiene de origen el punto que valga la redundancia es el origen $(0,0)$. 

aprovechemos el gráfico para explicar algunos detalles un poco obvios pero que son importantes para definir mejor un vector, vemos que aparte de los puntos que lo forman el vector tiene una flecha que apunta a algún lado y ademas esa flecha tiene una longitud es decir que tiene "magnitud", pues es verdad y de echo son lo que definen a un vector.

**Vector:** es un elemento que tiene un sentido (dirección), magnitud y que comienza y termina en un punto.

**Magnitud de un vector:** la magnitud de un vector es aquella que mide cuanta distancia recorre y se puede calcular a través de su norma, la norma de un vector es una función que le asigna un número o escalar a un vector y se denota y calcula de la siguiente manera:
$$
||\vec{v}||=\sqrt{ v_{1}²+v_{2}²+v_{3}²+\dots+v_{n}^2 }
$$
la suma de los elementos del vector al cuadrado le calculo la raíz cuadrada y me devuelve la magnitud del vector.

**Propiedades de la norma:**

1. $||\vec{v}||\geq 0$
2. $||k \vec{v}||=k||\vec{v}||$
3. $||\vec{v}+\vec{u}||\leq ||\vec{v}||+||\vec{u}||$

**El producto escalar:** también conocido como producto interno es una función que se le aplica a dos vectores y devuelve un numero real, se denota y calcula de la siguiente manera:
$$
\begin{gather}
\text{sea }\vec{v}=(v_{1},v_{2},v_{3},\dots,v_{n}) \text{ y } \vec{u}=(u_{1},u_{2},u_{3},\dots,u_{n}) \\ \\
\vec{v} \cdot \vec{u} = <\vec{v},\vec{u}> = v_{1}\cdot u_{1} + v_{2} \cdot u_{2} + v_{3} \cdot u_{3} + \dots + v_{n} \cdot u_{n}
\end{gather}
$$
a esa definición se la conoce también como producto interno usual, pero yo puedo definir mis propios productos internos, por que todo producto interno es aquel que cumple los siguientes axiomas:

 * $\forall \vec{u},\vec{v} \in \mathbb{V} \land \forall k \in \mathbb{R}:$
 * **Axioma-1:** $<\vec{u},\vec{v}> = <\vec{v},\vec{u}>$
 * **Axioma-2:** $<k \vec{u},\vec{v}> = k<\vec{u},\vec{v}>$ 
 * **Axioma-3:** $<\vec{u},\vec{v}+\vec{w}> = <\vec{u},\vec{v}>+<\vec{u},\vec{w}>$
 * **Axioma-4:** $<\vec{u},\vec{u}> \geq 0$
 * **Axioma-5:** $<\vec{u},\vec{u}> = 0 \Leftrightarrow \vec{u}= \odot$

##### Ejercicio 1. Dados los siguientes vectores:
$\vec{u_{1}}=(-2,3) \quad  \vec{u_{2}}=(3,5) \quad \vec{u_{3}}=(0,-2) \quad  \vec{v_{1}}=(3,2,0) \quad \vec{v_{2}}=(-2,4,2) \quad   \vec{v_{3}}=(2,3,-5)$

**a) representarlos gráficamente según corresponda.**
**b) realizar las siguientes operaciones entre vectores:**
$$
\begin{gather}
i)~2\vec{u}_{2} \quad \quad ii)~-2\vec{u}_{2} \quad \quad iii)~\vec{u_{1}}+\vec{u_{2}} \quad \quad iv)~ \vec{u_{1}}+2u_{2}-u_{3} \\ \\
v)~ \vec{2u_{1}}+\vec{v_{2}} \quad \quad vi)~ \vec{v_{2}}-\vec{v_{3}} \quad \quad vii)~\vec{v_{1}}-3\vec{v_{2}}+\vec{v_{3}}
\end{gather}
$$
##### Solución:
**b)** $$
\begin{gather}
i)~ 2(3,5)=(6,10) \quad \quad ii)~ -2(3,5)=(-6,-10) \quad \quad iii)~(-2,3)+(3,5)=(1,8) \\ \\
iv)~ (-2,3)+(6,10)-(0,-2)=(4,11) \quad \quad v)~2(3,2,0)+(-2,4,2)=(4,8,2) \\ \\
vi)~ (-2,4,2)-(2,3,-5)=(-4,1,7) \quad \quad vii)~(3,2,0)-3(-2,4,2)+(2,3,-5)=(11,13,-11)
\end{gather}
$$
### Ejercicio 2.
**a) utilice la definición de producto interno para decidir si las siguientes funciones definen un producto interno en $\mathbb{R}²$, siendo $\vec{u}=(u_{1},u_{2})~~~ y ~~~\vec{v}=(v_{1},v_{2})$.**
* $i)~~~ <\vec{u},\vec{v}> \Rightarrow \vec{u_{1}}\vec{v_{2}}+\vec{u_{2}}\vec{v}_{1}$
* $ii)~~~<\vec{u},\vec{v}> = \vec{u_{1}}\vec{v_{1}}+\vec{u_{2}}\vec{v_{1}}+\vec{u_{1}}\vec{v_{2}}+2\vec{u_{2}}\vec{v_{2}}$

##### Solución:
i)$$
\begin{gather}
\\ a_{1}: <(u_{1},u_{2}),(v_{1},v_{2})> \quad = \quad <(v_{1},v_{2}),(u_{1},u_{2})> \\ \\
<\vec{u},\vec{v}>\quad = \quad \underbrace{u_{1}v_{2}+u_{2}v_{1}}_{\begin{matrix}
\text{def }<\vec{u},\vec{v}>
\end{matrix}} =  \underbrace{v_{2}u_{1}+v_{1}u_{2}}_{\begin{matrix}
\text{conmutativa} \\
\text{del producto}
\end{matrix}} = \underbrace{v_{1}u_{2}+v_{2}u_{1}}_{\begin{matrix}
\text{conmutativa} \\
\text{de la suma}
\end{matrix}} = \quad \underbrace{< \vec{v},\vec{u}>}_{\begin{matrix}
\leftarrow \text{def }<\vec{v},\vec{u}>
\end{matrix}} \\ \\
a_{2}: <k\vec{u},\vec{v}> = k<\vec{u},\vec{v}> \\ \\
k<\vec{u},\vec{v}> \quad = \quad \underbrace{k(u_{1}v_{2}+u_{2}v_{1})}_{\begin{matrix}
\text{def: }k<\vec{u},\vec{v}>
\end{matrix}} = \underbrace{ku_{1}v_{2}+ku_{2}v_{1}}_{\begin{matrix}
\text{distributiva del} \\
\text{producto}
\end{matrix}} = \underbrace{<k \vec{u},\vec{v}>}_{\begin{matrix}
\leftarrow \text{def: }<k \vec{u},\vec{v}>
\end{matrix}} \\ \\
a_{3}: <\vec{u},\vec{v}+\vec{w}> \quad = \quad \vec{u},\vec{v}> + <\vec{u},\vec{w}> \\ \\
 <\vec{u},\vec{v}+\vec{w}> \quad = \quad u_{1}(v_{2}+w_{2})+u_{2}(v_{1}+w_{1}) = u_{1}v_{2}+u_{1}w_{2}+u_{2}v_{1}+u_{2}w_{1} \\ \\
 <\vec{u},\vec{v}> = u_{1}v_{2}+u_{2}v_{1} \quad,\quad <\vec{u},\vec{w}> = u_{1}w_{2}+u_{2}w_{1} \\ \\
 < \vec{u},\vec{v}>+<\vec{u},\vec{w}> = u_{1}v_{2}+u_{2}v_{1}+u_{1}w_{2}+u_{2}w_{1} = u_{1}v_{2}+u_{1}w_{2}+u_{2}v_{1}+u_{2}w_{1} = <\vec{u},\vec{v}+\vec{w}> \\
 \\
a_{4}: <\vec{u},\vec{u}> \quad \geq \quad 0 \\ \\
<\vec{u},\vec{u}> = u_{1}u_{2}+u_{2}u_{1}  = u_{1}u_{2}+u_{1}u_{2} = 2u_{1}u_{2} \\ \\
\text{luego vemos que no cumple el axioma 5, por contra ejemplo:} \\ \\
\exists (-1,1) \in \mathbb{R}² \quad \land \quad <(-1,1),(-1,1)> \quad = \quad (-1)(1)+1(-1)=-2<0 
\end{gather}
$$
ii) $$
\begin{gather}
a_{1}: \\ \\
< \vec{u},\vec{v}> = u_{1}v_{1}+u_{2}v_{1}+u_{1}v_{2}+2u_{2}v_{2} \\
<\vec{v},\vec{u}> = v_{1}u_{1}+v_{2}u_{1}+v_{1}u_{2}+2v_{2}u_{2} = v_{1}u_{1}+v_{1}u_{2}+v_{2}u_{1}+2v_{2}u_{2} \\
= u_{1}v_{1}+u_{2}v_{1}+u_{1}v_{2}+2u_{2}v_{2} = <\vec{u},\vec{v}> \\ \\
a_{2}:  \\ \\
k<\vec{u},\vec{v}> = k(u_{1}v_{1}+u_{2}v_{1}+u_{1}v_{2}+2u_{2}v_{2}) = ku_{1}v_{1}+ku_{2}v_{1}+ku_{1}v_{2}+2ku_{2}v_{2} \\
k \vec{u}=k(u_{1},u_{2})=(ku_{1},ku_{2}) \Rightarrow <k \vec{u},\vec{v}>= ku_{1}v_{1}+ku_{2}v_{1}+ku_{1}v_{2}+2ku_{2}v_{2} \\
k<\vec{u},\vec{v}> = <k \vec{u}, \vec{v}> \\ \\
a_{3}: \\
 \\
\vec{v} + \vec{w} = (v_{1},v_{2})+(w_{1},w_{2})=(v_{1}+w_{1},v_{2}+w_{2}) \\
<\vec{u},\vec{v}+\vec{w}> = u_{1}(v_{1}+w_{1})+u_{2}(v_{1}+w_{1})+u_{1}(v_{2}+w_{2})+2u_{2}(v_{2}+w_{2}) \\
=u_{1}v_{1}+u_{1}w_{1}+u_{2}v_{1}+u_{2}w_{1}+u_{1}v_{2}+u_{1}w_{2}+2(u_{2}v_{2}+u_{2}w_{2}) \\
<\vec{u},\vec{v}> + <\vec{u},\vec{w}> = (u_{1}v_{1}+u_{2}v_{1}+u_{1}v_{2}+2u_{2}v_{2})+(u_{1}w_{1}+u_{2}w_{1}+u_{1}w_{2}+2u_{2}w_{2}) \\
<\vec{u},\vec{v},\vec{w}> = <\vec{u},\vec{v}>+<\vec{u},\vec{w}> \\ \\
a_{4}: \\ \\
<\vec{u},\vec{u}> = u_{1}u_{1}+u_{2}u_{1}+u_{1}u_{2}+2u_{2}u_{2}=u_{1}²+2u_{1}u_{2}+2u_{2}² \\
\text{luego esa expresión es siempre positiva pues }u_{1}²+2u_{2}² \\
\text{es siempre positiva y ademas es mas grande que } 2u_{1}u_{2}: \\ \\
u_{1}²+2u_{2}² \quad \geq \quad 2u_{1}u_{2} \\
(u_{1}²+2u_{2}²)² \quad \geq \quad (2u_{1}u_{2})² \\
u_{1}⁴+4u_{1}u_{2}+4u_{2}⁴ \quad \geq \quad 4u_{1}u_{2} \\
u_{1}⁴+u_{2}⁴ \quad \geq  \quad 0 \\
\therefore \text{esto es verdadero }\forall \mathbb{R} \Rightarrow u_{1}²+2u_{1}u_{2}+2u_{2}² \quad \geq \quad 0 \\ \\
a_{5}: \\ \\
consultar
\end{gather}
$$
**Vectores unitarios:** los vectores unitarios son aquellos cuya magnitud (norma) es 0. Por ejemplo: $\vec{u}= \left ( \frac{1}{2}, \frac{\sqrt{ 3 }}{2} \right) \Rightarrow ||\vec{u}||= \sqrt{ \left( \frac{1}{2} \right)²+ \left( \frac{\sqrt{ 3 }}{2} \right)² }= \sqrt{ \frac{1}{4} + \frac{3}{4} }=1$ .

es posible encontrar un vector unitario a partir de un vector, esto nos sirve por que el vector resultante tiene la misma dirección y puede ser útil para cuando veamos ortogonalidad.

sea $\vec{u} \in \mathbb{V}$ el vector unitario representado por $\vec{u}$ es: $\frac{1}{||\vec{u}||}\vec{u}$

### Ejercicio  3. 

**a) calcule las normas usando el producto interno usual de los siguientes vectores:**
1. $u_{2}$
2. $2u_{2}$
3. $u_{1}+u_{2}$
**b) determine los vectores unitarios correspondientes de $u_{1},u_{2},v_{1},v_{2}$**
**c) usando los vectores $u_{2},u_{3}$ verifique la desigualdad de Cauchy-Schwarz** .

##### Solución:
**a)** $$
\begin{gather}
1) \quad |u_{2}| = \sqrt{ 3²+5² } = \sqrt{ 9+25 }=\sqrt{ 34 }=5.83 \\ \\
2) \quad |2u_{2}|=\sqrt{ 6²+10² } =\sqrt{ 36+100 } = \sqrt{ 136 }=11.66 \\
 \\
3) \quad |u_{1}+u_{2}| = \sqrt{ 1²+8² } = \sqrt{ 65 } = 8.06
\end{gather}
$$
**b)** $$
\begin{gather}
u_{1}=(-2,3) \Rightarrow \frac{1}{||u_{1}||}u_{1} = \frac{1}{\sqrt{ 13 }}(-2,3) = \left( -\frac{2}{\sqrt{ 13 }}, \frac{3}{\sqrt{ 13 }} \right) \\ \\
u_{2}=(3,5) \Rightarrow \frac{1}{||(3,5)||} (3,5) = \left(  \frac{3}{\sqrt{ 34 }}, \frac{5}{\sqrt{ 34 }} \right) \\ \\
v_{1}= (3,2,0) \Rightarrow \frac{1}{||(3,2,0)||}(3,2,0) = \left( \frac{3}{\sqrt{ 13 }}, \frac{2}{\sqrt{ 13 }} , 0 \right) \\ \\
v_{2}=(-2,4,2) \Rightarrow \frac{1}{||(-2,4,2)||} (-2,4,2) = \left( -\frac{2}{\sqrt{ 24 }} , \frac{4}{\sqrt{ 24 }} , \frac{2}{\sqrt{ 24 }}\right) = \left( -\frac{1}{\sqrt{ 5 }} , \frac{2}{\sqrt{ 5 }} , \frac{1}{\sqrt{ 5 }} \right)
\end{gather}
$$
**c)** $$
\begin{gather}
\text{la desigualdad de Cauchy-Schwarz nos dice lo siguiente: } \\ \\
|<\vec{u},\vec{v}>| \leq ||\vec{u}||\cdot ||\vec{v}|| \\ \\
|<u_{2},u_{3}>| \leq ||u|| \cdot ||v|| \\ \\
|9|\leq ||(-2,3)|| \cdot ||(3,5)|| \\
9 \leq \sqrt{ 13 } \cdot \sqrt{ 34 } \\
9\leq \sqrt{ 442 } \\
9\leq 21.02
\end{gather}
$$
**ortogonalidad:** un vector es ortogonal a otro cuando el angulo que se comprende entre ellos es de 90°, es fácil calcular un vector que sea ortogonal a otro para ello usaremos la siguiente formula:
$$
\cos \phi = \frac{<\vec{u},\vec{v}>}{||\vec{u}||\cdot ||\vec{v}||}
$$
esa formula nos dice que el coseno del angulo de dos vectores es igual al producto interno sobre el producto de las normas.

y si necesitamos que el angulo sea 90° entonces: $\phi = 90° \Rightarrow \cos 90 = 0 \Rightarrow <\vec{u},\vec{v}> = 0$.

	si el producto interno da 0 entonces los vectores son ortogonales entre si

**Angulo entre dos vectores:** de mismo modo yo puedo calcular el angulo entre dos vectores con la formula anterior, solo debemos pasar el coseno al otro miembro para dejar a phi solo, y eso significa multiplicar por $\cos^{-1}$ en ambos miembros, pero la inversa del coseno es en realidad el arcos.
$$
\phi = \arccos \left( \frac{<\vec{u},\vec{v}>}{||\vec{u}||\cdot||\vec{v}||} \right)
$$
un vector es ortogonal a un conjunto de vectores si es ortogonal a cada uno de ellos.

### Ejercicio 5.
**dados los siguientes vectores:** $v_{1} = (1, 0, 2), v_{2} = (2, 1, −1),y v_{3} = (−1, k2, 2)$

* **Un vector unitario que tenga la misma dirección y el mismo sentido que $v_{1}$**.
* **Un vector de norma 1 y ortogonal a $v_{1}$**.
* **El conjunto de todos los vectores ortogonales a $v_{2}$ y pruebe que es un espacio de $\mathbb{R}³$** .
* **El valor de k para que  $v_{2} \quad y \quad v_{3} \quad$ sean ortogonales.**

##### Solución:
$$
\begin{gather}
1) \quad \frac{1}{||(1,0,2)||} (1,0,2) = \frac{1}{\sqrt{ 5 }}(1,0,2) = \left( \frac{1}{\sqrt{ 5 }}, 0, \frac{2}{\sqrt{ 5 }} \right) \\ \\ \\
2)\quad \vec{u}=(x,y,z) \Rightarrow <\vec{u},\vec{v_{1}}> = 0 \\
xv_{1}+yv_{2}+zv_{3} = 0 \\
x+2z=0 \\
x=-2z \\
\text{sea } \vec{u}=(-2z,0,z) \text{ si } z=1 \Rightarrow \vec{u}=(-2,0,1) \\
<(1,0,2),(-2,0,1)>= 0 \\ \\ \\
3 ) \quad <(2,1,-1),(x,y,z)>=0 \\
2x+y-z=0 \\ 
S = \{\forall (x,y,z) \in \mathbb{R}^3: 2x+y-z=0 \} \\
G(S): \{z=2x+y\} \\
\text{lugo todos los vectores con la forma: }(x,y,2x+y) \text{ seran ortogonales a }v_{2} \\ \\ \\
4 ) \quad <(2,1,-1),(-1,k²,2)>= 0 \\
-2+k²-2=0 \\
k²-4=0 \\
(k+2)(k-2)=0 \\
\therefore k=2 \quad \land \quad k=-2 \\
<(2,1,-1),(-1,4,2)>=0
\end{gather}
$$
### Ejercicio 6.
**considere los siguientes vectores:**
$$
v_{1}=(3,1,0)\quad \quad \quad v_{2}=(1,3,0) \quad \quad \quad v_{3}=(3,3,5)
$$
**a) calcule el $\cos \phi$ entre:    $i) \quad v_{1},v_{2}$     $ii) \quad v_{1},v_{3}$     $iii) \quad v_{1},2v_{3}$    , luego calcule también a $\phi$**
**b) Determine un vector unitario u tal que forme con $v_{1}$ y con $v_{2}$ ángulos iguales.**
**c) ídem al inciso anterior consiga el conjunto de vectores unitarios que tenga el mismo angulo.**

###### Solución:
**a)** $$
\begin{gather}
i)\quad \cos \phi = \frac{<(3,1,0),(1,3,0)>}{||(3,1,0)|| \cdot ||(1,3,0)||} \\ \\
\cos \phi = \frac{6}{\sqrt{ 10 }\cdot \sqrt{ 10 }}= \frac{6}{10}  \\ \\
\phi = arcos \left( \frac{6}{10} \right)=53° \\ \\ \\
ii) \quad \cos \phi = \frac{<(3,1,0),(3,3,5)>}{||(3,1,0)||\cdot||(3,3,5)||} \\ \\
\cos \phi = \frac{12}{\sqrt{ 10 }\sqrt{ 43 }}=\frac{12}{143} \\ \\
\phi=\arccos\left( \frac{12}{\sqrt{ 143 }} \right)=54.64° \\ \\ \\
iii) \quad \cos \phi = \frac{<(3,1,0),(6,6,10)>}{||(3,1,0)||\cdot||(6,6,10)||} \\ \\
\cos \phi = \frac{24}{\sqrt{ 10 }\sqrt{ 172 }}=\frac{3}{\sqrt{ 5 }\sqrt{ 43 }} \\ \\
\phi = \arccos\left( \frac{3}{\sqrt{ 129 }} \right)=74.68
\end{gather}
$$
**b)** $$
\begin{gather}
\text{sea } u = (u_{1},u_{2},u_{3}) \\ \\
\arccos \left( \frac{<(u_{1},u_{2},u_{3}),(3,1,0)>}{||(u_{1},u_{2},u_{3})|| \cdot ||(3,1,0)||} \right) =  \arccos \left( \frac{<(u_{1},u_{2},u_{3}),(1,3,0)>}{||(u_{1},u_{2},u_{3})||\cdot ||(1,3,0)||} \right) \\ \\
\arccos\left( \frac{3u_{1}+u_{2}}{\sqrt{ 10(u_{1}²+u_{2}²+u_{3}²) }} \right)=\arccos \left(  \frac{u_{1}+3u_{2}}{\sqrt{ 10(u_{1}²+u_{2}²+u_{3}²) }}  \right) \\ \\
\frac{3u_{1}+u_{2}}{\sqrt{ 10(u_{1}²+u_{2}²+u_{3}²) }}= \frac{u_{1}+3u_{2}}{\sqrt{ 10(u_{1}²+u_{2}²+u_{3}²) }}  \\ \\
3u_{1}+u_{2} = u_{1}+3u_{2} \\ \\
3u_{1}-u_{1} = 3u_{2}-u_{2} \\ \\
2u_{1}=2u_{2} \\ \\
u_{1}=u_{2} \\ \\
\text{si }u=1 \text{ entonces: }u=(1,1,0) \\ \\
\arccos\left( \frac{<(1,1,0),(3,1,0)>}{||(1,1,0)||\cdot ||(3,1,0)||} \right)=\arccos\left( \frac{4}{\sqrt{ 20 }} \right) \\ \\
\arccos \left( \frac{<(1,1,0),(1,3,0)>}{||(1,1,0)|| \cdot ||(1,3,0)||} \right)=\arccos\left( \frac{4}{\sqrt{ 20 }} \right) \\ \\
\therefore\text{el vector u tiene el mismo angulo con }v_{1} \text{ y } v_{2}. 
\end{gather}
$$
**c)** podemos ver del inciso anterior que podemos expresar una forma general del vector u donde todo vector con esa forma va a tener el mismo angulo con $v_{1}$ y $v_{2}$: $\forall u \in \mathbb{R}³: u = (u_{1},u_{1},u_{3})$.

**Proyecciones ortogonales:**
### Ejercicio 7. 
**considere los siguientes vectores:** $u_{1}=(1,2)\quad u_{2}=(3,-2) \quad v_{1}=(2,-3,1) \quad v_{2}=(-5,2,1)$

**calcule :** $proy_{u_{1}}^{u_{2}}; \quad proy_{u_{2}}^{u_{1}}; \quad proy_{v_{1}}^{v_{2};} \quad proy_{u_{2}}^{u_{1}}$.

##### Solución:
$$
\begin{gather}
proy_{u_{1}}^{u_{2}}= \frac{<(1,2),(3,-2)>}{||(1,2)||²}(1,2)=-\frac{1}{5}(1,2)=\left( -\frac{1}{5} , -\frac{2}{5} \right) \\ \\
proy_{u_{2}}^{u_{1}} = \frac{<(1,2),(3,-2)>}{||(3,-2)||²}(3.-2)=-\frac{1}{13}(3,-2)=\left( -\frac{3}{13} , \frac{2}{13} \right) \\ \\
proy_{v_{1}}^{v_{2}}= \frac{<(2,-3,1),(-5,2,1)>}{||(2,-3,1)||^2}(2,-3,1)=-\frac{15}{14}(2,-3,1)=\left( -\frac{15}{7} , \frac{45}{14} , -\frac{15}{14} \right) \\ \\
proy_{v_{2}}^{v_{1}}= \frac{<(2,-3,1),(-5,2,1)>}{||(-5,2,1)||²}(-5,2,1)=-\frac{1}{2}(-5,2,1)=\left( \frac{5}{2} , -1, -\frac{1}{2} \right)
\end{gather}
$$

**Complemento ortogonal**

Sabemos que podemos determinar si un conjunto de vectores es un subespacio de algún espacio vectorial dado, podemos decir algo como $\mathbb{S}$ es subespacio de $\mathbb{V}$. podemos encontrar el conjunto de vectores que pertenecen a $\mathbb{V}$ de manera que todos esos vectores sean ortogonales al subespacio $\mathbb{S}$.

a ese conjunto lo denominamos complemento ortogonal de $\mathbb{S}$ y su definición en símbolos es la siguiente:
$$
\mathbb{S}^{\perp} = \{\forall \vec{x} \in \mathbb{V}: <x,y>=0, \forall \vec{y} \in \mathbb{S} \}
$$
**Producto Vectorial**

hemos definido con anterioridad el producto interno entre dos vectores que su resultado nos devuelve un numero real, sus aplicaciones eran importantes como la posibilidad de ver que un vector es ortogonal a otro o para calcular el angulo, norma era necesario también, ahora veremos un producto entre vectores que se llama vectorial porque devuelve un vector y sus aplicaciones son mas interesantes aún.

**Definición:**
$$
\begin{gather}
\text{sean los vectores: } \\
\vec{u} = a_{1}i+b_{1}j+c_{1}k \\
\vec{v}= a_{2}i+b_{2}j+c_{2}k \\ \\
\text{entonces el prducto vectorial entre } u \times v \text{ es un nuevo vector que resulta: } \\ \\
\vec{u} \times \vec{v} = (b_{1}c_{2}-c_{1}b_{2})i+(c_{1}a_{2}-a_{1}c_{2})j+(a_{1}b_{2}-b_{1}a_{2})k
\end{gather}
$$
también al producto vectorial se lo conoce como producto cruz, por que esta demostrado que se puede resolver con un producto cruzado como se muestra a continuación:
$$
\vec{u} \times \vec{v} = \begin{vmatrix}
i&j&k \\
u_{1}&u_{2}&u_{3} \\
v_{1}&v_{2}&v_{3}
\end{vmatrix} = \begin{vmatrix}
u_{2}&u_{3} \\
v_{2}&v_{3}
\end{vmatrix} i -\begin{vmatrix}
u_{1}&u_{3} \\
v_{1}&v_{3}
\end{vmatrix}j+\begin{vmatrix}
u_{1}&u_{2} \\
v_{1}&v_{2}
\end{vmatrix}k
$$
aunque se ve parecido a un determinante no llega a serlo porque $(i,j,k)$ no son números, pero nos ayuda la notación a recordar el producto cruz, ya que el resultado es como hacer laplace por la primera fila.

ahora veamos algunos teoremas interesantes del producto vectorial, es curioso como sin ser un determinante se cumplen varias de sus reglas:

1. $\vec{u} \times 0= 0 \times \vec{u} = 0$
2. $\vec{u} \times \vec{v}=-(\vec{v} \times \vec{u})$
3. $\alpha  \vec{u} \times \vec{ v} = \alpha ( \vec{u} \times \vec{v})$
4. $\vec{u} \times (\vec{v} + \vec{w}) = (\vec{u} \times \vec{v})+(\vec{u} \times \vec{w})$
5. $<(\vec{u} \times \vec{v}),\vec{w}> = <\vec{u}, \vec{v} \times \vec{w}>$
6. el producto vectorial me devuelve un vector que es ortogonal tanto a $\vec{u}$ como a $\vec{v}$.
7. si el producto me devuelve el vector nulo y ninguno de los operandos era el nulo entonces resulta que u y v son paralelos.

### Ejercicio 11.
**Dados los vectores $u = (1, 2, 1)$ y $v = (1, −2, 3)$ y $w = 2i + 3j + 2k$**

**a) determine $u \times v$ y $v \times u$**
**b) Determine un vector unitario y que sea ortogonal simultáneamente a $u \quad y \quad  v$.**
**c) Determine un vector paralelo a $u \times w$ y cuya longitud sea 2 unidades.**

##### Solución:
**a)**$$
\begin{gather}
u \times v = \begin{vmatrix}
i&j&k \\
1&2&1 \\
1&-2&3
\end{vmatrix} = \begin{vmatrix}
2&1 \\
-2&3
\end{vmatrix}i-\begin{vmatrix}
1&1 \\
1&3
\end{vmatrix}+\begin{vmatrix}
1&2 \\
1&-2
\end{vmatrix}k = (8,-2,-4) \\ \\
v \times u = \begin{vmatrix}
i&j&k \\
1&-2&3 \\
1&2&1
\end{vmatrix} = \begin{vmatrix}
-2&3 \\
2&1
\end{vmatrix}i - \begin{vmatrix}
1&3 \\
1&1
\end{vmatrix}j+\begin{vmatrix}
1&-2 \\
1&2
\end{vmatrix}k = (-8,2,4)
\end{gather}
$$
**Obvservación:** podemos ver con claridad uno de los teoremas en funcionamiento con el ejercicio, $u \times v = -(v \times u)$.

**b)** $$
\begin{gather}
\text{el producto vectorial nos devuelve un vector ortogonal tanto a }u\text{ como a } v,\text{ es decir:} \\
w=(8,-2,-4) \Rightarrow w \perp u \quad \land \quad w \perp v \\ \\
\text{si ademas a }w \text{ lo normalizamos obtenemos un vector ortogonal y unitario:} \\ \\
w_{1}= \frac{1}{||w||}w = \frac{1}{\sqrt{ 64+4+16 }} (8,-2,-4) = \left( \frac{8}{\sqrt{ 84 }} , -\frac{2}{\sqrt{ 84 }} , -\frac{4}{\sqrt{ 84 }} \right)
\end{gather}
$$
**c)** $$
\begin{gather}
u \times w = \begin{vmatrix}
i&j&k \\
1&2&1 \\
2&3&2
\end{vmatrix} = \begin{vmatrix}
2&1 \\
3&2
\end{vmatrix}i - \begin{vmatrix}
1&1 \\
2&2
\end{vmatrix}j + \begin{vmatrix}
1&2 \\
2&3
\end{vmatrix}k = (1,0,-1) \\
\\
\text{para conseguir un vector paralelo a } s= \underbrace{(1,0,-1)}_{u \times w} \text{ usamos el teorema que dice que dos vectores } \\
\text{son paralelos si su producto vectorial da el vector nulo, y ademas ambos son distintos del nulo: } \\
\\
s \times x =  (1,0,-1) \times (x,y,z) = \odot \Rightarrow (1,0,-1) \times (x,y,z) = (0,0,0) \\
\\
\begin{vmatrix}
i&j&k \\
1&0&-1 \\
x&y&z
\end{vmatrix} = \begin{vmatrix}
0&-1 \\
y&z
\end{vmatrix}i- \begin{vmatrix}
1&-1 \\
x&z
\end{vmatrix}j + \begin{vmatrix}
1&0 \\
x&y
\end{vmatrix}k = (y,-x-z,y) \\
\\
(y,-x-z,y) = (0,0,0) \\
\\
\begin{cases}
y=0 \\
-x-z=0 \\
y=0
\end{cases} \sim \begin{pmatrix}
0&1&0 \\
-1&0&-1 \\
0&1&0
\end{pmatrix} \sim \begin{pmatrix}
1&0&1 \\
0&1&0 \\
0&1&0
\end{pmatrix}\sim \begin{pmatrix}
1&0&1 \\
0&1&0 \\
0&0&0
\end{pmatrix} \sim \begin{cases}
x+z=0 \\
y=0
\end{cases} \\
\\
\text{luego 2 ecuaciones y 3 incognitas } = 1VL, \text{ elegimos como variable libre a z y tenemos que:} \\
\\
x=-z  \Rightarrow s=(-z,0,z) \\
\\
\text{este seria el vector generico que cumple que sea paralalelo a }u \times w\text{ pero como nos piden uno solo} \\
\text{basta con buscar un }z\text{ y ver que forma tiene el vector, si } z = 1 \Rightarrow (-1,0,1)
\end{gather}
$$
![[Pasted image 20261022230855.png]]

