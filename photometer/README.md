# Flow-through photometer and temperature sensor module

This module comprises the development of a flow-through photometer and temperature sensor unit for the determination of culture density and temperature.

### Design Goals
- Continuous density measurements
- Easy to (dis-)assemble
- Good culture density resolution

### Main Idea
The culture is constantly pumped (peristaltic pump) through a glass tube where the OD is constantly measured. The Photometer unit is based on a single module of the [test tube photometer](http://openplant.science/2017/12/09/photometer-shopping-list.html).

You can directly jump to the subsections:
- [Main components](#main-components)
- [Measuring cell components](#measuring-cell-components)
- [Build instructions](#build-instructions)
- [Usage](#usage)
- [First results](#first-results)


<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/sketch.png" width=400px />

### Main components
1. **Arduino or similar microcontroller**<br>
You need something to read the analog input of the sensors in a measuring routine. We used an Arduino Nano.

2. **LCD display**<br>
This one is optional but nice if you instantly want to see the measured values. It is useful for easy calibration and for discontinuous measurements with the photometer. You can use any available LCD which works well with the microcontroller. We used a standard HD44780 16x2 LCD Display and a I2C backpack.

3. **Measuring cell**<br>
All the components you need to build a measuring cell are listed below.

4. **Pasteur pipette tube**<br>
Be carful not to cut yourself while you prepare your pasteur pipette! Carefully remove the tip of the pipette and melt the edges with heat.

5. **Housing**<br>
Well, this is optional too but it helps to keep the electronics save!

<img align="right" src="https://raw.githubusercontent.com/vektorious/cOD/master/img/sketch2-2.png" width=400px />

### Measuring cell components

1. **Cell housing and housing cover**<br>
You can find the 3D models in this repository. The housing has slots for the LED and the photodiode, which are fixed with the housing cover. If you do not have access to a 3D printer you can find service providers online. We printed it with standard black PLA and we recommend you to use black material, too, because it improves sensitivity of the system significantly. You might have to adjust the parameters of the housing to fit with your pasteur pipette tube!

2. **LED**<br>
It is really important to use a high quality LED because it determines the wavelength you are measuring with. We used a 600 nm LED from [Roithner LaserTechnik](http://www.roithner-laser.com/index.html). If you prefer to measure at a different wavelength choose your LED accordingly!

3. **Photodiode**<br>
This is the heart of the measuring cell. We used an [opt101](http://www.ti.com/lit/ds/symlink/opt101.pdf) from Texas Instruments because it contains an on-chip operational amplifier, and responds to light in the range of 300–1100 nm (linear dependence between 400–800 nm!). We added a external potentiometer to achieve a DC gain of up to 2 million volts per ampere to optimize the output voltages.

### Build instructions
1. **Assemble the cell housing**<br>
The housing consists out of two parts, the main body and a sleeve. There are two respective holes in the main body in which you can place the sensor and the LED. Slowly pull the sleeve over the main body with the LED and Sensor pins sticking out (see picture above). Please remember the sensor orientation for the correct wiring of the pins!

<p align="center">
<img src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/cell_cover_fused.png" width=500px></p>

2. **Wiring**<br>
Now you can start and solder wires to the sensor an LED pins. If you have problems soldering the sensor pins with the housing assembled you can remove the sensor, solder the wires and then assemble the housing. But then you might have to use some force to fit the soldered pins through the gaps.
I labeled each wire to make it easier for me to connect them later.<br><br>
<img align="right" src="https://raw.githubusercontent.com/vektorious/test_tube_photometer/master/pictures/sketch3.png" width=180px/>

**You should end up with five wires from the sensor:**<br>
- Power (V, pin 1)<br>
- Input/Additional Feedback (-In, pin 2)<br>
- Power/Ground (-V, pin 3)<br>
- Output (Output, pin 5)<br>
- Input/Ground (Common, pin 8)

3. **Connect it to the microcontroller**<br>
Connect sensor pin 1 to 5V, pin 3 and 8 to ground. Sensor pin is connected to pin 5 with a potentiometer (or 1 MΩ resistor) in between (see circuit diagram on the right). You can now connect the sensor output (pin 5) to any analog input pin of your microcontroller and you are ready to measure light. <br>
Speaking of light, you still have to connect the LED with one of the digital output pins of the microcontroller to switch the light on and off.

4. **Insert the pasteur pipette tube**<br>
Attach tubing to the smaller end of the pasteur pipette tube and insert it into the measuring cell. Try and position it completely inside the cell. The tube should be fixed inside (conical ending)!
<p align="center">
<img src="https://raw.githubusercontent.com/vektorious/cOD/master/img/pipette_tubing.png" width=400px></p>

5. **Assemble the complete module**<br>
Insert the measuring cell into the housing and attach the LCD display to the housing lid. Connect the LCD and the temperature sensor to the microcontroller and arrange everything inside the housing.

<p align="center">
<img src="https://raw.githubusercontent.com/vektorious/cOD/master/img/setup_v1.jpg" width=400px></p>

### Usage
The finished module can be attached to any peristaltic pump which fits the tube size (we used 6 mm tubing). Both ends of the tubing are inserted into the culture and the liquid should be pumped through the measuring cell. For data transfer the microcontroller can be connected to a single-board computer via a serial connection.

<p align="center">
<img src="https://raw.githubusercontent.com/vektorious/cOD/master/img/setup_v2.jpg" width=400px></p>


### First results

**20.09.2018**<br>
We finished a first prototype of the flow-through photometer and tested it with an E. coli cultures ([Jupyter Notebook with data analysis](https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/photometer/photometer_data.ipynb)).
<br>Conclusion: Culture density can be measured but the precision has to be improved with further tests and setting of the potentiometer.

**17.10.2018**<br>
After a second completely failed test (pump stopped ca. 1 h after it was started) we performed a third run which was finally successful. We cultured *Pseudomonas syringae* (a plant pathogen, Alex's favorite bug) in a 300 ml flask and measured the OD with the photometer. Here are the results:
<p align="center">
<img src="https://raw.githubusercontent.com/vektorious/2018-opensourcebioreactor/master/photometer/pst_181017.png" width=300px></p>

The data seem to represent the real bacteria growth in the flask! You can easily distinguish the different growth phased of the culture ([about growth phases](https://en.wikipedia.org/wiki/Bacterial_growth)). The variation of the values at higher OD is due to the underlying calculations (negative logarithmic) and the sensitivity limits of photometers (in general!).

**22.10.2018**<br>
The fourth test run showed the same results as the previous run. Here are the results:
<p align="center">
<img src="https://raw.githubusercontent.com/vektorious/2018-opensourcebioreactor/master/photometer/pst_181022.png" width=300px></p>

There seem to be slight differences but this might be due to different scaling of the plots AND because we did not inoculate the culture with a specific OD. In fact in this test run the liquid culture was inoculated with bacteria from an agar plate.

All in all it seems like the results are reproducible but we still need to test it with different bacteria (e.g. *E. coli*) and other microorganisms (e.g. microalgae or yeast)
