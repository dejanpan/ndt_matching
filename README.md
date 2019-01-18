## Install ROS2
See: https://index.ros.org/doc/ros2/Installation/Linux-Install-Debians/.  
**Note:** Stop at "Install additional RMW implementations".

## Clone, build and run this package
```sh
cd
mkdir ndt_ws/src -p
cd ndt_ws/src
git clone https://github.com/dejanpan/ndt_matching.git
cd ..
colcon build
./install/lib/ndt_matching/ndt_node
```

## Organization
The package contains an [executable](src/ndt_node.cpp) and a [library](src/ndt_lib.cpp). The library should contain
an implemented algorithm and the executable, a ROS2 node, should subscribe to two
PointCloud2 messages and publishes one PoseStamped message.

Two PointCloud2 messages will be played back by the [rosbag2](https://github.com/ros2/rosbag2) tool and can be
together with the Pose message visualized in [rviz2](https://github.com/ros2/rviz/tree/crystal) tool.

Look for `TODO` placeholders in the ROS2 node and fill them in.
