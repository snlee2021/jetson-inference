# jetson-inference

(https://github.com/dusty-nv/jetson-inference/blob/master/docs/building-repo-2.md)


$ sudo apt-get update

$ sudo apt-get install git cmake libpython3-dev python3-numpy

$ git clone --recursive https://github.com/dusty-nv/jetson-inference

$ cd jetson-inference

$ mkdir build

$ cd build

$ cmake ../

$ make -j$(nproc)

$ sudo make install

$ sudo ldconfig



$ video-viewer csi://0 

$  cd ~/jetson-inference/build/aarch64/bin

$ detectnet-camera.py  csi://0 

# Deep Learning Nodes for ROS

 (https://github.com/dusty-nv/ros_deep_learning#detectnet-node-1)
 
 sudo apt-get install ros-melodic-image-transport ros-melodic-vision-msgs
 
 cd ~/ros_workspace/src
 
 git clone https://github.com/dusty-nv/ros_deep_learning
 
 catkin_make

 source devel/setup.bash
 
 roslaunch ros_deep_learning detectnet.ros1.launch input:=csi://0 output:=display://0
