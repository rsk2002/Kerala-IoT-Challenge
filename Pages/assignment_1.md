# **Kerala IoT Challenge: Level-1**

# Assignment 1 : Create an automatic night lamp model using LDR and LED

> Use LDR to make an automatic night lamp, which turns on in the dark

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


# Assignment 2 : Digital Dice

> Create a Digital Dice using 7 Segment Display and Push Button

## Components Required

* Arduino UNO
* 7 Segment display
* Push button
* 10kohm resistor
* BreadBoard
* Jumper wires
* USB cable

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1ZaT_-s36NgR3Osl2GrQjE962WbmuNPsN/preview" width="640" height="480" allow="autoplay"></iframe>

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

pinMode(3, INPUT);
}
void loop()
{
  if (digitalRead(3)==HIGH) {
    switch(random(1, 7)) {
      case 1:
        digital_1();
        break;
      case 2:
        digital_2();
        break;
      case 3:
        digital_3();
        break;
      case 4:
        digital_4();
        break;
      case 5:
        digital_5();
        break;
      case 6:
        digital_6();
        break;
    }
  }
}

```

## Output

<iframe src="https://drive.google.com/file/d/1ZqP8FFvah6xflJxY1cYhEMh2vdOuBrqr/preview" width="640" height="480" allow="autoplay"></iframe>
