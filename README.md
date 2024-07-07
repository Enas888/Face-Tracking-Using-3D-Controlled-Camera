# Face-Tracking-Using-3D-Controlled-Camera
The video captured can be transmitted to a server machine either via network (in case of IP camera) or by direct USB connection (in case of USB camera). The later
was utilized in this project, however an IP camera also could have been used. The captured video is then streamed over a local network (or HTTP network) to the
client. The client can either turn on the camera control in auto mode or control the camera position manually. The auto mode lets the server detect a human face for a
person setting in front of the camera. If the face moves then the server will communicate with the stepper motors and rotate them accordingly to center the detected face in the captured video frame.

The server can control the camera position by communicating wirelessly (via WiFi connection) with a microcontroller chip (ESP8266 in our case). The microcontroller 
receives from the server three parameters, which motor to be rotated, how many steps, and the direction of rotation. The microcontroller then
generates the necessary signal (sequence) to control each motor.
