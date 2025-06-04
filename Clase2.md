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

Aqui vamos a presentarlas ecuaciones diferenciales, mas generales del sistema:

### Ecuaciones diferenciales y función de transferencia

#### Ecuación diferencial del sistema masa-resorte-amortiguador:

$$\[m \frac{d^2x}{dt^2} + b \frac{dx}{dt} + kx = f(t)\]$$

#### Transformada de Laplace y función de transferencia:

$$\[X(s) = F(s) \cdot \frac{1}{ms^2 + bs + k}\]$$

#3.2 Representacion de los Diagramas de Bloques
Aqui se puede representar de manera grafica, el sistema complejo, con su respectiva entrada y salida.



