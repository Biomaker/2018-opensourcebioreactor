# Flow-through photometer and temperature sensor module

This module comprises the development of a flow-through photometer and temperature sensor unit for the determination of culture density and temperature.

### Design Goals
- Continuous density measurements
- Easy to (dis-)assemble
- Good culture density resolution

### Main Idea
The culture is constantly pumped (peristaltic pump) through a glass tube where the OD is constantly measured

## Photometer
The Photometer unit is based on one module of the [test tube photometer](http://openplant.science/2017/12/09/photometer-shopping-list.html)

<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/sketch.png" style="width: 500px ;" hspace="20" vspace="20"/>

### Main components
1. **Arduino or similar microcontroller**<br>
You need something to read the analog input of the sensors in a measuring routine. We used an Arduino Nano.

2. **LCD display**<br>
This one is optional but nice if you instantly want to see the measured values. It is useful for easy calibration and for discontinuous measurements with the photometer. You can use any available LCD which works well with the microcontroller. We used a standard HD44780 16x2 LCD Display and a I2C backback.

3. **Measuring cell**<br>
All the components you need to build a measuring cell are listed below.

4. **Pasteur pipette tube**<br>
Be carful not to cut yourself while you prepare your pasteur pipette! Carefully remove the tip of the pipette and melt the edges with heat.

5. **Housing**<br>
Well, this is optional too but it helps to keep the electronics save!

### Measuring cell components
<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/sketch2.png" style="width: 250px ;" hspace="120" vspace="130"/>

1. **Housing and housing cover**<br>
You can find the 3D models in this repository. The housing has slots for the LED and the photodiode, which are fixed with the housing cover. If you do not have access to a 3D printer you can find service providers online. We printed it with standard black PLA and we recommend you to use black material, too, because it improves sensitivity of the system significantly. You might have to adjust the parameters of the housing to fit with your pasteur pipette tube!

2. **LED**<br>
It is really important to use a high quality LED because it determines the wavelength you are measuring with. We used a 600 nm LED from [Roithner LaserTechnik](http://www.roithner-laser.com/index.html). If you prefer to measure at a different wavelength choose your LED accordingly!

3. **Photodiode**<br>
This is the heart of the measuring cell. We used an [opt101](http://www.ti.com/lit/ds/symlink/opt101.pdf) from Texas Instruments because it contains an on-chip operational amplifier, and responds to light in the range of 300–1100 nm (linear dependence between 400–800 nm!). We added a 1MΩ external resistor to achieve a DC gain of 2 million volts per ampere to optimize the output voltages.


<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/cell_cover_fused.png" style="width: 500px ;" hspace="20" vspace="20"/>
### Build Instructions
1. **Assemble the housing**<br>
The housing consists out of two parts, the main body and a sleeve. There are two respective holes in the main body in which you can place the sensor and the LED. Slowly pull the sleeve over the main body with the LED and Sensor pins sticking out (see picture above). Please remember the sensor orientation for the correct wiring of the pins!

2. **Wiring**
<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/cell_wiring.jpg" style="width: 500px ;" hspace="20" vspace="20"/><br>
Now you can start and solder wires to the sensor an LED pins. If you have problems soldering the sensor pins with the housing assembled you can remove the sensor, solder the wires and then assemble the housing. But then you might have to use some force to fit the soldered pins through the gaps.
I labeled each wire to make it easier for me to connect them later.<br><br>
**You should end up with five wires from the sensor:**<br>
- Power (V, pin 1)<br>
- Input/Additional Feedback (-In, pin 2)<br>
- Power/Ground (-V, pin 3)<br>
- Output (Output, pin 5)<br>
- Input/Ground (Common, pin 8)

### Connect it to the microcontroller ###
<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/sketch3.png" style="width: 300px ;" hspace="20" vspace="20"/>

Connect sensor pin 1 to 5V, pin 3 and 8 to ground. Sensor pin is connected to pin 5 with a 1 MΩ resistor in between (see circuit diagram on the right). You can now connect the sensor output (pin 5) to any analog input pin of your microcontroller and you are ready to measure light. <br>
Speaking of light, you still have to connect the LED with one of the digital output pins of the microcontroller to switch the light on and off.
