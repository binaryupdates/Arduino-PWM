# Pulse Width Modulation: PWM in Arduino
<p>The PWM is cool technique and can be implemented in Arduino is several ways.</p>

<p>The question is where it can be used; Let me give you one example. We have seen very often to turn LED/Light, <b>ON</b> or <b>OFF</b>. But then what, if we don't want to turn either ON or OFF. Rather we want to precisely control brightness of an LED/Light. With <b>PWM</b> we can control the <b>Duty Cycle</b> of a <b>Clock.</b></p>

<p>Let's look at the picture where we have Clock Frequency in the form of Square Wave. This is <b>Period</b> and <b>Pulse Width</b></p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/pwm_1.png" alt="display this" width=300 height=100 >

<p>Now Let's first understand Period of Clock (Tcycle). It is used to determine speed of our Microcontroller. This Clock is represented as Clock cycle, which is the amount of time between two pulses of an Oscillator. And then Duty cycle is an fraction of time in which signal or system is active.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/clock_period.png" alt="display this" width=200 height=100 >


Arduino Support a function called analogWrite(pin, dutyCycle). Where Duty Cycles value between 0 to 255 and Pin will be one of the PWM pins (3, 5, 6, 9, 10, or 11)on Arduino Uno board.

Let’s do live Demo to Change Brightness of an LED Connected to Pin No: 9 of an Arduino Uno

<b>STEP 1:</b>
<p>Let's write a code where we will just add <b>analogWrite(9, 0)</b> to the existing Sketch. With value <b>0</b> we will achieve <b>0% Duty Cycle</b> means LED Stays OFF.</p>

<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step1.gif" alt="display this" width=300 height=100 >


<b>STEP 2:</b>
<p>Now as soon as we change value from <b>0</b> to <b>64</b> in a function <b>analogWrite(9, 64)</b> in the existing Sketch. We will achieve <b>25% Duty Cycle<b> means 1/4th or Quarter of the Highest Brightness of an LED.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step2.gif" alt="display this" width=300 height=100 >


<b>STEP 3:</b>
<p>This is an Simple code where we will just add <b>analogWrite(9, 127)</b> to the existing Sketch. With value 127 we will achieve 50% Duty Cycle means Half of the Highest Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step3.gif" alt="display this" width=300 height=100 >


<b>STEP 4:</b>
<p>This is an Simple code where we will just add <b>analogWrite(9, 191)</b> to the existing Sketch. With value 191. We will achieve 75% Duty Cycle means 75% of Highest Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step4.gif" alt="display this" width=300 height=100 >


<b>STEP 5:</b>
<p>This is an Simple code where we will just add <b>analogWrite(9, 255)</b> to the existing Sketch. With value 255 we will achieve 100% Duty Cycle means Highest Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step5.gif" alt="display this" width=300 height=100 >


