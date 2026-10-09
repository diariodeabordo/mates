# TEMA 2. ESPACIOS VECTORIALES
## Ficha de estudio — Estilo Navarro

**Hilo conductor:** un espacio vectorial es un mundo de flechas que pueden sumarse y estirarse.

## 1. Espacios vectoriales: un mundo de flechas

### ❓ ¿Qué es un espacio vectorial?

La idea fundamental es sencilla: tenemos un conjunto de objetos, llamados **vectores**, sobre los que podemos realizar dos operaciones:

- Sumar vectores para obtener otro vector.
- Multiplicar un vector por un número para obtener otro vector.

Estos números se llaman **escalares**.

### 🧠 Definición 1. Espacio vectorial

Un espacio vectorial $V$ es un espacio de vectores en el que están definidas la suma de vectores y la multiplicación por escalares, de modo que ambas operaciones cumplen las propiedades habituales de un espacio vectorial.

Denotaremos los vectores por $u,v,w,\ldots$ y los escalares por letras griegas, como $\lambda,\mu,\alpha,\beta,\ldots$.

Las dos operaciones fundamentales son

$$
u+v\in V,\qquad \lambda u\in V.
$$

💡 **Intuición.** Imagina un mundo de flechas. Podemos colocar dos flechas consecutivamente para obtener su suma, o estirar, encoger e invertir una flecha multiplicándola por un número. El resultado sigue perteneciendo al mismo mundo.

Por ejemplo, multiplicar una flecha por $2$ duplica su longitud; multiplicarla por $-1$ invierte su sentido; multiplicarla por $0$ produce el vector nulo.

**Límite de la imagen.** No todos los espacios vectoriales están formados literalmente por flechas dibujadas en un plano. Las flechas son una imagen para comprender las operaciones; los vectores también pueden ser matrices, tuplas u otros objetos.

### 🔍 Cómo leer los signos

| Signo | Se lee | Imagen mental |
|---|---|---|
| $V$ | Espacio vectorial | El mundo completo |
| $u,v\in V$ | $u$ y $v$ pertenecen a $V$ | Dos flechas del mismo mundo |
| $u+v$ | Suma de $u$ y $v$ | Componer dos flechas |
| $\lambda u$ | Producto de $\lambda$ por $u$ | Estirar, encoger o invertir |
| $0$ | Vector nulo | La flecha que no se desplaza |
| $\mathbb R^n$ | Espacio de $n$-tuplas reales | Un mundo con $n$ coordenadas |

La definición completa exige, además, las propiedades habituales: asociatividad y conmutatividad de la suma, existencia del vector nulo y del opuesto, y compatibilidad de la multiplicación por escalares con las operaciones del cuerpo base.

La idea no es memorizar una lista sin sentido: estas propiedades garantizan que sumar y estirar vectores funcione de manera coherente.

### 🧪 Ejemplos de espacios vectoriales

**1. Los espacios $\mathbb R^n$**

$$
\mathbb R^2,\quad \mathbb R^3,\quad \mathbb R^4,\quad \ldots,\quad \mathbb R^n.
$$

Sus vectores son tuplas de números reales. Por ejemplo, un vector de $\mathbb R^3$ tiene la forma

$$
(x,y,z),\qquad x,y,z\in\mathbb R.
$$

**2. Las matrices cuadradas de orden $2$**

$$
\mathbb R^{2\times2}
=
\left\{
\begin{pmatrix}
a&b\\
c&d
\end{pmatrix}
:a,b,c,d\in\mathbb R
\right\}.
$$

Podemos sumar dos matrices y multiplicar una matriz por un número real. Ambas operaciones producen otra matriz del mismo tipo.

**3. El origen también puede constituir un espacio vectorial**

Por ejemplo,

$$
\{(0,0)\}\subseteq\mathbb R^2,
\qquad
\{(0,0,0)\}\subseteq\mathbb R^3.
$$

También tenemos el espacio formado únicamente por la matriz nula:

$$
\left\{
\begin{pmatrix}
0&0\\
0&0
\end{pmatrix}
\right\}
\subseteq\mathbb R^{2\times2}.
$$

💡 **Intuición.** Un espacio vectorial no tiene por qué contener muchas flechas. Incluso un mundo con una única flecha, la flecha nula, es suficiente: sumarla consigo misma o multiplicarla por cualquier escalar no nos saca de ese mundo.

### 🧭 El punto de referencia

