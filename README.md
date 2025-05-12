# ece3301l-lab-12-fan-speed-measurement-with-speed-control-through-pwm-solved
**TO GET THIS SOLUTION VISIT:** [ECE3301L LAB 12-Fan Speed measurement with Speed control through PWM Solved](https://www.ankitcodinghub.com/product/ece3301l-lab-12-fan-speed-measurement-with-speed-control-through-pwm-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91464&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE3301L LAB 12-Fan Speed measurement with Speed control through PWM Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
LAB 12: Fan Speed measurement with Speed control through PWM

The goal of this lab is to control the speed of a fan using PWM (Pulse Width Modulation) by varying an input voltage. Beside the speed control feature, this lab will also measure the speed that the fan is rotating by capturing the number of tach pulses from the fan. The result will be displayed on the TFT panel.

Part A) Fixed time-based measurements using a timer

We will be using the fan that I have provided in the kit along with a wall plug +12V power supply. The fan has four wires:

<ol>
<li>1) &nbsp;Black wire: Ground pin to be connected to the power supply’s ground pin and also to the system’s ground.</li>
<li>2) &nbsp;Y ellow wire: +12V pin to be connected to the power supply’ s +12V .</li>
<li>3) &nbsp;Green wire: Tach signal providing a pulse when the fan makes 1⁄2 the revolution.</li>
<li>4) &nbsp;Blue wire: PWM wire to control the speed of the fan.</li>
</ol>
To measure the speed of a fan, we just need to count the number of pulses generated on the Tach signal (green wire). When a fan makes a full revolution, a total of two (2) pulses will be generated. We now use a counter to count the number of pulses within a fixed period of time. Let us use the timer T1 as a counter. To setup it up as a timer, use the datasheet of the PIC18F4620:

http://ww1.microchip.com/downloads/en/devicedoc/39626e.pdf

and go to chapter 12 starting on page 137 and look at the register T3CON. Set the following:

Bit 7: RD16 – We don’t need 16-bit operations Bits 6,3: Ignore these two bits

Bit 5-4: No prescaler used (1:1)

Bit 2: Synchronize to external clock

Bit 1: External clock is from T13CKI Bit 0: Disable Timer 3 first

Derive the correct value for T3CON. Initialize T3CON in the main initialization routine.

We need to write next a routine called int get_RPM() to measure and to return the RPM (revolution per minute) of the fan. We know that RPM = 60 * RPS where RPS is revolution per second. To get RPS, we can count the number of pulses from the Tach signal per second and

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
since there are 2 tach pulses per revolution, then RPS will be half the amount of pulses counted in one second.

</div>
</div>
<div class="layoutArea">
<div class="column">
int get_RPM() {

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
int RPS = TMR3L / 2;

TMR3L = 0; return (RPS * 60);

</div>
<div class="column">
// read the count. Since there are 2 pulses per rev // then RPS = count /2

// clear out the count

// return RPM = 60 * RPS

</div>
</div>
<div class="layoutArea">
<div class="column">
Put this routine in the provided ‘Fan_Support.c’.

Next, take the program used on lab 11 and add the line: rpm = get_RPM(); when a new second has been detected. Add to the printf statement the value of RPM to display the speed of the fan.

Note: We need to turn on the fan for this part of the lab. Set the lines:

FAN_EN = 1; FAN_PWM = 1;

to turn on the FET in order to get the fan going. We will remove this line later on.

Part B) Fan Speed control

Part B1)

To control the speed of the fan, we are going to use the signal ‘PWM_Pulse’. This signal uses the principle of duty cycle to increase or decrease the speed. A signal with a duty cycle has a pulse that is set high for a fixed amount of time with respect to the entire period of the signal. Here are some examples:

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
The concept of PWM allows the use of duty cycle to vary the speed. A PWM with 50% duty cycle will force the fan to run a half-speed. If PWM is set to 1 (100 % duty cycle), the fan will run at full speed. On the other hand, if PWM is set to 0, then the fan will rotate at its lowest speed.

The provided fan can take a PWM pulse with a frequency range from 18Khz to 30 Khz. Let assume that we are going to use 25 Khz as the frequency.

Next, let us use the following link:

http://www.micro-examples.com/public/microex-navig/doc/097-pwm-calculator.html

Enter the value of 8 Mhz for the PIC’s operating frequency.

Next, enter 25000 for frequency of the PWM_pulse. This is the frequency required by the fan when PWM is used. By varying the value in duty cycle box from 0 to 99, you should see the value of the registers needed to be modified – PR2, T2CON, CCP1CON and CCPR1L – being changed accordingly.

I have compiled a routine that will change those registers based on a specified value of the duty cycle:

void do_update_pwm(char duty_cycle) {

</div>
</div>
<div class="layoutArea">
<div class="column">
float dc_f;

int dc_I;

PR2 = 0b00000100 ;

T2CON = 0b00000111 ; //

</div>
</div>
<div class="layoutArea">
<div class="column">
// set the frequency for 25 Khz

// calculate factor of duty cycle versus a 25 Khz // signal

// get the integer part

// round up function

Place this routine in the ‘Fan_Support.c’ file.

Next, go back to the program developed on part A) above. Before, the while(1) loop, place the following lines:

