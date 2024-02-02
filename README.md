# Dual Axis Sun Tracking Solar Panel System without Microcontrollers

OVERVIEW:
A dual-axis sun tracker represents a significant advancement in solar energy harvesting compared to fixed solar panels. The fundamental principle underlying this enhanced efficiency lies in the tracker's ability to dynamically follow the sun's movement on both the horizontal and vertical axes throughout the day.
Unlike fixed solar panels that remain stationary, a dual-axis sun tracker continually adjusts its orientation to directly face the sun, optimizing the incident sunlight angle. This dynamic alignment ensures that the solar panels receive sunlight perpendicular to their surface, maximizing the exposure to solar radiation. Here's how a dual-axis sun tracker harnesses more energy
This project presents a comprehensive solution for a Dual Axis Sun Tracking Solar Panel System, designed entirely without the use of microcontrollers. Leveraging basic logic components, the system ensures precise solar panel orientation for optimal energy harnessing. The approach combines ingenuity with practicality to achieve efficient sun tracking without the complexities of microcontroller programming.

COMPONENTS USED:<br>
•	LM324 op-amps<br>
•	2-way switch<br>
•	SPDT relays<br>
•	L298 H-bridge circuit<br>
•	Limit switches<br>
•	555 timer IC<br>

FUNCTIONALITIES OF EACH CIRCUIT MODULE<br>

LDR Circuit (LM324 Op-Amp):<br>
Configured as comparators in a voltage divider setup with four Light Dependent Resistors (LDRs), two for each axis (x and Y). Enable precise voltage comparison to determine sunlight intensity. Use PROTEUS simulation File for more understanding. 

Joystick Control (LM324 Op-Amp):<br>
Manual control is implemented through a joystick, employing a similar LDR voltage divider configuration. Allows for manual override of the sun tracking system. This helps maintain purposes and allows users to change the sun panel position as they need.<br>
Outputs of the both, joystick circuit and LDR Circuit are,<br>
     1-1 ---> No change<br>
     0-1 ---> Anti-clockwise direction<br>
     1-0 ---> Clockwise direction<br>
     0-0 ---> No change<br>
<br>
2-Way Switch and Relay_circuit_1:<br>
Facilitates toggling between automatic and manual control modes.
Utilizes a relay circuit with 4 SPDT relays to isolate the outputs of the two control circuits. As we know all circuit components have their specific reverse breakdown voltage levels. So if that level is exceeded that respective component gets burnt. This relay_circuit_1 is implemented for that reason. When one configuration is in working position other circuits get no current as well as relay circuit isolates the outputs of opamps. Refer Proteus Simulation File for more details.<br>
<br>
H-Bridge L298 Circuit:<br>
As we know to change the direction of a DC motor, we have to change the polarity of the voltage supply manually. to make this automated the H-bridge circuit was used. So l298 module has two H-bridge circuits. So, it can drive both X and Y-axis movements. Ensures smooth and controlled motion based on the input from the comparator circuits.<br>
<br>
Limit Switches and Relay_circuit_2: <br>
These two circuits were implemented to restrict the turning angles of the solar panel in both the X and Y axes. Each axis has two limit switches to control right and left, up and down movements. When 1-0 comes as the outputs the solar panel starts to rotate clockwise direction, and at the limit angle it closes the limit switch, and it ignites the respective relay and makes 1(High) to 0(low-GND). For every direction this happens. <br>

<br>
PWM Generator with 555 Timer IC:<br>
Regulates the turning speed by generating Pulse Width Modulation (PWM) signals. Feeds into the voltage reference pins of the L298 drivers for precise motor control.
<br>
<br>
Functionalities:<br>
•	Automatic sun tracking using LDRs and LM324 op-amps.<br>
•	Manual control via joystick for user intervention.<br>
•	Circuit isolation and mode toggling using a 2-way switch and relay circuit.<br>
•	Limit switches to prevent over-rotation in both X and Y axes.<br>
•	PWM-based speed control for smooth and controlled movements.<br>
<br>
Conclusion:<br>
This project showcases a robust sun-tracking system, emphasizing simplicity and effectiveness without relying on microcontrollers. The detailed integration of various components demonstrates a thorough understanding of electronic circuits and automation principles. The provided functionalities offer a versatile and reliable solution for optimizing solar energy capture.


