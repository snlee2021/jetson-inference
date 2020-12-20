# jetson-inference

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
