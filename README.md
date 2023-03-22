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


