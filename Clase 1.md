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

$$\s^4 + 3s^3 + 3s^2 + s + 2\]$$

Factorizamos o aplicamos algún método de raíces:

Suponiendo que se prueba con:

$$\[(s+1)(s+2) = s^2 + 3s + 2\]$$

Entonces:

$$\s^2 + 3s + 2 = 0\]$$

Aplicamos la fórmula general:

$$\s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\]$$

Donde:

$$\a = 1, \quad b = 3, \quad c = 2\]$$

$$\s = \frac{-3 \pm \sqrt{9 - 8}}{2} = \frac{-3 \pm \sqrt{1}}{2}\]$$

$$s = \frac{-3 \pm 1}{2}\]$$

$$s_1 = -1, \quad s_2 = -\]$$

---

### Otro ejemplo con raíz cuadrada:

$$s = -3 + \sqrt{(3)^2 - 4(1)(2)}\]$$

$$s = \frac{-3 \pm \sqrt{9 - 8}}{2} = \frac{-3 \pm 1}{2}\]$$


### Resultado:

Polos en:

$$s = -1, \quad s = -2\]$$


### Representación gráfica en el plano complejo

Se dibujan los polos y ceros en el plano con ejes reales e imaginarios:

- Polos en: \( s = -1 \), \( s = -2 \)
- Ceros en: \( s = -2 \pm \sqrt{3} \)

(Dibujo de plano cartesiano con marcas en los valores correspondientes).








