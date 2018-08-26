# Pulse Width Modulation: PWM in Arduino
<p>The PWM is cool technique, in which we can Generate Analog Result means Analog Voltage by Digital Input. Arduino allows us to implement PWM in several ways.</p>

<p>The question is where it can be used; Let me give you one example. We have seen very often to turn LED/Light, <b>ON</b> - <b>OFF</b>. But then what, if we don't want LED to turn ON - OFF. Rather we want to precisely control the brightness of an LED/Light. And this can be done with Pulse Width Modulation Technique <b>(i.e PWM)</b>. Using <b>PWM</b> we can control the <b>Duty Cycle</b> of a <b>Clock.</b> Which in result control brightness of an LED/Light.</p>

<p>Let's look at the picture where we have Clock Frequency in the form of Square Wave. This is <b>Period</b> and <b>Pulse Width</b></p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/pwm_1.png" alt="display this" width=300 height=100 >

<p>Now Let's first understand Period of Clock (Tcycle). It is used to determine speed of our Microcontroller. This Clock is represented as Clock cycle, which is the amount of time between two pulses of an Oscillator. And then Duty cycle is an fraction of time in which signal or system is active.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/clock_period.png" alt="display this" width=200 height=100 >

<p><b>Arduino PWM Frequency is 500 Hertz ~ 2 milliseconds</b></p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/Ton%20Toff%20relation.jpg" alt="display this" width=200 height=100 >
</p>

<b>Note</b>
<p>This PWM in Arduino doesn't provide any control over Frequency. Even if the name os function is <b>analogWrite(pin, dutyCycle)</b>, the output is a digital signal, often referred it as a <b>Square Wave.</b></p>

<p>We have talked enough. Let’s implement it in live project. Where we will Change the Brightness of an LED Connected to <b>Pin No: 9</b> of an Arduino Uno</p>

<p>Lets connect an <b>RED LED</b> to <b>Arduino Pin 9</b>, make sure we must conenct longer leg of LED connects to Pin No:9 and Shorter leg goes to <b>Ground</b></p>

<b>STEP 1:</b>
<p>Let's write a code where we will just write <b>64</b> in a function <b>analogWrite(9, 64)</b> in the existing Sketch. With value <b>64</b>. We will achieve <b>25% Duty Cycle</b> means LED will glow 1/4th or Quarter of the Highest Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step2.gif" alt="display this" width=300 height=100 >


<b>STEP 2:</b>
<p>Now as soon as we increase the value of Duty Cycle to 127 in <b>analogWrite(9, 127)</b> function. With value <b>127</b> we will achieve <b>50% Duty Cycle</b> means <b>50%</b> Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step3.gif" alt="display this" width=300 height=100 >


<b>STEP 3:</b>
<p>Let's write value <b>191</b> in function <b>analogWrite(9, 191)</b>. With this value will achieve <b>75% Duty Cycle</b> means <b>75% </b> of an Highest Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step4.gif" alt="display this" width=300 height=100 >


<b>STEP 4:</b>
<p>Let's insert value <b>255</b> into function <b>analogWrite(9, 255)</b>. With value 255 we will achieve <b>100% Duty Cycle</b> means Highest possible Brightness.</p>
<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step5.gif" alt="display this" width=300 height=100 >

<b>STEP 5:</b>
<p>Finally Let's write <b>0</b> to function <b>analogWrite(9, 0)</b> to the existing Sketch. With value <b>0</b> we will achieve <b>0% Duty Cycle</b> means LED will turn OFF.</p>

<img src="https://github.com/binaryupdates/Arduino-PWM/blob/master/step1.gif" alt="display this" width=300 height=100 >

<p>So now we have seen how one can change <b>Duty Cycle</b> of a <b>Clock</b> and change the Brightness of an LED. Lets write a program which will vary duty cycle to generate variable voltage with an delay of every <b>1 Second</b>. This will allows us to create dimming effect with LED.</p>




