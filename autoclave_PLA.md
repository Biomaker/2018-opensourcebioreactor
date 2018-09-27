<p align="center">
<img alt="UM robo" src="{{ "robo2.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}" style="margin-right: 5%" width="400"/><h1 align="center"> Can you autoclave PLA? </h1>
</p>

For our project we were looking into cheap ways to create small (plastic) parts for the interior of the reactor and 3D-printing was the first choice. An important requirement for these parts is that they can be easily decontaminated because they get in contact with bacteria. An easy and thorough sterilization method of lab equipment and instruments is autoclaving [(high temp/pressure + saturated steam)](https://en.wikipedia.org/wiki/Autoclave)! But would PLA, THE standard 3D-printing material, survive 20 minutes at 121 °C in steam? To answer the question for us, we performed a test series and autoclaved Benchy [(the 3D-printer benchmark boat)](http://www.3dbenchy.com/) multiple times.
## What's the answer?

Well, unfortunately we have to add another inconclusive answers to the ones out there: __Yes, but No!__<br>
Have a look at my documentation of the test series and judge it yourself:

### First and second time

we printed two Benchy models with my Anet A8 printer using standard setting and cheap PLA. One of the models we put into a jar and autoclaved it (20 Minutes at 121 °C). we couldn't detect any changes in the autoclaved model compared to the not-autoclaved one. This was quite surprising for me because we expected at least some tiny bends at the overhangs. After the second time in the autoclave Benchy still looked very similar to its not-autoclaved clone. However, we could see some minor bends at its stern.

<p align="center">
  <img alt="First round" src="{{ "benchy1.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}" style="margin-right: 5%" style="margin-top:2%" width="300"/>
  <img alt="Second round" src="{{ "benchy2.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}" style="margin-right: 5%" style="margin-top: 2%" width="300"/>
</p>

### Third and fourth time

After the third and fourth time autoclaving Benchy the minor bends at its stern, which we already saw after the second round, intensified. Interestingly they did not look like if the model melted a tiny bit but rather caused by expansion forces in material due to the heavy temperature changes.
<p align="center">
  <img alt="Third round" src="{{ "benchy3-1.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/>
  <img alt="Third round" src="{{ "benchy4-1.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/><br>
  <img alt="Fourth round" src="{{ "benchy3-2.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/>
  <img alt="Fourth round" src="{{ "benchy4-2.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/>
</p>

### Fifth and last times  

The next round in the autoclave seemed to increase the bends and also the color seemed a bit more whitish. We tried to twist the model a bit and it turned out to be very brittle. It instantly fell apart. We did not test the integrity of the model so it is likely that it already was brittle before.
<p align="center">
  <img alt="Third round" src="{{ "benchy5-1.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/>
  <img alt="Third round" src="{{ "benchy5-2.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/><br>
  <img alt="Fourth round" src="{{ "/assets/img/autoclavePLA.jpg" | prepend: "https://github.com/BioMakers/2018-opensourcebioreactor/blob/master/img/PLA/" }}"  style="margin-right: 5%" style="margin-top:2%" width="300"/>
</p>

### Final Conclusion

Well, PLA gets very brittle rather than heat-deformed in an autoclave. That's why I (Alex) think that you actually can autoclave PLA maybe up to 10 times but only if your print is not exposed to forces!
