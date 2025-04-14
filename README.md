![front](https://github.com/user-attachments/assets/04fc73c2-717d-4b06-80cf-da1db81b104b)
![back](https://github.com/user-attachments/assets/00612b87-f02c-4283-8265-d86f0e3c4a03)
If anyone really wants to replace an LT1085 doing 3.3V duty on a 486 motherboard with a buck converter equivalent and doesn't mind the prospect of rewiring some stuff for it, I've made 'Yorp', a three pin buck converter board based on the Diodes AP63203WU 3.3V 2A Synchronous Buck. 

Now, mind you, LT1085s are rated up to 3A but the AMD Am5x86-133 is specced up to 960mA-ish worst case (so slightly less than 1A), so you've still got around an amp of headroom with this. I've made one of these and put it in my PB450 motherboard based Packard Bell Legend 10CDT, where it works quite well driving an Am5x86 at 100MHz (lower speed is because I forgot to solder in the multiplier jumper on the mobo, LOL). 

Depending on how the LT1085 is set up on your motherboard, you _might_ have to remove some parts and do some rewiring so that the GND terminal actually goes to GND without causing something else on the motherboard to misbehave. As always, rigorously check for bad things like short circuits to ground using a multimeter before applying power!

Bill of materials:

-1x AP63205WU 3.3V Buck Regulator in SOT-23-5 (https://www.digikey.com/en/products/detail/diodes-incorporated/AP63205WU-7/9858424)

-5x 10uF 25V 2012/3216 metric SMD ceramic caps, X5R/X7R 

-1x 100nF 0805/2012 metric SMD ceramic cap, C0G

-1x 3.9uH 6.3mm x 6.3mm SMD inductor rated for _at least_ 2A saturation current (I used one of these: https://www.digikey.com/en/products/detail/murata-electronics/1255AY-3R9N-P3/6205579)

-1x 2.54mm pitch, 3-pin, pin header
