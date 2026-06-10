# Lesson 03 - Button Input

## Objective

Learn how to read input from a push button and control an LED using Arduino.

---

## Components Required

* Arduino Uno
* Push Button
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires

---

## Theory

Until now, Arduino was controlling the LED automatically.

In this lesson, Arduino will wait for user input from a push button.

When the button is pressed:

* LED turns ON

When the button is released:

* LED turns OFF

This introduces the concept of digital input.

---

## Circuit Connections

| Arduino Pin | Component        |
| ----------- | ---------------- |
| D2          | Push Button      |
| D13         | LED Positive (+) |
| GND         | LED Negative (-) |

---

## Arduino Code

```cpp
const int buttonPin = 2;
const int ledPin = 13;

void setup() {
  pinMode(buttonPin, INPUT_PULLUP);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  if (digitalRead(buttonPin) == LOW) {
    digitalWrite(ledPin, HIGH);
  }
  else {
    digitalWrite(ledPin, LOW);
  }
}
```

---

## Code Explanation

### pinMode(buttonPin, INPUT_PULLUP)

Configures the button pin as an input.

### digitalRead(buttonPin)

Reads the current state of the button.

### digitalWrite(ledPin, HIGH)

Turns the LED ON.

### digitalWrite(ledPin, LOW)

Turns the LED OFF.

---

## Expected Output

* Press Button → LED ON
* Release Button → LED OFF

---

## Challenge Activity

Modify the program so that:

* Pressing the button turns the LED ON for 3 seconds.
* Then LED automatically turns OFF.

---

## Homework

1. What is digital input?
2. What is INPUT_PULLUP?
3. What does digitalRead() do?
4. What happens when the button is pressed?
5. What happens when the button is released?

---

## Next Lesson

Lesson 04 - Buzzer
