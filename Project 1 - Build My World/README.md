## Project 1 - Build My World

## About the Project
  - This project is to use tools leanred in Gazebo to build my first simulation environment
  - Key skilles demonstarted 
    - Launching a Gazebo environment
    - Designing in Gazebo
    
## Tasks
  - Build a single floor wall structure using the **Building Editor** tool in Gazebo
  - Model any object of choice using the **Model Editor** tool in Gazebo
  - Import structure and two instances of the model inside an empty Gazebo World
  - Import at least one model from the **Gazebo online library** and implement it in the existing Gazebo world
  - Write a C++ **World Plugin** to interact with the world and display **"Welcome to (x)'s World!"**

## Structure 
Naming might be different 
```
    .Project1                          # Build My World Project 
    ├── model                          # Model files 
    │   ├── Building
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── HumanoidRobot
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script      
    │   ├── welcome_message.cpp
    ├── world                          # Gazebo main World containing models 
    │   ├── UdacityOffice.world
    ├── CMakeLists.txt                 # Link libraries 
    └──                              
```

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
