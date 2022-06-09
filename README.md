EXP-02-INTERFACING-DIGITAL-INPUT-SENSOR-WITH-ARDUINO-PUSH-BUTTON
AIM: To interface a digital input (push button) and blink and LED upon activation.

COMPONENTS REQUIRED:

1 KΩ Resistor
Arduino Uno
Bread board
USB Interfacing cable
Jumper wires
LED of choice
THEORY :

Arduino UNO - The Uno is a microcontroller board based on the ATmega328P. It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz quartz crystal, a USB connection, a power jack, an ICSP header and a reset button. It contains everything needed to support the microcontroller; simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started.

Technical specifications of Arduino UNO :

a.Microcontroller ATmega168/328 b.Microcontroller ATmega168/328 c.Operating Voltage 5V d.Input Voltage (recommended) 7-12V e.Input Voltage (limits) 6-20V f.Digital I/O Pins 14 (of which 6 provide PWM output) g.Analog Input Pins 6 h.DC Current per I/O Pin 40 mA i.DC Current for 3.3V Pin 50 mA j.Flash Memory 16 KB (ATmega168) or 32 KB (ATmega328) of which 2 KB used by boot loader k.SRAM 1 KB (ATmega168) or 2 KB (ATmega328) l.EEPROM 512 bytes (ATmega168) or 1 KB (ATmega328) m.Clock Speed 16 MHz

PIN DIAGRAM FOR ATMEGA 328

![image](https://user-images.githubusercontent.com/89122599/172775395-c3532adc-bc5f-4f51-9ed6-7bfab63b7deb.png)


FIGURE-01

![image](https://user-images.githubusercontent.com/89122599/172775603-0bff4bad-18d2-4aed-8e8d-4d122c807999.png)



PROCEDURE:

Open tinker cad account

Select Arduino uno , bread board , digital input and digital output
Connect the circuit as given in the figure
Develop the program and compile it for any errors
.Execute the program
Check the simulation
CIRCUIT DIAGRAM:

![image](https://user-images.githubusercontent.com/89122599/172775737-d0327041-8ae3-407d-b8c2-bde6ec467280.png)


FIGURE -02

![image](https://user-images.githubusercontent.com/89122599/172775258-2dbd7242-896c-4430-a1d0-afda35c7197e.png)


PROGRAM:

const int BUTTON = 2;

const int LED = 8;

int BUTTONstate = 0;

void setup()

{

  pinMode(BUTTON, INPUT);
  
  pinMode(LED, OUTPUT);
  
}

void loop()

{

  BUTTONstate = digitalRead(BUTTON);
  
  if(BUTTONstate == HIGH)
  
  {
  
    digitalWrite(LED, HIGH);
    
  }
  
  else{
  
    digitalWrite(LED, LOW);
    
  }
  
}

Output of the simulation :

![image](https://user-images.githubusercontent.com/89122599/172775819-beaf01c0-bfc6-412a-a9ca-44b90634da56.png)


Result:

Thus, we have interfaced a digital input (push button) and blink of LED upon activation.
