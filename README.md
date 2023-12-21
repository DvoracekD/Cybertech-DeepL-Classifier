# Cybertech-DeepL-Classifier
NN detection, classification, localization for KUKA Cybertech for Deep Learning course for CIIRC Testbed for Industry 4.0

# Current state and previous works:
David, Artem, Martin, Vítek, Varun, Jirka

**NDA applies, do not share**  



<details>
  <summary><i>Real footage folder tree</i></summary>  
  <img width="167" alt="image" src="https://github.com/martimik10/Cybertech-DeepL-Classifier/assets/88324559/e88e9726-a8c0-41b9-89b6-1295901d73a4">
</details>  





[Github repo (CIIRC)](https://github.com/testbedCIIRC/Robot-Vision-PickPlace/tree/main)

[IEEE-CASE 2023 Paper](https://ieeexplore.ieee.org/document/10260601)

## HW setup
Our setup consists of a KUKA KR Cybertech industrial robot, a PLC, a conveyor belt with rotary encoder and an Intel Realsense RGBD camera. We mounted apriltags on the conveyor for robot workspace detection.
![StateMachineSimple](readme_imgs/StateMachineSimple.png)
![HWSetup](readme_imgs/HWSetup.png)

## Robot system and control
The high level control, coded in Python, utilizes an OPC UA Client that runs on the PC. It includes a finite state machine for the trajectory planning based on visual recognition, which reads sensor and robot data from the OPC UA nodes and sends high level control actions and path trajectory updates to the OPC UA Server on the PLC. These inputs are converted into control instructions using the mx Automation package and are sent to the robot controller via Profinet.

## Vision
Currently, only HSV and simple computer vision algorithms are implemented for successful pick & operations

![RobotVideo](readme_imgs/robot_video.gif)
![detection_frame](readme_imgs/detection_frame.gif)
![packets](readme_imgs/packet_optimal_pt.gif)


# Our task
Martin, Ondra, Dominik

Create data synthesization for datasets and use knowledge from DTU Deep Learning course to create NN-based classifier + localizer of objects

![data_synth](readme_imgs/image_1.png)