duty_cycle = 50; do_update_pwm(duty_cycle) ;

Change the different value of ‘duty_cycle’ by modifying the value and rerun the program. Observe on TeraTerm that the fan runs faster or slower if ‘duty_cycle’ is increased or decreased.

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
dc_f = ( 4.0 * duty_cycle / 20.0) ;

</div>
</div>
<div class="layoutArea">
<div class="column">
dc_I = (int) dc_f;

if (dc_I &gt; duty_cycle) dc_I++;

CCP1CON = ((dc_I &amp; 0x03) &lt;&lt; 4) | 0b00001100; CCPR1L = (dc_I) &gt;&gt; 2;

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Part B3)

When the above task works successfully, then implement two new functions to control the outputs of the two RGB LEDs D1 and D2:

LED D1: void Set_DC_RGB(int duty_cycle) LED D2: void Set_RPM_RGB(int rpm)

Here are the requirements for the routine Set_DC_RGB(int duty_cycle):

<ol>
<li>a) &nbsp;If duty cycle = 0, no color to be displayed</li>
<li>b) &nbsp;Ifdutycycle&gt;0and&lt;33,colorisRED</li>
<li>c) &nbsp;If duty cycle &gt;= 33 and &lt; 66, color is YELLOW</li>
<li>d) &nbsp;If duty cycle &gt;= 67, color is GREEN</li>
</ol>
Here are the requirements for the routine Set_RPM_RGB(int rpm):

<ol>
<li>a) &nbsp;If rpm = 0, no color to be displayed</li>
<li>b) &nbsp;Ifrpm&gt;0and&lt;1200,colorisRED</li>
<li>c) &nbsp;If rpm &gt;=1200 and &lt; 2400, color is PURPLE</li>
<li>d) &nbsp;If rpm &gt;= 2400, color is BLUE</li>
</ol>
Part C) Fan Operational Control using remote control

Now we are going to use the remote control that we have developed on lab 10 to control the operations of the fan. Three buttons on the remote will be used:

<ul>
<li>Button ‘-‘ or button number 6</li>
<li>Button ‘+’ or button number 7</li>
<li>Button ‘Play/Pause’ or button number 5
The code for the ‘Interrupt.c’ done in lab 11 should be moved into this project. Based on the code on lab 10, use the variable ‘found’ to do the following:

<ul>
<li>If found is ‘Play/Pause’ call the function Toggle_Fan()</li>
<li>If found is ‘-‘ call the function Decrease_Speed()</li>
<li>If found is ‘+’ call the function Increase_Speed()
Next, we will need to implement those three functions to be placed in the Fan_Support.c file.

• Toggle_Fan():

o If the variable ‘Fan’ is 1, call function Turn_On_Fan(); o Else call function Turn_Off_Fan()
</li>
</ul>
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Write up the code for both Turn_On_Fan() and Turn_Off_Fan() to be also placed in the Fan_Support.c file

o Turn_On_Fan():

 Set the variable Fan to be 1

 Call function do_update_pwm(duty_cycle) to set the proper speed  Turn on the fan using FAN_EN

 Turn on the fan LED FAN_LED

o Turn_Off_Fan():

 Set the variable Fan to be 0

 Turn off the fan using FAN_EN  Turn off the fan LED FAN_LED

• Increase_Speed():

o Check if duty_cycle is at 100

 If 100, then generate two beep codes using Do_Beep() function  If not, then increase duty_cycle by 5 and change the pwm

• Decrease_Speed():

o Check if duty_cycle is at 0

 If 0, then generate two beep codes using Do_Beep() function  If not, then decrease duty_cycle by 5 and change the pwm

Note: The function Do_Beep() is simply the sequence of Activate_Beep, Wait_One_Sec() (for loop), Deactivate_Beep() and followed by a call to re-initialize the pwm because the Activate_Beep() function will destroy the original pwm.

Run the program and use the remote control to turn on/off the fan and to increase/decrease the speed. Make sure to have the program starts with the fan in the off state (FAN_EN = 0) and the duty_cycle set at 50.

Part D) Fan Operation Status on LCD

Make sure that the file ‘Main_Screen.c’ is now included in the project. Do the following:

<ol>
<li>1) &nbsp;Place the line Initialize_Screen(); after the line Do_Init();</li>
<li>2) &nbsp;Place the line Update_Screen(); after the printf lines in the while (1) loop</li>
<li>3) &nbsp;Fill the missing lines in the Update_Screen() located in Main_Screen.c file.</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
When these tasks are completed, the LCD will display the same information shown on TeraTerm.

Part E) Time Reloading

Add a simple code in the check of the remote control’s buttons. If the button is the ‘EQ’ or button 8, then call the routine to reload the time into the RTC.

</div>
</div>
</div>
