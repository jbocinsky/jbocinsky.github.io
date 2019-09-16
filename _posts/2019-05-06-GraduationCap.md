---
layout: single
title: LED Graduation Cap
description: Tutorial to create a LED matrix graduation cap that plays GIFs and scrolls text using a teensy, powerbank, microSD card, and LED matrix.
tags: Projects
header:
  teaser: assets/images/ThesisGulfportRGB.jpg
toc: true
toc_label: "Quick Links"
toc_icon: "list"
---

<p align="center">
	<img src="/assets/images/MSGradVid.gif" width="400" height ="400" />
</p>

In this project I created a graduation cap that I could wear during graduation to display GIFs and text to the audience. This post showcases my graduation cap and as well shows others how to do this themselves. The goal is to create something fun for the audience to look at that is 100% portable and hidden. With this, the design requirements are:

1. Obscure while off
2. Stay powered for more than 3 hours
3. Display both text and GIFs
4. Have a way to turn it on from my pocket
5. Be light weight and comfortable enough to wear

## Parts needed

1. 32 x 32 LED Matrix board from adafruit. [Link](https://www.adafruit.com/product/2026?gclid=EAIaIQobChMI6cq9jMnV5AIVho3ICh3_gAaSEAQYASABEgJtnfD_BwE)
2. SmartMatrix SmartLED Shield (V4) for Teensy 3. [Link](https://www.adafruit.com/product/1902)
3. Teensy 3.6 [Link](https://www.adafruit.com/product/3266)
4. MicroSD card, at least 4 GB
5. Headers
6. Small wire for soldering components together
7. Power bank capable of supplying 2A. [Anker PowerCore 20100mAh](https://www.amazon.com/Portable-Charger-Anker-PowerCore-20100mAh/dp/B00X5RV14Y/ref=sr_1_3?keywords=battery+power+bank&qid=1568653865&s=gateway&sr=8-3)
8. Thicker wires for soldering power cables for power bank
9. 1 USB cable at least 3 feet long
10. Solder and soldering iron
11. Electrical tape or heat shrink tube
12. Scisors
13. Hot glue gun
14. Transparent black fabric from materials store like JOANNs

## Cap Disassembly

First we need to dissassemble the cap to see what we are working with. Most caps are similar where it is simply some fabric wrapped around coardboard with a thumbnail type connection for the stump at the center of the cap where the tassel attaches. As well a small separate piece of fabric glued to the base that holds the cap to your head. Here you can see what the cap looks like disassembled. Make sure when you disassemble this yourself you preserve the condition of the separate piece that holds the cap to your head. We will reuse this piece.

## Code

Fortunately I was able to find someone who had already implemented code for the Teensy to cycle through GIF files on a microSD card and write them to the LED Matrix via the SmartMatrix Shield. This was a huge time saver for me and I want to give a big thank you to INSERT NAME HERE for providing your code on github. His github with the original code can be found here: [Github](LinkHere).

I have modified his code slightly and my code can be found here: [Github](LinkHere). My code modifies:

- The probability of a GIF showing vs a text
- Making GIFs display in order, not random order
- The colors of the text
- The actual text itself

If you want to endeavor into this project yourself. You will need to modify the code to display text of your own.

## Micro SD card GIFs

To use GIFs on the LED matrix, the GIFs need to be formatted to fit the screen. Namely, the GIFs need to be a perfect square and be 32 x 32 pixels. I used this [adafruit_documentation]({{ site.url }}/assets/images/smartmatrix-animated-gif-player-documentation.pdf) to format the GIFs to conform to the LED matrix. You'll find on page 16 how to do so yourself by using [ezgif.com](www.ezgif.com).

Once you've formatted the GIFs as specified you will need to place them on your microSD card in the folder specified in the code. Then the teensy will search that folder to read the GIFs in for displaying them.

## Soldering Electronics

Before performing soldering consider testing the functionality of your code, GIFs, and electronic connections by using the existing connections on the board. This will help make you confident that you are soldering your components together before you do so.

### Desoldering Connectors

Next we need to solder our electronics together to make our cap as flat as possible. You are able to use the electronics specified without soldering, but because I wanted the cap to be as obscure as possible I decided to solder the wires together to get a more flush solution.

In order to solder our components together, we first need to remove the extra plastic housing on the bottom and desolder the original connectors on the LED matrix. The housing can be removed by unscrewing the screws on the top of the LED matrix. These screws will not be needed anymore. The connectors can be removed by holding a soldering iron next to the pads of the connectors and lifting up on the connectors themselves. Before doing this though, use plyers to lift up on the plastic parts of the connectors to remove the plastic before desoldering the metal parts of the connectors one by one. Be careful not to rip off any of the pads by lifting too firmly before the solder is liquified when performing this step.

### Soldering Components

Now we can now solder our components together to the board via jumper wires. Our objective here is to make this as flat as possible. We can do this by offsetting the shield and soldering jumper wires from the shield to the LED matrix. This can be seen in the image below. If you follow the wires in the image, you will see that the wires are in order with the pads on the board.

Now that we have this in place you can also solder the headers on to the Teensy board. This can simply be plugged into the shield itself once the headers have been soldered. Lastly you can place your microSD card into the Teensy so it is ready to go once we get the power cables fabricated.

### Fabricating Power Cable

Lastly, we need to fabricate a power cable to power our LED matrix from the powerbank that will be in our pocket. The power cables will be soldererd to the LED matrix and have a usb connector at the other end so we can plub it in to the powerbank. This power cable will run down the back of our cap, inside the liner around our head, and into our gown to stay obscure and as minimal as possible. When performing this step, it is very important you solder the power wires to the right pads so not to damage your LED matrix.

Our fabricated power cable is going to use a usb cable so we have a way to plug into the powerbank. By splicing into the usb cable we can pull out the power and ground wires of the usb cable and extend these to solder onto our LED matrix pads. In my solution I used two usb cables leading to one set of power and ground wires, but I found only one usb cable was necessary to power the system.

To create this power cable you need to cut the usb cable as far away from the usb plug as possible and strip out the black and red wire. You can cut away the shielding and extra data wires to make it easier to work with. Once these usb power/ground wires are accessible we can solder our addititonaly thicker wires to the LED matrix and as well to these usb wires. Once this is done, simply add electrical tape or heat shrink tubing to make the connection safe from shorting against each other.

Lastly, this is not necessary, but I had some flexible electical tubing laying around, so I added this around the power cables to make them more durable and obscure when running down the back.

## Testing Functionality

Again, I highly suggest testing as much as possible while you build your cap and even test everything works before you start solding by just using the original existing connectors on the cap. Before we assemble the cap back together though we want to make sure our cap is working as expected. Go ahead and plug in your powerbank and see your hard, patient work come together.

## Assembly

Finally we can assemble our cap back together. First we want to make sure to use a more transparent fabric so our LEDs can shine through our cap. A fabric like this can be found at JOANNs. I just used the flashlight funcitonality on my phone to test out different fabrics. I also picked out a stretchy fabric so it could be tightly wrapped around the cardboard.

The original cardboard piece will be reused, but we do need to cut out some pieces of it to make room for the electronics that will hang off the underside of the board. By doing this we can obtain a cap that is more flat. This includes making cutouts for the capacitors, Teensy board and matrix, and the power cables. Keep in mind, the power cable will need to be routed towards the center of the cardboard so it can be run down the back of the inside liner around our head.

Next we can place the LED matrix into place on the cardboard, pulling the power cable through the cutout. Once it is centered and you are happy with the placement you can use a hot glue gun or other adhesive to glue the underside of the LED matrix to the top of the cardboard. During this step I also tested the weight balance of the hat to slightly move the whole system towards the front since the back was more heavy.

Next, with the stretchy transparent fabric, cut it to be roughly the same shape as the original fabric that was on top of the cap. It should be slightly larger to allow room for the electronics and LED matrix. Then fold the fabric over the cardboard as shown and use a hot glue gun or other adhesive to adhear to the cardboard.

Then, we can cut a hole in the back portion of the head liner carboard that sits on top of the head liner to feed the power cable through. Next, we can carefully glue on the head liner cardboard to the bottom of our graduation cap, being careful not to push too much on our electronics. Finally, align the gradutation tassel nob to the center of the top of the cap and glue down.

## Final Results

Here you can see the final results of our cap. It's certainly fun to play with and will remain on my wall for the future. Feel free to check out these videos showing off the final solution.

Thanks,
James

---
