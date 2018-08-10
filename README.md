# jetsonTX2GPIO
A straightforward C/C++ library to interface with the NVIDIA Jetson TX2 Development Kit GPIO pins.

Modified based on https://github.com/jetsonhacks/jetsonTX1GPIO


Based on Software by RidgeRun
https://developer.ridgerun.com/wiki/index.php/Gpio-int-test.c
 * Copyright (c) 2011, RidgeRun
 * All rights reserved.

and ideas from Derek Malloy Copyright (c) 2012
https://github.com/derekmolloy/beaglebone

exampleGPIApp.cpp describes a simple usage case using a tactile button and LED as input and output.


# Description
To add more GPIO pins, modify jetsonGPIO.h and add pin numbers you want.

* Example: 
setup and initialize GPIO388 (Pin37) as output pin on TX2:
```
jetsonTX2GPIONumber control = gpio388; 
gpioExport(control);
gpioSetDirection(control,outputPin);

gpioSetValue(redLED, on);     //Pull high
gpioSetValue(redLED, off);    //Pull low
```

That's it, very easy. Hope this file helps.

