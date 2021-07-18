# Robot-Navigation-Using-SLAM-ROS
- This task is about controling the TurtleBot3 Robots (ROS standard platform robot) with the SLAM concept (simultaneous localization and mapping) to create a map using Lidar sensor and save the map.

## **Task(2) steps:**
---

1. Create a new project using ROS melodic at https://app.theconstructsim.com/#/MyRosjects.

<img width="635" alt="Screen Shot 1442-12-07 at 6 20 52 PM" src="https://user-images.githubusercontent.com/86277104/126044278-1de6852b-d4a4-4cb1-a4d0-95c216c5ab62.png">

---

2. Install TurtleBot3 Packages by using the following commands:
```
 $ sudo apt-get install ros-melodic-dynamixel-sdk
 $ sudo apt-get install ros-melodic-turtlebot3-msgs
 $ sudo apt-get install ros-melodic-turtlebot3
 ```
<img width="578" alt="Screen Shot 1442-12-07 at 6 24 20 PM" src="https://user-images.githubusercontent.com/86277104/126044810-cb995e55-7d93-4342-8352-eff234451cc2.png">


---

3. Install Simulation to run the Trurtlebot3 in an environment, by using the following codes in the terminal to install Simulation packages:
```
$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
```
<img width="925" alt="Screen Shot 1442-12-07 at 6 38 13 PM" src="https://user-images.githubusercontent.com/86277104/126052548-b8474ecc-0a95-492a-8b0c-34da5d714952.png">

- After this step open a new terminal and write ``` $ source ~/catkin_ws/devel/setup.bash ```

---

4. Launch Simulation World.There are 3 simulation environments are set for TurtleBot3 and I will lunch them one by one for testing.

- Empty world with a robot called "burger"
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
```
<img width="975" alt="Screen Shot 1442-12-08 at 2 38 29 AM" src="https://user-images.githubusercontent.com/86277104/126052771-7619ed95-87cc-46e1-8188-2e1b5863e203.png">

- TurtleBot3 World with a robot called "waffle"
```
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
<img width="874" alt="Screen Shot 1442-12-08 at 2 40 06 AM" src="https://user-images.githubusercontent.com/86277104/126052839-197a3004-b8e9-4162-8b2a-462e230c3f7d.png">

- TurtleBot3 House with a robot called waffle_pi
```
$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_gazebo turtlebot3_house.launch
```
<img width="969" alt="Screen Shot 1442-12-08 at 2 42 12 AM" src="https://user-images.githubusercontent.com/86277104/126052864-dd88a364-8b87-4329-8655-3b38ff7ca4b8.png">

-Then we will choose one of the previous robot which is waffle and we will control it using the keybored keys W: Forward, A: Left, S:Stop, D: Right, X:Backward.  And run the previous command for waffle robot. Then open new terminal and run the following command:
``` $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch ```

---

5. SLAM Simulation. In a new terminal Run these commands in the terminal to launch the simulation world:
```
$ export TURTLEBOT3_MODEL=waffle 
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
<img width="874" alt="Screen Shot 1442-12-08 at 2 40 06 AM" src="https://user-images.githubusercontent.com/86277104/126053109-6a3043a4-f9fb-48bf-9f48-e6769c5ad9e2.png">

---

6. Run the SLAM Node and see the generated map by the Robot, by using the following command in a new terminal:
```
$ export TURTLEBOT3_MODEL=waffle  
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
<img width="1183" alt="Screen Shot 1442-12-08 at 3 01 03 AM" src="https://user-images.githubusercontent.com/86277104/126053392-e7e5f87c-fdb9-49b5-82e9-2e72fb63a880.png">

---

7. Run Teleoperation Node to be able to interact and control the robot, by using the following command in a new terminal:
```
$ export TURTLEBOT3_MODEL=waffle 
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
<img width="978" alt="Screen Shot 1442-12-08 at 3 07 58 AM" src="https://user-images.githubusercontent.com/86277104/126053377-3017f0d5-4190-41c4-b381-4bca0dcdae04.png">


- **Now in the terminal we can control the robot using the W,A,S,D,X keybored keys to roam around the gazebo simulated map.**

---

8. Save a Map. After the map is created successfully in Rviz, open new terminal and save it using the command below:
```
$ rosrun map_server map_saver -f ~/map
```
<img width="943" alt="Screen Shot 1442-12-08 at 3 16 45 AM" src="https://user-images.githubusercontent.com/86277104/126053436-77482a7a-b65f-41c4-bd5c-98c58fdf4ad3.png">
<img width="514" alt="Screen Shot 1442-12-08 at 5 37 26 AM" src="https://user-images.githubusercontent.com/86277104/126053937-fda668cc-ae18-4c86-a4e5-d9924560dca8.png">




