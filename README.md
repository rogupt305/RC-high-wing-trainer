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


# STEP 2: Assembling the Power Pod, Readying Electronics, Caring for your Battery

## Caring for Your LIPO Battery
The battery holds the greatest risk for fire or damage to you and your surroundings. It's important that you excersize good care for the battery whenever using it. BEFORE PROGRESSING, make sure to read <a href="https://www.hobby-addicts.com/blogs/news/the-ultimate-guide-to-rc-lipo-battery-care-and-maintenance?srsltid=AfmBOooGn46RWfYM8x0MsRsV87lkDkGGGyxn2zXOQoy9Z1O1La-4co_E"> this article <a/> from HobbyAddicts in all it's entirety - I found this a very detailed and useful explanation for how to understand the battery. Read this till the end, as everything here is important. SOme key numbers: 4.2V - typically the max voltage per cell when fully charged. 3.8V - the storage voltage. The battery can theoretically sit at this voltage for many months without chenical degredation. NEVER let the battery go below 3.65 volts for an extended period of time (around a few hours max), keeping it at full charge is reccomended for only about a day or two before discharging to storage voltage.

The power pod and electronics are extremely critical components of any RC aircraft, providing and regulating the power, housing the battery and other components, and providing the ability to control the yaw, pitch and roll. 
## Power Pod
To assemble the power pod, I followed <a href="https://www.youtube.com/watch?v=vuh7Gc3Dbh0"> this video from FliteTest <a/> , which details the basic assembly of the structure. Following this, I made my own modifications, adding two horizontal spars for a snug compartment for the battery. Additionally, I made the ESC dangle from below the structure, as it will be tucked in between the bottom of the power pod and the bottom of the fuselage. 
INSERTIMAGE
INSERTIMAGE
INSERTIMAGE

## Electronics
Before getting into anything, I'd highly reccomend that you watch <a href="https://www.youtube.com/watch?v=3wKZbQoLtBY"> this video <a/>: it provides an overview of circutry in an RC plane, as well as all of the electronics likely involved. 

### Servos
The first main step to preparing the electronics is centering the servo motors. This term refers to ensuring that the servos are turned to exactly 90 degrees, and are in the center position of their 180 degree range. When turning on the completed craft, the servos will automatically assume their 90 degree position - so it's important that they are pre-aligned before being attached. Luckily, the servos are shipped with an almost exact alignment at 90 degrees - but it's always important to verify the position of each motor. 

First, identify this piece: it's called the servo aligner:
INSERTIMAGE

To properly align the servos, I used <a href="https://www.youtube.com/watch?v=3wKZbQoLtBY"> this video from FliteTest <a/>, which details how to safely utilize the servo aligner, such as how to plug in the servos and the battery. However, I attached the servo horns differently - so after watching the video, please be sure to refer back to this page. 

For all of the servos, I attached the horn horizontally, like this:
INSERTIMAGE

### Reciever
After aligning the servos, the next step is to plug them in in the correct order, along with the ESC, to the reciever. To plug them in correctly, leave the BATT port empty. Plug in the servo-resembling cord from the ESC into port 1, plug in the Y-connector (I'll explain what that is in a bit) into port 2, plug the elevator servo into pin 3, and finally plug in the rudder servo into pin 4. 
Here's a reference image from my build of the reciever with the sires plugged in, and with the numberings (BATT, 1, 2, 3, 4) next to each port:
INSERTIMAGE

### Y-connector and Roll Direction
The Y-connector, as it's name suggests, looks like a regular servo extension cable - but branches out into two other cables in the middle. On the wing of any plane, the roll is controlled by the ailerons. To turn the plane left or right, one alieron goes up, and the other one goes down - deflecting the wind and turning the plane. This means that the alierons never both move up or down - the movement of one is always in the opposite direction of the other. This is the purpose of the Y-connector - it reverses the direction of each of the wing servos, creating opposite movements. To attach them, simply plug in the two wing servos to the two cables coming from the joint of the y-connector - being careful to ensure that ground goes to ground, power to power, and servo to servo. Then, plug the Y-connector into Pin 2 on the reciever. 
It's important to know the orientation of each servo on the wing - otherwise, the plane might turn in the opposite direction. We'll confirm this in the next section of this step.

## Binding the Reciever to the Controller
In order to control the plane, we need to bind the reciever to the transmitter (controller). For my setup, I used the Spektrum DX6E controller, along with the Spektrum AR410 Reciever, as mentioned in the parts list in Step 1. Here's how to do it:
1. Ensure that the circutry is perfect - short circuts can occur if even one wire is wrongly connected.
2. Plug in the yellow "banana connector" to the same one present on the ESC - it's the one with just two wires, the red (power) and the black (ground).
3. After a few loud beeps, the reciever should have an orange light flashing - indicating that it's on bind mode.
4. Ensure that the left joystick is pulled DOWN, otherwise, the controller will indicate "throttle high" when turned on and it may accidentally spin the motor. Always ensure that the throttle is turned all the way down whenever turning on the controller for the first time - though it should warn you before spinning the propellor.
5. With the transmitter/controller OFF, locate the BIND button and hold it. Then, while holding the BIND button, power on the transmitter.
6. Keep holding the BIND button until the LED on the reciever turns solid, confirming a successful bind.
7. Move the left and right joysticks to move the servos, throttle, and ensure everything is working. It's advised to take off the propellor blade at this stage when spinning the throttle, for safety reasons
8. Confirm if your servos are plugged in to the correct ports: the right joystick should control the alieron servos (horizontal movement of the joystick) and the elevator (vertical movement), and the left one should control the rudder servo (horizontal) and the throttle (vertical).

### Distinguishing the Left Wing Servo from the Right Wing Servo
To do this, follow these steps:
1. Provide power to the transmitter and the setup correctly, ensure that the reviecer and transmitter are connected
2. Place both wing servos next to each other, with the horns facing outward.
3. Move the alieron joystick LEFT, and observe the direction the horns moved: the horn that moved DOWN is the servo for the right wing, and the one that moved UP is for the left wing.
4. Test it by moving it RIGHT: this time, the servo that moved down is for the left wing, and the one moving up is for the right wing.
Label each servo with a Post-It and disconnect the circutry, leave the wiring aside for now

## Important Note about Battery Voltage
During the above processes, the battery will likely lose very little voltage. However, if you repeat this multiple times for testing, ensure that your battery voltage is between 3.75V and 3.85V: the optimal storage voltage is 3.8V per cell for the Tattu 3S battery.

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
To create a sturdy fuselage, I utilized a new sheet of foamboard - dividing it into four sections along it's longest side, each with a height of 2 inches. Following this, I scored the cuts, careful not to break through the entire length of foamboard. On the left is how I made the cuts, and on the right is how I folded it (with the crevices from the cuts facing outside) :
<img src="https://i.postimg.cc/9QjXbgrY/img1.jpg" alt="My iPhone photo" width="400">

Following this, I added hot glue along the full length of each exposed crevice, for all four of them. This increases the integrity of the fuselage, preventing the structure from bending along the folds, and ensuring that the openings retain their square shape. If you don't have enough hot glue, I'd reccomend adding spars throughout the fuselage, though this method adds more weight to the plane. 
