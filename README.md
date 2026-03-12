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
TL555: Actúa como el controlador central que gestiona los tiempos de carga y descarga··
Condensador (100UF): Funciona como un depósito de energía que se llena y vacía para marcar el ritmo del tiempo··
Resistencias (1KU,14KU,220KU): Controlan la velocidad con la que fluye la corriente hacia el condensador, determinando así la duración de la onda··
Regulador LM7805: Asegura que el circuito reciba un voltaje constante de 5V desde la batería de 9V, protegiendo los componentes.

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