Cuando aparece una estructura nueva, conviene tener presente un ejemplo conocido. Las diapositivas eligen el plano $\mathbb R^2$.

En él podemos visualizar la suma y la multiplicación por escalares. A partir de ese modelo construiremos nuestra intuición, aunque las conclusiones se aplicarán también a espacios menos visuales.

### ⚠️ No confundir

Un espacio vectorial no es necesariamente un plano geométrico. $\mathbb R^2$ es nuestro modelo visual, pero $\mathbb R^3$, $\mathbb R^4$ y el espacio de matrices también son espacios vectoriales.

### 📝 Comprobación

1. ¿Cuáles son las dos operaciones fundamentales?
2. ¿Qué significa que el resultado de una operación permanezca en el espacio?
3. ¿Por qué el conjunto formado solo por el vector nulo es un espacio vectorial?

### 🎞️ Película mental

Un mundo de flechas. Las flechas se suman y se estiran. Las reglas garantizan que el resultado siempre siga perteneciendo al mundo.

---

## 2. Subespacios vectoriales: mundos dentro de un mundo

Una vez entendido el espacio completo, podemos mirarlo por dentro.

La pregunta es: **¿podemos seleccionar una parte del espacio que, por sí sola, siga siendo un espacio vectorial?**

### 🧠 Definición 2. Subespacio vectorial

Sea $V$ un espacio vectorial. Un subconjunto $U\subseteq V$ es un **subespacio vectorial** de $V$ cuando también es un espacio vectorial con las mismas operaciones.

En ese caso escribimos

$$
U\leq V.
$$

💡 **Intuición.** Dentro del mundo de todas las flechas de un plano podemos escoger, por ejemplo, las que están sobre una recta que pasa por el origen. Si al sumar dos de esas flechas o estirar cualquiera de ellas seguimos dentro de la recta, hemos encontrado un mundo más pequeño que conserva las reglas del original.

La clave no es que $U$ tenga una forma geométrica especial. La clave es que las operaciones no nos expulsen de $U$.

### 📐 Teorema 3. Criterio para subespacios

Sea $V$ un espacio vectorial y $U\subseteq V$. Entonces $U$ es un subespacio vectorial si y solo si:

1. **Estabilidad por producto escalar:**

   $$
   \lambda\in\mathbb R,\ u\in U
   \quad\Longrightarrow\quad
   \lambda u\in U.
   $$

2. **Estabilidad por suma:**

   $$
   u,v\in U
   \quad\Longrightarrow\quad
   u+v\in U.
   $$

💡 **Intuición.** Son las dos reglas del mundo de las flechas aplicadas ahora a un mundo interior: estirar una flecha de $U$ no debe sacarnos de $U$, y sumar dos flechas de $U$ tampoco.

**Precisión lógica.** El criterio se entiende suponiendo $U\neq\varnothing$, o exigiendo explícitamente que $0\in U$. Sin esta condición, el conjunto vacío cumpliría vacíamente las dos implicaciones, pero no es un espacio vectorial. En adelante, cuando apliquemos el criterio, tendremos presente esta condición.

En efecto, si $U$ no es vacío y es estable por producto escalar, para cualquier $u\in U$ tenemos

$$
0u=0\in U.
$$

Así aparece necesariamente el vector nulo.

### 🧪 Ejemplos de subespacios

**1. Todo espacio vectorial es subespacio de sí mismo.**

$$
V\leq V.
$$

No hay nada que comprobar: sumar o multiplicar por escalares vectores de $V$ nos mantiene en $V$.

💡 **Intuición.** El mundo completo siempre es un mundo dentro de sí mismo.

**2. El origen es un subespacio.**

$$
\{(0,0)\}\leq\mathbb R^2,
\qquad
\{(0,0,0)\}\leq\mathbb R^3.
$$

También lo es el conjunto formado por la matriz nula.

💡 **Intuición.** La flecha nula permanece en su sitio al sumarse con ella misma y al multiplicarse por cualquier escalar.

**3. La recta $y=x$ es un subespacio de $\mathbb R^2$.**

Consideremos

$$
U=\{(x,y)\in\mathbb R^2:y=x\}.
$$

Sus vectores tienen la forma $(t,t)$. Si tomamos dos de ellos,

$$
(t,t)+(s,s)=(t+s,t+s),
$$

la suma sigue verificando que la segunda coordenada coincide con la primera. Además,

$$
\lambda(t,t)=(\lambda t,\lambda t)
$$

también pertenece a $U$. Por el criterio, $U\leq\mathbb R^2$.

