---
title: "CodeBoard"
author: "Alfonsoce11"
description: "A keyboard specially made for coding with quicker access to common characters."
created_at: "2024-06-18"
---

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
