---
title: "Multi-Material Pliers"
excerpt: "Needle nose pliers that are capable of gripping and picking up through-hole resistors"
header:
  image: /assets/img/Image 10-8-23 at 4.34 PM.jpeg
  teaser: /assets/img/Image 10-8-23 at 4.32 PM.jpeg
gallery:
  - image_path: /assets/img/Image 10-8-23 at 4.32 PM.jpeg
  - image_path: /assets/img/Image 10-8-23 at 4.33 PM.jpeg
  - image_path: /assets/img/Image 10-8-23 at 4.34 PM.jpeg
  - image_path: /assets/img/IMG_0774.jpeg
  - image_path: /assets/img/IMG_0775.jpeg
  - image_path: /assets/img/IMG_0776.jpeg
---

### CAD Model

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6ec3df58f471dd91e1?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

### Take a Look!

![](/assets/img/Plier1.gif)

![](/assets/img/pliers2.gif)

### Goals

  My objective was to create and manufacture needle-nose pliers with the ability to grasp and lift a through-hole resistor. These pliers incorporated a flexible material for a spring mechanism, ensuring they automatically return to the open position when not in active use. My pliers were produced through filament printing using a combination of PLA and 95A TPU materials. The handles are made of PLA and the connector is TPU. 
  
### Design Features

  I created a spring mechanism inspired by the previous class's designs and other pliers I saw on the internet. Each bar in the spring component is 1 mm wide. They separate the open elements of the spring. It allows for ample resistance while closing the pliers. The tension resets them to the open position when finished. 

  I added my own touch with the puzzle piece connection to upgrade the performance of my pliers. I also made my pliers on the larger side. I wanted to be able to pick up large and small objects to increase the versatility of my pliers. The pliers are 180 mm long and 100 mm wide. At a resting position, the plier’s jaws are a little over 13 mm wide. They fully close when squeezed. 

  PLA and TPU lack strong chemical adhesion as the filament is printed, so I had to utilize mechanical connections to prevent the entire assembly from falling apart. The puzzle piece geometry keeps both parts together under the tension of squeezing the pliers. It allows for more surface area adhesion for each material in order to stay in place. Multi-material Fused Filament Fabrication (FFF) enables the design and fabrication of mechanical connections that would be unattainable with conventional additive and subtractive manufacturing methods.

  With the print itself, TPU, being a flexible filament, requires a slower printing speed compared to PLA. Multi-material filament printing results in a reduction in the number of components and connectors, ultimately leading to fewer potential problems during the print and assembly. There is nothing to assemble after the pliers are printed. The right extruder was PLA. It printed at temperatures of 205-210 C. The left extruder was the TPU side and printed between 230-235 C. Each side printed 2 layers and alternated in order to minimize the number of transitions between extruders. 

  I utilized an Independent Print Carriage (IDEX) printer. While adding more than two (2) extruders is more expensive and difficult because of the build plate limitation, these printers are some of the most reliable multi-material printers on the market. They require less exact calibrations than printers with mechanically actuating nozzles and dual-fixed nozzles. 

  The multi-material print makes it susceptible to extruder leakage during periods of inactivity, and it takes longer for the nozzle to maintain a consistent extrusion speed after a pause. Therefore, when the TPU extruder is activated, it's essential to clean the ooze and prime the nozzle properly. To ensure this, I used a wipe tower. This allows the nozzle ample time to establish a smooth flow of molten plastic and provides a surface to capture any filament that may have oozed onto the nozzle. However, these wipe towers waste a lot of material for a relatively small print. A drawback of multi-material printing is the wastefulness of the extruders in order to maintain a consistently smooth print. 

{% include gallery caption="Needle-Nose Pliers Gallery" %}