💡 **Intuición.** Las flechas de esa recta pueden sumarse y estirarse sin abandonar la recta.

**4. Un subespacio de matrices.**

Consideremos el conjunto de matrices simétricas de orden $2$:

$$
U=
\left\{
\begin{pmatrix}
a&b\\
b&d
\end{pmatrix}
:a,b,d\in\mathbb R
\right\}
\subseteq\mathbb R^{2\times2}.
$$

La característica común es que las dos entradas situadas fuera de la diagonal principal coinciden.

Si sumamos dos matrices de esta forma, obtenemos

$$
\begin{pmatrix}
a&b\\
b&d
\end{pmatrix}
+
\begin{pmatrix}
a'&b'\\
b'&d'
\end{pmatrix}
=
\begin{pmatrix}
a+a'&b+b'\\
b+b'&d+d'
\end{pmatrix}.
$$

La estructura se conserva. También se conserva al multiplicar por un escalar. Por tanto, $U$ es un subespacio.

💡 **Intuición.** Aunque aquí no dibujemos flechas en un plano, la idea es la misma: elegimos matrices que cumplen una condición y comprobamos que las operaciones respetan esa condición.

### 📏 Observación 4. Todo subespacio contiene el origen

Si $U\leq V$, entonces

$$
0\in U.
$$

💡 **Intuición.** Todo mundo de flechas vectorial debe contener la flecha nula. Si el origen falta, no puede ser un subespacio.

Esta observación proporciona una primera prueba rápida: si un conjunto no contiene el vector nulo, podemos descartar inmediatamente que sea un subespacio.

### 🚧 Contraejemplos

**1. El conjunto $\{(1,1)\}$ no es un subespacio de $\mathbb R^2$.**

No contiene el origen. En consecuencia, no puede ser un subespacio.

También podemos verlo mediante la multiplicación por escalares:

$$
0(1,1)=(0,0)\notin\{(1,1)\}.
$$

**2. La recta $y=1+x$ no es un subespacio de $\mathbb R^2$.**

El origen no pertenece a ella, pues $0\neq1+0$.

💡 **Intuición.** Una recta que no pasa por el origen no puede ser un mundo vectorial: al multiplicar por cero cualquiera de sus vectores, llegaríamos al origen, que está fuera de la recta.

### 🚧 El ejemplo de la parábola

Consideremos

$$
P=\{(x,y)\in\mathbb R^2:y=x^2\}.
$$

La parábola contiene el origen, ya que $0=0^2$. Sin embargo, **no es un subespacio vectorial**.

En efecto, los vectores $(1,1)$ y $(-1,1)$ pertenecen a $P$, porque sus coordenadas verifican $y=x^2$. Pero su suma es

$$
(1,1)+(-1,1)=(0,2),
$$

y $(0,2)\notin P$, pues $2\neq0^2$.

💡 **Intuición.** Tener el origen no basta. La parábola contiene la flecha inicial y ciertas flechas simétricas, pero al sumar dos de ellas podemos salir de la curva. Le falta la estabilidad por suma.

### ⚠️ No confundir

- Contener el origen es necesario, pero no suficiente.
- Ser una recta o una curva tampoco basta: hay que comprobar las operaciones.
- Para descartar un subespacio basta encontrar un fallo: una suma o un producto escalar que salga del conjunto.

### 📝 Comprobación

1. ¿Qué dos comprobaciones permiten reconocer un subespacio?
2. ¿Por qué una recta que no pasa por el origen no puede serlo?
3. ¿Qué falla en la parábola $y=x^2$?

### 🎞️ Película mental

Imagina un mundo grande y selecciona una región. Ahora suma y estira flechas que estén dentro de ella. Si alguna operación te lleva fuera, esa región no es un subespacio. Si las operaciones siempre permanecen dentro —y el conjunto no está vacío—, sí lo es.

---

## 3. Combinaciones lineales: fabricar flechas

Ya sabemos qué es un mundo vectorial y qué significa que una parte suya conserve sus reglas. El siguiente paso consiste en estudiar cómo podemos construir flechas nuevas a partir de otras.

Solo tenemos dos operaciones: sumar y multiplicar por escalares. **Toda construcción obtenida mediante estas operaciones se llama combinación lineal.**

### 🔍 Ejemplo 5. Combinar vectores

Sean

$$
u=(1,0),\qquad v=(2,1).
$$

Podemos combinar $u$ consigo mismo:

$$
u+u,\qquad -u,\qquad u+2u,\qquad u-u=0.
$$

