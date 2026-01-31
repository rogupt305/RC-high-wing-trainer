# RC Plane Project
## A Beginner's Guide to Entering the Field of RC Aviation

Welcome to my personal journey into the world of RC (Radio-Controlled) aircraft. This detailed repository documents my very first attempt at constructing an RC airplane entirely from scratch - no prefabricated kits, no commercial airframes, and no prior experience. 
What commenced as a simple curiosity quickly evolved into a full-fledged engineering and design challenge that taught me fundamentals in aerodynamics, electronics, materials, and mechanical design. 

This project isn't just a simple build log - it's a beginner-friendly, step-by-step resource for anyone who wants to get into RC planes on a realistic budget, using widely available materials, and with a focus on reusability and scalability. Every decision I made during this process was carefully balanced between performance, cost, and long-term value. For example, while this plane utilizes affordable components, the transmitter and reciever setup are overly expensive, yet they allow me to reuse the same controller across multiple aircraft in the future - enabling easy growth within the hobby without repeatedly reinvesting in new gear. 

This guide was created by a newcomer, and with complete newcomers in mind. If you've ever thought about building your own RC airplane but felt overwhelmed by the complexity or cost, this project is for you. I cover everything from:

1. Material selection (why I chose foamboard over cardboard or balsa wood)

2. Airframe design (including blueprint planning, airfoil testing, CG calculations, and structural reinforcements)

3. Power system setup (motor, ESC, battery, propellor matching)

4. Control surface layout and servo placement

5. Mounting and wiring tips

6. Test flights, crash recovery and iteration

Throughout the build, I prioritized DIY accessibility. My goal was not just to build something that flies, but to understand why it flies and how each subsystem works. I hand-cut every piece, tuned it through real test throws, and adapted the design to match the materials I had on hand. The result is a high-wing, beginner-friendly trainer that is straightforward, efficient, and durable enough to withstand the learning process - including crashes and hand-launched test flights. 

This project is meant to spark inspiration and lower the barrier to entry into a rewarding, challenging, and, realistically, a costly hobby. It's not just about flying - it's about building, innovating, iterating, creating, and designing something that flies. 

Whether you're a student, hobbyist, or simply someone who enjoys making things, I hope this guide helps you take your first steps into RC aviation. If you're looking to build your own plane from scratch, feel free to explore the folders and documentation here - and don't hesitate to use, modify, or improve upon what I've done. 

Enjoy the process!



# STEP 1: Parts Selection, Electronics, Accessories, Everything Necessary to Make a Plane Fly

Before designing and assembling the airframe, I began by selecting the key electronic components required to make an RC airplane functional and controllable. Since this was my first RC build, I chose to source the main electronics from Flite Test - a well-known and beginner-friendly site that offers high-quality, affordable parts designed for DIY foamboard aircraft. While the components are described individually, it's crucial to note that some parts are grouped with others to form a kit, which can be found on the Flite Test website. At the end of this step, there is a table which shows the exact costs, links, and parts that I purchased. 
Here is a detailed breakdown of the components, accessories, and parts I selected, and what each one does:



## ELECTRONICS

### Battery - LiPo (Lithium Polymer) or LiFePO₄ (Lithium Iron Phosphate)
PURPOSE: Powers the entire plane - the motor, reciever, and servos. 

SPECS: Usually a 2S (6.6-7.4V) or a 3S (11.1V) battery with 1000-1500 mAh capacity. 

MY CHOICE: Tattu 1300mAh 45C 3S1P 11.1V Lipo Battery Pack With XT-60 Plug

CHARGER CHOICE: B6 Charger (Search this on Flite Test)
THINGS TO KEEP IN MIND: When selecting a battery, it is critical to note that LiPo batteries are more prone to explosions if not kept properly, and require extensive charging and security measures, such as a fireproof bag. However, these batteries generally last longer and offer better performance than LiFePO₄ batteries. In the end, it really is a matter of your preference - performance or safety. Also, I reccomend purchasing multiple batteries (to swap out) - because even the best battery will only power your craft for no more than 15 minutes.


### ESC (Electronic Speed Controller)
PURPOSE: Connects the battery to the motor and regulates power based on your throttle input.

FUNCTION: Converts DC battery voltage into three-phase power for the brushless motor.

MY CHOICE: FT 25 Amp ESC with XT60 and 3.5mm Bullet Connectors


### Brushless Motor
PURPOSE: Spins the propellor to generate thrust

SPECS: Rated by KV (RPM per Volt). A ~1300KV motor is deal for beginner planes - strong, but not overly fast. 

MY CHOICE: FT Radial 2212-1050kV (Slightly less than 1300KV, but will get the job done.)


### Propellor
PURPOSE: Converts rotational motion into forward thrust.

SPECS: Usually something along the lines of 8x4 or 9x5, directly matched to the motor's power range.

MY CHOICE: Propellers (9x4.5)


### Reciever
PURPOSE: Recieves signals from your transmitter, and relays them to the servos and ESC. 

