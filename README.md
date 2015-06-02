# OpenErgMonitor-
Smartphone based open source rowing ergometer monitor

This project aims to create digital monitor for a rowing ergmeter that is as cheap as possible and open source. 

The open monitor should to complement Jim Flood's excelent [openergo.webs.com]("Open Ergo"  project), which gives detailed plans for building a DIY erg with simple and available materials. The idea is to create a viable alternative to expensive commercial ergometers, such as Concept2 and RowPerfect, especially in developing countries. Unfortunately, despite a good "feeling" of the DIY machine, lack of feedback and motivation from a monitor greatly reduces the potential uses. So a DIY monitor is needed. 

In order to keep costs down, the monitor will ran on a Smart phone (Android for starters) and preferably require as little as possible of external sensors and dedicated control boards. 

The project breaks down into two components: (a) hardware: measuring the accelerations and decelerations of the fan (disc, flywheel) of the rower with sufficient precision and communicating that to the smart phone (b) software: from the changes in fan speed deduct all the relevant information for a rowing erg monitor (stroke rate, power (watts, split), displacement, etc)



## Hardware: Measuring the speed of the fan precisely

### Precision parameters

Before choosing the best hardware set up for the sensors, we need an estimate of how the rotation speed fluctuates through a stroke. Here is a back of the envelope (gu)estimate of rotation speeds (if you know better let me know): 

* A concept2 uses a 14 tooth sprocket. Assuming it uses a regular bicycle chain (is this true?) (pitch = 12.7mm), the circumference = 1.27cm x 14 = 17.78cm. --> radius=17.78mm/2pi = 2.83cm 
* Drive length: 190cm --> rotations per drive = 190/17.78=10.68 r/drive
* Drive time(duration): lets assume 0.5s (this is what I'm most unsure off. Any ideas?). Thus: 
* Average rotation speed : 10.68(r/drive)/(0.5s/drive)= 21.37r/s. But the wheel actually accelerates through the stroke. 
* Assuming linear acceleration starting at 0, max rotation speed would be 42.74r/s (it is not, it should accelerate at decreasing returns, and not starting at zero, but lets overestimate a bit).

So the **sensor needs to be precise/fast enough to detect rotation speed changes even at 42.74r/s speeds.**  





XXX
I have been asking about this at some forums, and got some very interesting feedback. Links are listed bellow

XXXX


## Software: 

Software part consist of receiving the stream speed measurements and extracting the relevant information on stroke rate, power, displacement, etc). This should be an app that, developed for Android, and preferably compatible, as much as possible, with older android versions. 

Important References: 

* [Physics of Ergometers](atm.ox.ac.uk/rowing/physics/#ergo): This documents explains the relevant physics, which should be incorporated in to the app. 
* 





