---
title: "CodeBoard"
author: "Alfonsoce11"
description: "A keyboard specially made for coding with quicker access to common characters."
created_at: "2024-06-18"
---

**Total Time Spent: about 28h**

# June 19th: Decided on the layout and created the schematic.
I wanted it to have a good layout because once I start making it I wouldn't be able to change the layout without restarting completely so I ended up spending like more 2 hours deciding on the layout. 

At first I was planning on trying to change the normal keyboard layout to optimize it for coding. Then I realized that it would actually make it slower for me if I changed the position of keys or something so instead I decided it would make more sense to not change the layout very much and instead add common coding characters to the right side, kinda like the numpad but for coding. 

For the coding characters to the side I decided to add characters I use often in coding and that I think most people use often. I put some basic operators, some other common symbols I use, and all of the different brackets. For most of the brackets and quotation marks I decided I'm gonna make them macros so that I can put the curser bewteen them. I didn't for the < and > symbols because they are only really used as brackets in HTML while all other languages use them for conditions so I figured it would make more sense to separate them. 

I also figured I should have navigation keys but I didn't want to put them in the normal layout because I didn't want to make it too long. First I though of putting all the navigation keys on top of each other but then I decided that would probably be pretty awkward to use. Then I decided I could put them in a square where the up and down arrows and on top and the left and right buttons are below and this would also leave a perfect spot for a microcontroller. 

This is the layout I finally decided on:
<img width="1071" alt="Screenshot 2025-06-19 at 1 17 02 PM" src="https://github.com/user-attachments/assets/4acc408e-9cfc-4872-a184-f66ff669f4d9" />

Now that I decided on the layout I started working on the schematic. I decided to use a raspberry pi pico because its cheap and it would have enough pins for all the keys. This is my first time using a key matrix so it took me a while to learn how it works and how to make it but I think I did it correctly. I made the key matrix similar to the actual layout of the keyboard to make it simplier to understand and, I assume, easier to program. I also am using net labels for the first time so I had to figure out how they work. Although in reality it wasn't too hard to make the schematic but it took a while to finish making the key matrix since I had a lot of keys, 81 in total.

This is what I ended with and I'm pretty sure its right:
<img width="636" alt="Screenshot 2025-06-19 at 7 51 42 PM" src="https://github.com/user-attachments/assets/14b5bb9e-8647-40ee-95f7-c8a5fd2e6623" />

**Total time spent: about 7h**

# June 20th: Made the PCB

Now that I finished the schematic I had to assign all the footprints so that I could start on the PCB. I think I used the right footprints for everything.

After that I put it into the PCB and got this:

<img width="563" alt="Screenshot 2025-06-20 at 11 48 42 AM" src="https://github.com/user-attachments/assets/1854c6fb-3966-4ab4-b82d-60d57c072968" />

I realized I needed to have some sort of guide to place the keys so I used the raw kayboard layout data and ai03 plate generator to generate the plate and I imported it into kicad so that I could know where to place the keys and I made the outer rectangle the edge cuts.

<img width="1103" alt="Screenshot 2025-06-20 at 11 49 26 AM" src="https://github.com/user-attachments/assets/844c1d3a-9e70-4ab9-b30d-e3ebc348dc39" />

So then I put the the pico in the spot I left for it and started the long process of placing all the keys. I also learned I needed to use stabilizers for longer keys like shift and the space bar so I found those and added them. After finally placing the keys and stabilizers, this is what I had:

<img width="759" alt="Screenshot 2025-06-20 at 3 23 20 PM" src="https://github.com/user-attachments/assets/ff8882a4-8390-47ee-b55d-92f6d5a63b7e" />

Now I had to do an equally long process of placing the diodes. There wasn't really a perfect spot for them so I put them between each key. I hope that there is enough space there for them.

<img width="904" alt="Screenshot 2025-06-20 at 7 07 31 PM" src="https://github.com/user-attachments/assets/4b9f7bf8-64c6-4250-95b6-b077507a547e" />

Now to finish my pcb the last thing I had to do was route everything. It took a while but I did it faster than it took me to place the keys or diodes. So now I finished the PCB and heres what I ended with:

