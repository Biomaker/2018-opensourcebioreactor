# pH Control System
As of today, we have tested the pH control system that consists of a traditional pH probe and a peristaltic pump, both controlled by Arduino Uno through XOD software. The peristaltic pump was chosen over the syringe pump because we wanted to reuse it for our optical density sensor. 

While testing IGEM 2015 pump, we came across several problems with the existing design. Firstly, the parts that form tubing enclosure, laser-cut from Plexiglas, are positioned in layers, and thus their sharp edges can break the silicone tube. Secondly, the existing enclosure is not easy to assemble, mainly due to the number of parts that need to be arranged on top of each other. This may present a problem because the enclosure has to be (dis)assembled before every run of bioreactor in order to put in new sterile tubing.

We propose an alternative enclosure, which is 3D-printable. It will consist of three parts and will not include layers or sharp edges. A pump with 3D-printed enclosure will not require an additional piece of equipment to make, i.e. the laser-cutter.  

Since our bioreactor will at least require one more peristaltic pump (to measure the optic density), we aim to create pump design that can be easily adjusted to a different tubing size. Our pump size parameters can be quickly changed within the 3D modelling software ([OpenJSCAD](https://openjscad.org/)) we are developing.

