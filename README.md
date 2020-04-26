# Map My World Project

Solution for the Udacity Map my world project, part of the Robotics Software Engineer nano degree.

## Overview

The solution was developed on the Udacity Virtual Machine image running locally until performance issues began to cause issues, at which point I migrated to the Udacity on line workspace.

The project is primarily focused on configuring an using the rtabmap packages to perform slam on a created world environment.

The resulting generated map is too large to be uploaded to github so is available at the link:
https://drive.google.com/open?id=1HnmQ6jEjYKQMF3NewuaYbLKyWgbUGIi2

The repository contains the teleop and rtmap files necessary to run.
Once cloned and sourced, running catkin_make will generate the required packages.



## Setup

Running the code requires 3 terminals.

### Terminal 1

After sourcing the ros environment run:

> roslaunch my_robot midworld.launch

This will run gazebo, rviz and spawn a robot within a medium sized world.

### Terminal 2

> rosrun teleop_twist_keyboard teleop_twist_keyboard.py

## Terminal 3

> roslaunch my_robot mapping.launch


## mapping
In order to map, use the telop terminal to drive the robot round the map. 2-3 times is normally sufficient to generate loop closures.
The resulting map is at the link:
https://drive.google.com/open?id=1HnmQ6jEjYKQMF3NewuaYbLKyWgbUGIi2

Mapping in progress
![Alt text](/screenshots/mapping_in_progress.png?raw=true "mapping")

Generated map viewed in rtabmap viewer
![Alt text](/screenshots/database_view.png?raw=true "rtabmap db view")



## useful stuff

install rtabmap_ros
> sudo apt-get install ros-kinetic-rtabmap-ros

update
> sudo apt-get update && sudo apt-get upgrade -y

> to build for kinetic in root of repo cloned from rtabmap run git checkout kinetic-devel
