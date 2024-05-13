## Autonomous Mobile Robot (AMR)

This repository contains my work on an Autonomous Mobile Robot (AMR) with skid steer drive. The robot was built using the Unified Robot Description Format (URDF).

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


