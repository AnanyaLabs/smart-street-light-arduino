# Smart Street Light Using Arduino
## Project Image

(Project image will be added soon.)

## Project Overview

This project demonstrates how an Arduino can automatically switch on a street light when the surrounding environment becomes dark.

The system uses an LDR (Light Dependent Resistor) to detect light intensity. When the light level falls below a predefined value, the Arduino turns on an LED that represents a street light.

## Learning Objectives

* Understand how sensors collect information.
* Learn how Arduino processes sensor input.
* Explore basic automation concepts.
* Build a real-world smart lighting system.

## Components Required

| Component     | Quantity    |
| ------------- | ----------- |
| Arduino UNO   | 1           |
| LDR Sensor    | 1           |
| LED           | 1           |
| 220Ω Resistor | 1           |
| Breadboard    | 1           |
| Jumper Wires  | As Required |

## Working Principle

1. The LDR measures ambient light.
2. Arduino continuously reads the sensor value.
3. When the environment becomes dark, Arduino turns ON the LED.
4. When sufficient light is available, Arduino turns OFF the LED.

## Circuit Connections

* LDR → Analog Pin A0
* LED Positive → Digital Pin 13
* LED Negative → GND
* Arduino powered through USB

## Arduino Code

```cpp
int ldrPin = A0;
int ledPin = 13;
int ldrValue = 0;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  ldrValue = analogRead(ldrPin);

  if (ldrValue < 500) {
    digitalWrite(ledPin, HIGH);
  }
  else {
    digitalWrite(ledPin, LOW);
  }
}
```

## Applications

* Automatic street lighting
* Garden lighting
* Smart homes
* Energy-saving systems

## Future Improvements

* Add solar charging.
* Add IoT monitoring.
* Control multiple street lights.
* Include motion detection.

## Author

AnanyaLabs
