# Robot-LED-Eyes

## intoduction 
When we say what the robot is, the simplest definition of the robot is half of him human and half of him is machine, which means simulate the organs of the human into the machine.
In this project we will simulate the human’s eyes into the machine to be called “Robot eyes”, There are too many methods to simulate the robot’s eyes, one of them is using LEDs, that what we did in the project.

##Components
*	9V Battery
*	7805 Voltage Regulator
* 2x Capacitor
*	Arduino UNO
*	BJT 
*	2x LEDs


## Principle of work

## The 7805 Voltage Regulator

In order to feed the circuit, the 9V Battery is used, which is connected to the capacitor to reduce the noise and improve the DC Signal.
Now the voltage that the LEDs need is 5V, and the voltage of battery is 9V, so how can we reduce the voltage to be 5V?
In this case the 7805 Voltage Regulator is used, which responsible of reduce and regulate the voltage from the value of input voltage to 5V.
The 7805 Voltage Regulator has three pins, which are in, ground and out, which are connected as:
* In >> input side (9V Battery) 
* Ground >> Ground
* Out >> output side (LEDs)


## PWM
In order to reduce the voltage that feeding LEDs, we have used PWM technique. PWM (Pulse Width Modulation) is technique that reduce the average voltage by changing the percentage of the period of ‘ON’ over the full period in one cycle, this percentage is called “Duty Cycle”.
In this project, we have programmed the arduino to make the duty cycle 50% in order to reduce the voltage to the half of the value of voltage using BJT (Bipolar Junction Transistor) electronic switch. 
The BJT has three pins, which are collector, base and emitter and it’s connected with the circuit as:
* Collector >> voltage regulator side.
* Base >> digital output of the arduino pin 5.
* Emitter >> LEDs side.


## LEDs
LED (Light Emitting Diode) is semiconductor the emit the light when the forward current is passing through it. It has two terminals, which are Anode (+ terminal) and Cathode (- terminal) .
Because the robot has 2 eyes, the number of LEDs must be at least 2, but the question is “what is the type of the connection between two LEDs? Is it series or parallel and why?”
The answer is series, for several reasons, one of them is saving the power consumption by reducing the total current of the circuit.
