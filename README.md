# I3DR Titania Kinova Simulated
ROS workspace for simulated I3DR Titania stereo camera with Kinova robotic arm

## Installation

For an easy setup, a rosinstall file is provided in 'install' folder of this repo which can be used to get this package and it's dependent ros packages in your workspace. 
In your ROS workspace use the following command:
```
wstool init src https://raw.githubusercontent.com/i3drobotics/i3dr_titania_kinova_sim-ros/master/install/i3dr_titania_kinova_sim_https.rosinstall
```
If you already have a wstool workspace setup then use the following command instead:
```
wstool merge -t src https://raw.githubusercontent.com/i3drobotics/i3dr_titania_kinova_sim-ros/master/install/i3dr_titania_kinova_sim_https.rosinstall
wstool update -t src
```

If you do not use wstool, you can download the packages using the following command:
```
cd PATH_TO_ROS_WS/src
git clone https://github.com/i3drobotics/i3dr_stereo_camera-ros.git
git clone https://github.com/i3drobotics/i3dr_ur10-ros.git
git clone https://github.com/Kinovarobotics/kinova-ros.git
git clone https://github.com/i3drobotics/i3dr_titania-ros.git
git clone https://github.com/i3drobotics/i3dr_pcl_tools-ros.git
```

To install package dependences use rodep:
```
rosdep install --from-paths src --ignore-src -r -y
```

Build using catkin (tested with catkin_make and catkin_build):
```
catkin_make
or
catkin build
```
