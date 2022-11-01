## Project 5 - Home Service Robot

## About the Project
  - This project is to use SLAM package to autonomously map the Gazebo world and integrate it with path planning and navigation ROS packages to move an object from one place to another on the map
  - Key skills demonstrated
    - Advanced ROS and Gazebo integration
    - ROS Navigation stack
    - Path planning

## Structure
Naming might be different
```
.Project5                                        # Home Service Robot Project
├── catkin_ws                                             # Catkin workspace
│   ├── src
│   │   ├── add_markers                                   # add_markers package        
│   │   │   ├── launch
│   │   │   │   ├── view_home_service_navigation.launch   # launch file for home service robot demo
│   │   │   ├── src
│   │   │   │   ├── add_markers.cpp                       # source code for add_markers node
│   │   │   │   ├── add_markers_demo.cpp                  # source code for add_markers_demo
│   │   ├── pick_objects                                  # pick_objects package     
│   │   │   ├── src
│   │   │   │   ├── pick_objects.cpp                      # source code for pick_objects node
│   │   │   │   ├── pick_objects_demo.cpp                 # source code for pick_objects_demo
│   │   ├── rvizConfig                                    # rvizConfig package        
│   │   │   ├── home_service_rvizConfig.rviz              # rvizConfig file for home service robot demo  
│   │   ├── scripts                                       # shell scripts files
│   │   │   ├── add_marker.sh                             # shell script to model virtual objects  
│   │   │   ├── home_service.sh                           # shell script to launch home service robot demo  
│   │   │   ├── pick_objects.sh                           # shell script to send multiple goals  
│   │   │   ├── test_navigation.sh                        # shell script to test localization and navigation
│   │   │   ├── test_slam.sh                              # shell script to test SLAM
│   │   ├── slam_gmapping                                 # gmapping_demo.launch file
│   │   ├── turtlebot                                     # keyboard_teleop.launch file
│   │   ├── turtlebot_interactions                        # view_navigation.launch file
│   │   ├── turtlebot_simulator                           # turtlebot_world.launch file package        
│   │   ├── CMakeLists.txt                                # compiler instructions
```
    
## Tasks
  - Create **add_markers** ROS node held as a virtual object and subscribes to robot's odometry values
  - Add **add_markers** to **view_navigation.launch** and save this as a new Rviz configuration
  - Create **home_service.sh** that launches **turtlebot**, **AMCL**, **Rviz config file**, **pick_object**, and **add_markers** ROS nodes

## Running Code
  - Initialize a ROS workspace `project5/catkin_ws/src`
  - `cd project5/catkin_ws/src`
  - `git clone` this repo
  - `cd ..`
  - `catkin_make`
  - `source devel/setup.bash`
    - `./launch.sh` to test launching gazebo and rviz
    - `./test_slam.sh` to test mapping and localization with **teleop** package
    - `./test_navigation` to test 2D navigation goal in Rviz for autonomous navigation and obstacle avoidance
    - `./pick_object` to test sending robot to two different locations one after the other assuming they are locations of the object to be picked up
    - `./add_marker` to test object pickup/drop-off by spawnign a virtual box at one location once robot navigates to the box, box disappears and re-appears again at when robot arrives at the destination
    - `./home_service` to test the final project: end-to-end autonomous navigation and collision avoidance to pick up and drop-off a box


## Results
Refer to [/pics](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%205%20-%20Home%20Service%20Robot/pics)
