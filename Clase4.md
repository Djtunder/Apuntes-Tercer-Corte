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

Ejemplo 4.2

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/e52af1b8b4e6e29ad89dd75fa03f0bf00b2b9a19/img/ejemplo%202.jpg" width="300">
</div>

## Ejemplo - Diagrama de Flujo con Método de Mason

### Ganancias de Trayectoria Directa

$$\( P_1 = G_1 G_2 G_3 G_4 G_5 \)$$ 
$$\( P_2 = G_1 G_6 G_4 G_5 \)$$
$$\( P_3 = G_1 G_2 G_7 \)$$

---

### Ganancias de Lazo

$$\( L_1 = -G_4 H_1 \)$$
$$\( L_2 = -G_2 G_7 H_2 \)$$ 
$$\( L_3 = -G_6 G_4 G_5 H_2 \)$$  
$$\( L_4 = -G_2 G_3 G_4 G_5 H_2 \)$$

---

### Determinante del Sistema

$$\[\Delta = 1 - (L_1 + L_2 + L_3 + L_4) + L_1 L_2\]$$


### Cofactores

$$\[\Delta_1 = 1, \quad \Delta_2 = 1, \quad \Delta_3 = 1 - L_1\]$$

> Nota: \( L_1 \) no toca la trayectoria \( P_3 \)

---

### Función de Transferencia Total

$$\[\frac{C(s)}{R(s)} = \frac{1}{\Delta} \left( P_1 \Delta_1 + P_2 \Delta_2 + P_3 \Delta_3 \right)\]$$

$$\[\frac{C(s)}{R(s)} = \frac{G_1 G_2 G_3 G_4 G_5 + G_1 G_6 G_4 G_5 + G_1 G_2 G_7 (1 + G_4 H_1)}{\Delta}\]$$

## 6. Tabla: Elementos y Reglas de los Diagramas de Flujo de Señal

| **Elemento**          | **Símbolo / Forma**           | **Descripción**                                                                 |
|-----------------------|-------------------------------|---------------------------------------------------------------------------------|
| **Nodo**              | Punto o círculo               | Representa una señal o variable del sistema.                                   |
| **Rama (arco)**       | Flecha con ganancia (ej: G(s))| Indica la relación funcional entre dos nodos. Multiplica la señal de entrada.  |
| **Fuente de entrada** | Nodo R(s)                     | Señal de entrada al sistema.                                                   |
| **Salida del sistema**| Nodo C(s)                     | Señal de salida del sistema.                                                   |
| **Ganancia**          | Etiqueta sobre la flecha      | Puede ser una constante, G(s), H(s), etc.                                      |
| **Suma de señales**   | Nodo con varias entradas      | Suma algebraica de las señales que llegan.                                     |
| **Retroalimentación** | Flecha que regresa a un nodo  | Representa un lazo de realimentación.                                          |


## 7. Ecuaciones## 📘 Fórmula de Mason para Diagramas de Flujo de Señal

Sea la función de transferencia de un sistema representado por un diagrama de flujo de señal:

$$\[T = \frac{Y(s)}{X(s)} = \frac{\sum_{k=1}^{n} P_k \Delta_k}{\Delta}\]$$

### 📌 Donde:

- \( P_k \): Ganancia de la k-ésima trayectoria directa desde la entrada hasta la salida.
- \( \Delta \): Determinante del sistema (considerando todos los lazos).
- \( \Delta_k \): Determinante del sistema excluyendo los lazos que tocan la trayectoria \( P_k \).

---

### 🔄 Cálculo del determinante \( \Delta \):

$$\[\Delta = 1 - \sum (\text{lazos individuales}) + \sum (\text{productos de dos lazos no tocantes}) - \sum (\text{productos de tres lazos no tocantes}) + \cdots\]$$

### ✅ Pasos para aplicar la fórmula:

1. Identificar todas las trayectorias directas \( P_k \).
2. Identificar todos los lazos del sistema.
3. Calcular \( \Delta \) considerando la interacción de los lazos.
4. Calcular \( \Delta_k \) para cada trayectoria.
5. Sustituir los valores en la fórmula de Mason.

---

### 📌 Ejemplo básico:

