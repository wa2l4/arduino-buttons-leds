# Arduino Button & LED Project

## Project Overview
This project controls three LEDs using three buttons. When a button is pressed, the corresponding LED turns on. It's a simple setup using an Arduino and basic components.

## Code Explanation
- Three input pins are used for the buttons: pins 8, 9, and 10.
- Three output pins are used for the LEDs: pins 3, 4, and 5.
- In the `loop()` function:
  - If a button is pressed (reads LOW), its LED turns ON.
  - If the button is not pressed (reads HIGH), the LED turns OFF.

## Arduino Code

```cpp
void setup() {
  pinMode(8, INPUT);
  pinMode(9, INPUT);
  pinMode(10, INPUT);

  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
}

void loop() {
  int redbutton = digitalRead(8);
  int greenbutton = digitalRead(9);
  int yellowbutton = digitalRead(10);

  if (redbutton == LOW) {
    digitalWrite(3, HIGH);
  } else {
    digitalWrite(3, LOW);
  }

  if (greenbutton == LOW) {
    digitalWrite(4, HIGH);
  } else {
    digitalWrite(4, LOW);
  }

  if (yellowbutton == LOW) {
    digitalWrite(5, HIGH);
  } else {
    digitalWrite(5, LOW);
  }
}
