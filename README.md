# 5_buzzer_kp
Controlling the buzzer upon the number entered
# Controlling the Buzzer Based on Entered Number

## Overview

This project demonstrates how to control a buzzer using an Arduino based on whether a number entered via the Serial Monitor is odd or even. If the entered number is even, the buzzer will turn off. If the entered number is odd, the buzzer will turn on.

## Components

- Arduino board (e.g., Uno, Mega)
- Buzzer
- Breadboard and jumper wires

## Circuit Diagram

1. **Buzzer**
   - Connect the positive terminal of the buzzer to digital pin 2 on the Arduino.
   - Connect the negative terminal of the buzzer to GND on the Arduino.

## Code Explanation

### Variables

- `buzzerPin`: The pin connected to the buzzer (set to digital pin 2).
- `prevState`: A boolean flag to store the previous state of the buzzer.

### Setup

In the `setup()` function:
- The `buzzerPin` is set as an OUTPUT.
- Serial communication is initialized at 9600 baud.
- The buzzer is initialized to the OFF state with `digitalWrite(buzzerPin, LOW)`.
- A message is printed to the Serial Monitor prompting the user to enter a number.

### Loop

In the `loop()` function:
- The buzzer's state is set to the previous state stored in `prevState`.
- The code checks if any data is available in the Serial buffer.
- If data is available, the number is read as a string, trimmed, and printed to the Serial Monitor.
- The string is converted to an integer and checked to determine if it is odd or even.
  - If the number is even, the buzzer is turned off, and a message is printed to the Serial Monitor.
  - If the number is odd, the buzzer is turned on, and a message is printed to the Serial Monitor.
- The `prevState` variable is updated based on the current state of the buzzer.



## Usage Instructions

1. Assemble the circuit as per the circuit diagram.
2. Upload the provided code to the Arduino board.
3. Open the Serial Monitor from the Arduino IDE (Tools -> Serial Monitor) to view status messages.
4. Set the baud rate to 9600 in the Serial Monitor.
5. Enter a number in the Serial Monitor and press Enter.
6. Observe the buzzer turning on for odd numbers and off for even numbers.

## Example Output

- Entering `2` in the Serial Monitor will display:
  ```
  2
  Even number - Buzzer Off
  ```
  The buzzer will remain off.
- Entering `3` in the Serial Monitor will display:
  ```
  3
  Odd number - Buzzer On
  ```
  The buzzer will turn on.

This project demonstrates a simple method for using serial input to control hardware, providing a foundation for more complex interactions and controls with Arduino.

---

