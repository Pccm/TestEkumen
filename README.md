---------------------------------------------------------DESCRIPTION-----------------------------------------------

The next algorithm send data type "geometry_msgs/Twist" to topic "turtle1/cmd_vel" to can be read for any subscribe.
In this example the node "turtlesim_node"  subscribe to it.
The data must draw a star of 8 points in the "turtlesim_node".But first the turtle must be position in the start position.
only the software send 2 types of data : Linear velocity, and angular velocity. But   only It use X linear velocity and Z velocity angular.
the data of this 2 velocities is divided in 6 states:

state = 0; this is in the state initial, to position the turtle in the coordinate initial
state = 1; this is in the state initial, to position the turtle in the angle initial
state = 2; this is the state to walk in one side of star
state = 3; this is the state to turn right
state = 4; this is the state to turn left
state = 5; this is the state to stop.

In this algorithm I use the behavior of "turtlesim_node", in the "turtlesim_node" the turtle will stop after 1 second from the last data that it receive.
then I considered that each state must endure only 1 second, also considered velocity angular and linear constant without noise.
distanceLineal = VelocityLineal*Time  --> where time = 1s ---> distanceLineal = VelocityLineal (m)
distanceAngular = VelocityAngular*Time  --> where time = 1s ---> distanceAngular = VelocityAngular (rad)

//----------------------------------------------------EXECUTE-----------------------------------------------------
1)Run ROS:
	-open a new terminal
	-execute the command: roscore
2)Run "Turtlesim_node":
	-open a new terminal
	-execute the command: source ./devel/setup.bash
	-execute the command: rosrun turtlesim turtlesim_node
3)Run the Program:
	-open a new terminal
	-execute the command: source ./devel/setup.bash
	-execute the command: rosrun beginner_tutorials talker

To exit the program press Ctrl+C.

Thanks.
	

