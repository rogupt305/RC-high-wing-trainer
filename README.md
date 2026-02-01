# Design, Fabrication, and Flight-Test Analysis of a Custom High-Wing UAV

### OBJECTIVE
This repository documents a systematic approach to the design and construction of a scratch-built unmanned aerial vehicle (UAV). The primary engineering objective was to optomize a low-cost, high-lift airframe using foamboard while maintaining structural integrity and predictable flight characterists under a realistic aerodynamic load. 

### OVERVIEW
Rather than following a pre-set kit, I relied on intuitive design and observational research to develop a functional airframe. This project represents the complete design cycle for the following reasons:
1. Equipment: Sourced electronic components and matched power systems based on established hobbyist standards for trainer aircraft.
2. Airframe Fabrication: Hand-crafted the fuselage and wing surfaces from foamboard, utilizing a high-wing configuration to maximize stability and tighten control for a maiden flight. Ailerons can be swapped out later for bigger ones, enabling increased handling capabilities for more experienced flyers.
3. Experimental Iteration: Conducted initial flight trials to observe aerodynamic behavior. While the first flight resulted in a crash, it provided critical data points regarding balance and structural weak points.
4. Post-Flight Diagnostics: Currently analyzing the crash results to refine the Center of Gravity, and implement structural reinforcements, shifting from pure intuition toward a data-driven engineering approach.



# STEP 1: Component selection and Power System Design

### Objective
The initial phase involved identifying and sourcing a propulsion and control system capable of supporting a scratch-built foamboard airframe. The goal was to balance weight, thrust, and battery discharge rates to ensure a stable flight for a beginner-class trainer.

## Propulsion System Architecture
Brushless DC motors (BLDC) are more efficient than an alternative due to their superior power-to-weight ratio and efficiency. 
- Motor Selection: The FT Radial 2212-1050kV motor was the most appealing choice due to it's lower KV rating, which swung a 9x4.5 propellor, providing higher static thrust at lower speeds - ideal for the high-drag insinuated from the large wingspan of a foamboard trainer. It integrated perfectly into the system, requiring nearly 11.1V of power, therefore leaving just enough to cover the movement of the control surfaces via micro-servos.
- Electronic Speed Controller (ESC): Integrating a 25A ESC with an internal Battery Eliminator Circuit (BEC), the reciever and the servos recieved a stable, regulated 5V power supply even as the voltage of the main flight battery continuously fluctuated with the throttle.

## Energy Storage and Power Distribution
- Voltage Selection: A 3-cell (11.1V) configuration was chosen to provide teh necessary voltage to achieve the motor's peak RPM while maintaining a manageable total takeoff weight. It provides around 6-7 minutes of total flight time; two to three batteries would be precharged and loaded onto the aircraft independently.
- Capacity and Discharge: The 1300mAh capacity provides around 8-12 minutes of flight time, and a 45C discharge rating ensure the battery can handle high-current bursts during the takeoff and landing manuevers without significant voltage sag directly afterward.

## Command and Control Hardware
The aircraft utilizes a 2.4GHz DSMX protocol for interference-free communication, acting as a high-speed information relay platform. 
- Reciever: I integrated the Spektrum AR410, with it's 4-channel and antennaless features providing a compact shape - allowing for an efficient fit insde the fuselage.
- Transmitter: The Spektrum DX6E transmitter, with it's multi-connection ability, was the perfect controller. Paired with the extremely lightweight reciever, and with the total configuration providing up to 3000 nautical meters of connection, they fit efficiently with my setup.
- Actuation Motors: Four 9g micro-servo motors control the elevator, rudder, and ailerons. Providing sufficient torque for foamboard control surfaces with wind resistance, these servos also minimized weight, along with aft Center of Gravity (weight on the rear half of the fuselage)

## Ground Control
Rather than sourcing parts from online, wheels were constructed utilizing existing materials
- LEGO Technic wheels, with their strong durability, scalability, and their ability to attach at any point in the plane reduced the drag coefficient significantly - as their position is interchangable. 


## Specifications
|     **Component**     |                     **Specification**                     | **Case** |


| Motor | 2212 1050kV | High torque for stability at low speeds|
| Propellor | 9x4.5 | Optomized for static thrust |
| Battery | 3S11.1V 1300mAh | Balaning power and aerodynamic wing load |
| Radio Connection | 2.4GHz DSMX | Reliable signal in high-interference spots |

## Direct Links
|     **Item**     |                     **Parts List**                     | **Price** |**Link**|


