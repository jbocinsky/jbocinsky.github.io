---
layout: posts
title: Project - Sunshine Alarm
description: An alarm that wakes you up slowly with light
tags: Projects
header:
  teaser: assets/images/SeniorProject1AlarmPCB.PNG
---

For my first senior project, unlike most students, I created something that I could use in my day to day life. I often wake up before the sun rises to get a head start on the day, but found myself having a tough time getting out of bed. I knew if I could wake more naturally I would have a better day. So I decided to make a light alarm clock.


<p align="center">
	<img src="/assets/images/SeniorProject1AlarmPCB.PNG">
</p>


The alarm's core components consisted of the following:

* A personally developed PCB

* A 40 pin PIC microprocessor

* A RTC

* A LCD display

* Multiple buttons and potentiometers for user's input

* A very bright LED

---

Full Bill of Materials for the project:


<p align="center">
	<img src="/assets/images/SunshineAlarmBOM.PNG">
</p>

---

Through this project I was able to accomplish:

1. Creating a custom PCB in Altium

2. Setting up a multiple state embedded processor 

3. Writing a I2C library for the PIC

4. Accessing register information from a RTC

5. Displaying current state information on LCD

6. Controling LED brightness with pulse width modulation

7. Power regulation through a LDO and capacitors

8. Powering a semi "high" current LED through a power mosfet

9. Using ADCs to read potentiometers (selectors)

10. Using a DAC to conrtol brightness of LCD

11. Using interrupts to receive button presses

<figure class="half">
	<img src="/assets/images/SunshineAlarmPCB1.PNG">
	<img src="/assets/images/SunshineAlarmPCB2.PNG">
	<figcaption>PCB design and layer pours</figcaption>
</figure>


If you would like to check out the detailed project report or source code please check out my [github repository](https://github.com/jbocinsky/SunshineAlarm "Sunshine Alarm Repository").


Thanks,  
James

---