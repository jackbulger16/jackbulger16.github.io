---
title: "Electric Skateboard"
excerpt: "Custom Made Skateboard with Generative Designed Trunks "
header:
  image: assets/img/PPP-3.jpeg
  teaser: assets/img/c9063288-4a77-4a44-ad9e-4840c2907b4e.PNG
gallery:
  - image_path: assets/img/PPP-3.jpeg
  - image_path: assets/img/c9063288-4a77-4a44-ad9e-4840c2907b4e.PNG
  - image_path: assets/img/IMG_1282.jpeg
  - image_path: assets/img/IMG_1283.jpeg
  - image_path: assets/img/IMG_1284.jpeg
  - image_path: assets/img/IMG_1293.jpeg
  - image_path: assets/img/IMG_1295.jpeg
  - image_path: assets/img/IMG_1309.jpeg
  - image_path: assets/img/IMG_1314.jpeg
  - image_path: assets/img/Skateboard LF3D v13.png
---
### CAD Models

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6ec42cf91a2557a619?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6ef477bb5ae9749baf?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6ea1c9eff25cdac335?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

### Skateboard Deck Design and Large Format 3D Printing

We printed the skateboard deck with a large format 3D printer.  Material extrusion 3D printers face challenges in maintaining structural integrity during overhangs due to the prolonged softness of extruded fibers with the large nozzle diameters required to print at this size. While the strong adhesion between neighboring fibers enhances mechanical properties, it hinders support material removal, except in cases of quick cooling, known as bridging, where extruded fibers can span unsupported regions between two supported points.

The LF3DP printer boasts a substantial build volume of 44"x44"x44", featuring a 5 mm nozzle diameter and an output of approximately 1 kg per hour. It can only print overhang angles greater than 45°, bridge distances less than 100 mm, and has a minimum feature size of 20 mm. It operates without support material, due to the nature of the speed of cooling the material. 

The length of a longboard significantly influences its performance, with longer boards offering a larger turning radius for stability, while shorter ones provide agility. Additionally, the board's thickness is a critical design factor, impacting stability and weight, with thicker decks providing stability but being heavier, and thinner ones offering responsiveness but risking excess flex that could lead to ground contact or breakage; a load simulation for ABS material with a 200lbs rider weight should ensure a maximum deflection of no more than 12 mm, prompting adjustments to the CAD model if necessary.

I decided to make my board 39” because I wanted it to be on the stable side of the skateboard spectrum. I do not plan on doing a bunch of tricks and kick-flips on the board due to my inexperience of riding a skateboard. Therefore, I opted for the more stable, efficient size for everyday riding. Also, I made the thickness of the board 25 mm because I did not want a lot of deflection while riding. I thought this amount was going to be a little overkill on the thickness before testing in the simulation with my 200lbs body weight, but it turned out to be within the 12 mm deflection maximum.  The safety factor and deflection were in a safe range. 

The design was inspired by wanting to do some sort of lattice structure within the board. The minimum feature size with the LF3DP was 22 mm, so I could not do anything too fine. I decided to extrude a Vanderbilt Logo in the middle and make parallel cutouts along the width of the board. I also created a boarder around the skateboard for stability that was colinear with the top and bottom of the Vanderbilt “V”. Overall, I was very happy on how my design turned out. 

Directly attaching the trucks to the 3D printed skateboard includes a risk of compressing the deck because of the forces from the bolt potentially shearing the extruded material lines. To address this concern, we used an aluminum plate featuring a hole pattern identical to that of the trucks will be employed to distribute this force across a more extensive section of the printed deck. In my design, there is a 106 mm x 74 mm cutout at the ends of the longboard. Lastly, my board tapers into the wheel well, so the board does not interfere with turning the wheels. It allows the wheels to go through their full range of motion. 


### Trunk Generate Design and Powder Bed Fusion

The evolution of additive manufacturing technologies has introduced a new era of design possibilities and manufacturing efficiency. Among these technologies, powder bed fusion and generative design have emerged as a powerful and useful pairing, commonly utilized in the aerospace and automotive industries. This discussion explores the combination between powder bed fusion and generative design, looking into their applications and the impact they have on the manufacturing processes. 

Powder Bed Fusion:

Powder bed fusion, a subset of additive manufacturing, involves layer-by-layer deposition and fusion of powdered materials, typically metals or polymers, using a laser or electron beam. The precision and intricacy afforded by PBF make it an ideal candidate for complex, lightweight, and high-strength components, characteristics highly sought after in aerospace and automotive applications. It’s a great way to create intricate designs due to its ability to print without support materials. 

In aerospace, PBF has redefined the manufacturing landscape by enabling the production of intricate components with reduced weight and enhanced performance. Components made by SLS exhibit high strength-to-weight ratios. The aerospace industry's relentless pursuit of fuel efficiency and performance gains has driven the widespread adoption of powder bed fusion for prototyping and production.

Generative Design:

Generative design is a computational design approach that employs algorithms and artificial intelligence to explore and optimize multiple design iterations. By specifying design parameters and constraints, generative design algorithms generate novel, organic forms that often defy traditional design conventions. This methodology allows engineers to find solutions that balance performance, weight, and structural integrity. With the rise in artificial intelligence, one might believe this is solely computer driven, however, in class we kept referencing, “garbage in, garbage out.” Unlike ChatGPT, it will not figure out a solution without the proper information. It requires load cases, preserve geometry, obstacle geometry, and constraints in order to keep the computer from creating an unuseable design. Using our skateboard as an example, the lightest and most efficient skateboard hanger might interfere with the wheels or motor belt, making the design unusable. Before generating the results, a lot of thought is required to create a usable design. 

In the automotive industry, generative design has become a game-changer. Traditionally, automotive components were designed with a focus on manufacturability and cost-effectiveness, often resulting in compromises in performance and weight. Generative design breaks free from these constraints, providing engineers with designs that are both efficient and structurally sound. This is particularly relevant for components like suspension parts, engine components, and even entire chassis structures.

The Synergy of Powder Bed Fusion and Generative Design:

The convergence of PBF and generative design unlocks possibilities in terms of design freedom and manufacturing efficiency. Generative design algorithms can create complex geometries that optimize material usage and structural integrity, often pushing the boundaries of what is achievable with traditional manufacturing methods. SLS, with its layer-by-layer approach, seamlessly translates these intricate designs into physical components with high precision.

Aerospace applications benefit significantly from this synergy. Jet engine components, for instance, can be designed with intricate internal structures that enhance cooling efficiency and overall performance. The marriage of generative design and SLS allows for the production of components that were previously deemed too complex or costly to manufacture, driving innovation in aircraft design and performance.

Applications in Aerospace:

Turbine Components: Lightweight, aerodynamically optimized turbine components, improving efficiency and fuel consumption in aircraft.
Structural Elements: Components that are not only strong but also tailored to the specific loads they encounter during flight.

Applications in Automotive:

Suspension Components: Suspension geometries that are lightweight, high-strength components, enhancing vehicle handling and ride comfort.
Engine Parts: Creation of intricate, heat-efficient engine components, contributing to improved fuel efficiency and reduced emissions.

Conclusion

The unique pairing of powder bed fusion and generative design has created a new era of innovation in the aerospace and automotive industries. The seamless integration of these technologies allow for the creation of highly complex, lightweight, and performance-optimized components that were once considered unattainable. As these industries continue to push the boundaries of design and efficiency, the collaborative power of powder bed fusion and generative design stands as a testament to the transformative potential of additive manufacturing in shaping the future of aerospace and automotive engineering.


{% include gallery caption="Skateboard" %}
