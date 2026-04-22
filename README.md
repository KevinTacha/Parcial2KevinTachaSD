# Parcial-2-KevinTacha-SD

---

### Parcial Teorico - Practico segundo Corte

---
#LINK DE ESTE REPOSITORIO:


---
FUNDACION UNIVERSITARIA COMPENSAR

Estudiante: 

-Kevin Alejandro Tacha Herrera

Profesor: Diego Alejandro Barragan Vargas

---

### PARTE CONCEPTUAL
# ¿Cual es la diferencia entre latch y un flip flop?, ademas ¿cuales son los diferentes tipos de latch y flip flops?, explique por favor las caracteristicas.

La diferencia clave es que un latch cambia de estado inmediatamente según sus entradas (es asíncrono), mientras que un flip-flop solo cambia cuando recibe un pulso de reloj (es síncrono). Ambos son circuitos biestables usados para almacenar un bit de información, pero su control y aplicaciones varían

Tipos de Latches
Latch S-R (Set-Reset)

Dos entradas: S (set) y R (reset).

Permite establecer la salida en 1 o 0.

Problema: condición indeterminada cuando S=R=1.

Latch D (Data o Delay)

Una entrada de datos D y una de habilitación.

La salida sigue a D mientras la habilitación está activa.

Elimina la condición indeterminada del S-R

Tipos de Flip-Flops
Flip-Flop S-R

Similar al latch S-R, pero controlado por reloj.

También presenta la condición indeterminada si S=R=1.

Flip-Flop D (Data)

La salida Q toma el valor de la entrada D en el flanco del reloj.

Es el más usado en registros y memorias.

Flip-Flop J-K

Versión mejorada del S-R.

Si J=K=1, la salida conmuta (toggle) en cada pulso de reloj.

Muy versátil, usado en contadores.

Flip-Flop T (Toggle)

Conmuta la salida en cada pulso de reloj.

Útil para divisores de frecuencia y contadores binarios

Características importantes de los flip-flops
Retardo de propagación: tiempo que tarda la salida en reflejar el cambio de entrada.

Setup time: tiempo mínimo que la entrada debe estar estable antes del pulso de reloj.

Hold time: tiempo mínimo que la entrada debe mantenerse estable después del pulso.

Frecuencia máxima de operación: límite de velocidad de trabajo.


<p align="center">
<img src="imagenes/img1.png" width="500">
</p>



# ¿Cual es la diferencia entre un multiplexor y un demultioplexor?. Desarrollar la explicacion de un multiplexor 8 entradas y un demultiplexor de 8 salidas.

Diferencia principal
Multiplexor (MUX): Selecciona una sola salida entre varias entradas de datos, según las líneas de selección.

Demultiplexor (DEMUX): Toma una sola entrada y la distribuye hacia una de varias salidas, también controlado por líneas de selección.

En otras palabras:

El MUX es como un “switch de entrada” → muchas entradas, una salida.

El DEMUX es como un “switch de salida” → una entrada, muchas salidas.

Multiplexor de 8 entradas (8:1 MUX)
Entradas de datos: 8 (D0, D1, …, D7).

Líneas de selección: 3 (S0, S1, S2), porque 
2
3
=
8
.

Salida: 1 (Y).

Funcionamiento:

Según el valor binario de las líneas de selección, se conecta una de las 8 entradas a la salida.

Ejemplo: si S2S1S0 = 101 (binario de 5), la salida Y será igual a D5.

Aplicaciones: transmisión de datos, selección de señales, reducción de hardware.

Demultiplexor de 8 salidas (1:8 DEMUX)
Entrada de datos: 1 (D).

Líneas de selección: 3 (S0, S1, S2).

Salidas: 8 (Y0, Y1, …, Y7).

Funcionamiento:

Según el valor binario de las líneas de selección, la entrada se dirige a una de las 8 salidas.

Ejemplo: si S2S1S0 = 011 (binario de 3), la salida Y3 recibirá el valor de D, mientras las demás estarán en 0.

Aplicaciones: distribución de datos, direccionamiento de memoria, control de periféricos.


<p align="center">
<img src="imagenes/img2.png" width="500">
</p>


# Explicar de forma sencilla que es un sumador completo, un sumador medio y circuitos secuenciales.

Sumador medio (Half Adder)
Es un circuito que suma dos bits (A y B).

Produce dos salidas:

Suma (S): resultado de A ⊕ B (XOR).

Carry (C): acarreo, resultado de A · B (AND).

Limitación: no puede sumar un acarreo previo, solo dos bits simples.

 Ejemplo:

A=1, B=1 → S=0, C=1.

Sumador completo (Full Adder)
Es un circuito que suma tres bits: A, B y un acarreo de entrada (Cin).

Produce dos salidas:

Suma (S): resultado de A ⊕ B ⊕ Cin.

Carry (Cout): acarreo de salida, que se genera si al menos dos de las entradas son 1.

Se construye combinando dos sumadores medios.

 Ejemplo:

 Circuitos secuenciales
Son circuitos digitales cuya salida depende no solo de las entradas actuales, sino también del historial previo (estado).

Se diferencian de los circuitos combinacionales, que dependen únicamente de las entradas presentes.

Usan elementos de memoria como latches y flip-flops para guardar estados.

Tipos principales:

Secuenciales síncronos: controlados por un reloj (ejemplo: registros, contadores).

Secuenciales asíncronos: cambian de estado inmediatamente según las entradas, sin reloj.

Ejemplos de aplicación:

Máquinas de estados finitos (FSM).

Controladores de tráfico.

Registros de memoria.

Contadores binarios.

A=1, B=1, Cin=1 → S=1, Cout=1.

<p align="center">
<img src="imagenes/img3.png" width="500">
</p>


# ¿Que es un mapa de Karnaugh? y para que sirve?

¿Qué es un mapa de Karnaugh?
Es una representación bidimensional de una tabla de verdad.

Organiza las combinaciones de variables en una cuadrícula especial (basada en el código Gray).

Cada celda representa una combinación de entradas y se llena con el valor de salida (0 o 1).

Fue desarrollado en los años 50 por Maurice Karnaugh en Bell Labs para facilitar la minimización de funciones booleanas.

¿Para qué sirve?
Simplificación de expresiones booleanas: reduce ecuaciones complejas a su forma mínima.

Optimización de circuitos lógicos: permite usar menos compuertas y componentes.

Diseño eficiente de hardware digital: circuitos más pequeños, rápidos y económicos.

Visualización clara: evita cálculos algebraicos largos y facilita encontrar patrones.

¿Para qué sirve?
Simplificación de expresiones booleanas: reduce ecuaciones complejas a su forma mínima.

Optimización de circuitos lógicos: permite usar menos compuertas y componentes.

Diseño eficiente de hardware digital: circuitos más pequeños, rápidos y económicos.

Visualización clara: evita cálculos algebraicos largos y facilita encontrar patrones.


<p align="center">
<img src="imagenes/img4.png" width="500">
</p>


---

### PARTE DE DISEÑO