Supongamos:
- Una trayectoria directa: \( P_1 = G_1 G_2 \)
- Un lazo: \( L_1 = -H G_2 \)

Entonces:

$$\[\Delta = 1 - (-HG_2) = 1 + HG_2\]$$

$$\[\Delta_1 = 1 \quad \text{(ya que el lazo toca la trayectoria directa)}\]$$

$$\[T = \frac{P_1 \Delta_1}{\Delta} = \frac{G_1 G_2}{1 + H G_2}\]$$

## 8. Ejercicios

Obtener la funcion de transferencia, utilizando la formula de mazon del siguiente ejemplo.
<div aqlign="center">+
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/c8eb7c1cc1183b623f43494cb552ee2d798c02cd/img/ejercicio%203.jpg" width="300">
</div>
### Trayectoria directa

$$\[P_1 = G_1 G_2 G_3\]$$

### Lazos cerrados

$$\[L_1 = -G_1 G_2 H_1\]$$

$$\[L_2 = -G_2 G_3 H_2\]$$

$$\[L_3 = -G_1 G_2 G_3\]$$

### Determinante

$$\[\Delta = 1 - (L_1 + L_2 + L_3)\]$$

$$\[\Delta = 1 + G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3\]$$

### Cofactor

\[\Delta_1 = 1\]

### Función de transferencia

$$\[\frac{C(s)}{R(s)} = \frac{P_1 \Delta_1}{\Delta}\]$$

$$\[\frac{C(s)}{R(s)} = \frac{G_1 G_2 G_3}{1 + G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3}\]$$

Ejercicio 5.2
Obtener la funcion de trasnferecnia de la siguuiente figura usando formula de mazon

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/0c36ccdadf44d29106fe096648101734146d16bc/img/ejercicio%204.jpg" width="300">
</div>

Solucion

### Trayectorias directas

\[P_1 = G_1 G_2 G_3 G_4 G_5\]


### Lazos individuales

\[L_1 = -G_1 G_2 H_1\]

\[L_2 = -G_3 G_4 H_3\]

\[L_3 = H_2\]

---

### Productos de lazos no tocantes

No hay lazos no tocantes entre sí.

---

### Determinante

\[\Delta = 1 - (L_1 + L_2 + L_3)\]

\[\Delta = 1 + G_1 G_2 H_1 + G_3 G_4 H_3 - H_2\]

### Cofactores

Todos los lazos tocan la trayectoria directa, por tanto:

\[\Delta_1 = 1\]

### Función de transferencia

\[\frac{Y(s)}{R(s)} = \frac{P_1 \Delta_1}{\Delta}\]

\[\frac{Y(s)}{R(s)} = \frac{G_1 G_2 G_3 G_4 G_5}{1 + G_1 G_2 H_1 + G_3 G_4 H_3 - H_2}\]

## 9. Codigo

💡Ejemplo 4:

% Aplicación de la fórmula de Mason en un sistema sencillo
% Trayectoria directa: P1 = G1 * G2
% Lazo: L1 = -H * G2

G1 = 2;     % Ganancia del bloque 1
G2 = 3;     % Ganancia del bloque 2
H  = 0.5;   % Ganancia de retroalimentación

P1 = G1 * G2;           % Ganancia de la trayectoria directa
L1 = -H * G2;           % Ganancia del lazo
Delta = 1 - L1;         % Determinante del sistema

T = P1 / Delta;         % Fórmula de Mason

disp(['La función de transferencia es: T = ', num2str(T)]);

# 10. Conclusiones
1. Aprendimos que los diagramas de flujo de señal permiten representar gráficamente las relaciones funcionales entre las variables de un sistema dinámico.
2. Los Diagramas de señal Ayudan a entender cómo fluye la información desde la entrada hasta la salida, especialmente en sistemas con retroalimentación

 
# 11. Referencias
[1] Autor desconocido, Dinámica de sistemas, Jul. 2017. [En línea]. Disponible en: https://dademuchconnection.wordpress.com/wp-content/uploads/2017/07/dinamica_de_sistemas.pdf

 Jorge Cote.(2025). Clase 4: Diagramas de flujo de señal [Diapositivas de clase]. Curso Dinámica de Sistemas, ETITC.





