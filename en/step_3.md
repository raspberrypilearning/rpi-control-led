## Blink an LED

You can use a `while True` loop to make the LED blink on and off.

![An LED and resistor connected from GPIO 17 to GND on the Raspberry Pi](images/led-gpio17.png)


--- task ---

Add a loop and an extra `sleep` to your code. Make sure that the commands to turn the LED on and off are indented by 4 spaces, beneath the loop.

--- /task ---

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 6-10
---
from gpiozero import LED
from time import sleep

red = LED(17)

while True:
    red.on()
    sleep(1)
    red.off()
    sleep(1)
--- /code ---

--- task ---

Save the file and run the code with by clicking on **Run**. Your LED should keep blinking until you click on **stop**

--- /task ---

`while True` loops run until you quit the program. You might want your LED to blink while other things are happening. gpiozero has the `blink` method to make this easy.

--- task ---

Remove the `while True` loop, and replace it with the `blink` method.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 6
---
from gpiozero import LED
from time import sleep

red = LED(17)

red.blink()
--- /code ---

--- /task ---

You can control the how often and how many times the LED blinks.

--- task ---

Use the numbers below, for the time the LED is on, off, and the number of times it blinks. then experiment with different numbers.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 
line_highlights: 6
---
from gpiozero import LED
from time import sleep

red = LED(17)

red.blink(0.2, 0.2, 50)
--- /code ---

--- /task ---