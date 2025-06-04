# Nombre: Kevin Nicolas Perez Tobar
# Curso: M6A
# Dinamica de Sistemas
 
## 1. Introducción
En la dinámica de sistemas, la función de transferencia es una herramienta matemática fundamental que describe el comportamiento de un sistema lineal e invariante en el tiempo (LTI)
en el dominio de Laplace. Esta función permite analizar cómo un sistema responde a una entrada dada, sin tener que resolver directamente las ecuaciones diferenciales que lo gobiernan.

## 2. Resumen
La función de Transferencia es una herramienta que nos permite modelar un movimiento dinamico que permite mirar si esta en el dominio del tiempo, vamos a ver los tres tipos de casos,
ejercicios, graficas y comportamientos segun el sistema lo reqiuiera.

# 3. Definición
🔑 Función de Transferencia: La función de transferencia también puede considerarse como la respuesta de un sistema inicialmente inerte a un impulso como señal de entrada: y la respuesta como función del tiempo se halla con la transformada de Laplace inversa de Y(s): Cualquier sistema físico (mecánico, eléctrico, etc.)

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/e75a5fb923dd89fb523c3e875b5307957f578b32/Build/Funcion%20de%20Transferencia.png?raw=true" width="300">
</div>

 En el área de control se usa otro tipo de representación matemática denominada función de transferencia
 • Consiste en la transformada de Laplace de la ecuación diferencial
 
### 3.1 Clasificacion de las Funciones de Transferencia

3.11 Función impropia: Cunado el grado del Denominador es mas grande que el denominador.

3.12 Funcion Bipropia: Cuando el grado del Numerador y El Denominador es igual.

3.13 Funcion estrictamente propia: Cunado el grado del Numerador es mas grande que el Denominador.

## 4. Ejemplos
Clasificar las siguientes funciones segun el orden

$$s^2 + 1 \hspace{2cm} \textit{impropia}$$

$$2 \hspace{3.6cm} \textit{bipropia}$$

$$\frac{1}{s + 1} \hspace{2cm} \textit{Estrictamente propia}$$

$$\frac{s^2 - 1}{s + 1} \hspace{1.2cm} \textit{impropia}$$

$$\frac{s - 1}{s + 1} \hspace{1.6cm} \textit{bipropia}$$

# 4.1 Zeros de una Funcion de Transferencia
Son los valores de S que todos los valores de transferencia obtienen los valores de "S" que cumplen la condicion.


# Ejemplo

### Hallar los ceros de una función de transferencia

$$\frac{s^2 + 4s + 1}{s^4 + 3s^3 + 3s^2 + s + 2}$$

### Paso 1: Igualar el numerador a cero

$$s^2 + 4s + 1 = 0$$

Aplicamos la fórmula general:

$$s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Donde:

Sustituyendo:

$$s = \frac{-4 \pm \sqrt{(4)^2 - 4(1)(1)}}{2(1)} = \frac{-4 \pm \sqrt{16 - 4}}{2}\]$$

$$s = \frac{-4 \pm \sqrt{12}}{2} = \frac{-4 \pm 2\sqrt{3}}{2}$$

$$s = -2 \pm \sqrt{3}\]$$


### Representación en el plano complejo

Se ubican los ceros en el eje real, ya que no tienen parte imaginaria:

$$ \( s_1 = -2 + \sqrt{3} \)$$
$$\( s_2 = -2 - \sqrt{3} \)$$


### Nota:

$${Los ceros siempre van a dar un número real.}$$

### Análisis de los polos — cuando el denominador se hace cero

$$\[G(s) = \frac{Y(s)}{U(s)} = \frac{s^2 + 4s + 1}{s^4 + 3s^3 + 3s^2 + s + 2}\]$$

### Paso: Hallar los polos

El denominador:

$$s^4 + 3s^3 + 3s^2 + s + 2\$$

Factorizamos o aplicamos algún método de raíces:

Suponiendo que se prueba con:

$$(s+1)(s+2) = s^2 + 3s + 2\]$$

Entonces:

$[\s^2 + 3s + 2 = 0\]$$

Aplicamos la fórmula general:

$$[s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\]$$

Donde:


$$\[a = 1, \quad b = 3, \quad c = 2\]$$

$$\[s = \frac{-3 \pm \sqrt{9 - 8}}{2} = \frac{-3 \pm \sqrt{1}}{2}\]$$

