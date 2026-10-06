existen varias métricas a la hora de evaluar si un bloque de código es lo suficientemente bueno, podemos medir el tiempo en el que tarda en ejecutarse, la cantidad de pasos que realiza o la magnitud de su salida si se usan muchos datos, por lo general el tiempo que tarada en ejecutarse es una de las métricas mas importantes.

en el momento de resolver algún problema podemos encontrar un algoritmo que lo resuelva, sin embargo, es sabido que distintos algoritmos resuelven un solo problema, pero todos comparten la misma entrada y misma salida, ¿entonces que cambia? lo que cambia es la cantidad de pasos y como procesa los datos en su interior y medir cual es el mejor si todos resuelven el problema radica en contar la cantidad de operaciones elementales que este realiza.

**Operaciones elementales:**
	Las operaciones elementales es la sentencia mas simple que realiza el algoritmo, como por ejemplo: un calculo aritmético, una comparación, un retorno de una función o procedimiento o el acceso a memoria de un array entre otras cosas.

**código de ejemplo:**
```java
int x;
x=0;
x=x+1;
System.out.println(x);
```

1. La asignación de x = 0 es una operación elemental.
2. La suma aritmética de x +1 es otra operación elemental pero también le estoy asignando así que en dicha linea estoy usando 2 OE.
3. en total tengo 3 OE.

voy a listar a continuación una serie de reglas para la contabilización de operaciones elementales:

* if(condición){ segmento 1} else { segmento 2}
	 en el caso de una sentencia de control como la del if-else las OE se cuentan de la siguiente manera:
	* $T(condición)$, el tiempo que cuesta la condición del if.
	* $T_{max}(S_{1},S_{2})$, el tiempo que cuesta el segmento 1 o el segmento 2, depende cual sea el que se elija según cual cueste más.
	* $T=T(condición)+T(S_{1},S_{2})$ 
* $switch(condicón)\{\text{case a: }S_{1}\text{ case b: }S_{2}\text{ case n: }Sn\}$ 
	 en el caso de una sentencia de switch cases, se cuenta de la siguiente forma:
	* $T(condición)*k$, donde k es la cantidad de comparaciones que hace antes de entrar a un case.
	* $T(S)=max(S_{1},S_{2},\dots,S_{n})$
	* $T[(condición)*k]+T(S)$
* $for(\text{int i = 1 ; i < n ; i ++})\{sentencia\}$ 
	 para contabilizar las operaciones de un for se utiliza la siguiente formula, donde n es la cantidad de iteraciones:
$$
T=n+ \sum_{j=1}^{n}S_{j}
$$
* para el ciclo while tenemos la siguiente formula:
* $$
T=((N°iteraciones)\cdot (T(S)+ T(condición)))+T(condición)
$$
	esta formula se debe a que antes de salir del ciclo hace una ultima evaluación de la condición si es falsa sale del ciclo por eso se suma un $T(condición)$ al final, luego la principal expresión es $n$ veces la evaluación de la condición que dan verdaderas antes de que se corte el ciclo y $n$ veces la sentencia.


estamos listos para poner a prueba los ejercicios del trabajo practico con código de programación y luego veremos las reglas para el pseudocodigo.

```pascal
CONST n =...; (* num. maximo de elementos de un vector *)
TYPE vector = ARRAY [1..n] OF INTEGER;
FUNCTION Buscar(VAR a:vector;c:INTEGER):INTEGER; 
VAR j: INTEGER; 
BEGIN j:= 1; 
WHILE (a[j]<c) AND j<n DO 
	j:=j+1
end
IF a[j]=c THEN
	RETURN j
ELSE
	RETURN 0
end
end {Buscar};
```

empezamos a contar desde la linea 5, que tiene una asignación, luego la siguiente linea es un while donde aplicamos la formula, después sumamos las OE del if-else:
$$
T=\underbrace{1}_{j:=1}+\underbrace{\left( 3+(n*(3+2)) \right)}_{\text{formula del while}} +\underbrace{2+1}_{\text{if-else}} = 5n+7
$$
```Pascal

FUNCTION Producto(n,m: Integer): Integer; 
VAR i,prod: integer; 
BEGIN 
	Prod:= 0; 
	For i:=1 to n do 
		Prod:= prod+m; 
	Producto:= prod 
END; {Producto}
```