Todas estas expresiones son múltiplos de $u$. En general, tienen la forma

$$
\lambda u.
$$

También podemos combinar $u$ y $v$:

$$
u+v,\qquad v-u,\qquad 3u-2v,\qquad 7u+5v.
$$

La forma general es

$$
\lambda u+\mu v.
$$

💡 **Intuición.** Partimos de unas flechas disponibles. Podemos estirarlas, invertirlas y sumarlas. Cada elección de escalares produce una nueva flecha.

### 🧠 Definición 6. Combinación lineal

Sean $v_1,\ldots,v_n\in V$. Una **combinación lineal** de esos vectores es cualquier vector de la forma

$$
\lambda_1v_1+\cdots+\lambda_nv_n,
$$

donde $\lambda_1,\ldots,\lambda_n$ son escalares.

Los escalares indican cuánto aporta cada vector a la combinación. Pueden ser positivos, negativos o nulos.

💡 **Intuición.** Cada vector aporta una dirección y un factor de escala. La combinación reúne todas esas aportaciones en una única flecha.

Por ejemplo, si un coeficiente es cero, el vector correspondiente no contribuye a la suma. Si es negativo, contribuye en sentido contrario.

### 🧪 Ejemplo 7. Una combinación concreta

Con los vectores del ejemplo anterior,

$$
u=(1,0),\qquad v=(2,1),
$$

consideremos $2u+3v$. Calculamos:

$$
\begin{aligned}
2u+3v
&=2(1,0)+3(2,1)\\
&=(2,0)+(6,3)\\
&=(8,3).
\end{aligned}
$$

Por tanto, $(8,3)$ es una combinación lineal de $u$ y $v$.

💡 **Intuición.** Duplicamos la primera flecha, triplicamos la segunda y sumamos los resultados. La flecha final es $(8,3)$.

### 🧭 El principio que conecta todo

Si $U$ es un subespacio, cualquier combinación lineal de vectores de $U$ pertenece a $U$.

Recíprocamente, un subconjunto no vacío de $V$ es un subespacio si contiene todas las combinaciones lineales finitas de sus vectores.

En símbolos,

$$
U\leq V
\quad\Longleftrightarrow\quad
\text{$U$ contiene todas las combinaciones lineales finitas de sus propios vectores.}
$$

💡 **Intuición.** El subespacio es un mundo cerrado a la fabricación de flechas: cualquier flecha que construyas a partir de las que ya están dentro permanece dentro.

La parábola del ejemplo anterior no cumplía esta condición: dos vectores de la parábola daban lugar a una suma que ya no pertenecía a ella.

### ⚠️ No confundir

Una combinación lineal es una **operación concreta** sobre unos vectores. Un subespacio es un **conjunto** que conserva todas esas operaciones. Una cosa es construir una flecha; otra, tener un mundo en el que todas las construcciones permitidas permanecen dentro.

### 📝 Comprobación

1. ¿Cuál es la forma general de una combinación lineal de $v_1,\ldots,v_n$?
2. ¿Qué papel desempeñan los escalares?
3. ¿Por qué la estabilidad por suma y producto escalar garantiza la estabilidad por combinaciones lineales finitas?

### 🎞️ Película mental

Tienes unas flechas de partida. Puedes estirarlas, invertirlas, anular algunas y sumarlas. La colección de todos los resultados posibles es el conjunto de flechas que puedes fabricar a partir de ellas.

---

## 4. Sistemas de generadores: ¿podemos fabricar todo el espacio?

La pregunta natural es ahora la siguiente: si partimos de unas pocas flechas, ¿podemos obtener todas las flechas del espacio?

### 🧪 Ejemplo 8. Generar nuevos vectores

Las diapositivas vuelven a considerar

$$
u=(1,0),\qquad v=(2,1).
$$

Ya hemos visto que podemos obtener

$$
2u+3v=(8,3).
$$

Pero podemos elegir otros escalares y fabricar muchas otras flechas. Esto conduce a una pregunta más ambiciosa: **¿podemos generar un espacio vectorial completo a partir de un conjunto finito de vectores?**

### 🧠 Definición 9. Sistema generador

Sean $v_1,\ldots,v_n\in V$. Decimos que estos vectores **generan $V$** si todo vector de $V$ es combinación lineal de ellos.

El conjunto $\{v_1,\ldots,v_n\}$ se llama **sistema generador** de $V$. Escribimos

$$
\langle v_1,\ldots,v_n\rangle=V.
$$

