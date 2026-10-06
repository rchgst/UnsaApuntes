### Ejercicio N° 1 Calcular el costo temporal en el mejor caso, peor caso y caso promedio del siguiente algoritmo:

```pascal
CONST n = ...; (* num. maximo de elementos de un vector *)
TYPE vector = ARRAY [1..n] OF INTEGER;
FUNCTION Buscar (VAR a: vector; c: INTEGER): INTEGER; 
VAR j: INTEGER; 
BEGIN j := 1; 
	WHILE (a[j] < c) AND (j < n) DO 
		j := j + 1; 
	END; 
	IF a[j] = c THEN 
		RETURN j 
	ELSE 
		RETURN 0 
	END 
END {Buscar};
```
$$
i)~~~~T_{min}(n)= 1+2+3=6
$$
$$
ii)~~~~T_{máx}(n)=1+ \left(\left(\sum_{i=1}^{n-1} 4+2 \right) +4 \right)=6n+2
$$
$$
iii)~~~~ T_{med}= \sum_{i=1}^n (6i+2) \cdot \frac{1}{n}=\frac{1}{n} \left[ 6\sum_{i=1}^n i+ 2\sum_{i=1}^n 1\right] = \frac{1}{n} \left[ 6 \cdot \frac{(n+1)n}{2} +2n\right]
$$
## N° 2 Calcular el costo temporal de los siguientes algoritmos:
```Pascal
FUNCTION Producto (n, m: Integer): Integer;
VAR i, prod: Integer;
BEGIN
    prod := 0;
    FOR i := 1 TO n DO
        prod := prod + m;
    Producto := prod
END; {Producto}
```
$$
T_{max}(n) = 1 + \left( n+\sum_{i=1}^n 2 \right)+ 1=3n+2
$$
```Pascal
FUNCTION Producto (n, m: Integer): Integer;
VAR i, j, prod: Integer;
BEGIN
    prod := 0;
    FOR i := 1 TO n DO
        FOR j := 1 TO m DO
            prod := prod + 1;
    Producto := prod
END; {Producto}
```
$$
T_{máx}(n)= 1+ \left[ m + \sum_{i=1}^m \left( n + \sum_{j=1}^n 2 \right) \right]+1= 1+ \left[ m+m \cdot \left( n+2n \right) \right] +1= m+4mn+2
$$
$$
\text{sea n } = máx(m,n) \Rightarrow 4n^2+n+2
$$
