


First we need to install the core dependencies of TurtleBot, which can be done by executing the following command in a terminal:


sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
  ros-noetic-rosserial-python ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rviz \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers



We also need to install the following package for the servo actuators (motors) used on TurtleBot:

Next, install this package that defines the messages that TurtleBot uses to communicate with ROS:
Additionally, we need to install the main TurtleBot3 package:


sudo apt install ros-noetic-dynamixel-sdk
sudo apt install ros-noetic-turtlebot3-msgs
sudo apt install ros-noetic-turtlebot3

Once the main installation is complete, we need to install the TurtleBot3 Simulations package from source, by cloning it with Git into our Catkin Workspace:

cd ~/catkin_ws/src/
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
Finally, we need to navigate back to the root of the Catkin Workspace to run a catkin_make:

cd ~/catkin_ws && catkin_make