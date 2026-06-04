# Design-an-fridge-door-opening-alarm-circuit-using-Eagle-software

## AIM:
To design the schematic and PCB layout diagram of an fridge door opening alarm circuit using Eagle software.

## EQUIPMENT REQUIRED:
● Hardware: Personal Computer (PC)
● Software: Eagle

## PROCEDURE:
```
 Create a New Project:
o Launch EAGLE and start a new project for your PCB design.
o Within the project, create a new schematic file.
 Add Components:
o Utilize the built-in libraries in EAGLE or create custom libraries if needed.
o Use the 'Add' tool to place the required components onto the schematic sheet.
 Make Connections:
o Connect the components using the 'Net' tool.
o Label the nets clearly to maintain clarity and organization in your design.
 Check for Errors:
o Once the schematic design is complete, perform an Electrical Rule Check (ERC) to identify and correct any errors.
o Save the schematic after confirming that no errors are present.
 Switch to Board Layout:
o Click on the 'Generate/Switch to Board' button to create the PCB layout from the schematic.
 Arrange Components and Route Traces:
o In the board layout editor, arrange the components to optimize space and reduce signal interference.
o Use the 'Route' tool to connect the components based on the schematic design.
o Ensure proper routing by utilizing the available editing tools in EAGLE to avoid design rule violations.
 Design Rule Check (DRC):
o Perform a Design Rule Check (DRC) to ensure that the routing and layout comply with design standards and that there are no issues.
o Save the board layout after resolving any errors.
 Generate Gerber Files:
o Go to File > CAM Processor and configure the CAM jobs to generate Gerber files for all PCB layers, such as copper layers, silkscreen, solder mask, and drill files.
o Verify the generated files to ensure they contain all necessary information for manufacturing.
 Save Manufacturing Files:
o Save the Gerber files and any other required manufacturing files to send to your PCB manufacturer for fabrication.
```

## THEORY:
The fridge door opening alarm circuit consists of a 9V supply, an LDR light sensor, and two NE555 timer ICs configured in monostable and astable modes. The LDR is positioned such that it remains in the dark when the fridge door is closed, resulting in very high resistance. This keeps the voltage at the trigger pin of the first 555 timer (U1) above the threshold level, so the IC does not activate. When the fridge door opens, the fridge light falls on the LDR and its resistance decreases sharply, causing the trigger pin voltage to fall below the trigger point. This event enables U1 to switch ON and generate a pulse of fixed duration, determined by components R3, R4, and capacitor C1. The diode D1 ensures correct polarity protection, while the remaining resistors provide stable biasing and timing control.

The output of U1 is supplied to the second 555 timer (U2), which is configured in astable mode to produce continuous square wave pulses. When enabled by U1, the astable oscillations repeatedly turn the LED and buzzer ON and OFF, resulting in a blinking light and beeping sound that alerts the user that the fridge door has been left open. Components R5, R6, and C2 decide the rate of blinking and beeping. Once capacitor C1 in the first timer fully charges, U1 automatically switches OFF, thereby stopping the activation of U2 and turning the alarm OFF even if the fridge door remains open. This design saves battery power and prevents irritation due to continuous alarm sound. Overall, the circuit offers a reliable, low-cost electronic solution for reminding the user to close the fridge door, reducing cooling loss and preserving stored food effectively.

## CIRCUIT DIAGRAM:
<img width="783" height="285" alt="image" src="https://github.com/user-attachments/assets/d82043db-a3b3-4e42-a309-316f81aa2bec" />

## EXPECTED OUTPUT:

### Schematic diagram
<img width="1600" height="852" alt="image" src="https://github.com/user-attachments/assets/1737f23c-0c39-4449-ab09-e0b8bbd4dfe4" />

### Layout diagram
<img width="1600" height="857" alt="image" src="https://github.com/user-attachments/assets/97e23b14-0cd7-4356-bc18-a420f9a0829f" />

## RESULT:
Thus, the schematic and PCB layout for the fridge door opening alarm circui has been successfully designed using Eagle software.
