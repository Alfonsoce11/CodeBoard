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
