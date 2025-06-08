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
