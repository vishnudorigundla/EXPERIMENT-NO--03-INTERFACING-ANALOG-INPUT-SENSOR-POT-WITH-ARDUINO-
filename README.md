# EXPERIMENT-NO--03-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-




# **AIM**:  

To interface a Analog  input (angular displacement sensor POT) and scale the values up on change in the input.


# **COMPONENTS REQUIRED:**
1.	10 KΩPOT
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	LED of choice 



# **THEORY**: 

## **Analog signals:**

Analog signals – directly measurable quantities in terms of some other quantity.
## Examples:
1. Thermometer – mercury height rises as temperature rises
2. Car Speedometer – Needle moves farther right as you accelerate
3. Stereo – Volume increases as you turn the knob
Reason for conversion of analog to digital quantity is that as the controller or any microprocessor works with digital signals in the form of 0 and 1s, in order to make the signal compatible  most of the analog signals are converted into its equivalent digital level signals using an analog to digital converter .
Quantizing - breaking down analog value is a set of finite states
Encoding - assigning a digital word or number to each state and matching it to the input signal
 There are two ways to best improve accuracy of A/D conversion:
Increasing the resolution which improves the accuracy in measuring the amplitude of the analog signal.
Increasing the sampling rate which increases the maximum frequency that can be measured.
General specifications of analog sensor
	1. Range
	2. Accuracy
	3.Linearity
	4.Compatiblity
	5. signal conversion capability

# **Potentiometer**:
A potentiometer, informally a pot, is a three-terminal resistor with a sliding or rotating contact that forms an adjustable voltage divider. If only two terminals are used, one end and the wiper, it acts as a variable resistor or rheostat.
Potentiometers are commonly used to control electrical devices such as volume controls on audio equipment. Potentiometers operated by a mechanism can be used as position transducers, for example, in a joystick. Potentiometers are rarely used to directly control significant power (more than a watt), since the power dissipated in the potentiometer would be comparable to the power in the controlled load
CIRCUIT DIAGRAM




## FIGURE -01:

![image](https://user-images.githubusercontent.com/36288975/163530788-eec3cdc3-95e8-4d2d-8349-6d0ea4c9439c.png)




# **PROCEDURE:**

1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 



# **PROGRAM** :
```
Developed By: Vishnu vardhan reddy
Reference Number : 212221230023

int potPin=A5;
int ledPin= 2;

void setup()
{
  pinMode (potPin, INPUT);
  pinMode (ledPin, OUTPUT);
  Serial.begin(9600);
}
void loop()
{
  int PotMeasure = analogRead(A5);
  
 if (PotMeasure >=450)
 {
   digitalWrite (2, HIGH);
 }
  else
    digitalWrite(2, LOW);
}
```
 
# Simulation output:


![1](https://user-images.githubusercontent.com/94175324/165758345-3ac901e0-a341-4ab6-a980-7d31f252df07.png)






# RESULT: 

Arduino uno analog input functioning is learned and interfaced with digital input switch by using tinkercad software.



