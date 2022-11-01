## Project 3 - Where Am I

## About the Project
  - This project is to interface my own mobile robot with the Adaptive Monte Carlo Localization algorithm in ROS to estimate robot's position as it travals through predifined world from [project2](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%202%20-%20Go%20Chase%20It)
  - Tune different parameters to increase the localization efficiency
  - Key skills demonstrated
    - Implementation of Adaptive Monte Carlo Localization in ROS
    - Understanding of tuning parameters required

## Structure
Naming might be different
```
    .Project2                          # Go Chase It Project
    ├── my_robot                       # my_robot package                   
    │   ├── launch                     # launch folder for launch files   
    │   │   ├── robot_description.launch
    │   │   ├── world.launch
    │   ├── meshes                     # meshes folder for sensors
    │   │   ├── hokuyo.dae
    │   ├── urdf                       # urdf folder for xarco files
    │   │   ├── my_robot.gazebo
    │   │   ├── my_robot.xacro
    │   ├── world                      # world folder for world files
    │   │   ├── <yourworld>.world
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info
    ├── ball_chaser                    # ball_chaser package                   
    │   ├── launch                     # launch folder for launch files   
    │   │   ├── ball_chaser.launch
    │   ├── src                        # source folder for C++ scripts
    │   │   ├── drive_bot.cpp
    │   │   ├── process_images.cpp
    │   ├── srv                        # service folder for ROS services
    │   │   ├── DriveToTarget.srv
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info                  
    └──   
```
    
## Tasks
  - Create **drive_bot** ROS package
    - Create **my_robot** ROS package to hold robot, whiet ball, and Gazebo simulation world
    - Design a differential drive robot with the Unified Robot Description Format with a LiDAR and a camera and add Gazebo plugins
    - Create a new wrold that is different from [Project 1](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/tree/main/Project%201%20-%20Build%20My%20World) and house the robot in the new world
    - Add white ball to Gazebo world and save a copy of this world
    - Create **world.launch** file to launch the saved world in the terminal
  - Create **ball_chaser** ROS package to hold C++ ROS nodes
    - Write **drive_bot** C++ ROS node to provide `ball_chaser/command_robot` service to drive the robot by controlling its linear x and angular z velocities, publish to wheel joints of robot and get back requested velocities
    - Write **process_image** C++ ROS node that read camera image to determine the presence of the white ball and request a service to drive robot toward the ball
    - Create **ball_chaser.launch** that launches **drive_bot** and **process_image** nodes

## Running Code
  - Initialize a ROS workspace `project2/catkin_ws/src`
  - `cd project2/catkin_ws/src`
  - `git clone` this repo
  - `cd ..`
  - `catkin_make`
  - `source devel/setup.bash`
  - `roslaunch my_robot world.launch`
  
  - Open second terminal
  - `cd project2/catkin_ws`
  - `source devel/setup.bash`
  - `roslaunch ball_chaser ball_chaser.launch`
  
  - Open third terminal
  - `cd project2/catkin_ws`
  - `source devel/setup.bash`
  - `rosrun rqt_image_view rqt_image_view`
  
  - In Rviz, select **odom** for **fixed frame
  add **RobotModel**, **Camera** (topic: `/camera/rgb/image_raw`), **LaserScan** (topic: `/scan`)

## Results
Robot and White Ball         |  Robot Chasing White Ball
:-------------------------:|:-------------------------:
![](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/blob/main/Project%202%20-%20Go%20Chase%20It/pics/pic_2.PNG)  |  ![](https://github.com/ase1997/Udacity-Robotics-Software-Engineer/blob/main/Project%202%20-%20Go%20Chase%20It/pics/pic_3.PNG)
