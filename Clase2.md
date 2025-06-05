# Nombre: Kevin Nicolas Perez Tobar
# Curso: M6A
# Dinamica de Sistemas
# Clase 2: 
 
## 1. Introducción
El modelamiento de sistemas complejos en ingeniería implica representar matemáticamente componentes físicos interconectados, tales como solenoides, motores de corriente directa (DC), transmisiones por engranajes y sistemas de poleas. Estos elementos presentan dinámicas particulares que deben integrarse en un modelo global para predecir el comportamiento del sistema completo. Una estrategia consiste en obtener la función de transferencia individual de cada componente, lo cual permite analizar y diseñar el sistema en bloques. Otra alternativa es utilizar modelos ya estandarizados y validados, que facilitan la construcción de sistemas más complejos con mayor eficiencia. Sin embargo, ambos enfoques enfrentan retos debido a la variabilidad de procesos y dispositivos involucrados.

## 2. Resumen
El modelamiento de sistemas complejos que incluyen solenoides, motores DC, engranajes y poleas puede abordarse mediante la obtención de funciones de transferencia individuales o usando modelos ya existentes. Estos enfoques permiten construir modelos precisos para representar sistemas dinámicos, aunque su aplicación depende del tipo de dispositivo y proceso implicado.

## 3. Definiciones

3.1 Selenoide: 

🔑 Definición
El electroimán atrae una masa acoplada por medio de un resorte y se considera el mortiguamiento dado por la envolvente de la bobina.Cuando se pasa electricidad por la bobina, se crea un campo magnético. Este campo magnético mueve un émbolo o núcleo dentro de la bobina. Este movimiento del émbolo es lo que permite que se utilicen para una amplia variedad de aplicaciones, desde válvulas de control hasta interruptores eléctricos.

Son fundamentales en una gran cantidad de productos y sistemas que utilizamos a diario, desde los electrodomésticos en nuestros hogares hasta la maquinaria industrial. Su capacidad para convertir energía eléctrica en energía mecánica los convierte en una tecnología esencial en una amplia gama de industrias.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/17e548d4e792fe1a0b040a5fdcb99999f53198b5/Build/imagen%20de%20selenoide.png" width="300">
</div>
Figura 3.1 Imagen de un selenoide 

Aqui vamos a presentarlas ecuaciones diferenciales, mas generales del sistema:

## Ecuaciones diferenciales y función de transferencia

## Ecuación diferencial del sistema masa-resorte-amortiguador:

$$\[m \frac{d^2x}{dt^2} + b \frac{dx}{dt} + kx = f(t)\]$$

##  Transformada de Laplace y función de transferencia:

$$\[X(s) = F(s) \cdot \frac{1}{ms^2 + bs + k}\]$$

💡# Ejemplo 3.11
⚙️ Sistema físico:
Un selenoide controla la posición de una válvula hidráulica. Cuando se aplica un voltaje 
𝑉(𝑡)V(t), el selenoide genera una fuerza magnética que mueve el núcleo, desplazando así la válvula.

📐 Supuestos del modelo:
El desplazamiento lineal del núcleo es x(t).

El selenoide tiene resistencia 
𝑅 Resistencia. 
𝐿, Inductancia.
K, constante de fuerza.
𝐾𝑓, Constante de friccion.
>>
Hay:
una masa 𝑚
fricción 𝑏
resorte con constante 𝑘
k que resiste el movimiento del núcleo.

## 🔹 Ecuaciones del sistema

### 🔸 1. Ecuación eléctrica del selenoide

$$\[ V(t) = L \frac{di(t)}{dt} + R i(t) \]$$


### 🔸 2. Fuerza generada por el selenoide

$$\[F(t) = K_f \cdot i(t)\]$$

### 🔸 3. Dinámica del núcleo (ecuación de movimiento)

$$\[F(t) = m \frac{d^2x(t)}{dt^2} + b \frac{dx(t)}{dt} + k x(t)\]$$

---

## 🔹 Transformadas de Laplace

### 🔸 1. Corriente en función del voltaje

$$\[I(s) = \frac{V(s)}{L s + R}\]$$

### 🔸 2. Fuerza en función del voltaje

