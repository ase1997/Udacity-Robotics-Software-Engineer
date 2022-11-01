# Udacity-Robotics-Software-Engineer

## Type: Udacity Nanodegree, Robotics Software Engineer (Individual Exploration, Self-Learning)

## About the Repo.
  - This is an online degree that I took and learned on my own with Udacity between May and August of 2022
  - Topics learned in this nanodegree:
    - The software fundamentals to work on robotics using C++, ROS, and Gazebo
    - How to build autonomous robotics projects in a Gazebo simulation environment
    - Probabilistic robotics, including Localization, Mapping, SLAM, Navigation, and Path Planning
with five hands-on course projects that demonstrated skills in C++, ROS [1], Gazebo, Rviz, Localization, Mapping, SLAM, Navigation, and Path Planning
  

## Dependencies
  - Ubuntu Linux 20.04 LTS (Virtual Box on Windows 10)
  - ROS Neotic 
  - Python3/C++11 or above
  
## Tasks
  - Write CMake and launch files to spawn 12 coke cans at random poses and a table at x-y-z (1,0,0) rotated 90 degress about z-axis and its center is at (1,0,1.05) in Gazebo

![ase1997](https://github.com/ase1997/Can-Transformation/blob/main/random_cans.png)
<p align="center">
Figure 1. Objects Spawn.
</p>

  - Write a code to transform 12 coke cans in the following desired poses
  
![ase1997](https://github.com/ase1997/Can-Transformation/blob/main/ordered_cans.png)
<p align="center">
Figure 2. Desired Outcome.
</p>

  - Simulate/visualize the process on Gazeboo

## Running Code
  - open a terminal
  - `git clone` this repo. to a workspace
  - `cd` to that workspace and `catkin_make`
  - `source devel/setup.bash`
  - `roslaunch robotics_module1a module1.launch`
  - open another terminal and `source devel/setup.bash`
  - `rosrun robotics_module1 setup_table_v2 or settup_table`

## Author
Khoa Do

## Reference
N/A

## Additional Notes
N/A
