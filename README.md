# iot-traffic-controller
🚦 IoT Traffic Light Controller & Digital Devices Fundamentals

Course: CEIS 114 – Introduction to Digital Devices
Author: Shawn Hoefert
Date: July 2023
📌 Project Overview

This project explores foundational electronic, digital, and system integration concepts through the development of a series of IoT-based traffic light controllers. Utilizing ESP32 microcontrollers and various sensors, the project demonstrates practical skills in hardware interfacing, embedded programming, and implementing complex control logic for real-world applications. It progresses from basic traffic light control to incorporating crosswalk functionality, emergency alerts, and smart sensor integration.
🎯 Key Objectives

    Hardware Interfacing: Connect and configure microcontrollers (ESP32) with LEDs, push buttons, LCD displays, PIR motion sensors, and buzzers.

    Embedded Programming: Develop C++ code (Arduino IDE) to manage digital and analog inputs/outputs, implement timing sequences, and control device behavior.

    Control System Logic: Design and implement sequential and event-driven logic for traffic light patterns, pedestrian crosswalks, and emergency responses.

    IoT Fundamentals: Understand the basic principles of connected devices and their role in automated systems.

    Data Communication: Utilize serial communication for debugging and monitoring system states.

    System Integration: Combine multiple components and logical modules into a cohesive, functional system.

🔧 Tools & Technologies

    Microcontroller: ESP32 Board

    Development Environment: Arduino IDE

    Components:

        Colored LEDs (Red, Yellow, Green, Blue)

        220 Ohm Resistors

        Push Buttons

        LCD Unit with I2C Adapter

        Active Buzzer

        PIR Motion Sensor

        Breadboards, Wires

    Programming Language: Arduino C++

    Concepts: Digital I/O, Analog I/O, Timers, State Machines, Serial Communication, Interrupts (for buttons), Sensor Integration.

🔄 Workflow & Modules Summary

This project involved building progressively complex traffic light systems:

    Module 3: Basic Traffic Light Controller:

        Objective: Implemented a single traffic light sequence (Red, Yellow, Green) using an ESP32 board and LEDs.

        Skills: Basic circuit wiring, pinMode, digitalWrite, delay functions.

    Module 4: Multiple Traffic Light Controller:

        Objective: Expanded to control two sets of traffic lights, simulating an intersection.

        Skills: Managing multiple digital outputs, coordinating light sequences.

    Module 5: Traffic Light with Crosswalk:

        Objective: Added a pedestrian crosswalk button that interrupts the traffic light sequence to allow pedestrians to cross.

        Skills: Button input handling (INPUT_PULLUP), conditional logic, Serial.print for status updates.

    Module 6: Traffic Light with Crosswalk & Emergency Buzzer/LCD:

        Objective: Integrated an LCD display for status messages and an emergency buzzer.

        Skills: LCD interfacing (I2C), Wire.h, LiquidCrystal_I2C.h libraries, incorporating audible alerts.

    Final Project Component (Option 2): Traffic Light with Crosswalk, Emergency Buzzer, and SMART Sensor (PIR Motion Sensor):

        Objective: Enhanced the system with a PIR motion sensor for automated emergency light activation and integrated all previous functionalities.

        Skills: PIR sensor integration, motion detection logic, advanced system integration.

💻 Code Examples & Logic

While specific project files may not be available, the core logic and programming concepts applied in this project are outlined below, demonstrating proficiency in embedded systems development.
Basic Traffic Light Sequence Logic (Module 3/4)

    Setup: Initialize GPIO pins for multiple Red, Yellow, and Green LEDs as outputs.

    Loop: Implement a continuous loop that cycles through traffic light states (e.g., Green for 2 seconds, Yellow for 1 second, Red for 3 seconds) by setting appropriate digitalWrite commands for each LED.

Crosswalk Button Logic (Module 5)

    Input: Digital read from a push button configured as INPUT_PULLUP.

    Logic: When the crosswalk button is pressed, the traffic light sequence transitions to a "Stop All Traffic" state (both directions red), activates a "Walk" countdown on the Serial Monitor, and then returns to normal operation.

    Output: LED state changes, Serial Monitor output for countdown.

LCD Display & Emergency Buzzer Logic (Module 6)

    Setup: Initialize the LCD display via I2C. Initialize buzzer GPIO as output.

    Logic:

        Display status messages on the LCD (e.g., "Do Not Walk", "Walk").

        Activate the buzzer for emergency alerts or specific sequence changes.

    Output: Text on LCD, audible alerts.

PIR Motion Sensor Integration (Final Component)

    Input: Digital read from a PIR motion sensor.

    Logic: When motion is detected by the PIR sensor, an emergency light (e.g., a blue LED) is activated, and potentially an emergency buzzer, overriding normal traffic light operations.

    Output: Emergency light activation, potential buzzer alert, Serial Monitor messages (e.g., "motion detected", "Emergency button was pressed").

📈 Skills Demonstrated

    Embedded Systems & IoT: Practical experience with microcontrollers (ESP32) and building connected devices.

    Hardware Interfacing: Proficient in wiring and integrating various sensors (PIR, push buttons) and actuators (LEDs, LCD, buzzer).

    Programming (Arduino C++): Ability to write, debug, and implement control logic for real-time embedded applications.

    Control Systems: Design and implementation of sequential and event-driven control logic for complex systems.

    Problem-Solving & Troubleshooting: Diagnosing and resolving issues in hardware connections and code functionality.

    Data Communication: Utilizing serial communication for system monitoring and debugging.

    System Integration: Combining multiple modules and components into a cohesive, functional project.
