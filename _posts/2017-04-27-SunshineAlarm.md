---
layout: posts
title: Project - Sunshine Alarm
description: An alarm that wakes you up slowly with light
tags: Projects
header:
  teaser: assets/images/SeniorProject1AlarmPCB.PNG
---

For my first senior project, unlike most students, I created something that I could use in my day to day life. I often wake up before the sun rises to get a head start on the day, but found myself having a tough time getting out of bed. I knew if I could wake more naturally I would have a better day. So I decided to make a light alarm.


<p align="center">
	<img src="/assets/images/SeniorProject1AlarmPCB.PNG">
</p>


The alarm's main components consisted of the following:

* A personally developed PCB

* A 40 pin PIC Microprocessor

* A RTC

* An LCD display

* Multiple Buttons and Potentiometers for user's input

* A very bright LED

Full Bill of Materials for the project:


<p align="center">
	<img src="/assets/images/SunshineAlarmBOM.PNG">
</p>

---

Through this project I was able to accomplish:

1. Writing an I2C library

2. Setting up a multiple state embedded processor 

3. Accessing register information from an RTC

4. Displaying current state information on LCD

5. Using pulse width modulation to control LED brightness

6. Power regulation through an LDO and capacitors

7. Powering a semi "high" current LED through a power mosfet

9. Using ADCs to read potentiometers (selectors)

10. Using the DAC to conrtol brightness of LCD

11. Use interrupts to receive button presses

<figure class="half">
	<img src="/assets/images/SunshineAlarmPCB1.PNG">
	<img src="/assets/images/SunshineAlarmPCB2.PNG">
	<figcaption>PCB Design and Layer Pours</figcaption>
</figure>


---

If you would like to check out the detailed project report or source code please check out my [github repository](https://github.com/jbocinsky/SunshineAlarm "Sunshine Alarm Repository").