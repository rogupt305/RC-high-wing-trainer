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

# STEP 2: System Integration and Control
## Electronic Component Configuration
Before airframe assembly, I conducted a bench test of the propulsion and control systems focalizing on electrical viability and signal integrity of the setup. I selected a three-phase brushless motor and a 25A ESC, matching them to a 3S LiPo battery to provide a reliable power-to-weight ratio for a trainer-class aircraft. 
FIGURE 1 (left): a map of the connected components, featuring the motor (far left), ESC (middle), reciever (far right), servo motors (far right, bottom)
FIGURE 2 (right): Assembly in real-world

<img src="https://i.postimg.cc/y6XGJ3jP/Screenshot-2026-01-31-225043.png" alt="FIG 1" width="400">             <img src="https://i.postimg.cc/wx0V8X0X/IMG2-676767.jpg" alt="FIG 2" width="400">

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

# STEP 3: Airframe Archetecture
The lift and control surfaces are by far the most crucial part of any aircraft, since they are what allows it to lift off the ground and control pitch, yaw and roll. 

## Objective
The goal was to design and fabricate a high-wing airframe capable of stable, low-speed flight, high acceleration, and manueverability, maximized by a trainer-style configuration to prioritize self-leveling abilities and high lift:drag ratios. 

## Wing Geometry and Lift
A single sheet of foamboard was utilized to create a modified KFm-1 airfoil (Kline-Fogleman)
- Design choice: A modified stepped profile is easy to fabricate, and generates consistent lift at high angles of attack
- Full Spherical Scope: Design choice theoretically (NOT proven for this model) allows for inverted flying and vertical stability
- Structural Reinforcement: Integration of a double-reinforced foamboard spar at the 17.3% chord position acts as the primary structural enforcement, preventing wing-flex, and allowing the airframe to withstand aerodynamic loads experienced during high G-force manuevers, including climbing and rolling.

## Fuselage Construction and Component Housing
Maintaining a low weight, the fuselage was designed as a square-rectangular profile to maximize rigidity. 
- Fabrication Method: A "score-and-fold" techuique creates a seamless inner skin, while reinforcing the exterior with hot glue increases strength.
- Internal Layout: The fuselage houses a removable power pod, allowing for mdular maintenance of the motor, battery, and ESC. The battery compartment is adjustable for fine-tuning the CG during pre-flight checks.

## Empennage and Control Surfaces
The tail section (empennage) was designed with an oversized vertical stabilizer and elevator to provide maximum control at low airspeeds. At max speed, however, this results in an over-agile craft - increasing the risk of structural breakdown via sudden movements.
- Hinge Design: Control surfaces were attached utilizing a "foam-hinge" method, with a bevel at 45 degrees to allow for maximum air deflection without mechanical resistance.

# Phase 4: Experimental Flight Testing and Failure Analysis

## Flight Test Environment and Objectives
The intial maiden flight was conducted on a low-friction dirt surface to evaluate the aircraft's takeoff performance and pitch stability. The primary objective was to verify the thrust-to-weight ratio and the effectiveness of the control surfaces under manual input.

## Takeoff Dynamics and observations
- Ground Clearance Issues: Initial taxiing revealed insufficient landing gear height, causing the propellor to skim the grass, necessitating a need for redesigned, high-clearance landing gear struts.
- Power Abundance: Upon successful takeoff, the aircraft demonstrated a high thrust-to-weight ratio, achieving a near-vertical climb, confirming that the 1050kV motor and 3S battery provided too much power for the airframe's mass.

## In-Flight Instability and Stall Event:
- Pitch-Up Moment: Immediately after liftoff, the aircract exhibited extreme pitch sensitivity, indicating an aft Center of Gravity, where the tail is too heavy relative to the wing's center of lift. After the flight, I realized that my CG was located at the 56% chord length, rather than the optimal 25%.
- Aerodynamic Stall: DUe to the steep andle and low horizontal airspeed, the wing reached a Critical Angle of Attack: resulting in a stall.
- Uncertainty: Due to my incorrect reflexes, immediately rotating the elevator down was to severe, resulting in an immediate nose-dive. I am currently unable to identify the actual cause of the aerodynamic stall, as due to the motion of the craft, the power generated by the motor seemed to be sufficient to allow the craft to continue climbing at a vertical 90 degree angle of attack.

## Post-Crash Structural Integrity 
Despite the impact, the airframe demonstrated high durability.
- Intact Systems: The fuselage, wings, servos, and internal circutry remained fully functional, validating the "score-and-fold" method used in Phase 3. The power pod, despite incurring the majority of the force during the crash, sustained no significant damage - likely due to the propellor blade acting as a cushion, compared with the soft dirt and grass on the ground
- Mechanical Failure: The 9x4.5 propellor, likely after cushioning the majority of the force, snapped. Being replacable and detachable from the motor, this isn't a major issue.

## Next Steps
- CG Recalibration: Shift the battery forward to achieve the intended 25% chord CG
- Landing Gear Redesign: Increasing the strut length to provide better propeller clearance
- Optimal Flying Speed: Conduct various tests at lower throttle percentages to find the optimal cruise speed before attempting high-AOA (angle of attack) maneuvers. 

# Conclusion and Future Technical Roadmap
While the initial flight resulted in a structural failure, the craft demonstrated significant structural stability and the potential for high G-force manuevers. The data regarding the longitudinal stability and the thrust-to-weight ratios is critical for the next iteration of this project. 

## Upcoming Objectives
- Redesign the Landing Gear: Extending the struts
- CG Optiumization: Implementing a better battery tray for easy adjustment
- Stabilization: My long term goal is to integrate an onboard flight controller to implement PID (Proportional-Integral-Derivative) control loops, providing an active pitch and roll stabilization to counter the high-theta instabilities observed during the flight.

NOTE: This project remains an ongoing study in aerospace engineering, with the next flight test and data collection upcoming. I will continue editing this repository, keeping it up to date with the latest developments as they arrive.
