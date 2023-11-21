mkdir catkin_ws
cd catkin_ws
mkdir src
cd src
git clone https://github.com/asimfathekhani/hector_slam
cd ..
catkin_make
ls -l /dev |grep ttyUSB
sudo chmod 666 /dev/ttyUSB0
roscore
roslaunch rplidar_ros rplidar.launch
roslaunch hector_slam_launch tutorial.launch
