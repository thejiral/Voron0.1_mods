# Voron0.1_mods

# Modified skirts for Voron 0.1

I wanted to have skirts which fully enclose the PSU and everything else at the bottom of the V0.1, with more of a net look than the coarse honeycomb style in the original. At the same time air should still be able to circulate. 

![image1](https://github.com/thejiral/Voron0.1_mods/blob/main/175742.png)

![image2](https://github.com/thejiral/Voron0.1_mods/blob/main/IMG_20210822_174009%7E2.jpg)

![image3](https://github.com/thejiral/Voron0.1_mods/blob/main/IMG_20210822_173756%7E2.jpg)

I created the honeycomb net of the skirts with Prusa slicer via infill options. The ready to print models can be be found in the 3mf file. 
Alternatively the raw component stl files are included in the zip file as well. 

The modified foot is needed for mounting panel 3. Insert 2 heat inserts (same as in the Voron 0.1 BOM). 
Panels of type 1 and 2 are mounted the same way as the original blinds but do feature throughholes for the hex key. Panel 3 is mounted with 2 M3 6mm button head screws to the rear foot right modified. At the other side I fixed Panel 3 with a bit of VHB tape at the AC Inlet. 


_Contents_

2x Panel 1 (front panel, right side panel)

1x Panel 2 (left side panel)

1x Panel 3 (back side panel)

1x Modified Rear foot


# SEPA-rator: Voron 0.1 air filter (HEPA + refillable 50 g activated carbon cassette)

Needed components:
- 3x SEPA HY45T05A: https://www.reichelt.de/at/de/radial-luefter-45x45x5mm-5v-27db-5200u-min-gleitlager-sepa-hy45t05a-p291164.html?&nbc=1
- 1x HEPA filter: replacment filter for xiaomi Robot Vacuum Cleaner STYJ02YM https://www.aliexpress.com/item/4000155770683.html?spm=a2g0o.9042311.0.0.7ae94c4daSGJuo
- air purifier activated carbon pellets: https://www.luftundklima24.de/Aktivkohle-Pellets-Geruchsfilter-4-mm-1-kg-Luftfilter
  alternatively better but more expensive: Nevermore Printer Carbon: https://vonwange.com/product/nevermore-printer-carbon/
- Plastic solvent glue like UHU Plast (https://www.uhu-profishop.de/klebstoffe/kunststoffklebstoffe/137/uhu-plast-spezial-polystyrol-abs-niedrigviskos-flasche-mit-feindosierspitze-30g) or RevelL Contacta Professional (https://www.3djake.com/revell/contacta-professional)
- 2mm thick EPDM foam band 10 mm width: https://www.fugendichtband24.de/EPDM-Zellkautschuk-einseitig-selbstklebend-5m-Rolle-2mm-x-diverse-Breiten.htm
- Optionhal: 2mm thick EPDM foam mat for custom cutting: https://www.fugendichtband24.de/EPDM-Zellkautschuk-Matten-2mm-Staerke-einseitig-selbstklebend-diverse-Abmessungen.htm
- 2x M3 nut
- 2x M3 6-8 mm screws
- Optional: WAGO clamps: 3x WAGO 221-613: https://www.reichelt.de/at/de/verbindungsklemme-6-mm-3-leiter-wago-221-613-p222123.html?&trstct=pol_19&nbc=1

Printed parts from ABS or ABS+ (eg. TitanX)
-SEPA-rator print files.zip (Airfilter-V3.3mf, Aifilter-V3-partb.3mf)

Assembly

2 mm EPDM foam is applied in the areas shown below. These will hold the fans tight in place from both sides when housing is assembled. 

![image4](https://github.com/thejiral/Voron0.1_mods/blob/main/Adding%20EPDM%20to%20backplate.png)

![image5](https://github.com/thejiral/Voron0.1_mods/blob/main/Adding%20EPDM%20to%20mainpart.png)

A 2mm PDM ring with 10 mm width is applied all around the side of the top part of the active carbon cassette as can be seen in the image below:

![image6](https://github.com/thejiral/Voron0.1_mods/blob/main/carbon%20insert%20top%20with%20EPDM%20ring.png)


In the first step of the assembly, the backplate is oriented witht the flat side down. The fans inserted with the metalic side up and the air exhaust showing to the grill of the backplate. The cables leavethe housing on the open side. 
Apply sufficient plastic glue on all the top surfaces of the backplate. The main housing is oriented with the EPDM foam towards the fans and the "Voron" label is on the same side as the grill of the backplate. The EPD free parts of the main body should be flush with the glued side of the backbplate. Make sure that both parts are aligned well and seamlessly with each other and compress the EPDM foam with sufficient pressure. Put books or other heavy weights (1-2kg) to maintain that pressure and gapless contact of thet wo surfaces for at least 24h. 

The assembled body can be mounted with the two screw holes to 2 nuts inserted into the bottom frame. Alternatively it can be mounted with VHB-tabe to the frame.

![image6](https://github.com/thejiral/Voron0.1_mods/blob/main/Assembled%20airfilter%20without%20HEPA%20filter%20and%20AC%20cassette.png)

By drilling a small hole just below airfilter, the cables can exit the chamber and be connected via WAGO clamps to continuing cables.The yellow cables are not needed and can be cut and isolated. Red (minus) and black (plus) are connected to the 5V converter of the VO.1 and the orange cable is transmitting the PWM signal and is connected to a hardware PWM pin on the Raspberry Pi (eg GPIO12 on a Raspberry Pi 3). (https://pinout.xyz/pinout/pwm#)

The HEPA filter is removed from the clear plastic cassette it is sold in and is inserted into the airfilter body with the lash lookin outwards. 

![image7](https://github.com/thejiral/Voron0.1_mods/blob/main/Airfilter%20assembled%20with%20HEPA%20filter%20inserted.png)

The bottom of the cassette is filled flush with active carbon pellets and combined with the top part

![image8](https://github.com/thejiral/Voron0.1_mods/blob/main/filled%20active%20carbon%20insert%20bottom.png)

![image9](https://github.com/thejiral/Voron0.1_mods/blob/main/activated%20carbon%20cassette%20assembled.png)

The cassette is inserted into the airfilter body and the filter is ready for operation. If no PWM signal is provided the fans will run at full speed. If the PWM cables are connected to a Hardware PWM Pin of the Raspberry Pi it can be controlled among others with the Octoprint plugin "HardwarePWM" (set frequency to 23kHz). 
 
![image10](https://github.com/thejiral/Voron0.1_mods/blob/main/airfilter%20fully%20assembled.png)


Activated carbon should be exchanged frequently, the HEPA filter has a longer life cycle and needs to be replaced when airflow decreases. 