$$\[s = \frac{-3 \pm 1}{2}\]$$

$$\[s_1 = -1, \quad s_2 = -\]$$
### Otro ejemplo con raíz cuadrada:

$$\[s = \frac{-3 \pm \sqrt{(3)^2 - 4(1)(2)}}{2}\]$$


$$\[s = \frac{-3 \pm \sqrt{9 - 8}}{2} = \frac{-3 \pm 1}{2}\]$$


### Resultado:

Polos en:

$$\[s = -1, \quad s = -2\]$$


### Representación gráfica en el plano complejo

Se dibujan los polos y ceros en el plano con ejes reales e imaginarios:

- Polos en: \( s = -1 \), \( s = -2 \)
- Ceros en: \( s = -2 \pm \sqrt{3} \)

(Dibujo de plano cartesiano con marcas en los valores correspondientes).

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/f74095e5992c02b969b6be09056f1e95572bf907/Build/grafica%20de%20matlab.png" width="300">
</div>

## 4.2 Polos de una funcion de trasnferencia 

• Si se iguala D(s) a 0 se obtienen los valores de “s” que cumplen con la condición

• Si el denominador se hace 0 toda la función de transferencia se vuelve infinito de ahí el nombre para
  estos valores de “s”
  
• Estos valores pueden ser reales o complejos por lo tanto se pueden ubicar en un plano cartesiano

Ejemplo
Hallar la funcion de trasnferencia de la siguiente funcion. 

$$G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}$$

$$D(s) = s^2 + 3s + 2 = (s + 1)(s + 2)$$

$$\text{Polos: } s = -1, \quad s = -2$$

## 5. Ubicacion grafica de polos

<div align="center">
<img src= "https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/9783cc3e060592a3bf6fd53879ac5e7ef574a4dd/Build/grafica%20de%20polos.png" widht=300">
</div>

## 5.1 Grafica de Polos y zeros de la funcion de Transferencia

<div align="center">
<img src= "https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/493cc6be7d2dd5c7c1efb7404a4afaf6af327c1a/Build/Grafica%20de%20polos%20y%20zeros%20de%20una%20funcion%20de%20transferencia%20.png" widht=300">
</div>

## Grado de la funcion de Transferencia

 • Otra forma de clasificar las funciones de transferencia es  por su orden o grado
 
 • Esto lo define el polinomio característisco
 
 • Por ejemplo

La función de transferencia está dada por:

$$
G(s) = \frac{3s - 1}{s^2 + 3s + 2}
$$

Donde el **polinomio característico** de segundo orden es:

$$
D(s) = s^2 + 3s + 2
$$

La funcion de Transferencia es de segundo orden, debido a que es de grado 2.

## 5.2 Teorema del valor final

El error en estado estacionario corresponde al error 
medido en 𝑡 =∞

 • Es posible aprovechar el teorema del valor final para 
saber el valor final del error

$$\lim_{t \to \infty} f(t) = \lim_{s \to 0} sF(s)$$

### Función de Transferencia y Respuesta a Escalón

La función de transferencia del sistema es:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{4}{5s + 1}
$$

Multiplicando por \( U(s) \):

$$
Y(s) = \frac{4}{5s + 1} \cdot U(s)
$$

---

#### Entrada: Escalón Unitario

Un escalón unitario tiene transformada de Laplace:

$$
U(s) = \frac{1}{s}
$$

Entonces la salida será:

$$
Y(s) = \frac{4}{s(5s + 1)}
$$

### Teorema del Valor Final

El valor final de \( Y(s) \) se puede calcular aplicando el **teorema del valor final**:

$$\lim_{t \to \infty} y(t) = \lim_{s \to 0} sY(s)$$

Dado que:

$$Y(s) = \frac{4}{s(5s + 1)}$$

Entonces:

$$\lim_{s \to 0} sY(s) = \lim_{s \to 0} s \cdot \frac{4}{s(5s + 1)} = \lim_{s \to 0} \frac{4}{5s + 1}$$

Y finalmente:

$$\lim_{s \to 0} \frac{4}{5s + 1} = \frac{4}{1} = 4$$

## 7. Tablas

### Tabla: Tipos de funciones de transferencia, sus ecuaciones y respuestas