$$\[F(s) = K_f \cdot I(s) = \frac{K_f \cdot V(s)}{L s + R}\]$$

### 🔸 3. Movimiento del núcleo en Laplace

$$\[F(s) = (m s^2 + b s + k) \cdot X(s)\]$$

---

## 🔹 Función de Transferencia

$$\[G(s) = \frac{X(s)}{V(s)} = \frac{K_f}{(m s^2 + b s + k)(L s + R)}\]$$



#3.2 Representacion de los Diagramas de Bloques

Aqui se puede representar de manera grafica, el sistema complejo, con su respectiva entrada y salida.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/774438ef0825d4d0f775a8e946da5430f5de821f/Build/Representacion%20de%20Diagramas%20de%20Bloques%20%20.png" width="300">
</div>
Figra 3.2  Representacion grafica del Diagrama de Bloques

## 3.22 Motor DC 
🔑 Definición
Un motor de CD es un dispositivo formado por un circuito eléctrico y un sistema mecánico de rotación. Su i nalidad es la de proporcionar torque a una carga. En esta sección se considerarán dos versiones del motor de CD: aquél controlado por corriente de campo y el correspondiente controlado por corriente de armadura. Además, se incluirá una entrada adicional a la entrada de referencia, esto es, una entrada de perturbación,que equivale a una entrada no deseada, pero inevitable, y se analizará su efecto sobre el sistema. 

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/f65138c0c4cd4ce0228a9b00b143234f770be813/Build/Sistema%20Motor%20DC.png" width="300">
</div>

Figura 3.22 Motor DC, controlado por corriente de campo

Este sistema electromecanico esta formado por tres etapas que son:
3.21 La primera etapa cuesta de un circuito RL, donde viene la etapa de transducción y posteriormente la carga acoplada al rotor del motor (RL)

💡 Ejemplo 3.23 

Un motor de corriente directa (DC) está alimentado con un voltaje 
𝑉(𝑡) y se usa para controlar la velocidad de giro de un eje conectado a una carga con momento de inercia 
J y fricción viscosa b. La constante de par del motor es  Kt, y la constante de fuerza contraelectromotriz (fem) es Kb El circuito del motor tiene una resistencia  𝑅y una inductancia L.

##  Ecuaciones características
### 🔸 1. Ecuación eléctrica del motor

$$\[V(t) = L \frac{di(t)}{dt} + R i(t) + K_b \omega(t)\]$$

### 🔸 2. Par generado por el motor

$$\[T(t) = K_t \cdot i(t)\]$$

### 🔸 3. Dinámica rotacional (segunda ley de Newton)

$$\[T(t) = J \frac{d\omega(t)}{dt} + b \omega(t)\]$$

Transformación al dominio de Laplace

$$\[V(s) = (L s + R) I(s) + K_b \Omega(s)\]$$

$$\[T(s) = K_t I(s)\]$$

$$\[T(s) = (J s + b) \Omega(s)\]$$

Sustituyendo para obtener la función de transferencia

$$\[K_t I(s) = (J s + b) \Omega(s) \Rightarrow I(s) = \frac{(J s + b)}{K_t} \Omega(s)\]$$

$$\[V(s) = (L s + R) \cdot \frac{(J s + b)}{K_t} \Omega(s) + K_b \Omega(s)\]$$

$$\[V(s) = \left[ \frac{(L s + R)(J s + b)}{K_t} + K_b \right] \Omega(s)\]$$

\Rightarrow \boxed
$$[{G(s) = \frac{\Omega(s)}{V(s)} = \frac{K_t}{(L s + R)(J s + b) + K_t K_b}}]$$


## 4. Ecuaciones del Motor DC

## 4.1 Parte eléctrica:
Consta de una bobina de inductancia \( L_c \) y una resistencia \( R_c \):

$$[L_c \frac{di_c}{dt} + R_c i_c = v_c(t)\]$$

cuya representación en el dominio \( s \) es:

$$[I_c(s) = V(s) \cdot \frac{1}{sL_c + R_c}\]$$

## 4.2 El Torque del motor aplicado a la parte mecanica

El torque desarrollado es proporcional al Φ y a la corriente de armadura

