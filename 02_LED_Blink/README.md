# Lesson 02 - LED Blink

## Objective

Learn how to control an LED using Arduino and understand the basics of digital output.

---

## Components Required

* Arduino Uno
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires
* USB Cable

---

## Theory

An LED (Light Emitting Diode) is an electronic component that emits light when current flows through it.

In this lesson, Arduino will turn the LED ON and OFF repeatedly.

This process is called blinking.

---

## Circuit Connections

| Arduino Pin | Component                         |
| ----------- | --------------------------------- |
| D13         | LED Positive (+)                  |
| GND         | LED Negative (-) through resistor |

---

## Arduino Code

```cpp
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(1000);

  digitalWrite(13, LOW);
  delay(1000);
}
```

---

## Code Explanation

### pinMode(13, OUTPUT);

Sets pin 13 as an output pin.

### digitalWrite(13, HIGH);

Turns the LED ON.

### delay(1000);

Waits for 1 second.

### digitalWrite(13, LOW);

Turns the LED OFF.

---

## Expected Output

The LED will:

* Turn ON for 1 second
* Turn OFF for 1 second
* Repeat continuously

---

## Challenge Activity

Try changing:

```cpp
delay(1000);
```

to

```cpp
delay(500);
```

Observe what happens.

---

## Homework

1. What is an LED?
2. What is the purpose of pinMode()?
3. What does HIGH mean?
4. What does LOW mean?
5. What happens when delay(500) is used?

---

## Next Lesson

Lesson 03 - Button Input
