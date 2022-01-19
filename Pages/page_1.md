# **Kerala IoT Challenge: Level-1**

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

<iframe src="https://drive.google.com/file/d/1YVsUncvJI9P0f6c6wvlKDt7i-_iCFjk-/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int ledPin=13;   // define digital pin 10.

void setup() {
  pinMode(ledPin,OUTPUT); // define pin with LED connected as output.
}

void loop() {
  digitalWrite(ledPin,HIGH);  // set the LED on.
  delay(1000);                // wait for a second.
  digitalWrite(ledPin,LOW);   // set the LED off.
  delay(1000);                // wait for a second.
}

```

## Output

> The LED is blinked with a time interval of 1 second

<iframe src="https://drive.google.com/file/d/1YR6RU18iw2aAohKS4h9SS29SHtqQhAZW/preview" width="640" height="480" allow="autoplay"></iframe>

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

<iframe src="https://drive.google.com/file/d/1YPjiedcHP_Ihokb60dmVCOfKsKlr2Pdq/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int redLED = 13;
int yellowLED = 12;
int greenLED = 11;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(yellowLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
}

void loop() {
  digitalWrite(greenLED, HIGH);
  delay(5000);
  digitalWrite(greenLED, LOW);

  for (int i = 0; i < 3; i++) {
    delay(500);   // wait 5 seconds
    digitalWrite(yellowLED, HIGH);
    delay(500);
    digitalWrite(yellowLED, LOW);
  }
  
  delay(500);
  digitalWrite(redLED, HIGH);
  delay(5000);
  digitalWrite(redLED, LOW);
}
```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe src="https://drive.google.com/file/d/1YFgqY8lRTexVpO8koUJxKSJNxVLtN2fX/preview" width="640" height="480" allow="autoplay"></iframe>

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

