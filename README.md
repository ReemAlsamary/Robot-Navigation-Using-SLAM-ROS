# Robot-Navigation-Using-SLAM-ROS
- This task is about controling the TurtleBot3 Robots (ROS standard platform robot) with the SLAM concept (simultaneous localization and mapping) to create a map using Lidar sensor and save the map.

## **Task(2) steps:**
---

1. Create a new project using ROS melodic at https://app.theconstructsim.com/#/MyRosjects.

<img width="635" alt="Screen Shot 1442-12-07 at 6 20 52 PM" src="https://user-images.githubusercontent.com/86277104/126044278-1de6852b-d4a4-4cb1-a4d0-95c216c5ab62.png">

---

2. Install TurtleBot3 Packages by using the following commands:
- $ sudo apt-get install ros-melodic-dynamixel-sdk
- $ sudo apt-get install ros-melodic-turtlebot3-msgs
- $ sudo apt-get install ros-melodic-turtlebot3
<img width="578" alt="Screen Shot 1442-12-07 at 6 24 20 PM" src="https://user-images.githubusercontent.com/86277104/126044810-cb995e55-7d93-4342-8352-eff234451cc2.png">


---

3. Set TurtleBot3 Model Name, choose the Trurtlebot you want to work with:

In case of TurtleBot3 Burger

- echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc

In case of TurtleBot3 Waffle Pi

- echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc
