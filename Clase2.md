# Nombre: Kevin Nicolas Perez Tobar
# Curso: M6A
# Dinamica de Sistemas
# Clase 2: 
 
## 1. Introducción
El modelamiento de sistemas complejos en ingeniería implica representar matemáticamente componentes físicos interconectados, tales como solenoides, motores de corriente directa (DC), transmisiones por engranajes y sistemas de poleas. Estos elementos presentan dinámicas particulares que deben integrarse en un modelo global para predecir el comportamiento del sistema completo. Una estrategia consiste en obtener la función de transferencia individual de cada componente, lo cual permite analizar y diseñar el sistema en bloques. Otra alternativa es utilizar modelos ya estandarizados y validados, que facilitan la construcción de sistemas más complejos con mayor eficiencia. Sin embargo, ambos enfoques enfrentan retos debido a la variabilidad de procesos y dispositivos involucrados.

## 2. Resumen
El modelamiento de sistemas complejos que incluyen solenoides, motores DC, engranajes y poleas puede abordarse mediante la obtención de funciones de transferencia individuales o usando modelos ya existentes. Estos enfoques permiten construir modelos precisos para representar sistemas dinámicos, aunque su aplicación depende del tipo de dispositivo y proceso implicado.

## 3. Deficiones

3.1 Selenoide: 

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

#3.2 Representacion de los Diagramas de Bloques

Aqui se puede representar de manera grafica, el sistema complejo, con su respectiva entrada y salida.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/774438ef0825d4d0f775a8e946da5430f5de821f/Build/Representacion%20de%20Diagramas%20de%20Bloques%20%20.png" width="300">
</div>
Figra 3.2  Representacion grafica del Diagrama de Bloques

## Motor DC 
Un motor de CD es un dispositivo formado por un circuito eléctrico y un sistema mecánico de rotación. Su i nalidad es la de proporcionar torque a una carga. En esta sección se considerarán dos versiones del motor de CD: aquél controlado por corriente de campo y el correspondiente controlado por corriente de armadura. Además, se incluirá una entrada adicional a la entrada de referencia, esto es, una entrada de perturbación,que equivale a una entrada no deseada, pero inevitable, y se analizará su efecto sobre el sistema. 

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/f65138c0c4cd4ce0228a9b00b143234f770be813/Build/Sistema%20Motor%20DC.png" width="300">
</div>

Figura 3.2 Motor DC, controlado por corriente de campo

Este sistema electromecanico esta formado por tres etapas que son:
3.21 La primera etapa cuesta de un circuito RL, donde viene la etapa de transducción y posteriormente la carga acoplada al rotor del motor (RL)

## 4. Ecuaciones 

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

Los engranes y las bandas que están sobre una polea son dispositivos mecánicos que transmiten energía desde una parte del sistema a otra, en una forma tal que se alteran la
fuerza, el par, la velocidad y el desplazamiento angular. La Figura 5.11 ilustra dos engranes acoplados; la inercia y la fricción de los engranes se despreciarán momentáneamente en
el caso ideal considerado. 

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/b220c165e3830a4b013264ba09b3d88f14d25879/Build/Engranajes%20y%20Poleasd.png" width="300">
</div>

# 5.2 Ecuaciones de los Torques y desplazamientos Angulares

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

## 📚 5.3 Ejercicios

# 📚 Ejercicio 1 
Obtenga el circuito equivalente y la función de transferencia resultante para el sistema mostrado en la i gura 3.27, para lo que hay que considerar:

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/aea59a5a1a56e6acce047e5bb64c1a60748536b2/Build/Ejercicio%20de%20Engranajes%20y%20Poleas%202%20.png" width="300">
</div>

a) Masa despreciable de los engranes.
b) Halle la Funcion de Transferencia del Sistema.

Solución 

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





