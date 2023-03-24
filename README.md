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

# AUTOMATIC TEMPERATURE CONTROLLED FAN CIRCUIT WITH LM-741 OP-AMP

# Circuit Diagram 

![image](https://user-images.githubusercontent.com/68660836/227035306-1ff063df-8060-4774-91b2-491d5d2a549f.png)


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

# Circuit Diagram

![image](https://user-images.githubusercontent.com/68660836/227035237-eb551e08-3bb5-4bd6-a4da-8010960669bf.png)


# Components of the Circuit

-	Torch
-	Light Dependant Resistor (LDR)
-	NE555 Timer IC
-	Variable Resistor 
-	Q2N2222 Transistor
-	Light Emitting Diode (LED)
-	Voltage Regulator 
-	Resistances

# Working 

The IC7812 shown above is a voltage regulator, and it is responsible for providing a constant DC Voltage supply to the 555 Timer and also to the voltage divider circuit.

The ‘Trigger’ pin of the 555 Timer is connected in between the Variable Resistance (RV1) and the Light Dependent Resistor (LDR), thus forming a voltage divider circuit.

-	CASE-1: WHEN IT IS DIM

When the Torch is “OFF”, i.e. when it is dim, the LDR offers a high resistance, and thus the potential drop across the Resistor, RV1 is small, and since the Non-Inverting Voltage of the comparator 1 is set to VCC/3, by the internal voltage divider present in the 555 Timer, when the value of the potential drop across RV1 is below VCC/3, the output of the comparator is ‘1’, and thus the S pin of the Flip-Flop gets the value of ‘1’, which is then converted to ‘0’ by the Flip-Flop. The output that comes out of the Flip-Flop is ‘0’, which is then converted to 1 by the invertor placed at the Output Stage. So, the 555 Timer output is “HIGH”. 
Now since the output of the 555 Timer is “HIGH”, a large current flows through the Resistance R1 and the base of the Transistor Q, thus switching the transistor “ON”. Since the Transistor Q is switched “ON”, we can see that the Supply Voltage VCC placed above finds a straight path to the ground via the Resistor RV2 and the LED Diode D. Thus, the Diode gets switched “ON”, and Light gets turned “ON”.

-	CASE-2: WHEN IT IS BRIGHT

When the Torch is turned “ON”, i.e. when it is bright, the LDR offers a low resistance, and thus the potential drop across the Resistor RV1 is large, and since the Non-Inverting Voltage of the Comparator 1 is set to VCC/3, when the value of the potential drop across RV1 exceeds VCC/3, the output of the Comparator is ‘0’, so the S pin of the Flip-Flop gets the value of ‘0’, which is then converted to ‘1’ by the Flip-Flop. The output that comes out of the Flip-Flop is ‘1’, which is then converted to ‘0’ by the invertor placed at the Output Stage of the 555 Timer. So, the 555 Timer output is “LOW”. 
Now because the output of the 555 Timer is “LOW”, negligible current flows through the Resistor R1 and the Base of the Transistor Q. Thus, the transistor gets switched “OFF”. Since the transistor is “OFF”, we can see that the no current would flow through the LED Diode D, and thus is gets switched “OFF”.

Thus, we have seen how the torch can help control the Trigger of the 555 Timer, and thus generate Pulse Width Modulated Signals. And so, this circuit can be efficiently used to design an Automatic Light Controller Circuit. 

# Smart Home Automation System

The Smart Home Automation System works as a combination of both Automatic Temperature Controlled Fan Circuit and the Automatic Light Controller Circuit. This is
because the Automatic Temperature Controlled Fan circuit is used to switch the Fans ‘ON’, whenever it is hot, and switch them ‘OFF’ whenever it is cold. Also, the
Automatic Light Controller Circuit will switch the lights ‘ON’, whenever it is dark, and will switch the lights ‘OFF’, when It is bright. Hence, we get an automated
control over the fans and lights present in the Home. 

# Switched 'OFF'

![image](https://user-images.githubusercontent.com/68660836/227035480-64984ae5-b24a-401f-a4b3-08422da030c1.png)

# Switched 'ON'

![image](https://user-images.githubusercontent.com/68660836/227035567-1e1b2229-f0c3-4777-bf49-056311b62a4c.png)




