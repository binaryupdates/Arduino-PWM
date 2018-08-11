# Pulse Width Modulation: PWM in Arduino
<p>The PWM is cool technique, in which we can Generate Analog Result by Digital Input. Arduino allows us to implement PWM in several ways.</p>

<p>The question is where it can be used; Let me give you one example. We have seen very often to turn LED/Light, <b>ON</b> - <b>OFF</b>. But then what, if we don't want LED to turn ON - OFF. Rather we want to precisely control the brightness of an LED/Light. And this can be done with Pulse Width Modulation Technique <b>(i.e PWM)</b>. Using <b>PWM</b> we can control the <b>Duty Cycle</b> of a <b>Clock.</b> Which in result control brightness of an LED/Light.</p>

<p>Let's look at the picture where we have Clock Frequency in the form of Square Wave. This is <b>Period</b> and <b>Pulse Width</b></p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/pwm_1.png" alt="display this" width=300 height=100 >

<p>Now Let's first understand Period of Clock (Tcycle). It is used to determine speed of our Microcontroller. This Clock is represented as Clock cycle, which is the amount of time between two pulses of an Oscillator. And then Duty cycle is an fraction of time in which signal or system is active.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/clock_period.png" alt="display this" width=200 height=100 >

<b>Arduino PWM Frequency is 500 Hertz ~ 2 milliseconds</b>

The Arduino's programming language makes PWM easy to use. Arduino supports function called <b>analogWrite(pin, dutyCycle)</b>. Where <b>Duty Cycles</b> value will be between <b>0 to 255</b> and <b>Pin</b> will be one of the <b>PWM pins (3, 5, 6, 9, 10, or 11)</b>on Arduino Uno board. 

<b>Note</b>
This PWM in Arduino doesn't provide any control over Frequency. Even if the name os function is <b>analogWrite(pin, dutyCycle)</b>, the output is a digital signal, often referred it as a <b>Square Wave.</b>

We have talked enough. Let’s implement it in live project. Where we will Change the Brightness of an LED Connected to <b>Pin No: 9</b> of an Arduino Uno

<b>STEP 1:</b>
<p>Let's write a code where we will just add <b>analogWrite(9, 0)</b> to the existing Sketch. With value <b>0</b> we will achieve <b>0% Duty Cycle</b> means LED Stays OFF.</p>

<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step1.gif" alt="display this" width=300 height=100 >


<b>STEP 2:</b>
<p>Now as soon as we change value from <b>0</b> to <b>64</b> in a function <b>analogWrite(9, 64)</b> in the existing Sketch. We will achieve <b>25% Duty Cycle</b> means 1/4th or Quarter of the Highest Brightness of an LED.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step2.gif" alt="display this" width=300 height=100 >


<b>STEP 3:</b>
<p>Let's increase the value of Duty Cycle to 127 in <b>analogWrite(9, 127)</b> function. With value <b>127</b> we will achieve <b>50% Duty Cycle</b> means <b>50%</b> Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step3.gif" alt="display this" width=300 height=100 >


<b>STEP 4:</b>
<p>Let's move even further by making Duty Cycle to 191 in function <b>analogWrite(9, 191)</b>. With this value will achieve <b>75% Duty Cycle</b> means <b>75% </b> of an Highest Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step4.gif" alt="display this" width=300 height=100 >


<b>STEP 5:</b>
<p>Finally we will insert <b>255</b> into function <b>analogWrite(9, 255)</b>. With value 255 we will achieve <b>100% Duty Cycle</b> means Highest possible Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step5.gif" alt="display this" width=300 height=100 >