% Torque desarrollado por el motor

$$T_m = K_a \cdot i_a(t) \cdot K_c \cdot i_c(t)$$

% Torque en dominio de Laplace

$$T_m(s) = (K_a \cdot K_c \cdot I_a) \cdot I_c(s) = K_m \cdot I_c(s)$$

% Torque aplicado a la carga

$$T_c(s) = T_m(s) - T_p(s)$$

## 4.3 Motor DC en corriente de Campo 

% Ecuación diferencial del sistema mecánico

$$J \frac{d^2 \theta}{dt^2} + b \frac{d \theta}{dt} + k \theta = \tau(t)$$

% Función de transferencia en el dominio de Laplace

$$\Theta(s) = T_c(s) \cdot \frac{1}{s^2 J + b s}$$

## 4.4 La conexión de los modelos se realiza de la siguiente
 manera:
 ## 4.41  Torque desarrollado cuando la corriente de campo es constante
 
$$T_m(s) = (K_a \cdot K_c \cdot I_c) \cdot I_a(s) = K_m \cdot I_a(s)$$

## 4.42 Ecuación de voltaje en la armadura del motor DC

$$V_a(s) = (s L_a + R_a) \cdot I_a(s) + V_b(s)$$

## 4.43 Relación de torque con la carga

$$T_c(s) = T_m(s) - T_p(s)$$

## 4.44 Ecuación de movimiento (parte mecánica del sistema)

$$\Theta(s) = T_c(s) \cdot \frac{1}{s^2 J + b s}$$

Finalmente tenemos el modelo resultante del diagrama de Bloques.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/6f90e0eb1235facb7bbc7f61b98839452576609f/Build/Diagramam%20de%20bloques%202.png" width="300">
</div>

## 5.1 Engranajes y Poleas

🔑 Definición
Los engranes y las bandas que están sobre una polea son dispositivos mecánicos que transmiten energía desde una parte del sistema a otra, en una forma tal que se alteran la
fuerza, el par, la velocidad y el desplazamiento angular. La Figura 5.11 ilustra dos engranes acoplados; la inercia y la fricción de los engranes se despreciarán momentáneamente en
el caso ideal considerado. 

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/b220c165e3830a4b013264ba09b3d88f14d25879/Build/Engranajes%20y%20Poleasd.png" width="300">
</div>

💡## 5.22 Ejemplo 

Perfecto,vamos a construir un ejemplo a partir del sistema que aparece en tu imagen.Este representa un sistema mecánico rotacional con:

	Un resorte de torsión k
 
	Un disco con momento de inercia J
 
	Un amortiguador rotacional b
 
vamos a relacionatr la entra de la pocision angular con su respectiva salida:

$$ \theta_i(t) \quad \text{(Entrada angular)} $$

$$ \theta_o(t) \quad \text{(Salida angular)} $$

 
Ahora, vamos a llevar este sistema a una aplicación con engranajes y poleas para un ejemplo más completo.

## 🧮 Ecuaciones del sistema (ecuación de movimiento rotacional):

Sumatoria de torques en el eje de salida (despreciando fricción en los engranajes):

$$\[J \frac{d^2\theta_o(t)}{dt^2} + b \frac{d\theta_o(t)}{dt} + k \theta_o(t) = T_{\text{equiv}}(t)\]$$

$$\[T_{\text{equiv}}(t) = \left( \frac{N_1}{N_2} \right) T_{\text{input}}(t)\]$$

$$[\Rightarrow J \frac{d^2\theta_o(t)}{dt^2} + b \frac{d\theta_o(t)}{dt} + k \theta_o(t) = \left( \frac{N_1}{N_2} \right)^2 T_i(t)\]$$

## Transformada de Laplace

$$\[J s^2 \Theta_o(s) + b s \Theta_o(s) + k \Theta_o(s) = \left( \frac{N_1}{N_2} \right)^2 T_i(s)\]$$

##  Función de Transferencia

$$\[\Theta_o(s) = \frac{ \left( \frac{N_1}{N_2} \right)^2 K }{J s^2 + b s + k} \Theta_i(s)\]$$

