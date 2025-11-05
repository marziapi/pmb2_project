# Mobile Robotics project with pmb2 robot from PAL Robotics

This is the ROS2 Humble simulation environment with moving people for the group project of the course Mobile Robotics, Master’s Degree in Intelligent Systems Engineering​ at Università Campus Bio-Medico di Roma.
The robot is the pmb2 from PAL Robotics.

## Installation instruction
Clone this repository and the following packages:

```
git clone https://github.com/robotics-upo/hunav_sim.git
git clone https://github.com/robotics-upo/lightsfm.git
```
Copy the lightsfm library into your local files:

```
cd /usr/local/include/
mkdir lightsfm
cp /<path-to-your-workspace>/src/lightsfm/include/angle.hpp /usr/local/include/lightsfm/
cp /<path-to-your-workspace>/src/lightsfm/include/map.hpp /usr/local/include/lightsfm/
cp /<path-to-your-workspace>/src/lightsfm/include/sfm.hpp /usr/local/include/lightsfm/
cp /<path-to-your-workspace>/src/lightsfm/include/vector2d.hpp /usr/local/include/lightsfm/
```

## To use SLAM
Modify the file ~/ros2_ws/src/hunav_gazebo_wrapper/src/WorldGenerator.cpp on line 101 to disable collision with the pedestrians:

```
plug_use_collision_ = this->declare_parameter<bool>("use_collision", false);
```