| Tipo de Sistema                        | Función de Transferencia \( G(s) \)                                | Ecuación Diferencial (Tiempo)                                      | Tipo de Respuesta                      |
|----------------------------------------|--------------------------------------------------------------------|---------------------------------------------------------------------|----------------------------------------|
| Primer Orden                           | $$( \frac{K}{\tau s + 1} \)$$                                         | $$( \tau \frac{dy(t)}{dt} + y(t) = K u(t) \)$$                         | Exponencial decreciente                |
| Primer Orden con Polo en el Origen     | $$( \frac{K}{s(\tau s + 1)} \)$$                                     | $$( \tau \frac{d^2y(t)}{dt^2} + \frac{dy(t)}{dt} = K u(t) \)$$        | Rampa + estabilización                 |
| Segundo Orden Subamortiguado           | $$( \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2} \)$$       | $$( \frac{d^2y(t)}{dt^2} + 2\zeta\omega_n \frac{dy(t)}{dt} +\omega_n^2 y(t) = \omega_n^2 u(t) \)$$ | Oscilatoria amortiguada                |
| Segundo Orden Críticamente Amortiguado | $$( \frac{\omega_n^2}{s^2 + 2\omega_n s + \omega_n^2} \)$$           | Igual que arriba con \( \zeta = 1 \)                                | Más rápida sin oscilación              |
| Segundo Orden Sobreamortiguado         | $$( \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2} \)$$      | Igual que arriba con \( \zeta > 1 \)                                | Dos exponentes reales negativos        |
| Segundo Orden No Amortiguado           | $$( \frac{\omega_n^2}{s^2 + \omega_n^2} \)$$                          | $$( \frac{d^2y(t)}{dt^2} + \omega_n^2 y(t) = \omega_n^2 u(t) \)$$    | Oscilación sostenida                   |

## 8. Ejercicios 

## Ejercicio 8.1
 
La función de transferencia está dada por:

$$G(s) = \frac{s + 3}{s^3 + 11s^2 + 12s + 18}$$
---

### 🔹 Ceros

Los ceros son las raíces del numerador:

$$s + 3 = 0 \Rightarrow s = -3$$

---

### 🔹 Polos

Los polos son las raíces del denominador:

$$s^3 + 11s^2 + 12s + 18 = 0$$

Este polinomio cúbico no se puede factorizar fácilmente con raíces racionales simples. Se recomienda usar métodos numéricos (como en MATLAB o Python) para encontrar las raíces.

---

### ✅ Resultado final

- **Función de Transferencia**:

$$G(s) = \frac{s + 3}{s^3 + 11s^2 + 12s + 18}$$

- **Cero**: $s = -3$  
- **Polos**: raíces de $s^3 + 11s^2 + 12s + 18$
- 
  ## Ejercicio 8.2

{Función de Transferencia:}

$$G(s) = \frac{7}{s^2 + 5s + 10}$$

{1. Ceros:}

{El numerador es una constante (7), por lo tanto no hay ceros.}

{Ceros} = \varnothing

{2. Polos:}

{Se obtienen resolviendo el denominador:}

s^2 + 5s + 10 = 

{Usamos la fórmula cuadrática:}

$$\quad s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

a = 1, b = 5, c = 10

$$s = \frac{-5 \pm \sqrt{5^2 - 4(1)(10)}}{2(1)} = \frac{-5 \pm \sqrt{25 - 40}}{2}$$

$$s = \frac{-5 \pm \sqrt{-15}}{2} = \frac{-5}{2} \pm \frac{j\sqrt{15}}{2}$$

{Polos} 

$$s= \frac{-5}{2} \pm \frac{j\sqrt{15}}{2}$$

## 9. Conclusiones
9.1 Aprendimos que la funcion de Transferencia es una funcion matematica que describe como un sistema dinamico responde de una entrada a una salida .
Es importante analizar el sistema ya que nos permite ver como el sistema se comporta, bajo diferentes condiciones

9.2 Los polos y ceros de una función de transferencia determinan de forma directa el comportamiento dinámico de un sistema. Los ceros influyen en la forma de la respuesta del sistema, mientras que los polos definen su estabilidad y velocidad de respuesta. Estos va ser importante, ya que la ubicación de los polos va definir si el sistema si es estable, inestable o marginamente inestable.

## 10. Bibliografia 
Cote, J. (s.f.). Función de Transferencia [Diapositivas de clase]. Escuela de Tecnología Electrónica, ETITC.

Kuo, B. C. (1996). Dinámica de sistemas físicos (3.ª ed.). Prentice Hall.