💡 **Intuición.** Un sistema generador es un conjunto de flechas con el que podemos fabricar todas las flechas del espacio. No importa cuántas haya en el espacio: lo decisivo es que ninguna quede fuera de lo que podemos construir.

### 🧪 Ejemplos de sistemas generadores

**1. Generadores de $\mathbb R^2$**

El conjunto

$$
\{(1,0),(0,1)\}
$$

genera $\mathbb R^2$, porque cualquier vector $(x,y)$ se escribe como

$$
(x,y)=x(1,0)+y(0,1).
$$

**2. Otro sistema generador de $\mathbb R^2$**

También genera $\mathbb R^2$ el conjunto

$$
\{(1,-1),(0,2)\}.
$$

**3. La base canónica como sistema generador de $\mathbb R^3$**

El conjunto

$$
\{(1,0,0),(0,1,0),(0,0,1)\}
$$

genera $\mathbb R^3$. En efecto, todo vector $(x,y,z)$ puede escribirse como

$$
(x,y,z)=x(1,0,0)+y(0,1,0)+z(0,0,1).
$$

**4. Un sistema generador menos inmediato de $\mathbb R^3$**

Las diapositivas también presentan

$$
\{(1,1,0),(1,0,1),(0,1,1)\}.
$$

Este conjunto genera $\mathbb R^3$.

💡 **Intuición común.** En los cuatro casos hay un conjunto de flechas de partida y una regla para construir cualquier vector del espacio. Los generadores son las piezas con las que se fabrica el conjunto completo.

### 🧭 El subespacio generado

Si partimos de $v_1,\ldots,v_n$, el conjunto de todas sus combinaciones lineales es

$$
\langle v_1,\ldots,v_n\rangle
=
\left\{
\lambda_1v_1+\cdots+\lambda_nv_n:
\lambda_i\in\mathbb R
\right\}.
$$

Este conjunto es el **subespacio generado** por esos vectores.

💡 **Intuición.** No es necesario que unas pocas flechas generen todo el espacio ambiente. Siempre generan un subespacio: el mundo más pequeño que contiene las flechas de partida y todas las que podemos fabricar con ellas.

En $\mathbb R^3$, un único vector no nulo genera una recta que pasa por el origen. Dos vectores pueden generar un plano si aportan direcciones independientes; si uno es múltiplo del otro, generan solamente una recta. Tres vectores generan todo $\mathbb R^3$ cuando aportan las tres direcciones necesarias.

**Límite de la imagen.** El número de vectores, por sí solo, no determina la forma del subespacio generado. También importa la relación entre ellos.

### ⚠️ No confundir

- Un conjunto de vectores genera $V$ si permite obtener **todos** los vectores de $V$.
- El subespacio generado es el conjunto de **todas** las combinaciones lineales de los vectores iniciales.
- Tener muchos generadores no garantiza que generen todo el espacio: pueden estar relacionados entre sí.

### 📝 Comprobación

1. ¿Qué significa que $\langle v_1,\ldots,v_n\rangle=V$?
2. ¿Cómo se escribe un vector arbitrario de $\mathbb R^2$ usando la base canónica?
3. ¿Qué diferencia hay entre el espacio ambiente $V$ y el subespacio generado por unas flechas?

### 🎞️ Película mental

Empiezas con unas pocas flechas. Al estirarlas y sumarlas, vas ampliando tu colección. El conjunto de todas las flechas que puedes fabricar constituye el subespacio generado. Si puedes fabricar todas las flechas del espacio ambiente, tienes un sistema generador.

---

## 5. Mapa de lo aprendido

La primera parte del tema queda organizada en una cadena de ideas:

$$
\boxed{
\begin{array}{c}
\text{Espacio vectorial}\\
\downarrow\\
\text{Subespacio vectorial}\\
\downarrow\\
\text{Combinaciones lineales}\\
\downarrow\\
\text{Sistema generador}
\end{array}
}
$$

Cada paso responde a una pregunta:

- **Espacio vectorial:** ¿en qué mundo podemos sumar y estirar?
- **Subespacio:** ¿qué partes de ese mundo conservan las operaciones?
- **Combinación lineal:** ¿cómo construimos una flecha a partir de otras?
- **Sistema generador:** ¿podemos construir todas las flechas del espacio?

La idea que sostiene todo es la misma: **sumar y estirar flechas**. El resto consiste en precisar qué conjuntos permiten esas operaciones y hasta dónde nos llevan.
