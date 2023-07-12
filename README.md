# WALL-E
![Robot](https://github.com/bob4o-afk/wall-e/assets/80552018/c3634c99-9422-4410-bbde-72023dffe683)

This GitHub repository contains the code and necessary files for a robot that can recognize trash objects and pick them up. The robot utilizes machine learning and computer vision techniques to detect and locate trash objects, and it is equipped with a robotic arm for picking up the trash. The repository includes two main code files: one for object detection using ML5.js library and another for controlling the robot's movements and interactions.

## Object Detection Code (HTML and JavaScript)

The `index.html` file provides the user interface for controlling the object detection process. It includes a "Start Detecting" button that triggers the object detection algorithm using ML5.js. The code uses the COCO-SSD model for object detection. When the detection is running, the video stream from the robot's camera is processed, and any detected trash objects (specifically bottles) are highlighted with bounding boxes and labels. This information is then displayed on the video stream.

The JavaScript code in the `script` tags handles the initialization of the video capture, ML5 object detector, and drawing the detection results on the canvas. It also includes functions for starting and stopping the detection process. The code utilizes the p5.js library for creating and manipulating the canvas element.

## Robot Control Code (C++)

The main robot control code is written in C++ and runs on an ESP32 microcontroller. It handles the robot's movements, servo control, and communication with the web interface. The code uses the ESP32-CAM module for camera input and Wi-Fi connectivity.

The `setup()` function initializes the necessary components and configurations, including the camera, servo motor, and Wi-Fi connection. It also sets up the HTTP server for handling the web interface requests.

The `loop()` function runs continuously and handles the robot's actions based on the commands received from the web interface. It controls the robot's movement (forward, backward, left, right), stops the robot, and adjusts the servo position. Additionally, it handles the on/off state of a light connected to a GPIO pin.

The code also includes an HTML page stored as a C string (`INDEX_HTML`). This page provides the user interface for controlling the robot's movements and displaying the camera stream. It includes buttons for moving the robot in different directions, a slider for adjusting the servo position, and a button for controlling the light.

## Getting Started

To use this code for your trash recognition and pickup robot, follow these steps:

1. Set up the hardware components of the robot, including the ESP32 microcontroller, camera module, servo motor, and any other necessary components.

   ![Hardware Setup](hardware_setup.jpg)

2. Connect the hardware components according to the pin configuration specified in the code.

3. Upload the C++ code to the ESP32 microcontroller using the Arduino IDE or any other suitable development environment.

4. Ensure that the required libraries and dependencies are installed for both the HTML/JavaScript code (ML5.js, p5.js) and the C++ code (esp_camera.h, WiFi.h, etc.).

5. Modify the code as needed to adapt it to your specific robot configuration and requirements.

6. Connect the robot to a power source and turn it on.

   ![Robot Power](robot_power.jpg)

7. Connect a computer or mobile device to the same Wi-Fi network as the robot.

8. Open a web browser and navigate to the IP address of the robot (displayed in the serial monitor during setup).

   ![Web Interface](web_interface.jpg)

9. The web interface will be displayed, allowing you to control the robot's movements, adjust the servo position, and view the camera stream.

10. Start the object detection process by clicking the "Start Detecting" button on the web interface. The robot will detect and highlight trash objects (specifically bottles) in the camera stream.

## Contributions

Contributions to this project are welcome. If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request on the GitHub repository.

Let's build a cleaner future together with this trash recognition and pickup robot!

![Cleaner Future](cleaner_future.jpg)
Как се програмира:






![image](https://user-images.githubusercontent.com/80323655/233776831-18c0cd8b-260d-4f21-801d-d9201b0b7d03.png)

Примерна схема:




![image](https://user-images.githubusercontent.com/80323655/233776931-c38c405b-91ec-4109-9751-28fbdcf2d848.png)






Инсталиране на нужни библиотеки:
Във Arduino IDE отидете на File>Preferences 



![image](https://user-images.githubusercontent.com/80323655/233777703-c15c44a9-c530-4a31-9241-d2358589cdf2.png)


Примерен код:
In your Arduino IDE, go to File > Examples > ESP32 > Camera and open the CameraWebServer example.


![image](https://user-images.githubusercontent.com/80323655/233777531-aacc7813-754d-4fbf-ab33-0b5883469323.png)
