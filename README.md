## Autonomous Mobile Robot (AMR)

This project focuses on the development of an Autonomous Mobile Robot (AMR) with a skid steer drive. The AMR is designed to navigate autonomously in various environments and perform tasks with minimal human intervention.

The robot is built using the Unified Robot Description Format (URDF), which provides a detailed 3D model of the robot including its physical properties, visual aspects, and sensor placements. This allows for accurate simulation and control of the robot.

The project involves three main scenarios: navigating a maze, finding four different colored balls sequentially, and finding four different colored balls randomly placed inside a maze. For each scenario, two behavior tree-based control programs (Program A and Program B) are implemented. These programs guide the robot’s actions based on its current state and the environment.

The robot uses the gmapping package for laser-based SLAM (Simultaneous Localization and Mapping), creating a 2D occupancy grid map of its environment. It also uses AMCL (Adaptive Monte Carlo Localization) for probabilistic localization in 2D.

The navigation stack takes in information from odometry, sensor streams, and a goal pose, and outputs safe velocity commands that are sent to the mobile base using the move_base package. This enables the robot to navigate towards its goal while avoiding obstacles.

The performance of the two programs is compared based on the time taken to achieve the goal in each scenario. This provides valuable insights into the efficiency and effectiveness of different control strategies.

Overall, this project showcases the application of behavioral robotics in developing autonomous robots capable of complex behaviors and tasks. It demonstrates the potential of such robots in various applications, ranging from search and rescue operations to environmental monitoring and space exploration. 😊

## Packages

The project is organized into three packages:

## Description

The robot uses the gmapping package for laser-based SLAM (Simultaneous Localization and Mapping) to create a 2D occupancy grid map. AMCL (Adaptive Monte Carlo Localization) is used for probabilistic localization of the robot in 2D. The navigation stack takes in information from odometry, sensor streams, and a goal pose and outputs safe velocity commands that are sent to a mobile base using the move_base package.

## Usage

To run the robot in Gazebo, use the Following Code Sequence:
```
roslaunch gazebo_pkg gazebo.launch 
```
## Create 2D map
```
roslaunch navigtion_pkg gmapping.launch
```
## Save the map
```
 rosrun map_server map_saver 
```
## Run navigtion in Rviz
```
 roslaunch navigtion_pkg navigation.launch
```
this launch have ('Amcl' , 'move_base' , 'Map server' , 'rviz')