\Rightarrow \boxed{
$$[G(s) = \frac{\Theta_o(s)}{\Theta_i(s)} = \frac{K \left( \frac{N_1}{N_2} \right)^2}{J s^2 + b s + k}]$$


# 5.21 Ecuaciones de los Torques y desplazamientos Angulares

Relaciones entre los torques τ₁ y τ₂, los desplazamientos angulares θ₁ y θ₂, y los números de dientes N₁ y N₂ de los engranes son:

### Relaciones entre los torques \( \tau_1 \) y \( \tau_2 \), los desplazamientos angulares \( \theta_1 \) y \( \theta_2 \), y los números de dientes \( N_1 \) y \( N_2 \) de los engranes son:

$$[\frac{\tau_2}{\tau_1} = \frac{N_2}{N_1}, \quad \frac{N_2}{N_1} = -\frac{\theta_1}{\theta_2}]$$

---

### Así, las ecuaciones del primario y secundario son, respectivamente:

$$[\frac{\tau_2}{\tau_1} = \frac{N_2}{N_1}\]$$

$$[\frac{N_2}{N_1} = -\frac{\theta_1}{\theta_2}\]$$

Así, las ecuaciones del primario y secundario son, respectivamente:

$$[J_1 \frac{d^2 \theta_1}{dt^2} + \beta_1 \frac{d \theta_1}{dt} + \tau_1 = \tau]$$

$$[J_2 \frac{d^2 \theta_2}{dt^2} + \beta_2 \frac{d \theta_2}{dt} + \tau_2 = 0]$$

De acuerdo con las ecuaciones (3.51), \(\tau_2\) se escribe en términos de \(\tau_1\), y \(\theta_2\) en función de \(\theta_1\):

$$[\tau_2 = \tau_1 \frac{N_2}{N_1}\]$$

$$[\theta_2 = -\theta_1 \frac{N_1}{N_2}\]$$

## Engranajes y Poleas

• J y 𝐾𝑚 Cambian si se tiene en cuenta el efecto de los engranajes o poleas.

$$[J_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d^2\theta_1}{dt^2} + \beta_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d\theta_1}{dt} = \tau_1]$$

$$\left[J_1 + \left(\frac{N_1}{N_2}\right)^2 J_2\right] \frac{d^2\theta_1}{dt^2} + \left[\beta_1 + \left(\frac{N_1}{N_2}\right)^2 \beta_2\right] \frac{d\theta_1}{dt} = \tau]$$

$$[\Theta(s) = V_c(s) \frac{K_m}{(sL_c + R_c)(Js^2 + bs)} - T_p(s) \frac{1}{(Js^2 + bs)}]$$

Ecuación de la primera imagen (Soderberg criterion)
$$[J_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d^2\theta_1}{dt^2} + \beta_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d\theta_1}{dt} = \tau_1]$$

Ecuación simplificada o combinada de la primera imagen

$$[\therefore \left[J_1 + \left(\frac{N_1}{N_2}\right)^2 J_2\right] \frac{d^2\theta_1}{dt^2} + \left[\beta_1 + \left(\frac{N_1}{N_2}\right)^2 \beta_2\right] \frac{d\theta_1}{dt} = \tau]$$

Ecuación izquierda de la segunda imagen

$$[\Theta(s) = V_c(s) \frac{K_m}{(sL_c + R_c)(Js^2 + bs)} - T_p(s) \frac{1}{(Js^2 + bs)}]$$

% Ecuación derecha de la segunda imagen (Two dimensional Taylor Series)

$$[\frac{\Theta(s)}{V_c(s)} = \frac{K_m}{(sL_c + R_c)(Js^2 + bs)}]$$

 Ecuación principal de la tercera imagen 

$$[\left[J_1+\left(\frac{N_1}{N_2}\right)^2 J_2\right] \frac{d^2\theta_1}{dt^2}+\left[\beta_1+\left(\frac{N_1}{N_2}\right)^2 \beta_2\right] \frac{d\theta_1}{dt}=\tau]$$

 Ecuación bajo

"a) Masa despreciable de los engranes" 
$$[\therefore \left(\frac{N_1}{N_2}\right)^2 \left(J \frac{d^2}{dt^2}+\beta \frac{d}{dt}\right)\theta_1 = \tau]$$

 Ecuación bajo "
 b) Masa no despreciable de los engranes" 
 
