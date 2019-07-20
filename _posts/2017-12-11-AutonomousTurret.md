---
layout: posts
title: Autonomous Turret
description: A Portal game inspired, face tracking autonomous turret
tags: Projects
header:
  teaser: assets/images/seniorProjectCropped.jpg
---

Inspired by machine learning, embedded systems, and fun. I teamed up with my classmate [Mason Rawson](https://www.linkedin.com/in/masonrawson "Mason Rawson LinkedIn"), to make an autonomous turret. Specifically, we made one modeled after the turrets from the game Portal.

![alt text](/assets/images/portalTurret.jpg)

---

## Sentry Turret

![alt text](/assets/images/AutonomosTurretActual.JPG)


---


## Remote Controller

![alt text](/assets/images/AutonomousTurretControllerFront.jpg)

<p align="center">
	<img src="/assets/images/AutonomousTurret.gif" width="350" height ="350" />
</p>


---

## Hardware Overview


### High Level Overview
<p align="center">
	<img src="/assets/images/AutonomousTurretOverview.jpg"/>
</p>



### Sentry Overview
<p align="center">
	<img src="/assets/images/AutonomousTurretSentryOverview.jpg"/>
</p>



### Remote Controller Overview
<p align="center">
	<img src="/assets/images/AutonomousTurretControllerOverview.jpg"/>
</p>



### Full System Level Overview
<p align="center">
	<img src="/assets/images/AutonomousTurretFullOverview.jpg"/>
</p>


---

## Software Overview

### When in Manual Mode
<p align="center">
	<img src="/assets/images/AutonomousTurretFlowChart0.jpg"/>
</p>

### When in Autonomous Mode
<p align="center">
	<img src="/assets/images/AutonomousTurretFlowChart1.jpg"/>
</p>


---

## Videos

<p align="center">
	<img src="/assets/images/AutonomousTurretFindingFace.gif" width="350" height ="350" />
</p>

<p align="center">
	<img src="/assets/images/AutonomousTurretAiming.gif" width="350" height ="350" />
</p>

<p align="center">
	<img src="/assets/images/AutonomousTurretShooting.gif" width="350" height ="350" />
</p>


---

## Accomplishments

Through this project we were able to accomplish:

1. Creating 3 custom PCBs in Altium (Main, Power distribution, Controller)

2. Creating a real time system using interupts and timed synchronized events

3. Using two MSP432 microprocessers to process the main board and controller

4. Having multiple modes (Autonomous and Remote Controlled)

5. Using a Raspberry Pi containing OpenCV to obtain face pixel location 

6. Translating pixel location to an aim angle on pan tilt mounts

7. Integrating servo pan tilt motors to aim nerf guns via pulse width modulation

8. Using an ESP8266 (wifi node) to communicate the control position and activation from controller board to main board

9. Designing and 3D printing custom mounts to hold nerf guns to pan tilt mounts and push arm for stepper motors 

10. Shooting nerf guns via mounted stepper motors


---

## Schematics

<figure class="half">
	<img src="/assets/images/AutonomousTurretSchematic0.jpg">
	<img src="/assets/images/AutonomousTurretSchematic1.jpg">
	<figcaption>Turret Main Board Schematic</figcaption>
</figure>

<figure class="half">
	<img src="/assets/images/AutonomousTurretSchematic2.jpg">
	<img src="/assets/images/AutonomousTurretSchematic3.jpg">
	<figcaption>Turret Main Board Schematic</figcaption>
</figure>

<figure class="half">
	<img src="/assets/images/AutonomousTurretSchematic4.jpg">
	<img src="/assets/images/AutonomousTurretSchematic5.jpg">
	<figcaption>Controller Board Schematic</figcaption>
</figure>

---

## PCBs

<figure class="half">
	<img src="/assets/images/AutonomousTurretPCB0.jpg">
	<img src="/assets/images/AutonomousTurretPCB.jpg">
	<figcaption>Controller PCB and Main Turret PCB</figcaption>
</figure>


If you would like to check out the project report please check out my [github repository](https://github.com/jbocinsky/PortalTurret "Autonomous Turret Repository").


Thanks,  
James

---