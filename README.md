# COMP150 Reinforcement Learning: Path Planning Amidst Moving Obstacles
<img src=https://github.com/js0823/pedsim_ros/blob/master/pedsim_simulator/images/screenshot1.png width=400/>

### Requirements
- Ubuntu 16 is required as this project uses ROS-kinetic which is compatible with Ubuntu 16.
- ROS-kinetic full desktop install by:
```
sudo apt install ros-kinetic-desktop-full
sudo apt install ros-kinetic-turtlebot ros-kinetic-turtlebot-gazebo ros-kinetic-turtlebot-apps ros-kinetic-turtlebot-rviz-launchers
```
- ROS turtlebot and gazebo packages (I recommend updating gazebo 7.0.0, the default gazebo version, to 7.14.0)
```
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable lsb_release -cs main" > /etc/apt/sources.list.d/gazebo-stable.list'
wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
sudo apt-get update
sudo apt-get install gazebo7
gazebo --version (should return 7.14.0 or above)
```

### Package Installation

```
cd [workspace]/src
git clone https://github.com/js0823/pedsim_ros.git  
cd pedsim_ros
git submodule update --init --recursive
cd ../..
catkin_make
```

### Sample usage
Default method is to launch the turtlebot_RL.launch via this command.
```
roslaunch pedsim_simulator turtlebot_RL.launch
```
If you wish to control the turtlebot via keyboard, you can use this on your other terminal.
```
roslaunch pedsim_simulator keyboard_teleop.launch
```
### License
Original pedsim_ros package is here https://github.com/srl-freiburg/pedsim_ros.
