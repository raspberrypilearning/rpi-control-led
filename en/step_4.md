## Pulse an LED

**PWM** lets you control the brightness of an LED, by turning it off and on again at an extremely fast rate.

![An LED and resistor connected from GPIO 17 to GND on the Raspberry Pi](images/led-gpio17.png)

--- task ---

Import the `PWMLED` class from gpiozero, and create a new `PWMLED` object.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights:
---
from gpiozero import PWMLED
from time import sleep

red = PWMLED(17)
--- /code ---

--- /task ---

--- task ---

Set the LED to pulse on and off using the `pulse` method.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 6
---
from gpiozero import PWMLED
from time import sleep

red = PWMLED(17)

red.pulse()
--- /code ---

--- /task ---

The default for `pulse` is to brighten and dim for 1 second each, and to pulse forever.

--- task ---

Experiment changing the values used by `pulse`, to change the cycle of pulses and the number of times the LED pulses.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 6
---
from gpiozero import PWMLED
from time import sleep

red = PWMLED(17)

red.pulse(0.5, 2, 50)
--- /code ---

--- /task ---