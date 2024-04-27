# Robotics Prototype for Selective Agricultural Spraying
## Overview
This prototype showcases a robot designed for agricultural use, specifically for selectively spraying plants based on AI analysis. The robot consists of two main parts: the main robot and a communication module facilitating interaction between the computer and the robot.

## Operation
The robot traverses the field, continuously capturing photos using a Raspberry Pi and a Raspberry Pi Camera v3. These images are processed using YOLOv8 NANO AI model from Ultralytics to identify plant positions. By maintaining a fixed distance between the camera and the ground, pixel measurements can be translated to real-world distances.

## Calculation of Spray Angles
Using trigonometry, the robot computes the angles required for the servos to position a laser diode accurately on the identified plants. This involves determining the real positions of the plants relative to the camera and then calculating the angles based on the triangle formed by the plant positions and the camera.

## Communication
Communication between modules is facilitated by two NRF24L01+ transceivers, each controlled by an Arduino Nano microcontroller. One transceiver communicates with the Raspberry Pi, while the other communicates with the computer. Data, including servo angles and plant positions and categories, are processed on the Raspberry Pi and then transmitted to the computer via the Arduino Nano modules.

## Visualization
A desktop application developed using Tauri utilizes the plant positions and categories to generate scatter charts, providing a visual representation of the field. This allows for the creation of a detailed map displaying the location of each plant.

## Additional Components
1. Raspberry Pi 5
2. RPI Camera v3
3. 2x Arduino Nano
4. 2x NRF24L01+ Transceiver
5. DC-DC Step-Down Converter
6. 12V Power Supply
7. IMU ICM20948 (not fully integrated yet)
8. 2x Servo MG996 90 Degree
## Future Improvements
Integration of the IMU will enhance position calculation accuracy, especially when the robot doesn't move in a straight line. This will improve the precision of plant positioning over short distances, compensating for the sensor's inherent noise and limited precision in linear motion calculation.
