Research_Track2  first_assignment   (sai Krishna rama chander raju Alluri)(matricola 5060551)

### A brief explanation of the Algorithm
In the package a random goal is issued and the robot starts moving the plane by itself until it reaches the target.since thw user input cannot be interrupted,stoppint=g the robot is only possible only afetr the goal is reached orelse re-starting it by issuing a new goal


### content of package

`go_to_the_point.py` : The service manager controlles the robot speed depending on the goal recieved.

`user_interface.py` : To start and stop the robot.

`Position_service.cpp` : It generates the random pose as a responce to a request.

`State_machine.cpp` : It manages the request of a new pose when needed by sending its goal request.

 `sim.launch` : starts the simulation in a Gazebo environment.

`bridge_sim.launch` : it is dedicated to launch only the python scripts, due to the fact that the components of ros2 take care of the leaving part.

`coppelia_sim.launch` : starts the simulation in a Coppelia environment.

## How to run the code

git clone the package
`https://github.com/allurisai3/research-track-2-assignment-1.git `

create a workspace in root repositories

`mkdir "name of the workspace" `

move the git package to the src folder of that workspace

Build the package

`catkin_make`

To start the simulation in Gazebo

`roslaunch rt2_assignment1 sim.launch`

To start the simulation in Coppelia, it is necessary to run

`roslaunch rt2_assignment1 coppelia_sim.launch`

To launch only the python scripts

`roslaunch rt2_assignment1 bridge_sim.launch`
