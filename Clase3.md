# Nombre: Kevin Nicolas Perez Tobar
# Curso: M6A
# Dinamica de Sistemas
# Clase 3: Algebra de Bloques

# 1. Introducción al Álgebra de Bloques

En el campo de la Dinámica de Sistemas, el álgebra de bloques es una herramienta fundamental y poderosa para el modelado, análisis y diseño de sistemas complejos, especialmente aquellos que involucran múltiples componentes interconectados. Imagina un sistema como una maquinaria intrincada, donde cada pieza (o proceso) tiene una función específica y se relaciona con otras. El álgebra de bloques nos permite representar estas piezas y sus interconexiones de manera gráfica y matemática, simplificando la comprensión de cómo fluye la información y cómo se propagan las señales a través del sistema.

 # 2. Resumen
 
El álgebra de bloques es una herramienta esencial en la Dinámica de Sistemas para modelar, analizar y diseñar sistemas complejos con componentes interconectados. Representa visualmente las funciones de transferencia de los elementos de un sistema y su combinación, mostrando el flujo de información. Cada bloque es una operación que transforma una señal, y las flechas indican la dirección de la señal. Es fundamental en ingeniería de control y procesamiento de señales para comprender cómo las señales se propagan y cómo interactúan los subsistemas.

# 3. Definciones

# 3.1 Que es un de Diagrama de Bloques.

Los diagramas de bloques son una herramienta gráfica fundamental que facilita la comprensión de la interacción entr múltiples sistemas o componentes. Históricamente, su desarrollo se atribuye a J. Watt, quien comenzó a utilizarlos para explicar el funcionamiento de su primer sistema de control.

# 3.2 Elementos que componen los Diagramas de Bloques

3.21 Bloque: Es un símbolo para representar la operación matemática que sobre la señal de entrada hace el bloque para producir la salida.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/423e243f300ab894b330fba8a3b4b48cd35871bd/Build/bloques.png" width="300">
</div>
# Figura 3.21 Representacion grafica de un bloque

3.22 Flechas: La función principal de una flecha es mostrar el sentido en el que una señal se propaga de un componente a otro. Esto es crucial para entender la causa y efecto dentro del sistema. La señal solo puede ir en la dirección que la flecha indica, nunca en sentido contrario.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/423e243f300ab894b330fba8a3b4b48cd35871bd/Build/bloques.png" width="300">
</div>

3.23 Punto Suma: En el álgebra de bloques, este elemento se encarga de combinar señales, ya sea añadiéndolas o sustrayéndolas. Cada flecha que llega a este punto lleva un signo (+ o −) en su origen, indicando la operación específica que debe realizarse con la señal que transporta (sumar o restar, respectivamente).

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/423e243f300ab894b330fba8a3b4b48cd35871bd/Build/bloques.png" width="300">
</div>

3.24 Ramificación: Un punto de ramificación es aquel a partir del cual la señal de un bloque va de modo concurrente a otros bloques o puntos de suma.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/423e243f300ab894b330fba8a3b4b48cd35871bd/Build/bloques.png" width="300">
</div>

3.25  Interpretacion del Diagrama 
La salida de un bloque funcional corresponde a la señal de entrada (Dominio s) multiplicada por por la función de
transferencia del bloque. 

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/423e243f300ab894b330fba8a3b4b48cd35871bd/Build/bloques.png" width="300">
</div>

# 4. Ejemplos 

💡Ejemplo 4.1 
Vamos a ver como se soluciona los Diagramas de bloques conectados en cascada. 
<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/0526dedb12a3b6472d2e4de0e1c1a433cf88ec94/Build/diagrama%20de%20bloques%20metodo%20de%20casacada%20.png">
</div>

Las ecuaciones que describen este sistema son:

$$Y_1(s) = U_1(s)G_1(s)$$

$$Y_2(s) = Y_1(s)G_2(s)$$

Sustituyendo $Y_1(s)$ en la segunda ecuación, obtenemos:

$$Y_2(s) = (U_1(s)G_1(s))G_2(s)$$

$$Y_2(s) = U_1(s)G_1(s)G_2(s)$$

💡Ejemplo 4.2
Identificar los elementos de Sistema de la figura.

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/293a3b8bd662565c934caa904a7a9d6c70f506b4/Build/ejemplo%204.2.png" width="300">
</div>

Los elementos  que podemos ver en el diagrama de bloques son: 

1) Flechas: que conectan los elementos entre si, y que apuntan a la derecha son positivos y si apuntan a la izquierda son de orientación negativa.
2) Punto de Suma: Aqui podemos que Realiza operaciones (suma o resta) entre señales únicamente.
3) Bloques: aca podemos simbolos de la funcion matematica en este caso tenemos una ganancia de bloque G(S).
4) Ramificaciones: Aqui podemos ver una ramificacion en 

# 5. Aplicación del Diagrama de Bloques 

<div align="center">
<img src="
</div>

