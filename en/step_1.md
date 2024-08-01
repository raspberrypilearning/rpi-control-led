## Connect and test an LED

It is always a good idea to test that your circuit is working, before you write any code. You can test your circuit using a 3V3 and GND pins on the Raspberry Pi.

If you put too much current through an LED they may burn out or even explode. To stop this you should use a resistor in series with an LED.

The resistor can be anything between 47Ω and 330Ω. 

The lower the resistance, the brighter the LED will be.

--- task ---

Connect the long leg of an LED to the Raspberry Pi's 3V3 pin and the short leg to a GND pin. The resistor can go either side of the LED. In the diagram it is attached to the long leg of the LED.

![An LED and resistor connected from 3V3 to GND on the Raspberry Pi](images/led-3v3.png)

--- /task ---

The LED should light up. It will always be on, because it's connected to a 3V3 pin.

--- task ---

Now move it from 3V3 to GPIO pin 17:

![An LED and resistor connected from GPIO 17 to GND on the Raspberry Pi](images/led-gpio17.png)

The LED should now turn off, but now it's on a GPIO pin.

--- /task ---


