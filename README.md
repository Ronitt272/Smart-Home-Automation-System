# Smart-Home-Automation-System
- Designed a Smart Home Automation System to automate the lights and fans present in a house. It works in such a way that the lights are turned “ON”, when it is dark, and the fan is turned “ON” when it is hot.
- Designed the system on Proteus.

- The system comprised of two circuits: 
1. Automatic Temperature Controlled Motor. 
2. Automatic Light Controller.

- The Automatic Temperature Controlled Motor circuit was designed with the help of an Op-Amp (LM-741) and a Negative Temperature Coefficient (NTC) Thermistor. 
- The circuit works in a way that when it is hot, the transistor in series to the output of the Op-Amp gets switched “ON”, and thus the motor/fan gets turned “ON”. 

- The Automatic Light Controller was designed with the help of a 555 Timer IC (NE555) and a Light Dependent Resistor (LDR). 
- The circuit works in a way that when the torch is turned “OFF”, or when it is dim, the voltage across the LDR would fall, thus providing a trigger to the 555 Timer IC with the help of a Voltage Divider circuit.
So the 555 Timer IC activates the transistor connected in series to it, and thus the Lights also get turned “ON”. 
- This circuit utilises the ability of a 555 Timer IC to generate pulses and perform Pulse Width Modulation (PWM).

# AUTOMATIC TEMPERATURE CONTROLLED FAN CIRCUIT

# Circuit Diagram 

![image](https://user-images.githubusercontent.com/68660836/227026403-364f4b34-a2c2-42b1-b6ba-feb6e838bcd4.png)

# Components of the Circuit

- LM-741 Op-Amp IC 
-	Negative Temperature Coefficient (NTC) Thermistor
-	Resistances
-	Variable Resistor 
-	Transistor 
-	DC Motor (Fan)
-	Supply Voltage  

# Working 

-	The Automatic Temperature Control circuit as shown comprises of the Fan connected at the Output side of the Transistor Q1. The thermistor RT1 works in such a way that when the temperature increases, it’s resistance decreases. So, as we can see, the Non-Inverting input of the Op-Amp (pin 3) is connected to the potentiometer (Variable Resistance), which helps to agenerate a variable voltage. The Voltages are shown as V+ and V- (pin 1 and pin 5) are the VCC and -VEE respectively, to provide appropriate biasing. 

-	The Inverting Input of the Op-Amp (pin 2) is connected between the Fixed Resistor R2 and the NTC Thermistor RT1 to form a voltage divider circuit. When the temperature is low and it is cold, the resistance offered by the thermistor RT1 is very high and thus the value of the Inverting Input of the Op-Amp (V2) is very high and the Output Voltage of the Op-Amp (pin 6), given by:  
V0 = A*(Non-Inverting Input Voltage – Inverting Input Voltage) = A*(V3 - V2),                   
Where, A= Open Loop Gain of the Op-Amp.

-	Thus, we can see that because RT1 is high, V2 is high, and so the output voltage reduced. Due to this, very little current (almost negligible) flows through the output terminals of the Op-Amp, and thus the transistor Q1 remains in OFF condition.

-	As the temperature increases and it gets hot, the resistance offered by the Thermistor RT1 decreases and the Voltage V2 also reduces. Thus, the output voltage offered by the Op-Amp increases and so the current flowing through the base of the transistor Q1 increases and it gets switched ON. Now because the transistor Q1 is ON, the fan attached to the output of the Transistor gets turned ON.

# AUTOMATIC LIGHT CONTROLLER USING 555 TIMER IC