<img width="1116" alt="Screenshot 2025-06-20 at 11 45 25 PM" src="https://github.com/user-attachments/assets/18425974-32f5-4ef1-b9e2-79824083ce3c" />

<img width="1044" alt="Screenshot 2025-06-20 at 8 38 59 PM" src="https://github.com/user-attachments/assets/d66e7464-26fb-4018-9f56-9021ec5a2f6c" />

Overall, I didn't really do anything that was really hard today but it took a long time to place all the components and route everything.

**Total time spent: about 5h**

# June 21st: Started the Case and the assembly on OnShape

Now that I had the PCB finished, I had to start making the case. I really didn't have a perfect idea of what exactly I want it to look like so I started the case somewhat similar to how the hackpad tutorial does it. I pretty much made the bottom part of the case the size of the pcb with 1 extra millimeter of space on any side and then I added 9.5mm walls of the case. I also decided the best way to attach all the parts together would be the same way I did for my hackpad with the heat-set inserts and screws so I also put holes in it for the screws. I made the height of the bottom part of the case the same size I used for my hackpad which is 13mm. I also added a rectangle where the microcontroller will be so that I can plug it in and stuff and it doesn't look that good but I'll change it later to make it look better and closer to actual port instead of leaving such a large space open. Heres what I had: 

<img width="800" alt="Screenshot 2025-06-21 at 1 06 59 AM" src="https://github.com/user-attachments/assets/e8f62cd6-fedc-4a2e-bdb0-97feebe32521" />

Now I started on the plate and I used the ai03 plate generator again to get the plate and then I added 9.5mm to each side to make the plate. Then I realized that the bottom part was a little bit bigger than the plate because I added the 9.5 mm after adding 1mm to each side so I had to do the same with the plate and I fixed it. I also added a rectangle above the microcontroller so that there would be easier access to the port and also to display the micrcontroller since it looks cool. When I make the top part of the case I'll make it look better than just a rectangle. Heres the sketch I had for the plate: 

<img width="1043" alt="Screenshot 2025-06-22 at 12 58 32 AM" src="https://github.com/user-attachments/assets/1abaa0cd-fd22-4736-b522-5188f5f02ca9" />

And here's after I extruded it:

<img width="830" alt="Screenshot 2025-06-22 at 1 00 37 AM" src="https://github.com/user-attachments/assets/91025a46-195d-4858-913f-0296023f74ea" />

Then I wanted to start the main assembly so that I could make sure everything will fit together and stuff.

First I made an assembly of the pcb so that I would have to assemble the pcb in the main assembly and instead I could put the pcb together seperately. I imported the pcb from KiCAD and I also imported a model of the pico and the cherry mx switches. The stabilizers and diodes got imported from kicad with the pcb so they were already assembled. I put the pico on but the buttons were gonna take forever to put them all on. I started putting them on but only after putting on like 10 keys did it occur to me that there must be a faster way to do this. So I looked it up and I found the assembly linear pattern tool that allowed me to just put one key in each row and put the distance bewteen each key and select a line that says what direction it goes in and I can automatically place all the keys in that row. So in the end it didn't end up taking that long since I found out abotu the assembly linear pattern tool. I finished the PCB assembly and here's what it looked like:

<img width="1117" alt="Screenshot 2025-06-22 at 1 13 13 AM" src="https://github.com/user-attachments/assets/8d9ab229-e41a-4bda-8cb7-59772aa30fd0" />

Now I started on the main assembly. I also added the screws to get an idea of how they would fit. The screws stick out right now but after I add the top part of the case I'll make it so that the screws don't stick out like that. After putting it all together I realized that the pcb is just being held up by the switches so I added a part to the bottom part of the case to hold the pcb up. It looks like this on all the edges in the case: 

<img width="239" alt="Screenshot 2025-06-22 at 1 25 51 AM" src="https://github.com/user-attachments/assets/1c4768f5-db29-4de2-b778-97ef28884091" />

So right now the assembly looks like this:

<img width="1065" alt="Screenshot 2025-06-22 at 12 08 36 AM" src="https://github.com/user-attachments/assets/df3c6138-667a-48c4-bc9e-74637a26de2c" />

**Total time spent: about 6h**

# June 22nd: Finished the top part of the case, and the main assembly and I started the firmware