| LiPo Battery | Tattu 1300mAh 45C 3S1P 11.1V Lipo Battery Pack With XT-60 Plug | $126.99 | <a href="https://store.flitetest.com/tattu-1300mah-45c-3s1p-11-1v-lipo-battery-pack-with-xt-60-plug/"> Link </a> |
| FT Power Pack B Radial v.2 | ESC, Motor, 4x 9g Servos, Servo Cable Extenders, Propellors | $74.99 | <a href="https://store.flitetest.com/ft-power-pack-b-radial-v-2/?searchid=0&search_query=FT+power+pack"> Link </a> |
| Reciever | Spektrum 4-channel | $34.99 | <a href="https://store.flitetest.com/spektrum-ar410-4-channel-dsmx-aircraft-receiver-spmar410/?searchid=0&search_query=spek"> Link </a> |
| Charger | B6 Balance Charger | $39.99 | <a href="https://store.flitetest.com/b6-charger/?searchid=0&search_query=b6+"> Link <a/>|
| Power Pod | Flite Test Swappable Power Pod | $9.99 | <a href="https://store.flitetest.com/swappable-power-pod-firewall-5-pack-mkr2/?searchid=0&search_query=ft+power+pod"> Link <a/>|
| Foam Board | Flite Test Maker Foamboard | $69.99 | <a href="https://store.flitetest.com/flite-test-maker-foam-board-by-adams-v2-20-pack/"> Link <a/>|
| Assembly Kit | FT Crafty Kit v.2 - NOTE: Must be the v.2, not Basic version | $99.99 | <a href="https://store.flitetest.com/ft-crafty-kit-v2/?searchid=0&search_query=ft+crafty+kit"> Link <a/>|

## Scalability
This configuration is highly scalable, with the potential for usage in separate craft.
- The Spektrum DX6E, being a 6-channel reciever, connects to a maximum of 6 recievers, effectively controlling 6 different aircraft.
- Swappable power pod indicates 

# STEP 2: Assembling the Power Pod, Readying Electronics, Caring for your Battery
## Electronic Component Configuration
Before airframe assembly, I conducted a bench test of the propulsion and control systems focalizing on electrical viability and signal integrity of the setup. I selected a three-phase brushless motor and a 25A ESC, matching them to a 3S LiPo battery to provide a reliable power-to-weight ratio for a trainer-class aircraft. 

## Servo Calibration and Control Surface Neutralization
To ensure precise flight control, I performed a neutralization procedure for all micro-servos
- I used a pulse-width modulation (PWM) servo tester to set each motor to its 90° center position.
- I manually attached the control horns horizontally to ensure that the physical center position of the elevator and rudder matched the electronic neutral signal from the reciever

## Reciever Binding and Signal Language
I bound the Spektrum AR410 reciever to the transmitter to ensure a secure link
- Port Mapping: I assigned the ESC to the throttle channel and utilized a Y-harness for the ailerons to allow for synchronized, mirrored movement accross the wingspan.
- Directional testing: I performed a pre-flight check of all of the surfaces to ensure that the pitch, roll and yaw inputs moved the surfaces in the correct aerodynamic directions.

## Battery Safety and Storage Protocols
Recognizing the chemical volatility of Lithium Polymer (LiPo) cells, I implemented  strict maintenance protocols
- I monitored cell voltage to ensure it never dropped below 3.65V under load
- I maintained a 3.80V per cell storage charge to prevent internal resistance build-up and chemical degredation

<a href="https://www.hobby-addicts.com/blogs/news/the-ultimate-guide-to-rc-lipo-battery-care-and-maintenance?srsltid=AfmBOooGn46RWfYM8x0MsRsV87lkDkGGGyxn2zXOQoy9Z1O1La-4co_E">  <a href="https://www.youtube.com/watch?v=vuh7Gc3Dbh0"> <a href="https://www.youtube.com/watch?v=3wKZbQoLtBY">  <a href="https://www.youtube.com/watch?v=3wKZbQoLtBY"> 

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


This project is based on the Start Bootstrap Resume template (MIT License). Refer to the "License" tab on Github for more details.



<a href="https://www.hobby-addicts.com/blogs/news/the-ultimate-guide-to-rc-lipo-battery-care-and-maintenance?srsltid=AfmBOooGn46RWfYM8x0MsRsV87lkDkGGGyxn2zXOQoy9Z1O1La-4co_E">  <a href="https://www.youtube.com/watch?v=vuh7Gc3Dbh0"> <a href="https://www.youtube.com/watch?v=3wKZbQoLtBY">  <a href="https://www.youtube.com/watch?v=3wKZbQoLtBY"> 
