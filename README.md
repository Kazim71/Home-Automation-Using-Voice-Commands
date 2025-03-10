Voice-Controlled Home Automation System Using Python and Arduino
Project Overview
This project demonstrates how to design a Voice-Controlled Home Automation System using Python on a laptop and an Arduino Uno microcontroller. The system allows users to control home appliances such as LEDs and fans through simple voice commands. Voice recognition is handled using Python's speech_recognition library, and feedback is given through the pyttsx3 text-to-speech engine. Commands are transmitted via a serial connection to the Arduino, which executes the control logic to switch devices on and off.

Hardware Requirements
Arduino Uno Board
USB Cable
Red LED (2 pieces)
Blue LED (2 pieces)
DC Fan (controlled via transistor/mosfet circuit)
Transistor (for fan control)
Resistors (as per LED and transistor requirements)
Breadboard and Jumper Wires
Laptop/PC with Microphone
Software Requirements
Python 3.x
Arduino IDE
pyttsx3 Library (Text-to-Speech in Python)
speech_recognition Library (Speech to Text in Python)
pyserial Library (Communication between Python and Arduino)
Wiring Diagram (Hardware Connection)
Component	Arduino Pin
Red LED 1	Digital Pin 8
Red LED 2	Digital Pin 9
Blue LED 1	Digital Pin 10
Blue LED 2	Digital Pin 11
Fan (via transistor)	Digital Pin 4
GND (Common Ground)	GND
Fan Control Note:
The DC fan is connected to a transistor, which acts as a switch. The base of the transistor is connected to pin 4 through a resistor, while the collector is connected to the fan's negative terminal, and the emitter is grounded. The positive terminal of the fan is connected to the 5V supply (or external power if required).

Working Principle
The project captures voice commands through the microphone using the Python speech_recognition library. The recognized command is processed and then sent over a serial connection to the Arduino Uno. The Arduino parses the received commands and turns on/off LEDs and the fan based on the input.

Supported Voice Commands
"Red on" → Turns on both red LEDs
"Red off" → Turns off both red LEDs
"Blue on" → Turns on both blue LEDs
"Blue off" → Turns off both blue LEDs
"Fan on" → Turns on the fan
"Fan off" → Turns off the fan
"All on" → Turns on all LEDs and fan
"All off" → Turns off all LEDs and fan
"Exit program" (optional) → Stops the program (add this feature in Python)
How to Use
Hardware Setup:
Connect all components to the Arduino Uno as per the wiring table above.

Upload Arduino Code:

Open the Arduino IDE.
Write or paste the Arduino code.
Select the appropriate COM port and board (Arduino Uno).
Upload the code to the Arduino.
Run Python Code:

Install the required Python libraries:
nginx
Copy
Edit
pip install pyttsx3 speechrecognition pyserial
Connect the Arduino via USB to your laptop/PC.
Open and run the Python script in your terminal or IDE.
Speak one of the supported voice commands into the microphone.
Observe the Output:

Devices (LEDs or fan) will respond according to your voice commands.
The Python program provides audio feedback confirming the actions.
