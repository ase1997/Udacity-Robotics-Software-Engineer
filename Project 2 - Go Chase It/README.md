## Project 2 - Go Chase It

## About the Project
  - This project is to use tools leanred in ROS, C++ and Gazebo to build a ball-chasing robot
  - Place the robot in my Gazebo world 
  - Write C++ ROS node to make the robot chase a white ball
  - Key skilles demonstarted 
    - Building Catkin Workspaces
    - ROS node creation
    - ROS node communication
    - Using additional ROS packages
    - Gazebo world integration
    - Additional C++ practice
    - RViz Integration
    
## Tasks
  - Create **drive_bot** ROS package
    - Create **my_robot** ROS package to hold robot, whiet ball, and Gazebo simulation world
    - Design a differential drive robot with the Unified Robot Description Format with a LiDAR and a camera and add Gazebo plugins
    - Create a new wrold that is different from [Project 1](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%201%20-%20Build%20My%20World)

## Running Code
  - Open terminal in Linux \[virtual\] env
  - `sudo apt-get update`
  - `sudo apt-get upgrade`
  - `git clone` this repo.
  - `cd project_1`
  - `mkdir build && cd build`
  - `cmake ..`
  - `make`
  - `export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/project1/build`
  - `cd world`
  - `gazebo myworld`

## Results
Gazebo World         |  Gazebo Robot Model
:-------------------------:|:-------------------------:
![](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/blob/main/Project%201%20-%20Build%20My%20World/pics/pic_1.PNG)  |  ![](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/blob/main/Project%201%20-%20Build%20My%20World/pics/pic_2.PNG)
