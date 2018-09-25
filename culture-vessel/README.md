# Module A: Culture Vessel

This module involves design of the heated vessel and connections for various sensors and devices required to monitor and intervene in the bioreactor run.

### Design Goals

 - Glass, autoclavable bottle
 - Have low-cost connectors for the inputs and sensors that maintain sterility
 - Hold around 1L culture with plenty of air space (~ 2 L volume)

We looked at typical culture vessels supplied by lab brands such as Duran but the cost was prohibitive (£200 for a wide-mouthed Duran bottle and an additional for the lid with bioreactor attachments).

## Adhesive for connection of items in autoclavable units

Adhesives should be autoclavable i.e. have high heat, humidity and pressure resistance. Various adhesives companies market epoxy resins with these properties to the medical device market e.g.those produced by [MasterBond](https://www.masterbond.com/properties/sterilization-resistant-adhesives) and 

**Required features:**

 - Should withstand multiple autoclaving cycles of 3-15 minutes at 121-134°C under steam pressure up to 20 psi.
 - Pressure resistant to 20 psi
 - Maximum operating temperature above 121 C
 - Oil and water resistant
 - Non-corrosive
 - [If applicable] Biocompatible. Depending on if the adhesive will be in contact with the biological material in the reactor, it would be worth looking at biocompatability. Any material with USP Class VI certification is medical grade and considered to be biocompatible.
 
A potential lower cost solution (without biocompatability considerations) is to look to automobile ranges with silicon gasket makers and adhesives designed for vehicle parts that reach high temperatures.

**Chosen gasket maker**:
Visbella Silicone Engine Repair Gasket Seal Maker High Temperature (Heat Resistant from -80ºF to 600ºF) ([Amazon](https://www.amazon.co.uk/Visbella-Silicone-Engine-Temperature-Resistant/dp/B00XLO2R2Q/ref=pd_day0_hl_328_1?_encoding=UTF8&pd_rd_i=B00XLO2R2Q&pd_rd_r=a51db27e-c09f-11e8-953f-89c799ecfc7f&pd_rd_w=XqGt7&pd_rd_wg=HGprs&pf_rd_i=desktop-dp-sims&pf_rd_m=A3P5ROKL5A1OLE&pf_rd_p=f6359d5f-11a6-4577-a43b-58b9bb222f57&pf_rd_r=GKGZNWFA4N10G61EEHC8&pf_rd_s=desktop-dp-sims&pf_rd_t=40701&psc=1&refRID=GKGZNWFA4N10G61EEHC8) | [Manufacturer](http://visbellausa.com/products/gasket-makers/))

**Chosen adhesive resin**: JB Weld Original Cold Weld Formula Steel Reinforced Epoxy 8265 ([Amazon](https://www.amazon.co.uk/gp/product/B0006O1ICE/ref=ox_sc_act_title_1?smid=A3P5ROKL5A1OLE&psc=1) | [Manufacturer] (https://www.jbweld.com/collections/metal/products/j-b-weld-twin-tube))


## Autoclavable luer locks

There are numerous sites giving information on compatability of different plastics with different sterilisation methods, including this [useful table](http://www.industrialspec.com/images/files/plastics-sterilization-compatibility-chart-from-is-med-specialties.pdf) from industrialspec.com.

Ensinger Plastics ran tests with plastics exposed to pure saturated water vapour at 134 °C for 10 min at 3 bar pressure. This is in accordance with DIN EN 285 European standard for large steam sterilisers, whereby all surfaces of the objects being sterilised must be exposed to pure saturated water vapour at 134 °C for at least three minutes.

**Required features:**

 - Low coefficient of thermal expansion
 - Low moisture absorption
 - Temperature resistance up to 134 C

**Autoclave compatible plastics:**

 - Polypropylene  (Ensinger results: TECAPRO MT shows no significant loss of mechanical properties until 800 sterilisation cycles. However, discolouration and colour change (yellowing) is seen at 200 sterilisation cycles (does not apply to TECAPRO MT black). 
 - Polycarbonate can also withstand high temperatures. 
 - Polysulfone
 - Ultem®
 - PPSU (Ensinger results: TECASON P MT shows no significant loss of mechanical properties until 800 sterilisation cycles. Also, significant discolouration is not seen below 1,000 sterilisation cycles. 
 - PEEK (Ensinger results: TECAPEEK MT shows no significant loss of mechanical properties, even at more than 1,500 sterilisation cycles. Also, further negative influences like discolouration or colour change (yellowing), or even calcification are not seen above 1,500 cycles.)
 - POM-C medical grade (Ensinger results: TECAFORM AH MT shows no significant loss of the mechanical properties until 800 sterilisation cycles. However, discolouration may be seen at 200 sterilisation cycles. At around 500 sterilisation cycles, a colour change (yellowing) may also be seen.)
 - PFA (perfluoroalkoxy) 
 - FEP (fluorinated ethylene propylene) 
 - ETFE (ethylene tetrafluoroethylene) 
 - PCTE (polychlorotrifluoroethylene)
 - ECTFE (ethylene chlorotrifluoroethylene)

**NOT to be autoclaved:**

 - Polystyrene (PS)
 - Polyvinyl chloride (PVC)
 - Nylon
 - Acrylic
 - Low-density polyethylene (LDPE)
 - High-density polyethylene (HDPE) 
 - Polyurethane
 - Polylactic Acid (PLA): our tests showed significant issues with brittleness after five cycles
 


## Anti-Foam

Agitation can lead to bubbling in E.coli cultures to it is often necessary to add anti-foam chemicals. Low-cost and commonly available anti-foam agents include olive oil, sunflower oil, silicone, polyethylene glycol.
