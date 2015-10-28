# SLAM DEMO

## Dependencies 

	```bash
	    sudo apt-get install ros-$ROS-DISTRO$-turtlebot-gazebo ros-$ROS-DISTRO$-turtlebot-indigo ros-$ROS-DISTRO$-turtlebot-simulator
	```
## Install

	```bash
	    cd catkin_ws/src
		git clone https://github.com/ShibataLab/Turtlebot-SLAM-Demo
		roscd catkin_ws
		catkin_make
		source devel/setup.bash
	```

## Run
	*In terminal,
	```bash
		roscore
	```
	*Switch to new tab,
	```bash
	    source devel/setup.bash
		roslaunch turtlebot_gazebo turtlebot_world.launch		
	```
	this will launch gazebo window. 

	*Switch to new tab
	```bash
	    source devel/setup.bash
		roslaunch slam_demo mapServer.launch
	```

	*Switch to a new terminal window and make it always on the top
	```bash
	    source devel/setup.bash
		roslaunch turtlebot_telop keyboard_teleop.launch
	```
## To visualize
	
	*Switch to a new tab
	```bash
	    source devel/setup.bash
		rosrun rviz rviz
	```	
	set frame:= /odom and display "occupancygrid" topics subscribed to := /octomap_full
 