MY CHOICE: Spektrum AR410 4-channel DSMX Aircraft Receiver (A four-channel reciever, bound to my transmitter. This reciever can be swapped between aircraft in the future, making the investment reusable. 


### Transmitter (Radio Controller)
PURPOSE: The handheld remote that enables you to control throttle, pitch, roll and yaw by the joysticks. 

MY CHOICE: Spektrum DX6e 6-Channel DSMX 2.4GHz RC Radio Transmitter


### Servos (Micro Servo Motors)
PURPOSE: Move control surfaces (elevator, rudder, ailerons) to steer and redirect the plane. 

MY CHOICE: 3x 9g servos



## ACCESSORIES

### Foamboard

A versatile, easy to cut, strong material for RC aircraft

### Power pod

Encases electronics, can be swapped between planes; adds customization

### Firewall

Seperates the motor from rest of electronics/aircraft in case of motor fire

### Assembly kit

Crucial for assembling RC planes; includes glue, tape, servo centerers, etc.


## Direct Links
|     **Part**     |                     **Note**                     | **Price** |**Link**|


| LiPo Battery | Tattu 1300mAh 45C 3S1P 11.1V Lipo Battery Pack With XT-60 Plug | $126.99 | <a href="https://store.flitetest.com/tattu-1300mah-45c-3s1p-11-1v-lipo-battery-pack-with-xt-60-plug/"> Link </a> |
| FT Power Pack B Radial v.2 | ESC, Motor, 4x 9g Servos, Servo Cable Extenders, Propellors | $74.99 | <a href="https://store.flitetest.com/ft-power-pack-b-radial-v-2/?searchid=0&search_query=FT+power+pack"> Link </a> |
| Reciever | Spektrum 4-channel | $34.99 | <a href="https://store.flitetest.com/spektrum-ar410-4-channel-dsmx-aircraft-receiver-spmar410/?searchid=0&search_query=spek"> Link </a> |
| Charger | B6 Balance Charger | $39.99 | <a href="https://store.flitetest.com/b6-charger/?searchid=0&search_query=b6+"> Link <a/>|
| Power Pod | Flite Test Swappable Power Pod | $9.99 | <a href="https://store.flitetest.com/swappable-power-pod-firewall-5-pack-mkr2/?searchid=0&search_query=ft+power+pod"> Link <a/>|
| Foam Board | Flite Test Maker Foamboard | $69.99 | <a href="https://store.flitetest.com/flite-test-maker-foam-board-by-adams-v2-20-pack/"> Link <a/>|
| Assembly Kit | FT Crafty Kit v.2 - NOTE: Must be the v.2, not Basic version | $99.99 | <a href="https://store.flitetest.com/ft-crafty-kit-v2/?searchid=0&search_query=ft+crafty+kit"> Link <a/>|


## Why Flite Test?

As a beginner in the hobby, I found that Flite Test's Power Pack bundles are extremely useful. They group together all the motor, ESC, servo and connecter components that are guaranteed to work with each other and with foamboard-based scratch builds. I highly reccomend checking out their website, as they have a plethora of important information to share. 

This electronics setup is also scalable. This means that I can reuse components such as the power pod (see below) and all the electronics in future builds. 


# STEP 2: Assembling the Power Pod, Readying Electronics



# STEP 3: Assembling the Lift and Control Surfaces

The lift and control surfaces are by far the most crucial part of any aircraft, since they are what allows it to lift off the ground and control pitch, yaw and roll. 

## Wings
The most efficient wing design is an airfoil. ( <a href="https://www.naa.edu/airfoil-design/"> Link<a/> to how this works, in case you are unfamiliar with this concept). My airfoil was rather boxy in shape, with curves not as smooth as a traditional one. However, it was more than capable of getting the job done. 
Instead of using multiple pieces of foamboard and attaching them together, I found an efficient way that only utilizes one single sheet. Here's what I did:

Starting off with a full sheet of foamboard (__ x 30), I measured out and drew three lines at 7.5, 9.25 and 9.75 inches from the bottom of the foamboard sheet (See Figure 1). I then left that sheet of foamboard aside, and started making the spar.

My spar was a double-reinforced sheet of foamboard, and significantly bolsters the structural integrity of the wing. It is placed directly in the thickest portion of the airfoil, and retains it's shape. To make the spar, I first drew a line 1.5 inches from the bottom of a fresh piece of foamboard. Then, I cut out the entire 30-inch strip, before finally folding that entire strip in half and gluing each half together. The result was a sturdy length of foamboard that measured 30 inches long, 0.75 inches tall and 0.4 inches thick. 

After this, the next step was to glue the spar onto the wing-foamboard (See Figure 2). Before doing so, I used the FliteTest knife to lightly score each of the three lines, making sure not to accidentally cut them into four seperate strips (Only cut the top half of the foamboard's thickness, not the whole way). Then, I flipped the entire foamboard over onto the un-cut side, found the correct spot, and glued the spar in between the two closest scores on the foamboard.  

<img src="https://i.postimg.cc/NFv4dmy7/Whats-App-Image-2025-07-31-at-09-22-13-a29b1d0d.jpg" alt="My iPhone photo" width="400">        <img src="https://i.postimg.cc/NFv4dmy7/Whats-App-Image-2025-07-31-at-09-22-13-a29b1d0d.jpg" alt="My iPhone photo" width="400"> 



# STEP 4: Assembling the Fuselage, CG Testing

## Fuselage
To create a sturdy fuselage, I utilized a new sheet of foamboard - dividing it into four sections along it's longest side, each with a height of 2 inches. Following this, I scored the cuts, careful not to break through the entire length of foamboard. Below is a reference image for how to make the cuts:
<img src="(https://i.postimg.cc/9QjXbgrY/img1.jpg)" alt="My iPhone photo" width="400">
