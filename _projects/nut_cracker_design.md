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


