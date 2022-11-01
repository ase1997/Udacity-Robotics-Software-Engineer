## Project 4 - Map My World

## About the Project
  - This project is to interface my robot with an RTAB-Map ROS package for localization and 2D/3D mapping
  - Place the robot in my Gazebo world 
  - Key skills demonstrated
    - SLAM implementation with ROS/Gazebo
    - ROS debugging tools: rqt, roswtf

## Structure
Naming might be different
```
.Project4                                  # Map My World Project
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
│   │   │   │   ├── mapping.launch
│   │   │   │   ├── localization.launch
│   │   │   │   ├── rtabmap.db
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
│   │   ├── pgm_map_creator                    # pgm_map_creator        
│   │   │   ├── launch                         # launch folder for launch files   
│   │   │   │   ├── request_publisher.launch
│   │   │   ├── maps                           # maps folder for generated maps
│   │   │   │   ├── Backup_map.pgm
│   │   │   │   ├── map.pgm
│   │   │   ├── msgs                           # msgs folder for communication files
│   │   │   │   ├── CMakeLists.txt
│   │   │   │   ├── collision_map_request.proto
│   │   │   ├── src                            # src folder for main function
│   │   │   │   ├── collision_map_creator.cc
│   │   │   │   ├── request_publisher.cc
│   │   │   ├── world                          # world folder for world files
│   │   │   │   ├── office.world
│   │   │   │   ├── udacity_mtv
│   │   │   ├── CMakeLists.txt                 # compiler instructions
│   │   │   ├── LICENSE                        # License for repository
│   │   │   ├── README.md                      # README for documentation
│   │   │   ├── package.xml                    # package info
│   │   ├── teleop_twist_keyboard              # teleop_twist_keyboard
│   │   │   ├── CHANGELOG.rst                  # change log
│   │   │   ├── CMakeLists.txt                 # compiler instructions
│   │   │   ├── README.md                      # README for documentation
│   │   │   ├── package.xml                    # package info
│   │   │   ├── teleop_twist_keyboard.py       # keyboard controller
├── my_ball                                    # Model files 
│   ├── model.config
│   ├── model.sdf
├── screenshot.JPG                             # Screenshots
├── screenshot1.JPG                            # Screenshots
├── rtabmap.db
```
    
## Tasks
  - Create ROS package to interface with **rtabmap_ros** package
  - Build upon [Project 3](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%203%20-%20Where%20Am%20I) to make necessary changes
  - Use **teleop** package to move the robot around the Gazebo world and map it

## Running Code
  - Initialize a ROS workspace `project4/catkin_ws/src`
  - `cd project2/catkin_ws/src`
  - `git clone` this repo
  - `cd ..`
  - `catkin_make`
  - `source devel/setup.bash`
  - `roslaunch my_robot world.launch`
  
  - Open second terminal
  - `cd project4/catkin_ws`
  - `source devel/setup.bash`
  - `rosrun teleop_twist_keyboard teleop_twist_keyboard.py`
  
  - Open third terminal
  - `cd project4/catkin_ws`
  - `source devel/setup.bash`
  - `roslaunch my_robot mapping.launch`

## Results
Refer to [/pics](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%204%20-%20Map%20My%20Wolrd/pics)
