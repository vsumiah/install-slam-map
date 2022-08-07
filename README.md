# install-slam-map


To get a map, you must go through a basic site to download Commands.
( https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/ ) And copy the commands from him and start a new terminal.

1. Choose your current version such as noetic in the link above and copy Commands.

2. Go to Simulation for this link( https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/ )

And copy these Commands
~~~
$ cd ~/catkin_ws/src/
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
~~~

Then when finished, choose waffle with this command
~~~
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
~~~
Finally, 
~~~
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
~~~
3. Go to the last SLAM Simulation commands
( https://emanual.robotis.com/docs/en/platform/turtlebot3/slam_simulation/)

Open a new terminal

~~~
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
~~~

-Run SLAM Node

~~~

$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods
~~~

-Run Teleoperation Node

~~~
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
~~~

*To view map*

~~~
$ rosrun map_server map_saver -f ~/map
~~~

![1](https://user-images.githubusercontent.com/108010896/183294464-e2e1759b-999f-408f-bd6f-d90f50fb9433.jpeg)
![2](https://user-images.githubusercontent.com/108010896/183294471-5a817915-b904-4034-9802-314c3a6fd83e.jpeg)