I still needed to make the top part of the case. But before I did that I wanted to see how high the keycaps would be and how they would look and stuff so first I added all the keycaps to the assembly. This time I knew I could use the assembly linear pattern tool, so it didn't end up taking as much time.

<img width="1141" alt="Screenshot 2025-06-22 at 10 39 10 AM" src="https://github.com/user-attachments/assets/bf95f573-35fb-4104-b538-4acc7ea938ed" />

I wanted to make it high enough so that the screws didn't stick out and so that the bottom of the keycaps are the same height as the top of the case. I started on the sketch using the plate as a guide. The edges of all the parts of the case will the be the same so I just copied the edges from the plate to the sketch for the top part of the case. The top part of the case would be just an outer part to make the keyboard look complete. I also added circles at each corner for space for the screws but I wouldn't extrude it all the way up, only a little bit more than the screw so that the screw could fit but it would also would stick out and it would look better. I found the distance between the plate and the bottom of the keycaps to decide the height of the top part of the case. I also left a rectangle open to display the micrcontroller. I decided to do that mainly because otherwise there wouldn't be anything there and it would look plain in that spot and also because I think the micrcontroller looks cool displayed like that. I also chamfered the edges and filleted the inner part of the rectangle I made to display the micrcontroller. Here's what the top case ended up looking like: 

<img width="844" alt="Screenshot 2025-06-22 at 10 47 27 PM" src="https://github.com/user-attachments/assets/7d73d937-c2f2-4826-80ed-607d589bedcc" />

When putting it in the main assembly I also wanted to make the spot for the port look better than just a rectangle. I wanted it to be smaller around the port so I started on the bottom part of the case to make the opening look better. I made it a smaller opening and I also filleted the edges, then I did the same with the plate and also for the top part of the case I added a fillet aligned with the fillet from the other parts. Heres what it ended up looking like:

<img width="490" alt="Screenshot 2025-06-22 at 10 58 18 PM" src="https://github.com/user-attachments/assets/d31713ea-094c-4653-a19e-a6a41f6091b8" />

Now I finished the assembly and heres what it looked like:

<img width="1052" alt="Screenshot 2025-06-22 at 11 06 28 PM" src="https://github.com/user-attachments/assets/83b99e8b-662a-4d37-b62d-9aea4522f3d2" />

Also I got made sure the screws fit and everything. The screw doesn't go through the top part of the case but it goes through most of it and I think it will be enough to hold it all together. Heres a section view of how the screws fit into the spot I left for them:

<img width="250" alt="Screenshot 2025-06-22 at 7 26 55 PM" src="https://github.com/user-attachments/assets/1ade6766-0a86-4972-a0e6-e66aa72e370e" />

I also made an exploded view:

<img width="671" alt="Screenshot 2025-06-22 at 11 04 46 PM" src="https://github.com/user-attachments/assets/82073703-8058-41ab-a3f8-a4b2d4fa0a2a" />

Now I needed to start the firmware. I decided to use KMK since I know python and I also used it for my hackpad. Although it wasn't easy to figure out how to program the key matrix since I'd never used one before but it wasn't to hard to figure it out. Now I had to program each key and I haven't finished so I'll finish tomorrow but its been taking a while especially since some of the custom keys I added use macros like the brackets so that I could put both brackets then put the cursor between them.

**Total time spent: about 6h**

# June 23rd: Finished Firmware, found parts, and uploaded everything to github

I already finished most of the firmware so it didn't take me very long to finish it. I just needed to finish the keymap. After that I just need to find all the parts, upload everything to github and update the README and create the BOM.

I started looking for the parts I needed. It took a while to find everything. I managed to find most things on aliexpress. The only parts I didn't get from aliexpress were the raspberry pi pico and obviously the pcb. After adding everything up the total ending up being $81.47

Then I uploaded everything to github and organized it in a good way. I put the complete CAD model in CAD and the firmware python file in Firmware, pcb files from kicad in PCB and everything needed to make it (top case, plate, bottom case, gerbers, and firmware) in the Production folder. I organized it the same way I did for my hackpad. I also made the BOM in csv format and in the bottom of my README.

Now I'm gonna submit it. If it gets approved I'm 99% sure I'll go to undercity since I'm close enough to drive.

**Total time spent: about 4h**
