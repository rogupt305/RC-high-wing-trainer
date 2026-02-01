# ABSTRACT: Design, Fabrication, and Flight-Test Analysis of a Custom High-Wing UAV
The primary objective of this project was to design and prototype a scratch-build unmanned aerial vehicle (UAV) using low-cost, high-durability materials (EPS foamboard. Incorporating a high-propulsion system with a manually fabricated airframe, while ensuring predictable longitudinal stability required a bottom-up approach to systems integration, balancing the requirements of aerodynamic wing load, structural rigidity, and even weight distribution.

### Methodology
This documented repository follows a comlete engineering cycle, transitioning from intuitive prototyping to data-driven analysis:
- Propulsion: Sourcing a high-torque brushless DC (BLDC) motor and 11.1V LiPo power storage system to achieve a thrust-to-weight ratio exceeding 1:1, providing high vertical AOA (Angle of Attack) capabilities.
- Aerodynamic Wing Geometry: Implementing a modified KFm-1 (Kline-Fogleman) modified airfoil to optimize lift at low Reynolds numbers (~300,000 RE), supported by a dougle-reinforced foamboard spar at the 17.3% chord position
- Flight Analysis: Analyzing the aerodynamic stall and aft-CG displacement from maiden flights, I identified critical failure points in the initial design
- Iterations: Refocalizing the approach allows for data-driven iterations. Current work focuses on shifting from "intutive" balancing to a calculated Center of Gravity (CG) at the 35% chord length and planning the integration of PID control loops for active stabilization

### Experimental Observations
Initial flight trials served as a diagnostic for evaluating airframe integrity and balance. Data gathered from an immediate, high-AOA stall event confirmed aft-heavy Center of Gravity at the 56% chord, providing a quantitative baseline for future stabilization systems. The structural integrity of the fuselage was validated by minimal damage when the airfract suffered a nose-dive impact, with all failure limited to the fracturing of a propellor blade. 

### Conclusion and Future Trajectory
The project successfully demostrated the viability of manual UAV fabrication using modular components. Future work is directed towards the implementation of PID (Proportional-integral-Deravite) control loops active self-leveling and the recalibration of the battery placement to achieve a better CG. Due to the high thrust-to-weight ratio, space exists for additional sensory equipment. 

FIGURE 1 (far left): Completed UAV, featuring power pod and airframe

FIGURE 2 (middle): Completed UAV, featuring modified KFm-1 airfoil, front and rear landing gear

FIGURE 3 (far right): Completed UAV, featuring exposed fuselage for air displacement and easy access to electronics


<img src="https://i.postimg.cc/Rhnh30T1/IMG-4033.jpg" alt="FIG 1" width="322">  <img src="https://i.postimg.cc/8PpPQw2y/IMG-4035.jpg" alt="FIG 2" width="322">  <img src="https://i.postimg.cc/yYGqQPsx/IMG-4036.jpg" alt="FIG 3" width="322">


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

FIGURE 4 (left): a map of the connected components, featuring the motor (far left), ESC (middle), reciever (far right), servo motors (far right, bottom)

FIGURE 5 (right): Assembly in real-world



<img src="https://i.postimg.cc/y6XGJ3jP/Screenshot-2026-01-31-225043.png" alt="FIG 4" width="400">             <img src="https://i.postimg.cc/wx0V8X0X/IMG2-676767.jpg" alt="FIG 5" width="400">

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

FIGURE 6: Side-view of the wing, featuring internal and external dimensions of the wing, spar, and aileron

FIGURE 7: Top view of the wing

FIGURE 8: Dihedral angle

FIGURE 9: Tail dimensions

 <img src="https://i.postimg.cc/xTjQX81D/IMG-4038.jpg" alt="FIG 6" width="200"> <img src="https://i.postimg.cc/C5QcMcxX/IMG-4039.jpg" alt="FIG 7" width="200"> <img src="https://i.postimg.cc/P58RJnZ3/IMG-4041.jpg" alt="FIG 8" width="200"> <img src="https://i.postimg.cc/9MXbG6RX/IMG-4042.jpg" alt="FIG 9" width="200"> 


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

FIGURE ___: The propellor broken at the root
  <img src="https://i.postimg.cc/7YjSwmzW/IMG3-414141.jpg" alt="FIG ___" width="400">

  
## Next Steps
- CG Recalibration: Shift the battery forward to achieve the intended 25% chord CG
- Landing Gear Redesign: Increasing the strut length to provide better propeller clearance
- Optimal Flying Speed: Conduct various tests at lower throttle percentages to find the optimal cruise speed before attempting high-AOA (angle of attack) maneuvers. 

# Conclusion and Future Technical Roadmap
### Project Synthesis
The development of this high-wing UAV successfully demonstrated the feasibility of integrating high-output brushless propulsion systems with a hand-bamufacturef foabmoard airframe. While the initial flight envelope was limited by a longitudinal stability deficit, the airframe's performance confirmed an exceptional thrust-to-weight ratio and structural resilience. The project transitioned from an intuitive build to a diagnostic study of aerodynamic stall mechanics and center-of-gravity (CG) calibration.

### Key Findings
- Structural Integrity: The "Score-and-fold" method prvided significant structural integrity, sufficient for high-AOA and extreme G-force climbs, with no airframe deformation observed at all under maximum throttle. The hollowness of the fuselage contributes to an extremely aerodynamic design, despite high drag insinuated from the airfoil.
- Stability: Identification of a CG at the 56% chord position creates a critical pitch-up moment, exceeding the elevator's authority at both high and low speeds.
- Reinforcement: The usage of a power pod successfully isolated the kinetic energy to the replacable propellor, safeguarding the battery, motor, and ESC despite their location at the front of the aircraft.

### Future Technical Roadmap
- Static Margin Recalibration: Mechanically shifting the battery tray forward to lock the CG at the 25% chord ensures a self-leveling, energy-efficient flight path.
- Increased Ground Clearance: Redesigning the landing gear struts or purchasing professional landing gear allows for cleaner propellor rotation on unpaved rinways, offering less interference.
- Active Control: Implementing PID loops would allow for computerized stabilization, countering the high-theta instabilities identified during the intial flight test.



NOTE: This project remains an ongoing study in aerospace engineering, with the next flight test and data collection upcoming. I will continue editing this repository, keeping it up to date with the latest developments as they arrive.
