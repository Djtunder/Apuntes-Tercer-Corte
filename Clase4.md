# Nombre: Kevin Nicolas Perez Tobar
# Curso: M6A
# Dinamica de Sistemas
# Clase 4: Diagrmas de Flujo de Señal

## 1. Introducción
En esta clase vimos la representacion de los diagramas de señal, que se utilizan a nivel industrial donde facilitan la compresion del sistema. Por otro lado analizamos las caracterisiticas, ecuaciones, mediante ejercicios que facilitan la compresion del tema. Este método resulta especialmente útil cuando se aplica la fórmula de Mason, diseñada para analizar sistemas con múltiples trayectorias y bucles de retroalimentación.

## 2. Resumen
Los diagramas de flujo de señales permiten representar de forma clara sistemas complejos y facilitan el cálculo de la función de transferencia total. La fórmula de Mason es una herramienta clave en este tipo de análisis, ya que permite resolver sistemas con estructuras complicadas de manera más sencilla.

## 3. Definiciones
3.1 Nodo: Representan las señales de entrada o salida del Sistema.Se representa por medio de un círculo con una etiqueta que indique el nombre de la señal.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/75f830ff974a1ed7a184f5cf5310053ee5d706ee/img/nodos%2011.jpg">
</div>
Figura 3.1 "imagen de Nodos"
3.2 Flecha: Representa la relación entre las variables del sistema

• Se representa por medio de flechas que indicando el sentido de la relación

• La fleche sale de la señal (Nodo) de entrada y llega a la señal
de salida (Nodo).

• Se agrega una etiqueta a la flecha para indicar la función de
transferencia que relaciona la entrada y la salida.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/dc6e984cd414ce1c38dcc6ab0dded379d466ad9a/img/flechas.jpg">
</div>
Figura 3.2 "imagen de Flechas".

3.3 Camino o trayectoria: Camino o trayecto es un recorrido de ramas conectadas en el sentido de las flechas de las ramas.

• Si no se cruza ningún nodo más de una vez, el camino o trayecto es abierto.

• Si el camino o trayecto finaliza en el mismo nodo del cual partió, y no cruza ningún otro más de una vez, es un camino o trayecto cerrado.

## interpretación de Diagramas de bloques de señal.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/7dffd7b0752cf8d16bde70399e434d7c9a1be4aa/img/tabla%20de%20interpretacion%20de%20diagramas%20de%20se%C3%B1al..jpg" width="300">
</div>

3.4 Ganancia de lazo: La ganancia de lazo es el producto de las ganancias de ramas de lazo.

3.5 Trayecto o cmaino directo: Trayecto directo es el camino  o trayecto de un nodo de entrada a un nodo de salida, sin cruzar ningún nodo más de una vez. 

3.6 Lazo: Un lazo es un trayecto o camino cerrado.

## 4. Formula de Mason

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/7c09d6aac0c19f6bfc58b189310fb1f4a4375b51/img/formula%20de%20mason%20.jpg" width="300">
</div>
   
• 𝑃𝑘Ganancia de los caminos directos
• Δ = 1 − (suma ganancias de los lazos) + (suma producto de 2lazos que no se tocan) – (suma producto de 3 lazos que no se tocan)+…
• Δ𝑘 = 1 −(suma ganancias lazos que no toquen la trayectoria 𝑃𝑘)+(suma ganancias 2 lazos que no toquen la trayectoria 𝑃𝑘 y no se toquen entre sí)-(suma ganancias 3 lazos que no toquen
la trayectoria 𝑃𝑘 y no se toquen entre sí)+…

## 5. Ejemplos 
Hallar la función de transferencia del siguiente diagrama señal

Trayectoria directa

$$\( P_1 = 1 \cdot 1 \cdot G_1 \cdot G_2 \cdot G_3 \cdot 1 = G_1 G_2 G_3 \)$$

Lazos cerrados

$$\( L_1 = G_1 G_2 H_1 \)$$

$$\( L_2 = -G_2 G_3 H_2 \)$$

$$\( L_3 = -G_1 G_2 G_3 \)$$

$$\( \Delta = 1 - (L_1 + L_2 + L_3) \)$$

$$\( \Delta = 1 - (G_1 G_2 H_1 - G_2 G_3 H_2 - G_1 G_2 G_3) \)$$

Cofactor asociado a P1
$$\( \Delta_1 = 1 \)$$

Funcion de Transferencia

$$\[\frac{C(s)}{R(s)} = \frac{P_1 \Delta_1}{\Delta} = \frac{G_1 G_2 G_3}{1 - G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3}\]$$

Ejemplo 9.2