<iframe src="https://drive.google.com/file/d/1YFfUFuET5zrI-YSS3oZpTSIR15JlGHYu/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int BASE=8;  // the I/O pin for the first LED
int NUM=6;   // number of LEDs
void setup()
{
   for(int i=BASE;i<BASE+NUM;i++)     //for(i=2;i<8;i++){}
   {
     pinMode(i,OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for(int i=BASE;i<BASE+NUM;i++) 
   {
     digitalWrite(i,LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for(int i=BASE;i<BASE+NUM;i++) 
   {
     digitalWrite(i,HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}

```

## Output

<iframe src="https://drive.google.com/file/d/1YDprMIPLj3FYfdzLNPsVy7Q9H9shbN_5/preview" width="640" height="480" allow="autoplay"></iframe>

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

<iframe src="https://drive.google.com/file/d/1YBq2u9aHjchgyoIVmrtEQ9JwgMKEi-yD/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int pushButtonPin=12;
int ledPin=13;

void setup() {
  pinMode(pushButtonPin,INPUT);
  pinMode(ledPin,OUTPUT);
}

void loop() {
  int value=digitalRead(pushButtonPin);
  if(value==HIGH){
    digitalWrite(ledPin,HIGH);
    }
  else{
    digitalWrite(ledPin,LOW);
    }  
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe src="https://drive.google.com/file/d/1Y6xmlq9p5mUiMQepfQ5wVR2sjCmUo5zQ/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

<iframe src="https://drive.google.com/file/d/1Y5hUJzlOXsBBS9IrZyVCpD6pD6yYNKxb/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int buzzerPin=13;

void setup() {
  pinMode(buzzerPin,OUTPUT);
}

void loop() {
  digitalWrite(buzzerPin,HIGH);
  delay(5000);
  digitalWrite(buzzerPin,LOW);
  delay(2500);
}

```

## Output

> The Buzzer makes beep sound.

<iframe src="https://drive.google.com/file/d/1XyWcYJCwF3h9uvSERSxyQOSdAXWz2ad1/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1XmFxYbZHwWr0tk7OCtgd2zaW8WHxNU2A/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int redLED = 13;
int blueLED = 12;
int greenLED = 11;
int val;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(blueLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  for (val = 255; val > 0; val--)
  {
    analogWrite(greenLED, val);
    analogWrite(redLED, 255 - val);
    analogWrite(blueLED, 128 - val);
    delay(1);
  }
  for (val = 0; val < 255; val++)
  {
    analogWrite(greenLED, val);
    analogWrite(redLED, 255 - val);
    analogWrite(blueLED, 128 - val);
    delay(1);
  }
  Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe src="https://drive.google.com/file/d/1XhEnSxq1HnFSfi0XgshVMlyDbJEyUDXG/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 7 - LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

## LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

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

<iframe src="https://drive.google.com/file/d/1XgzarWqyyPgpXEH_vUUAd0IbH5DmQ7yN/preview" width="640" height="480" allow="autoplay"></iframe>

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

int ledPin=13;
int LDRPin=A0;
int value=0;

void setup() {
  pinMode(ledPin,OUTPUT);
  //pinMode(LDRPin,INPUT);
  Serial.begin(9600);
}

void loop() {
  value=analogRead(A0);
  Serial.println(value);
  if (value>500){
    digitalWrite(ledPin,HIGH);
    }
  else{
    digitalWrite(ledPin,LOW);  
    } 
}

```

## Output

<iframe src="https://drive.google.com/file/d/1XbU6n3e8ePEYpVorswPILWtwlOdOboz3/preview" width="640" height="480" allow="autoplay"></iframe>


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

<iframe src="https://drive.google.com/file/d/1XV9P-HEIYcq4y54LiaqF-ZfLmk4dxsoL/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int buzzer=13;
int flame=A0;
int value=0;

void setup() {
  pinMode(buzzer,OUTPUT);
  pinMode(flame,INPUT);
  Serial.begin(9600);
}

void loop() {
  value=analogRead(flame);
  Serial.println(value);
  if(value>100){
    digitalWrite(buzzer,HIGH);
    }
  else{
    digitalWrite(buzzer,LOW);
    }  
}

```

## Output

<iframe src="https://drive.google.com/file/d/1XNw2h7E_4inXNtW3OI6Y7ZCaCI-crQUM/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 9 : LM35 Temperature Sensor

> An experiment to understand the working of an LM35 Temperature Sensor.

## LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor. LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing. LM35 temperature sensor can produce different voltage by different temperature When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1XGLGuQnwZgHYoAvXQWEVlQhfRwG-phPL/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int potPin = A0; // initialize analog pin 0 for LM35 temperature sensor

void setup()
{
  Serial.begin(9600);// set baud rate at”9600”
}

void loop()
{
  int val;// define variable
  int dat;// define variable
  val = analogRead(0); // read the analog value of the sensor and assign it to val
  dat = (125 * val) >> 8; // temperature calculation formula
  Serial.print("Temp: ");// output and display characters beginning with Tep
  Serial.print(dat);// output and display value of dat
  Serial.println("°C");// display “C” characters
  delay(500);// wait for 0.5 second
}


```

## Output

<iframe src="https://drive.google.com/file/d/1XEVr7nVV2x0Y1JTUncNjKnf-1ymtzXvL/preview" width="640" height="480" allow="autoplay"></iframe>      


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

<iframe src="https://drive.google.com/file/d/1X6yESD9Q4owo2ekZMfBDB7sN1ZmtX2v7/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

#include <IRremote.h>
int RECV_PIN = 13;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
long on1  = 0x40BF30CF;
long off1 = 0x40BF10EF ;
long on2 = 0x40BF18E7;
long off2 = 0x40BF38C7;
long on3 = 0x40BF7A85;
long off3 = 0x40BF5AA5 ;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if ((i%2) == 1) {
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
//  pinMode(LED4, OUTPUT);
//  pinMode(LED5, OUTPUT);
//  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
//       on = !on;
//       digitalWrite(8, on ? HIGH : LOW);
//       digitalWrite(13, on ? HIGH : LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);      
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}

```

## Output

<iframe src="https://drive.google.com/file/d/1X4Ru4CVIit4cqBQSwJ74baSsvEYQwJjd/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 11 :Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.

## Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1WzIM1yM-7C7EoDS_RZOX-fHzLvs9aJUt/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

void setup() {
  pinMode(3, OUTPUT);
  pinMode(A0,INPUT);
  Serial.begin(9600);
}

void loop() {
  int value=analogRead(A0);
  Serial.println(value);
  analogWrite(3, map(value, 0, 1023, 0, 255));
}

```

## Output

<iframe src="https://drive.google.com/file/d/1Wyd-xkjQodtS97wCscYbZQjtODjurNKx/preview" width="640" height="480" allow="autoplay"></iframe>


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

<iframe src="https://drive.google.com/file/d/1WsuGEkjgj_OzIwbZdUDqOqCEVFp0-wWn/preview" width="640" height="480" allow="autoplay"></iframe>

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
}}

```

## Output

<iframe src="https://drive.google.com/file/d/1Wy-FFFSNu96L4qOok_DTdQCoGeKYZQ90/preview" width="640" height="480" allow="autoplay"></iframe>