comenzando desde la linea 4 tenemos:
$$
T = \underbrace{1}_{Prod:=0} + \underbrace{n(1+2)}_{for} + \underbrace{1}_{Producto:=prod} = 3n+2
$$
```Pascal
FUNCTION Producto(n,m: Integer): Integer; 
VAR i,j,prod: Integer; 
BEGIN 
	Prod:= 0; 
	For i:=1 to n do 
		For j:= 1 to m do 
			Prod:= prod+1; 
	Producto:= prod 
END; {Producto}
```

compliquemos un poco las cosas, al tener ciclos anidados estamos calculando sumatorias anidadas:
$$
T = 1 + n(1+(m(1+2)))+1= n+3nm+2 \Rightarrow \text{sea n: }max(n,m) \Rightarrow T= 3n²+n+2
$$
véase como hacemos el n(1+S) del primer for y adentro esta S = m(1+S2) del segundo for quedando : $n(1+(m(1+2)))$.

**Calculo de numero de operaciones con Pseudocodigo:**
	cuando se trata de pseudocodigo tenemos otros criterios para calcular las OEs, en este caso solo nos interesan los datos aritméticos, comparaciones y asignaciones, pero solamente cuando son sentencias no cuando son condiciones, ademas las funciones no existen en pseudocodigo lo que simplifica el calculo:

```Pseudocodigo
Factorizar_x_Gauss(A; n) 
	Definir L(n,n),U(n,n) 
	Sea U=A 
	Para k = 1 hasta n-1, hacer 
		L(k,k) = 1 
		Para i = k+1 hasta n, hacer 
			L(i,k) = U(i,k)/U(k,k) 
			U(i,k) = 0 
				Para j = k+1 hasta n, hacer 
					U(i,j) = U(i,j) − L(i,k) · U(k,j) L(n,n) = 1 
Retornar {L,U}
```

ahora se complico peor, porque si bien las únicas sentencias que suman algo son las de las lineas: $3,5,7,8,10,11$ . no nos olvidemos que están dentro de un ciclo lo cual indica aplicarles la formula:
$$
\begin{gather}
T(c) = (n-k-1) +\sum_{j=k+1}^{n} 2 = (n-k-1)+2(n-k) = 3n-3k-11
\end{gather}
$$



---
### Errores

Matemáticamente hablando existen infinitos números reales, pero al momento de tener que resolver problemas computables con números existe un problema, no podemos representar todos en una computadora, todas tienen un limite, y es necesario conocerlo para no operar dos números que no se puedan representar por que es muy probable que el resultado sea incorrecto y el error que se provoca sea enorme.

imaginemos que una calculadora quiere sumar dos números y el resultado correcto te hace aprobar un examen difícil, es de mucha importancia que yo pueda estar seguro que ese resultado va a estar bien, pero como se cuales son los números que se pueden representar?

**Representación de un número:**
	en la computadora supongamos de 32 bits la representación de un número es la siguiente:
	![[representacionNumero.excalidraw]]
	donde la mantisa es un numero en punto flotante, es decir, decimal.
	****
	****
	Podemos definir un conjunto finito donde quepan en el todos los números que pueden ser representado en ciertas condiciones, se va a denominar malla y se expresa de la siguiente  manera:
	$$
	F \subset \mathbb{R} : f = \pm m \cdot \beta ^{~e-t}
	$$
	donde $\beta$ es la base del número (por lo general base 2 o 16), el $t$ es la cantidad de dígitos de precisión que tiene un número, $e$ es el exponente pero cumple la particularidad de: $L<e<U$.**
	L es es el menor exponente con el que se pueden representar números en la maquina.
	U es el mayor exponente con el que se pueden representar números.
	m se denomina mantisa y es un número en punto flotante, también cumple la relación: $0<m\leq\beta^{t}-1$

**Limites en la malla:**
1. **La mayor mantisa representable es:** $(1-\beta)^{-t}$ 
2. **El mayor número representable es:** $(1-\beta)^{-t}\beta^{U}$
3. **La menor mantisa representable es:** $\beta^{-t}$
4. **El menor número representable es:** $\beta^{L-1}$
5. **Un número esta en punto flotante normalizado cuando:** $\pm m\cdot\beta^{e} \Rightarrow \frac{1}{\beta}\leq m<1$.
6. **La malla tiene esta cantidad de números:** $2(\beta-1)\cdot \beta^{t-1} \cdot (U-L+1)$
7. **La distancia entre dos representantes es:** $D = \beta^{e-t}$

a partir de ahora vamos a trabajar únicamente con valores que estén en punto flotante normalizado.


