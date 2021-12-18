# Kerala-IoT-Challenge

> Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.
# About Me
> Hi everyone! I’m Nouman N, 4'th year Electronics and Communication student from Eranad Knowledge City Technical Campus, Manjeri. I also a Diploma holder in Electronics. I’m here to explore new dimensions of the IoT world.And I also interested in Cyber Security

# Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.

> Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram

![1634898879183](https://user-images.githubusercontent.com/91405741/138440483-6eeb5475-4946-42e7-9f6b-3860c91efa42.jpg)

![5h7X9_3102_1627394356](https://user-images.githubusercontent.com/91405741/137279765-8a82a34f-1dc0-4afc-9bd3-a31d7f62c428.png)

## Code

```

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}

```

## Output

> The LED is blinked with a time interval od 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137283496-04e4fe43-bc6a-4ca5-a6e0-0f7ecdcd56c5.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

![1634898905963](https://user-images.githubusercontent.com/91405741/138440549-c4c958ec-0893-4e80-8aba-3a43cafe865e.jpg)

![yiU1x_3102_1627566759](https://user-images.githubusercontent.com/91405741/137288387-e85f8db9-ae97-49d0-888d-a2fc15e4c496.png)

## Code

```

int redled =10; // initialize digital pin 10.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds
digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137290512-e479c4b3-1810-4b72-966f-42348620b1f4.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

![1634898830010](https://user-images.githubusercontent.com/91405741/138440641-844673fc-0cc9-4e67-bf8c-f1dd30d7a970.jpg)

![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/91405741/137292096-feb60c91-1a9a-474b-a596-300285f7b011.png)

## Code

```

int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137293394-f7b99c4d-4659-44fc-87ca-d331f3b6ebaf.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 4: Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams

![1634898715966](https://user-images.githubusercontent.com/91405741/138440748-60c27803-19c4-42f1-a4ec-cc198598bae8.jpg)

![Ztk6E_3102_1628160172](https://user-images.githubusercontent.com/91405741/137344162-7149dfcf-836c-43ec-a01c-177d48958d12.png)

![wQGca_3102_1628160139](https://user-images.githubusercontent.com/91405741/137344321-3e662dee-cb00-421d-a34d-848c2ffd1a6f.png)

## Code

```

int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137346113-b41f1d56-84b5-4437-9d7a-3f11ab84991a.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

![BBr05_3102_1628160460](https://user-images.githubusercontent.com/91405741/137346830-1fa2408c-2a1d-4fdf-a049-5736aeb803ec.png)

![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/91405741/137346912-0f871dbf-8e86-4734-a337-fceeff454e33.png)

## Code

```

int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```

## Output

> The Buzzer makes beep sound.

![1634194968124](https://user-images.githubusercontent.com/91405741/137345459-3ad2e1ac-b091-40fd-bf7b-1bcccf29baec.jpg)


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

![1634898744599](https://user-images.githubusercontent.com/91405741/138440808-226f31cb-dfc3-487c-ba4f-a81c1cede5a0.jpg)

![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/91405741/137347719-6966c0b1-021d-471c-b0a7-48d0441752d0.png)

![A8a40_3102_1628160631](https://user-images.githubusercontent.com/91405741/137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72.png)

![TefdI_3102_1628167200](https://user-images.githubusercontent.com/91405741/137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818.png)

## Code

```

int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137348290-42dcbd25-ad12-4c09-b50b-b8edf17e6235.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>


# Experiment 7 - LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

## LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams

![InShot_20211022_104012830](https://user-images.githubusercontent.com/91405741/138399282-80073c77-63f1-423b-81e3-03a16524fca2.jpg)

![schema_Myt5vqqplZ](https://user-images.githubusercontent.com/91405741/138436635-60cb2ec4-091d-4f24-bf96-b0289e06fa00.png)

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

const int ledPin = 13;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}
void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus <= 200) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/138401141-851fe747-dac0-4600-9295-1a02e6ecacf8.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>


# Experiment 8 : Flame Sensor

> An experiment to understand the working of an Flame sensor.

## Flame Sensor

 **Usage**:These types of sensors are used for short range fire detection and can be used to monitor projects or as a safety precaution to cut devices off / on.

 **Range**:I have found this unit is mostly accurate up to about 3 feet.

 **How it works**:The flame sensor is very sensitive to IR wavelength at 760 nm ~ 1100 nm light.

**Analog output (A0)**: Real-time output voltage signal on the thermal resistance.

**Digital output (D0)**: When the temperature reaches a certain threshold, the output high and low signal threshold adjustable via potentiometer.

**Pins:**

* VCC - Positive voltage input: 5v for analog 3.3v for Digital.

* A0 - Analog output

* D0 - Digital output

* GND -  Ground

## Components Required

* Arduino UNO
* Flame Sensor
* LED
* Buzzer
* BreadBoard
* Jumper

## Circuit Diagrams

![1636554036921 1](https://user-images.githubusercontent.com/91405741/141130577-55ec7164-a222-4dac-8e57-ada3298bb18e.jpg)


   ## Code

```

const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;
int redled = 5;
int greenled = 6;
void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(redled, OUTPUT);
  pinMode(greenled, OUTPUT);

  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    digitalWrite(buzzerPin, HIGH);
    digitalWrite(redled, HIGH);
    digitalWrite(greenled, LOW);
  }
  else
  {
    digitalWrite(buzzerPin, LOW);
    digitalWrite(greenled, HIGH);
    digitalWrite(redled, LOW);
  }
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/141132540-37851868-036e-4169-a3cd-c0ab2560c2bc.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>


# Experiment 9 : LM35 Temperature Sensor

> An experiment to understand the working of an LM35 Temperature Sensor.

## LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor. LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing. LM35 temperature sensor can produce different voltage by different temperature When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagrams

![1636557270585 1](https://user-images.githubusercontent.com/91405741/141250276-d178d05c-69d6-45ba-b495-d9a1cf7bd232.jpg)

## Code

```
int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Temperatuture");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(2000);// wait for 2 second
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/141250697-7d83e0f5-8625-4855-9e0e-f9894e31dee3.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>        


# Experiment 10:IR Remote Control Using TSOP

> An experiment to understand the working of IR Remote Control using TSOP.

## Components Required

* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire 
* USB cable*1

## Circuit Diagrams

![Tsop 1](https://user-images.githubusercontent.com/91405741/141268754-70c61b07-123b-4ef2-8568-70e8610e7a98.jpg)

## Code

```

#include <IRremote.h> 
int RECV_PIN = 3;              
int c=0;                      
IRrecv irrecv(RECV_PIN);
decode_results results;
void setup()
{
   pinMode(8, OUTPUT);
   pinMode(9, OUTPUT);
   pinMode(10, OUTPUT);
   pinMode(11, OUTPUT);
   pinMode(12, OUTPUT);

   Serial.begin(9600);
  irrecv.enableIRIn();                     
}
void loop() {
  if (irrecv.decode(&results)) {
    Serial.println(results.value);
    irrecv.resume();                        
  if(results.value==16773645)      //Up                            
  {
             digitalWrite(8,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(8,LOW);
  }
   if(results.value==16763445)  //Down                                     
  {
             digitalWrite(9,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(9,LOW);
  }
    if(results.value==16769565) //left                                       
  {
             digitalWrite(10,HIGH);
  }
  else if(results.value==4294967295) 
  {
             digitalWrite(10,LOW);
  }
    if(results.value==16771605) //right                                       
  {
             digitalWrite(11,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(11,LOW);
  }
    if(results.value==16714485) //ok                                       
  {
             digitalWrite(12,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(12,LOW);
  }
  }
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/141269217-5ec78d6e-1fdf-41b5-a763-49da9c60eebf.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Experiment 11 :Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.

## Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

## Circuit Diagrams

![Pot 1](https://user-images.githubusercontent.com/91405741/141272087-4bd29d71-4a2d-4768-8576-3064f16acce4.jpg)

![Pot1 1](https://user-images.githubusercontent.com/91405741/141272429-4aca8d07-5f73-45af-9478-e1f1ca9a139d.jpg)

## Code

```

int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/141273425-63da8f76-d4bb-4f8e-91fe-65b2828de6bf.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Experiment 12 : 7 Segment Display
        
> An experiment to understand the working of 7 Segment Display.

## Components Required

* Arduino Uno Board*1
* digit LED Segment Display*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wires *several
* USB cable*1

## Circuit Diagrams

![7segment 1](https://user-images.githubusercontent.com/91405741/141274968-2c6c5718-d7a4-4016-ac9f-a068bf684f58.jpg)

![7segmant1 1](https://user-images.githubusercontent.com/91405741/141275127-e639183c-b12f-4cb5-a544-b634ee6aa64f.jpg)

![7segment2 1](https://user-images.githubusercontent.com/91405741/141275211-e0cd2e60-6849-40e4-b569-595440c3d500.jpg)

## Code

```

int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/141275839-72e6ad82-c56f-42b4-9fe0-153f392bea14.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Assignment 1 : Automatic Night Lamp

> An experiment to create automatic night lamp model using LDR and LED.

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Yellow M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire
* USB cable*1

## Circuit Diagrams 

![A1 1](https://user-images.githubusercontent.com/91405741/143880464-6d68d5e8-c112-4d8e-a034-e5c86089f4a7.jpg)

![A2 1](https://user-images.githubusercontent.com/91405741/143880614-69a909d0-73cf-4221-ae95-3aa6ae0a0d22.jpg)

## Code

```

const int ledPin = 13;   //the number of the LED pin
const int ldrPin = A0;  //the number of the LDR pin
void setup() {
  Serial.begin(9600);
  pinMode(ledPin, OUTPUT);  //initialize the LED pin as an output
  pinMode(ldrPin, INPUT);   //initialize the LDR pin as an input
}
void loop() {
  int ldrStatus = analogRead(ldrPin);   //read the status of the LDR value
  //check if the LDR status is <= 300
  //if it is, the LED is HIGH
   if (ldrStatus <=300) {
    digitalWrite(ledPin, HIGH);               //turn LED on
    Serial.println("LDR is DARK, LED is ON");
   }
  else {
    digitalWrite(ledPin, LOW);          //turn LED off
    Serial.println("LDR is Bright, LED is OFF");
  }
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/143884337-146d3a7a-1891-4a6e-9dcc-32cea78e5690.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 

                                                  
# Assignment 2 : Digital Dice  

> An experiment to create a Digital Dice using 6 LEDs and 1 Push Button

## Components Required

* Arduino Uno Board*1
* Breadboard*1
* Breadboard Jumper Wire
* USB cable*1
* LED*6
* Push Button*1
* 1KΩ Resistor*1
* 220Ω Resistor*6

## Circuit Diagrams 

![Dice1 2](https://user-images.githubusercontent.com/91405741/143881394-a2133fc4-d00e-4bc3-84f6-d449c5065521.jpg)

![Dice2 1](https://user-images.githubusercontent.com/91405741/143881492-3f52e6f5-468b-4de2-af3f-cf31e78133e4.jpg)
                                                                               
![Dice3 1](https://user-images.githubusercontent.com/91405741/143881686-362bb59d-6085-40cf-89ef-ac7450c5475a.jpg)
                                                                             
## Code

```

#define DEBUG 0
// 6 consecutive digital pins for the LEDs
int first = 2;
int second = 3;
int third = 4;
int fourth = 5;
int fifth = 6;
int sixth = 7;
// pin for the button switch
int button = 12;
// value to check state of button switch
int pressed = 0;
void setup() {
  // set all LED pins to OUTPUT
  for (int i=first; i<=sixth; i++) {
    pinMode(i, OUTPUT);
  }
  // set buttin pin to INPUT
  pinMode(button, INPUT);

  // initialize random seed by noise from analog pin 0 (should be unconnected)
  randomSeed(analogRead(0));
  // if we're debugging, connect to serial 
  #ifdef DEBUG
    Serial.begin(9600);
  #endif
}
void buildUpTension() {
  // light LEDs from left to right and back to build up tension
  // while waiting for the dice to be thrown
  // left to right
  for (int i=first; i<=sixth; i++) {
    if (i!=first) {
      digitalWrite(i-1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
  // right to left
  for (int i=sixth; i>=first; i--) {
    if (i!=sixth) {
      digitalWrite(i+1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
}

void showNumber(int number) {
  digitalWrite(first, HIGH);
  if (number >= 2) {
    digitalWrite(second, HIGH);
  }
  if (number >= 3) {
    digitalWrite(third, HIGH);    
  }
  if (number >= 4) {
    digitalWrite(fourth, HIGH);    
  }
  if (number >= 5) {
    digitalWrite(fifth, HIGH);    
  }
  if (number == 6) {
    digitalWrite(sixth, HIGH);    
  }
}
int throwDice() {
  // get a random number in the range [1,6]
  int randNumber = random(1,7);
  
  #ifdef DEBUG
    Serial.println(randNumber);
  #endif
  
  return randNumber;
}

void setAllLEDs(int value) {
  for (int i=first; i<=sixth; i++) {
    digitalWrite(i, value);
  }
}
void loop() {
  // if button is pressed - throw the dice
  pressed = digitalRead(button);

  if (pressed == HIGH) {
    // remove previous number
    setAllLEDs(LOW); 
    buildUpTension();
    int thrownNumber = throwDice();
    showNumber(thrownNumber);
  } 
}


```

## Output

![Dice4 1](https://user-images.githubusercontent.com/91405741/143881878-4790f5e5-3a54-42ad-b029-b6b5f070908e.jpg)

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/143882043-b0170f6b-5ee5-40d4-87fe-74c01e46b56d.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 

