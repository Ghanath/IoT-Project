# Lie Detector using Arduino

## Description
This project is a lie detector built using Arduino. It is designed to measure different physiological responses and represent them in real-time using an Arduino graph.

## Team Members
- Guna Shree (20191CSE0177)
- Ghanath V (20191CSE0167)
- Goutham V (20191CSE0173)
- G Lokesh (20191CSE0168)
- Eranna Raju C (20191CSE0140)

## Under the Guidance of
Prof. Riyazulla Rahman J, Assistant Professor-G1, Department of Computer Science and Engineering, School of Engineering, Presidency University, Bengaluru.

## Components Used
- Arduino Uno
- Breadboard
- LED
- Resistor
- Jumper wires

## Circuit Diagram
![Pinout Diagram](https://github.com/Ghanath/IoT-Project/assets/93461665/28110ca5-9af7-405a-8380-a4588f87961c)


## Code

<pre><code>
void setup() { 
  Serial.begin(9600); 
  pinMode(2, OUTPUT); 
  pinMode(3, OUTPUT); 
  pinMode(4, OUTPUT); 
  digitalWrite(2, HIGH); 
  delay(500); 
  digitalWrite(3, HIGH); 
  delay(500); 
  digitalWrite(4, HIGH); 
  delay(500); 
}

void loop() { 
  if (analogRead(A0) > 30) { 
    digitalWrite(4, HIGH); 
  } else { 
    digitalWrite(4, LOW); 
  } 
  if (analogRead(A0) > 15) { 
    digitalWrite(3, HIGH); 
  } else { 
    digitalWrite(3, LOW); 
  } 
  if (analogRead(A0) > 25) { 
    digitalWrite(2, HIGH); 
  } else { 
    digitalWrite(2, LOW); 
  } 
  Serial.println(analogRead(A0)); 
  delay(20); 
}
    </code></pre>



## Acknowledgements
Special thanks to our guide Prof. Riyazulla Rahman J and Dr. C. Kalairasan for their support and guidance in this project.
