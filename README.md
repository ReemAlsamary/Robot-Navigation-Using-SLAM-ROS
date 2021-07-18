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

3. Install Simulation to run the Trurtlebot in an environment, by using the following codes in the terminal to install Simulation packages:
```
{$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
}
```
<img width="925" alt="Screen Shot 1442-12-07 at 6 38 13 PM" src="https://user-images.githubusercontent.com/86277104/126052548-b8474ecc-0a95-492a-8b0c-34da5d714952.png">

