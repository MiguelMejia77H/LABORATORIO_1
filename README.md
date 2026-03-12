# LABORATORIO_1
Explicacion primer Laboratorio de Sistemas Digitales
# INTRODUCCION

En el presente trabajo se desarrolla el análisis y diseño de diferentes circuitos electrónicos utilizando componentes básicos y compuertas lógicas digitales. Como punto de partida se implementa un circuito generador de señal de onda cuadrada basado en el circuito integrado TL555 configurado en modo astable. Esta configuración permite que el circuito oscile continuamente entre un estado alto y uno bajo sin necesidad de una señal externa, lo que produce el encendido y apagado periódico de un LED.

El funcionamiento del circuito depende principalmente de la interacción entre resistencias, un condensador y el temporizador TL555, los cuales determinan los tiempos de carga y descarga que controlan la frecuencia de la señal generada. Además, se emplea un regulador de voltaje LM7805 para garantizar una alimentación estable de 5V, asegurando así el correcto funcionamiento y la protección de los componentes electrónicos.

Adicionalmente, el proyecto incluye el estudio y la implementación de diferentes compuertas lógicas fundamentales como AND, OR, NOT, NAND, NOR y XOR. Cada una de estas compuertas se analiza a partir de su función booleana y su respectiva tabla de verdad, permitiendo comprender cómo se procesan las señales de entrada para producir una salida específica representada mediante el encendido o apagado de un LED.

De esta manera, el trabajo integra conceptos de electrónica analógica y lógica digital, permitiendo comprender tanto el comportamiento de los circuitos temporizadores como el funcionamiento de las operaciones lógicas utilizadas en los sistemas digitales.

# Detalle del circuito TL555

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/0333936a-0582-48e5-8e2c-14533e273e93" /> <img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/0951b5ad-6c76-4e62-8548-36e731f3f02c" />

El circuito que se ha creado es un generador de señales de onda cuadrada, el cual se fundamenta en el circuito integrado TL555 y está configurado en modo astable. En esta configuración, el chip no presenta un estado estable, lo cual implica que oscila de manera continua entre un nivel bajo y uno alto sin requerir una intervención externa, provocando de este modo que el LED parpadee.

# Los componentes clave cumplen las siguientes funciones:
1. TL555: Actúa como el controlador central que gestiona los tiempos de carga y descarga··
2. Condensador (100UF): Funciona como un depósito de energía que se llena y vacía para marcar el ritmo del tiempo··
3. Resistencias (1KU,14KU,220KU): Controlan la velocidad con la que fluye la corriente hacia el condensador, determinando así la duración de la onda··
4. Regulador LM7805: Asegura que el circuito reciba un voltaje constante de 5V desde la batería de 9V, protegiendo los componentes.

# Paso a paso para el Cálculo de Componentes
La fórmula matemática determina la frecuencia y el tiempo del 555 astable. 
La ecuación a continuación se utiliza para calcular el periodo completo (T) de la señal de salida:
        T = T_alto + T_bajo
 En la que la ecuación simplificada es: 
T = 0.693 * (R1 + 2 * R2) * C

# Cálculo de la Resistencia 2 
Despejamos la fórmula para hallar el valor necesario para completar los 2 segundos:
Para obtener un periodo (T) de 2 segundos, despejamos R2 de la fórmula principal
        Sustitución de valores: 2 = 0.693 * (1000 + 2 * R2) * 0.0001
Despeje de la constante de tiempo: 2 / (0.693 * 0.0001) = 1000 + 2 * R2 28860 = 1000 2       * R2
Aislamiento de R2: 28860 - 1000 = 2 * R2 27860 = 2 * R2 R2 = 13930 Ohms = 13.93 kOhm
se requiere una resistencia R2 de aproximadamente 14 kOhm.


 # Descripción del Funcionamiento 
1.	Inicio de Carga: Al conectar la batería, la corriente pasa por R_1 y R_2 para cargar el condensador. En este momento, la Pata 3 entrega energía y el LED se enciende.
2.	Umbral Superior: Cuando el condensador se llena (llega a 2/3 del voltaje), la Pata 6 lo detecta y le dice al chip que cambie de estado.
3.	Descarga: El chip apaga la Pata 3 (el LED se apaga) y abre la Pata 7 para que el condensador se vacíe a través de R_2.
4.	Reinicio: Cuando el condensador se vacía hasta 1/3, la Pata 2 lo detecta y reinicia el proceso, creando la onda cuadrada infinita.

# Compuertas Logicas

## Compuerta AND 

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/6f11cd6c-3edf-4c50-81f0-e7728a096c4d" />

## Ficha técnica y esquema
1. Pines 1 y 2: Entradas de la primera puerta AND.
2. Pin 3: Salida de la primera puerta AND.
3. Pin 7: GND (Tierra/Negativo).
4. Pin 14: VCC (5V/Positivo).
5. En el circuito:
6. Las entradas (pines 1 y 2) están conectadas a los interruptores 1 y 2.
7. La salida (pin 3) está conectada al ánodo del LED a través de una resistencia.
   
