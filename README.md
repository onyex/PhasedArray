# PhasedArray
 Development for an easy to implement, low cost, lowish power, passive radar array.

 The general roadmap for now
    - Research
    - Research
    - Research

Current intention is to design a 4x4 array that can receive a 2.4GHz signal to detect signal azimuth and elevation. In addition the 2.4GHz source is intended to transmit information to identify itself and other information, allowing for identification of multiple sources and the potential for logic based on data transmitted. 

Currently researching existing commercial phased array systems and how they work. Several different methods are available to achieve the end product. Using COTS components is out of the question since a 4x4 array seems to run into the 5 digit USD range quickly. Individual components appear to be quite cheep in comparison to the boards they are on. This gives me some hope that with enough leg work a relatively cheep solution can be found.

Although the design is not limited to using passive only components, it appears that significant cost can be saved by not transmitting. This removed the need for a switch, phase shifter. For example the ARAR1000 connected to a ADRV9361 by Analog would be used in a hybrid approach to a beam former using analog summation and then converting to an analog to digital converter. Its seems as though the RX signal can be directly amplified and processed into an ADC since this appears to be the preferred method for getting signals information. Chips like the ADC09SJ800 from TI appear to have better sample rates and resolution compared to the analog offerings from Analog. The analog offering will set you back 4-6k where as it appears better performance can be achieved with more flexibility for cheeper. I am ignoring most of what the ADRV9361 is doing since I don't fully understand what it takes to stream this data to a Pi or some micro controller yet.