$$[\left[J_{N1}+\left(\frac{N_1}{N_2}\right)^2 (J+J_{N2})\right] \frac{d^2\theta_1}{dt^2}+\left(\frac{N_1}{N_2}\right)^2 \beta=\tau]$$

% Definición de beta_equiv de la cuarta imagen
$$[\beta_{equiv} = \left(\frac{N_1}{N_2}\right)^2 \beta]$$

 Definición de J_equiv de la cuarta imagen
$$[J_{equiv} = \left[J_{N1}+\left(\frac{N_1}{N_2}\right)^2 (J+J_{N2})\right]$$

 Función de transferencia G(s) de la cuarta imagen
$$[G(s) = \frac{\Theta(s)}{T(s)} = \frac{1}{s(J_{equiv}s + \beta_{equiv})}]$$

## 5.4 Palancas
🔑 Definición
Una palanca es un segmento rígido que posee un punto de apoyo fijo alrededor del cual puede realizar la rotación cuando se aplica sobre ella una fuerza externa o interna. La longitud de la palanca entre el punto de apoyo y el punto de aplicación de la resistencia se llama brazo de resistencia, y la longitud entre el punto de apoyo y el punto de aplicación de la fuerza se llama brazo de fuerza.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/5c2627ae172d67eb6371f38edb7c6b64c3060126/Build/Sistemas%20de%20Palancas.png" width="300">
</div>

## 5.5 Potenciometros 

🔑 Definición
es un elemento que queda descrito por una ecuación diferencial de orden cero, esto es, por medio de una relaciónalgebraica, en donde el voltaje de salida Vo es proporcional al  desplazamiento del cursor del potenciómetro, el cual puede ser de rotación

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/5e9a949c2656850d0f1689cb1e691b8299698828/Build/Poternciometro.png" width="300">
</div>

El comportamiento de rotacion del potenciometro esta definido con la siguiente ecuacion:

$$[V_o = \frac{\theta}{\theta_{\text{máx}}} V_c]$$

## 5.6 Tacometros

Son dispositivos que convierten la velocidad angular a voltaje.

$$[v(t) = k \frac{d\theta(t)}{dt}]$$

$$[G(s) = \frac{V(s)}{\Theta(s)} = ks]$$

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/91d9bced9952f7e97672ac51f3ed6b66d3fe055b/Build/tacometros.png" width="300">
</div>

## 6 Ecuaciones mas generales de todos los sistmeas Complejos 

#6.1 Selenoide

$$
F(s) = \frac{K_s}{(m s^2 + b s + k)} \cdot I(s)
$$

- \( F(s) \): fuerza generada  
- \( I(s) \): corriente aplicada  
- \( m \): masa móvil  
- \( b \): fricción viscosa  
- \( k \): constante de resorte  
- \( K_s \): constante del solenoide
  
# 6.2  Motor DC
$$
G(s) = \frac{\Omega(s)}{V(s)} = \frac{K_t}{(L s + R)(J s + b) + K_t K_b}
$$

- \( \Omega(s) \): velocidad angular  
- \( V(s) \): voltaje aplicado  
- \( L \): inductancia  
- \( R \): resistencia  
- \( J \): inercia  
- \( b \): fricción  
- \( K_t \): constante de torque  
- \( K_b \): constante de fem

# 6.3 Sistema de Poleas y Engranajes

$$
G(s) = \frac{\Theta_o(s)}{\Theta_i(s)} = \frac{K \left( \frac{N_1}{N_2} \right)^2}{J s^2 + b s + k}
$$

- \( \Theta_o(s), \Theta_i(s) \): ángulos de salida y entrada  
- \( N_1:N_2 \): relación de engranajes  
- \( J \): inercia equivalente  
- \( b \): amortiguamiento  
- \( k \): resorte de torsión  
- \( K \): constante del actuador (si aplica)

# 6.4 Tacometro

$$
V_{taco}(s) = K_t \cdot \Omega(s)
\quad \Rightarrow \quad G(s) = \frac{V_{taco}(s)}{\Omega(s)} = K_t
$$

- \( V_{taco} \): voltaje de salida del tacómetro  
- \( \Omega(s) \): velocidad angular  
- \( K_t \): constante del tacómetro

# 6.5 Potenciometros

$$
V_o(s) = K_p \cdot \Theta(s)
\quad \Rightarrow \quad G(s) = \frac{V_o(s)}{\Theta(s)} = K_p
$$

- \( V_o \): salida de voltaje  
- \( \Theta(s) \): posición angular  
- \( K_p \): constante del potenciómetro


## 7. Tablas
| **Sistema**           | **Ecuación Representativa**                                                             | **Función de Transferencia** $G(s)$                                     | **Descripción**                                                        |
| --------------------- | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Selenoide**         | $F = k \cdot i^2$ o modelo LR: $V = L\frac{di}{dt} + Ri$                                | $G(s) = \frac{I(s)}{V(s)} = \frac{1}{Ls + R}$                           | Actúa como actuador lineal, convierte corriente en fuerza lineal.      |
| **Motor DC**          | $V = L\frac{di}{dt} + Ri + K_b\omega$, $T = K_t i$, $J\frac{d\omega}{dt} + b\omega = T$ | $G(s) = \frac{\Omega(s)}{V(s)} = \frac{K_t}{(Js + b)(Ls + R) + K_tK_b}$ | Convierte voltaje en velocidad angular.                                |
| **Placa calefactora** | $C \frac{dT}{dt} = P - h(T - T_{amb})$                                                  | $G(s) = \frac{T(s)}{P(s)} = \frac{1}{Cs + h}$                           | Sistema térmico, donde la temperatura responde a la potencia aplicada. |
| **Tacómetro**         | $V_{out} = K_t \cdot \omega$                                                            | $G(s) = \frac{V_{out}(s)}{\Omega(s)} = K_t$                             | Transforma velocidad angular en voltaje.                               |
| **Potenciómetro**     | $V_{out} = V_{in} \cdot \frac{R_{ajustado}}{R_{total}}$                                 | $G(s) = \frac{V_{out}(s)}{V_{in}(s)} = \text{constante}$                | Dispositivo pasivo que divide voltaje.                                 |

## 6.1Descripcion de las Varuables de la Tabla
s es la variable de Laplace.
L: inductancia, 
R: resistencia.
𝐾𝑡: constante de torque, 
𝐾𝑏: Constante de Amortiguacion.
​J : constante de fuerza contraelectromotriz.
J: momento de inercia, 
b: fricción viscosa.
C: capacidad térmica, 
h: coeficiente de pérdida de calor.

## 📚 7.1 Ejercicios

Obtenga el circuito equivalente y la función de transferencia resultante para el sistema mostrado en la i gura 3.27, para lo que hay que considerar:

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/bf0193abca6a1efd1e495e4e7835cd119cd2dc6e/Build/ejercicio%20sistema%20de%20bandas%20y%20poleas.png" width="300">
</div>

a) Masa despreciable de los engranes.

