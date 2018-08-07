# Arduino-PWM
<p>The PWM is cool technique and can be implemented in Arduino is several ways.</p>

<p>The question is where it can be used; Let me give you one example. We have seen very often to turn LED/Light, ON or OFF. But then what, if we don't want to turn either ON or OFF. Rather we want to control voltage so that we can control brightness of an LED/Light. With PWM we can control the Duty Cycle of an Period of Clock. Now what is Duty Cycle and Period.</p>

<p>Now Let's first understand Period of Clock (Tcycle). It is used to determine speed of our Microcontroller. This Clock is represented as Clock cycle, which is the amount of time between two pulses of an Oscillator. And then Duty cycle is an fraction of time in which signal or system is active.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/clock_period.png" alt="display this" width=200 height=100 >

Arduino Support a function called analogWrite(pin, dutyCycle). Where Duty Cycles value between 0 to 255 and Pin will be one of the PWM pins (3, 5, 6, 9, 10, or 11)on Arduino Uno board.

Let’s do live Demo to Change Brightness of an LED Connected to Pin No: 9 of an Arduino Uno

<b>STEP 1:</b>
This is an Simple code where we will just add analogWrite(9, 0) to the existing Sketch. With value 0 we will achieve 0% Duty Cycle means LED remains Stays OFF.




<b>STEP 2:</b>
This is an Simple code where we will just add analogWrite(9, 64) to the existing Sketch. With value 64 we will achieve 25% Duty Cycle means 1/4th of the Highest Brightness.




<b>STEP 3:</b>
This is an Simple code where we will just add analogWrite(9, 127) to the existing Sketch. With value 127 we will achieve 50% Duty Cycle means Half of the Highest Brightness.



<b>STEP 4:</b>
This is an Simple code where we will just add analogWrite(9, 191) to the existing Sketch. With value 191. We will achieve 75% Duty Cycle means 75% of Highest Brightness.



<b>STEP 5:</b>
This is an Simple code where we will just add analogWrite(9, 255) to the existing Sketch. With value 255 we will achieve 100% Duty Cycle means Highest Brightness.




