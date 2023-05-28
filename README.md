# Dual-Axis Solar Tracker Documentation
## **Introduction**
The Dual-Axis Solar Tracker is a project designed to optimize the positioning of a solar panel to maximize its exposure to sunlight throughout the day. By utilizing two servomotors and four Light Dependent Resistor (LDR) sensors, controlled with an Arduino Uno microcontroller, this solar tracker adjusts the panel's orientation to follow the sun's movement across the sky or any other light source.
## **Project Overview**
The solar tracker consists of the following main components:
-	Arduino Uno: The Arduino board acts as the brains of the system, controlling the servomotors and processing sensor inputs.
-	Two Servo Motors: These motors are responsible for adjusting the solar panel's horizontal and vertical angles.
-	Four LDRs: Light Dependent Resistors sense the light intensity on different sides of the solar panel.
-	Mini Solar Panel: Represents the solar panel that the tracker is designed to control.
Through the integration of these components, the Dual-Axis Solar Tracker enables the solar panel to autonomously adjust its position, maximizing the absorption of solar energy and enhancing the overall energy output of the system. The project showcases the application of servomotors and sensor feedback to create an efficient and effective solar tracking solution.
## **Hardware Requirements**
**To build the Dual-Axis Solar Tracker, the following hardware components are required:**
-	Arduino Uno board
-	Two servomotors
-	Four resistors
-	Four LDRs
-	Mini solar panel
- Breadboard
-	Jumper wires
-	Power supply 
-	Mounting hardware 
## **Software Requirements**
To program the Arduino Uno board for the solar tracker, the following software tools are needed:
-	Arduino IDE
-	Servo library (included in Arduino IDE)
## **Circuit Diagram**
 ![Solar_Tracker_Dual_Axis](https://github.com/polinizal/Solar-Tracker-Dual-Axis/assets/71072498/3480a32e-5498-49c4-9ce3-3eee843522d6)
The circuit diagram illustrates the connections between the components. 
## **Code Explanation**
1.	The code uses the Servo library to control two servomotors: servohori for horizontal movement and servoverti for vertical movement.
2.	The code defines the limits of movement for each servomotor using variables such as servohLimitHigh and servohLimitLow.
3.	Four LDRs are connected to the analog input pins of the Arduino: ldrtopr, ldrtopl, ldrbotr, and ldrbotl.
4.	In the setup() function, the initial positions of the servo motors are set, and a delay is added for stability.
5.	In the loop() function, the code continuously reads the LDR values and calculates average values for different combinations.

**Based on the LDR readings, the code adjusts the servo positions:**
-	If the top LDR readings are lower than the bottom LDR readings, the vertical servo position is decreased by 1 degree, clamped to the upper limit.
-	If the bottom LDR readings are lower than the top LDR readings, the vertical servo position is increased by 1 degree, clamped to the lower limit.
-	If the LDR readings are equal, the vertical servo position remains unchanged.
-	Similar logic is applied to adjust the horizontal servo position based on left and right LDR readings.

## **Step-by-Step Instructions**
**Follow these instructions to build the Dual-Axis Solar Tracker:**
1. Assemble the hardware components on the breadboard.
2. Connect the servomotors to the appropriate pins on the Arduino Uno, ensuring proper power and ground connections.
3. Connect the LDRs to analog input pins on the Arduino Uno. Use the resistors to create a voltage divider circuit for each LDR.
4. Upload the code to the Arduino Uno using the Arduino IDE.
5. Power on the system and observe the servomotors adjusting the solar panel's orientation.
## **Testing and Troubleshooting**
**To test the Dual-Axis Solar Tracker, follow these steps:**
-	Place the solar tracker setup under sunlight.
-	Observe the servomotors' movement as they adjust the solar panel to track the sun.
-	Verify that the solar panel's orientation changes to maximize exposure to sunlight throughout the day.
**If you encounter any issues, consider the following troubleshooting tips:**
-	Check all connections and ensure they are properly secured.
-	Verify that the LDRs are positioned correctly to sense light accurately.
-	Ensure that the servomotors are powered and connected correctly.
-	Review the code for any syntax errors or incorrect pin assignments.
## **Safety Considerations**
**When building and operating the Dual-Axis Solar Tracker, keep the following safety considerations in mind:**
-	Be cautious while handling electrical components to avoid electric shocks.
-	Disconnect power before making any changes to the circuit.
-	Avoid exposing the components to moisture or extreme environmental conditions.
## **Conclusion and Future Improvements**
The Dual-Axis Solar Tracker project demonstrates a functional system for maximizing solar panel efficiency. With proper documentation and understanding, users can replicate or modify the design to suit their specific needs.
Possible future improvements for this project could include:
-	Adding a battery where the gathered solar energy can be saved.
-	Implementing a real-time clock module to track time accurately.
-	Incorporating wireless communication for remote monitoring and control.
-	Adding a light sensor for automatically turning off the tracker during nighttime.

# **Contact Information**
Our team consists of:
Polina Staneva ⇒ polina.staneva@yahoo.com
Kosta Ilev ⇒ kosta.ilev@gmail.com
Ekaterina Staneva ⇒ ekaterina18.st@gmail.com
This project was created by team “Power Trio Web Cats”
![image](https://github.com/polinizal/Solar-Tracker-Dual-Axis/assets/71072498/1d899e1e-869b-444a-8623-cb8dc3bd1cb9)