b) Halle la Funcion de Transferencia del Sistema.

# Solución

## a) Modelo del sistema (masa de engranajes despreciable)

Usando la analogía mecánica-rotacional, se representa el sistema mediante elementos de:

- Inercia rotacional: $\( J \)$
- Fricción viscosa: $\( b \)$
- Torque aplicado: $\( T \)$
- Relación de engranajes: $\( \frac{N_2}{N_1} \)$

La inercia equivalente 
>>
>>
$\( J_{\text{eq}} \)$ y la  **fricción equivalente**  $\( b_{\text{eq}} \)$ vistas desde el eje del engranaje de entrada, se ajustan usando la relación:
>>
>>
$$\[J_{\text{eq}} = J_{\text{salida}} \left( \frac{N_1}{N_2} \right)^2\]$$
>>
>>
$$\[b_{\text{eq}} = b_{\text{salida}} \left( \frac{N_1}{N_2} \right)^2\]$$
>>
>>
## b) Función de Transferencia

La función de transferencia del sistema en el dominio de Laplace es:

$$\[G(s) = \frac{\Theta_{\text{salida}}(s)}{T_{\text{entrada}}(s)} = \frac{1}{J_{\text{eq}} s^2 + b_{\text{eq}} s}\]$$

Donde:
$\( \Theta_{\text{salida}}(s) \)$ es el desplazamiento angular de salida
$ \( T_{\text{entrada}}(s) \)$ es el torque de entrada
$\( s \)$ es la variable de Laplace

