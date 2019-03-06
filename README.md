# EE4308 - Advances in Intelligent Systems and Robotics - Part 1 Project - NUS 2019 #
-----------------------------------
Turtlebot simulation in Gazebo. The aim of this project is to navigate the turtlebot autonomously from start position (x,y) = (0,0) to goal position (x,y) = (4,4) in a 9m x 9m map with unknown maze conifguration.

The project is part of the assessment in the first half of the course EE4308: Advances in Intelligent Systems and Robotics taught at the National University of Singapore (NUS) during Semester 2 of AY2018/19. 


## Software Tools ##
--------------------------
Ubuntu 16.04 (Xenial Xerus) installed.  
Robot Operating System (ROS) Kinetic Kame distribution installed.  
Gazebo 7 Simulator and Kobuki Turtlebot (v1.0.6) used.  

__Note: Our implementation requires Armadillo, the C++ linear algebra library to be installed.__  
If not present, please install Armadillo using:
	```
	$ sudo apt-get install libarmadillo-dev
	```
	


## How to run the code ## 
-------------------------
1. Create a catkin workspace (if not already created):
	```bash
	$ mkdir -p ~/catkin_ws/src
	```

2. Enter your source folder inside your catkin workspace:
	```bash
	$ cd ~/catkin_ws/src
	```

3. Clone the repository: 
	```bash
	$ git clone https://github.com/gaowq1994/ee4308_project_adriel_wenqi prj-grp-02
	```

4. Inside your catkin workspace, run catkin_make:
	```bash
	$ cd ~/catkin_ws
	$ catkin_make
	```

5. Run project\_init\_world_1.sh or project\_init\_world_2.sh to lauch either test world 1 or test world 2:
	```bash
	$ cd ~/catkin_ws/src/prj-grp-02
	$ chmod +x project_init_world_1.sh
	$ ./project_init_world_1.sh
	```
	or

	```bash
	$ cd ~/catkin_ws/src/prj-grp-02
	$ chmod +x project_init_world_2.sh
	$ ./project_init_world_2.sh
	```

This will launch the turtlebot world in Gazebo Simulator. This may take a while to load on the first launch.

6. Open a new terminal.

7. Before continuing source your new setup.*sh file:

	```bash
	$ cd ~/catkin_ws
	$ source devel/setup.bash
	```

8. Launch the launch file navigate.launch to make the turtlebot navigate towards the goal:

	```bash
	$ roslaunch prj-grp-02 navigate.launch 
	```

