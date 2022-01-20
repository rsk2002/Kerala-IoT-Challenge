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

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1ZaT_-s36NgR3Osl2GrQjE962WbmuNPsN/preview" width="640" height="480" allow="autoplay"></iframe>

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

<iframe src="https://drive.google.com/file/d/1ZqP8FFvah6xflJxY1cYhEMh2vdOuBrqr/preview" width="640" height="480" allow="autoplay"></iframe>
