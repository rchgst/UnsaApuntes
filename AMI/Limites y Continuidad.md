### demostración de limites para el final.

sean L, M, a y k números reales y  ademas:
$$
\begin{matrix}
\lim_{ x \to a } f(x) = L \\
\lim_{ x \to a } g(x) = M
\end{matrix} 
$$
demostrar a continuación los siguientes limites usando la definición formal de limites:

1. $$
\lim_{ x \to a } f(x)+g(x) = L+M
$$
$$
\begin{matrix}
\text{hipotesis: } 0<|x-a|<\delta \Rightarrow |f(x)+g(x) ~-~(L+M)| < \epsilon \\
\Rightarrow |(f(x)-L) + (g(x)-M)| < \epsilon \\
\text{sabemos por definicion de limites y a que el limite L y M existen: } \\ \\

0<|x-a|< \delta_{1} \Rightarrow |f(x)-L|< \epsilon \\
0<|x-a|< \delta_{2} \Rightarrow |g(x)-M|< \epsilon \\ \\

\text{por el teorema de desigualdad triangular tenemos que: } \\ \\
  
 |(f(x)-L) + (g(x)-M)|\leq |f(x)-L|+|g(x)-M| \\ \\
 
 \text{sea}~~ \delta_{\text{min}}(\delta_{1},\delta_{2}) \\ \\

\text{como } \delta \text{  es el minimo de ambos delta se cumple que: } \\ \\
 
0<|x-a|< \delta \Rightarrow |f(x)-L|< \frac{\epsilon}{2} \\
0<|x-a|< \delta \Rightarrow |g(x)-M|< \frac{\epsilon}{2}   \\ \\

|f(x)+g(x)-(L+M)|\leq |f(x)-L|+|g(x)-M|< \frac{\epsilon}{2} + \frac{\epsilon}{2} \\
|f(x)+g(x)-(L+M)| < \epsilon \\ \\

\text{q.e.d}
\end{matrix}
$$
2. $$
\lim_{ x \to a } k \cdot f(x) = k \cdot L
 $$
 $$
 \begin{matrix}
 \text{hipotesis: } 0<|x-a|<\delta \Rightarrow |k \cdot f(x) - k \cdot L| < \epsilon \\
 \Rightarrow |k| \cdot |f(x) - L| < \epsilon \\
 \Rightarrow |f(x)-L|< \frac{\epsilon}{|k|} \\
  \\
 \text{basta con tomar: } \delta = \frac{\epsilon}{|k|} \text{ y se cumple la definición.}
 \end{matrix}
 $$
 3. $$
 \lim_{ x \to a } f(x) \cdot g(x) = LM 
 $$
$$
\begin{matrix}
\text{Hipótesis 1: } \lim_{x \to a} f(x) = L \quad \text{y} \quad \text{Hipótesis 2: } \lim_{x \to a} g(x) = M \\
\text{Queremos probar que para todo } \epsilon > 0, \text{ existe un } \delta > 0 \text{ tal que:} \\
0 < |x - a| < \delta \Rightarrow |f(x)g(x) - LM| < \epsilon \\ \\

\text{Fase de análisis previo (Borrador):} \\
\text{Sumamos y restamos convenientemente el término intermedio } g(x)L: \\ \\

|f(x)g(x) - g(x)L + g(x)L - LM| < \epsilon \\
|[f(x)g(x) - g(x)L] + [g(x)L - LM]| < \epsilon \\
|g(x)[f(x) - L] + L[g(x) - M]| < \epsilon \\ \\

\text{Por propiedad de desigualdad triangular y del producto en valor absoluto:} \\ \\

|g(x)[f(x) - L] + L[g(x) - M]| \leq |g(x)[f(x) - L]| + |L[g(x) - M]| \\
\leq |g(x)| \cdot |f(x) - L| + |L| \cdot |g(x) - M| \\ \\

\text{Como no podemos controlar directamente a } g(x) \text{ en todo el dominio, la acotamos:} \\ \\

\text{Sabemos que } g(x) \to M. \text{ Si tomamos } \epsilon_1 = 1, \exists \delta_0 > 0 \text{ tal que si } 0 < |x - a| < \delta_0 \Rightarrow |g(x) - M| < 1 \\
\text{Por propiedad del valor absoluto: } |g(x)| - |M| \leq |g(x) - M| < 1 \\
\Rightarrow |g(x)| < 1 + |M| \\ \\

