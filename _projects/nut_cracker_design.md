---
layout: project
title: Nut cracker design
description: Just a thing that I designed

---
In ENGRD 2020, we were tasked with creating a nutcracker. 


We were to find the dimensions of a nutcracker based on 
the size of the macadamia (25mm)
average grip strength of a woman (32 kg)
force required to break a nut (222.18kg) - this value was found from https://doi.org/10.1007/s10071-007-0131-2


Making the assumption that the force would be applied at the very end of the handles, and the nut was 2 in away from the tip of the nutcracker,
and all forces are point forces, I calculated the distance ratio:
  222.18kg * g * 2 in = 32kg * g * x in, where x is 13.8 inches.

This design is unusable due to its length. It becomes inconvienent to store and requires full strength from a person, and you would also need to 
stretch your arms across the entire apparatus. Therefore, the assignment dictated we switch from human grip strength to a linear actuator. 

The linear actuator I picked had a 2-inch stroke length and a output force of 330lbs.  (Mini industrial actuator on https://www.progressiveautomations.com/collections/linear-actuators)

The plan becomes similar, but now the equation becomes:

 222.18kg * g * 2 in = 0.5*150kg * g * x in, where x = 5.9 inches. 

This allows for a more usable design, since the handles are over half as small. This design requires one actuator, and the stroke length ensures that the
nut will be cracked without the nutcracker having to take up too much space during the actual actuation itself. 

![Diagram of nutcracker design with actuator](https://github.com/Cornell-MAE-UG/sp26-portfolio-aj688-jpg/blob/main/assets/images/IMG_4049.jpg)

BENDING ANALYSIS

Now, we will consider handles that can bend under the forces applied by the nut and the actuator. We are considering the joint joining the two halves of the nutcracker as pinned, meaning it can provide a rxn force, but not a rxn moment (y = 0). 

We will first find where maximum deflection will occur. We will draw a FBD (picture appears with the math), where we will focus on one handle. All dimensions are from the previous drawing.

As we can see, the inital boundary conditions is that at x = 0, the starting angle is 14 degrees, and the starting deflection (y) is 0.

For the location of maximum deflection, it appears to be where the nut is; the nut is pushing up, creating an upwards deflection, and the actuator is pushing the handle downwards at the edge, which also leads to an upwards deflection in the middle. Therefore, the maximum deflection in the handle would be where the nut is. 

For picking the material, under the constraints that it is mass-efficent and the deflection is at most 2% of the total length, we first find the elastic curve equation, assuming a total length of 7 inches, as reasoned before. We use the idea that the second derivative of y * E * I = internal moment. 

![Math and FBD](https://github.com/Cornell-MAE-UG/sp26-portfolio-aj688-jpg/blob/main/assets/images/IMG_4049.jpg)

Doing the math, with the max deflection being (0.02) * 7 inches, at x = 2 inches, we end up with: 

3.6mm =( (-1.4kN * 1.3 x 10^5 mm^3 ) / 6 ) / EI + 12.2mm , where E and I are dictated by the beam design. We can pick arbitrary numbers for the cross-section
that would make a suitable beam design; my hand can comfortable grip a circular rod of cross section A = pi * (0.5in)^2 = 506 mm^2, leading to 

I = 2.0 x 10^4 mm^4. Then, solving for E, we get around 177 Mpa. This is incredibly small, and likely due to the vast oversimplifications that were made when doing this problem. Materials that fit this value could be some woods or plastics. 




