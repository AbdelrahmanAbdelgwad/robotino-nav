# Closed Loop Robotino Control

This is a ROS package that implements a closed-loop controller for controlling a Robotino robot in the CoppeliaSim environment.

## Requirements

- ROS (tested on ROS Melodic)
- CoppeliaSim

## Installation

1. Clone this repository into your workspace:

    ```
    cd ~/catkin_ws/src
    git clone https://github.com/AbdelrahmanAbdelgwad/robotino-nav.git
    ```

2. Build the package:

    ```
    cd ~/catkin_ws
    catkin_make
    ```

## Usage

1. Run roscore:

    ```
    roscore
    ```

2. Start CoppeliaSim and load the scene "robotino_control.ttt" located in the `closed_loop_robotino/simulation` folder.

3. Run the node `move_robotino_to_goal.py`:

    ```
    rosrun closed_loop_robotino move_robotino_to_goal.py
    ```

4. Publish the goal you want using this command:

    ```
    rostopic pub /robotino/goal geometry_msgs/Pose2D "x: 1.0 y: 1.0 theta: 0.0"
    ```
    
## Demo

To see a demo of the package in action, check out this [YouTube video](https://youtu.be/jZwYCSb5Pko).