\text{Sustituyendo este acotamiento en nuestra desigualdad principal nos queda:} \\ \\

|f(x)g(x) - LM| < (1 + |M|) \cdot |f(x) - L| + |L| \cdot |g(x) - M| \\ \\

\text{Ahora usamos las hipótesis para controlar el tamaño de cada parte de la suma. Dado } \epsilon > 0: \\ \\

\text{Por Hipótesis 1, } \exists \delta_1 > 0 \text{ tal que si } 0 < |x - a| < \delta_1 \Rightarrow |f(x) - L| < \frac{\epsilon}{2(1 + |M|)} \\
\text{Por Hipótesis 2, } \exists \delta_2 > 0 \text{ tal que si } 0 < |x - a| < \delta_2 \Rightarrow |g(x) - M| < \frac{\epsilon}{2(|L| + 1)} \\ \\

\text{Construcción de la Demostración Oficial:} \\
\text{Elegimos } \delta = \min(\delta_0, \delta_1, \delta_2). \text{ Si } 0 < |x - a| < \delta, \text{ se cumplen todas las acotaciones en simultáneo:} \\ \\

|f(x)g(x) - LM| \leq |g(x)| \cdot |f(x) - L| + |L| \cdot |g(x) - M| \\
< (1 + |M|) \cdot \left( \frac{\epsilon}{2(1 + |M|)} \right) + |L| \cdot \left( \frac{\epsilon}{2(|L| + 1)} \right) \\
< \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon \\ \\

\text{q.e.d.}
\end{matrix}
$$
4. $$
\lim_{ x \to a } \frac{1}{g(x)}=\frac{1}{M}
$$
$$
\begin{matrix}
\text{hipotesis: } 0<|x-a|<\delta \Rightarrow | \frac{1}{g(x)}-\frac{1}{M}| < \epsilon\\
\frac{|M-g(x)|}{|g(x)M|}<\epsilon \\
\frac{|M-g(x)|}{|g(x)||M|}<\epsilon \\ \\

\text{acotamos inferiormente a g(x) para controlarlo: } \\ \\

\text{usamos convenientemente un epsilon igual a la mitad del limite: }  \\
\epsilon = \frac{|M|}{2} \\
0<|x-a|<\delta_{1} \Rightarrow |g(x)-M | < \frac{|M|}{2} \\
|g(x)|-|M|\leq|g(x)-M|< \frac{|M|}{2} \\
|M|-|g(x)|< \frac{|M|}{2} \\
|M|- \frac{|M|}{2}<|g(x)| \Rightarrow \frac{|M|}{2}<|g(x)| \\ \\
\frac{|g(x)-M|}{|g(x)||M|}< \frac{|g(x)-M|}{\frac{|M|}{2}|M|} \\
\frac{|g(x)-M|}{|g(x)||M|}< \frac{2|g(x)-M|}{|M|^2}  \\ \\
\frac{2|g(x)-M|}{|M|^2} <\epsilon \\
|g(x)-M|< \frac{\epsilon \cdot |M|^2}{2} \\
\text{basta con tomar un }\delta = \frac{\epsilon \cdot |M|^2}{2}
\end{matrix}
$$
5. $$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \left[ f(x) \cdot \frac{1}{g(x)} \right]$$$$\text{Por el Teorema del Producto: } \left( \lim_{x \to a} f(x) \right) \cdot \left( \lim_{x \to a} \frac{1}{g(x)} \right)$$
$$\text{Y por el Teorema del Inverso: }~~ L \cdot \frac{1}{M} = \frac{L}{M}$$
$$q.e.d$$

6. $$
\lim_{ x \to a } [f(x)]^n = L^n 
$$
$$
\begin{matrix}
0<|x-a|<\delta \Rightarrow |[f(x)]^n-L^n|<\epsilon \\
tarea
\end{matrix}
$$
7. $$
\lim_{ x \to a } \sqrt{f(x)}=\sqrt{ L }
$$
8. $$
\text{unicidad del limite: } \lim_{ x \to a } f(x) = L_{1} ~~ \land ~~ \lim_{ x \to a } f(x) = L_{2} \Rightarrow L_{1} = L_{2}  
$$