## Función Booleana
La puerta AND tiene la siguiente lógica matemática: la salida será 1 (encendido) solo si ambas entradas son 1 (encendido).
La función es:

Y = A * B

Donde A y B son las entradas y Y es la salida.

<img width="813" height="420" alt="image" src="https://github.com/user-attachments/assets/af44107e-45b5-4fec-a6d2-138e29b2f522" />

## Compuerta OR

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/1b27f230-adbc-4e75-b4b8-6bc80c0b6228" />

## Ficha técnica y esquema
1. Pines 1 y 2: Entradas de la primera puerta OR.
2. Pin 3: Salida de la primera puerta OR.
3. Pin 7: GND (Tierra).
4. Pin 14: VCC (5V).
las entradas están conectadas a los interruptores 1 y 2, y la salida (pin 3) controla el LED, igual que en el ejemplo anterior.

## Función Booleana
La puerta OR funciona bajo el principio de "cualquiera de las dos". La salida es 1 (encendido) si al menos una de las entradas es 1.
La función es:
Y = A + B

Tabla

<img width="750" height="380" alt="image" src="https://github.com/user-attachments/assets/594f107f-f952-4b01-9ed4-75ac746afda4" />


## Compuerta NOT

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/9970b853-d729-412d-8e2d-43589d73b294" />

## Ficha técnica y esquema

El funcionamiento es el que invierte la señal de entrada.
1. Pin 1: Entrada de la primera puerta.
2. Pin 2: Salida de la primera puerta.
3. Pin 7: GND (Tierra).
4. Pin 14: VCC (5V).
Se conectado el interruptor 1 a la entrada (pin 1) y el LED a la salida (pin 2).

## Función Booleana
La lógica es simplemente la negación de la entrada:

Y = A

Tabla 

<img width="750" height="380" alt="image" src="https://github.com/user-attachments/assets/5ab28ef0-9944-48da-ac72-15dfa4602780" />

## Compuerta NAND

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/f7e24fd5-470b-48ed-a987-719231ef3390" />

## Ficha técnica y esquema
1. Pines 1 y 2: Entradas de la primera puerta NAND.
2. Pin 3: Salida de la primera puerta NAND.
3. Pin 7: GND (Tierra).
4. Pin 14: VCC (5V).
   
los interruptores 1 y 2 conectados a las entradas (pines 1 y 2) y el LED conectado a la salida (pin 3).

## Función Booleana
La puerta NAND es esencialmente una puerta AND cuya salida ha sido invertida. Por lo tanto, la salida será 0 (apagado) solamente cuando ambas entradas sean 1. En cualquier otro caso, la salida será 1.
La función es:
Y = A * B

Tabla

<img width="750" height="380" alt="image" src="https://github.com/user-attachments/assets/90956f6c-0b76-4d21-8978-a25b3ca7b4af" />

# Compuerta NOR 

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/f0ccf89c-87ea-4351-91bf-e42e4f13ffa0" />


## Ficha técnica y esquema
1. Pin 1: Salida.
2. Pines 2 y 3: Entradas.
3. Pin 7: GND (Tierra).
4. Pin 14: VCC (5V).
   
el cableado respeta esta configuración: los interruptores van a los pines 2 y 3, y el LED está conectado al pin 1.

## Función Booleana
La puerta NOR es el inverso de la puerta OR. La salida será 1 (encendido) solo cuando ambas entradas sean 0. Si cualquiera de las entradas es 1, la salida será 0.

La función es:

<img width="185" height="49" alt="image" src="https://github.com/user-attachments/assets/e80dbd3d-835c-49a9-9be9-cfba2338094c" />

Tabla

<img width="750" height="380" alt="image" src="https://github.com/user-attachments/assets/05eded0c-b170-4dc0-a369-5a0c8e38a764" />


# Compuerta XOR

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/174fc584-475e-4524-b43b-c3a1217bcebf" />

## Ficha técnica y esquema
1. Pines 1 y 2: Entradas de la primera puerta XOR.
2. Pin 3: Salida de la primera puerta XOR.
3. Pin 7: GND (Tierra).
4. Pin 14: VCC (5V).
los interruptores 1 y 2 están conectados a las entradas (pines 1 y 2), y la salida (pin 3) va hacia el LED.
## Función Booleana
La puerta XOR su salida es 1 (encendido) solo cuando las entradas son diferentes entre sí. Si ambas entradas son iguales (ambas 0 o ambas 1), la salida será 0.
La función es:

Y = A B


Tabla 
<img width="806" height="376" alt="image" src="https://github.com/user-attachments/assets/568c7bcb-37dc-4129-93bd-22bd871f78ca" />

















