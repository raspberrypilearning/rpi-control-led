## Light an LED

GPIO Zero is a Python library which provides a simple way to use the GPIO pins on the Raspberry Pi.

![An LED and resistor connected from GPIO 17 to GND on the Raspberry Pi](images/led-gpio17.png)

--- task ---

Open Thonny

--- /task ---

[[[thonny-install]]]
[[[thonny-chromebook]]]

--- task ---

Write the following code to use the gpiozero library and set up an LED on pin 17, then turn it on.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 
---
from gpiozero import LED

red = LED(17)

red.on()
--- /code ---

--- /task ---

The above uses the object name `red`, but you can use any name that you like.

--- task ---

Run your code, and your LED should switch on.

--- /task ---

--- task ---

Now you want to switch the LED off again. So add the `time` library to your imports. Then have your program pause for 2 seconds, before turning the LED off again.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 2, 7-8
---
from gpiozero import LED
from time import sleep

red = LED(17)

red.on()
sleep(2)
red.off()
--- /code ---

--- /task ---