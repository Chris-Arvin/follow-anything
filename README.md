# 1. how to build
mkdir -p ~/Documents/go2_ws/src
cd ~Documents/go2_ws/src
git clone ...
cd ~/Documents/go2_ws/src/livox_ros_driver2 && ./build.sh humble
cd ~/Documents/go2_ws && colcon build

# 2. Start worlds:
source Documents/go2_ws/install/setup.bash
ros2 launch go2_config gazebo_mid360.launch.py rviz:=true
ros2 launch go2_config gazebo_mid360.launch.py world:=$(ros2 pkg prefix go2_config)/share/go2_config/worlds/outdoor.world rviz:=true headless:=True

### note: headless:=True means that it will not open the gui.

# 3. control the robot with teleop
ros2 run teleop_twist_keyboard teleop_twist_keyboard














1. Install realsense: https://github.com/IntelRealSense/realsense-ros
2. sudo apt install xterm