Esta función representa un sistema de segundo orden sin constante de rigidez (sin muelle).

# 📚 Ejercicio 7.2  
Los engranes y las bandas que están sobre una polea son dispositivos mecánicos que transmiten energía desde una parte del sistema a otra, en una forma tal que se alteran la
fuerza, el par, la velocidad y el desplazamiento angular. La Figura 5.11 ilustra dos engranes acoplados; la inercia y la fricción de los engranes se despreciarán momentáneamente en
el caso ideal considerado. 

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/b220c165e3830a4b013264ba09b3d88f14d25879/Build/Engranajes%20y%20Poleasd.png" width="300">
</div>

#Relaciones entre los torques τ₁ y τ₂, los desplazamientos angulares θ₁ y θ₂, y los números de dientes N₁ y N₂ de los engranes son:

### Relaciones entre los torques \( \tau_1 \) y \( \tau_2 \), los desplazamientos angulares \( \theta_1 \) y \( \theta_2 \), y los números de dientes \( N_1 \) y \( N_2 \) de los engranes son:

$$[\frac{\tau_2}{\tau_1} = \frac{N_2}{N_1}, \quad \frac{N_2}{N_1} = -\frac{\theta_1}{\theta_2}]$$

---

### Así, las ecuaciones del primario y secundario son, respectivamente:

$$[\frac{\tau_2}{\tau_1} = \frac{N_2}{N_1}\]$$

$$[\frac{N_2}{N_1} = -\frac{\theta_1}{\theta_2}\]$$

Así, las ecuaciones del primario y secundario son, respectivamente:

$$[J_1 \frac{d^2 \theta_1}{dt^2} + \beta_1 \frac{d \theta_1}{dt} + \tau_1 = \tau]$$

$$[J_2 \frac{d^2 \theta_2}{dt^2} + \beta_2 \frac{d \theta_2}{dt} + \tau_2 = 0]$$

De acuerdo con las ecuaciones (3.51), \(\tau_2\) se escribe en términos de \(\tau_1\), y \(\theta_2\) en función de \(\theta_1\):

$$[\tau_2 = \tau_1 \frac{N_2}{N_1}\]$$

$$[\theta_2 = -\theta_1 \frac{N_1}{N_2}\]$$

## Engranajes y Poleas

• J y 𝐾𝑚 Cambian si se tiene en cuenta el efecto de los engranajes o poleas.

$$[J_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d^2\theta_1}{dt^2} + \beta_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d\theta_1}{dt} = \tau_1]$$

$$\left[J_1 + \left(\frac{N_1}{N_2}\right)^2 J_2\right] \frac{d^2\theta_1}{dt^2} + \left[\beta_1 + \left(\frac{N_1}{N_2}\right)^2 \beta_2\right] \frac{d\theta_1}{dt} = \tau]$$

$$[\Theta(s) = V_c(s) \frac{K_m}{(sL_c + R_c)(Js^2 + bs)} - T_p(s) \frac{1}{(Js^2 + bs)}]$$

Ecuación de la primera imagen (Soderberg criterion)
$$[J_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d^2\theta_1}{dt^2} + \beta_2 \left(\frac{N_1}{N_2}\right)^2 \frac{d\theta_1}{dt} = \tau_1]$$

Ecuación simplificada o combinada de la primera imagen

$$[\therefore \left[J_1 + \left(\frac{N_1}{N_2}\right)^2 J_2\right] \frac{d^2\theta_1}{dt^2} + \left[\beta_1 + \left(\frac{N_1}{N_2}\right)^2 \beta_2\right] \frac{d\theta_1}{dt} = \tau]$$

Ecuación izquierda de la segunda imagen

$$[\Theta(s) = V_c(s) \frac{K_m}{(sL_c + R_c)(Js^2 + bs)} - T_p(s) \frac{1}{(Js^2 + bs)}]$$

