## Project 3 - Where Am I

## About the Project
  - This project is to interface my own mobile robot with the Adaptive Monte Carlo Localization algorithm in ROS to estimate robot's position as it travals through predifined world from [Project 2](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%202%20-%20Go%20Chase%20It)
  - Tune different parameters to increase the localization efficiency
  - Key skills demonstrated
    - Implementation of Adaptive Monte Carlo Localization in ROS
    - Understanding of tuning parameters required

## Structure
Naming might be different
```
.Project3                                    # Where Am I Project
├── catkin_ws                                  # Catkin workspace
│   ├── src
│   │   ├── ball_chaser                        # ball_chaser package        
│   │   │   ├── launch                         # launch folder for launch files
│   │   │   │   ├── ball_chaser.launch
│   │   │   ├── src                            # source folder for C++ scripts
│   │   │   │   ├── drive_bot.cpp
│   │   │   │   ├── process_images.cpp
│   │   │   ├── srv                            # service folder for ROS services
│   │   │   │   ├── DriveToTarget.srv
│   │   │   ├── CMakeLists.txt                 # compiler instructions
│   │   │   ├── package.xml                    # package info
│   │   ├── my_robot                           # my_robot package        
│   │   │   ├── config                         # config folder for configuration files   
│   │   │   │   ├── base_local_planner_params.yaml
│   │   │   │   ├── costmap_common_params.yaml
│   │   │   │   ├── global_costmap_params.yaml
│   │   │   │   ├── local_costmap_params.yaml
│   │   │   ├── launch                         # launch folder for launch files   
│   │   │   │   ├── amcl.launch
│   │   │   │   ├── robot_description.launch
│   │   │   │   ├── world.launch
│   │   │   ├── maps                           # maps folder for maps
│   │   │   │   ├── map.pgm
│   │   │   │   ├── map.yaml
│   │   │   ├── meshes                         # meshes folder for sensors
│   │   │   │   ├── hokuyo.dae
│   │   │   ├── rviz                           # rviz folder for rviz configuration files
│   │   │   │   ├── default.rviz
│   │   │   ├── urdf                           # urdf folder for xarco files
│   │   │   │   ├── my_robot.gazebo
│   │   │   │   ├── my_robot.xacro
│   │   │   ├── worlds                         # world folder for world files
│   │   │   │   ├── empty.world
│   │   │   │   ├── office.world
│   │   │   ├── CMakeLists.txt                 # compiler instructions
│   │   │   ├── package.xml                    # package info
│   │   ├── pgm_map_creator                    # Create pgm map from Gazebo world file for ROS localization
│   │   │   ├── maps
│   │   │   │   ├── map.pgm                    # map files of office.world, generated by pgm_map_creator
├── my_ball                                    # Model files 
│   ├── model.config
│   ├── model.sdf
```
    
## Tasks
  - Create ROS Package containing AMCL, teleop, robot, world and map files
  - Create launch file contains the following nodes:
    - Map Server
    - AMCL
    - Move Base
  - Robot localize itself after being tele-operated in Gazebo or given navigation goal target in Rviz.

## Running Code
  - Initialize a ROS workspace `project3/catkin_ws/src`
  - `cd project3/catkin_ws/src`
  - `git clone` this repo
  - `cd ..`
  - `catkin_make`
  - `source devel/setup.bash`
  - `roslaunch my_robot world.launch`
  
  - Open second terminal
  - `cd project2/catkin_ws`
  - `source devel/setup.bash`
  - `roslaunch my_robot amcl.launch`
  
  - In Rviz, select **odom** for **fixed frame** add **RobotModel**, **Map** (topic: `/map`), **PoseArray** (topic: `/particlecloud`)

## Results
Initial Localization         |  Updated Localization
:-------------------------:|:-------------------------:
![](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/blob/main/Project%203%20-%20Where%20Am%20I/pics/pic_3.PNG)  |  ![](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/blob/main/Project%203%20-%20Where%20Am%20I/pics/pic_5.PNG)