% Ecuación derecha de la segunda imagen (Two dimensional Taylor Series)

$$[\frac{\Theta(s)}{V_c(s)} = \frac{K_m}{(sL_c + R_c)(Js^2 + bs)}]$$

 Ecuación principal de la tercera imagen 

$$[\left[J_1+\left(\frac{N_1}{N_2}\right)^2 J_2\right] \frac{d^2\theta_1}{dt^2}+\left[\beta_1+\left(\frac{N_1}{N_2}\right)^2 \beta_2\right] \frac{d\theta_1}{dt}=\tau]$$

 Ecuación bajo

"a) Masa despreciable de los engranes" 
$$[\therefore \left(\frac{N_1}{N_2}\right)^2 \left(J \frac{d^2}{dt^2}+\beta \frac{d}{dt}\right)\theta_1 = \tau]$$

 Ecuación bajo "
 b) Masa no despreciable de los engranes" 
 
$$[\left[J_{N1}+\left(\frac{N_1}{N_2}\right)^2 (J+J_{N2})\right] \frac{d^2\theta_1}{dt^2}+\left(\frac{N_1}{N_2}\right)^2 \beta=\tau]$$

% Definición de beta_equiv de la cuarta imagen
$$[\beta_{equiv} = \left(\frac{N_1}{N_2}\right)^2 \beta]$$

 Definición de J_equiv de la cuarta imagen
$$[J_{equiv} = \left[J_{N1}+\left(\frac{N_1}{N_2}\right)^2 (J+J_{N2})\right]$$

 Función de transferencia G(s) de la cuarta imagen
$$[G(s) = \frac{\Theta(s)}{T(s)} = \frac{1}{s(J_{equiv}s + \beta_{equiv})}]$$

## 8. Codigo en Matlab

% Parámetros del sistema

m = 0.5;      % masa [kg]

b = 1.0;      % fricción mecánica [N·s/m]

k = 0;        % constante del resorte [N/m] (0 si no hay)

L = 0.01;     % inductancia de la bobina [H]

R = 2.0;      % resistencia eléctrica [ohm]

K = 5.0;      % constante de fuerza del solenoide [N/A]

Ke = 0.5;     % constante de fuerza contraelectromotriz [V·s/m]

% Variables de estado: x1 = x (posición), x2 = dx/dt (velocidad), x3 = i (corriente)

A = [ 0         1          0;
     -k/m   -b/m      K/m;
      0     -Ke/L   -R/L];

B = [0; 0; 1/L];

C = [1 0 0];  % salida: posición x(t)

D = 0;

% Crear el sistema en espacio de estados

sys = ss(A, B, C, D);

% Simular respuesta a escalón de voltaje de entrada
t = 0:0.01:5;        % tiempo de simulación
step(sys, t);
title('Respuesta del sistema solenoide-masa a entrada escalón de voltaje');
xlabel('Tiempo (s)');
ylabel('Desplazamiento x(t)');
grid on;

Vamos a mostrar la grafica del comportamiento del sistema.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/5709eaeb9ce4d894787fe74e8276981026d1ff36/Build/respuesta%20Escalonda%20al%20sistema%20.png">
</div>

## 9. Conslusiones

9.1 Aprendimos que El modelamiento de sistemas como solenoides, motores DC, engranajes y poleas permite representar fenómenos mecánicos, eléctricos y electromecánicos bajo un mismo marco matemático utilizando funciones de transferencia. Esto facilita el análisis, diseño y control de sistemas complejos mediante herramientas de la teoría de sistemas lineales.

9.2 Analizando la grafica, pudimos observar que La simulación de la respuesta del sistema solenoide-masa ante una entrada escalón muestra una curva suavemente creciente, lo que indica un comportamiento de segundo orden subamortiguado o críticamente amortiguado. Este tipo de respuesta refleja que el sistema responde de forma estable pero con una velocidad limitada por la fricción mecánica y el efecto de la contraelectromotriz. A medida que el tiempo avanza, la posición tiende a un valor constante, demostrando que el sistema alcanza un estado estacionario sin oscilaciones, ideal para aplicaciones que requieren precisión y estabilidad.

## 10. Referencias



