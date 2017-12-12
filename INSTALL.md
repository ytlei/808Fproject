
## Installation

Basic requirements:
- ROS Kinetic (`/rosversion: 1.12.7`)
- Gazebo 8.1.1
- Python 3.5.2
- OpenCV3, installed from sources for Python 3 (`git clone https://github.com/Itseez/opencv.git`)
- OpenAI gym

#### ROS Kinetic dependencies
```
sudo pip3 install rospkg catkin_pkg

sudo apt-get install python3-pyqt4

sudo apt-get install \
cmake gcc g++ qt4-qmake libqt4-dev \
libusb-dev libftdi-dev \
python3-defusedxml python3-vcstool \
ros-kinetic-octomap-msgs        \
ros-kinetic-joy                 \
ros-kinetic-geodesy             \
ros-kinetic-octomap-ros         \
ros-kinetic-control-toolbox     \
ros-kinetic-pluginlib	       \
ros-kinetic-trajectory-msgs     \
ros-kinetic-control-msgs	       \
ros-kinetic-std-srvs 	       \
ros-kinetic-nodelet	       \
ros-kinetic-urdf		       \
ros-kinetic-rviz		       \
ros-kinetic-kdl-conversions     \
ros-kinetic-eigen-conversions   \
ros-kinetic-tf2-sensor-msgs     \
ros-kinetic-pcl-ros \
ros-kinetic-navigation
```

```
#Install Sophus
cd
git clone https://github.com/stonier/sophus -b indigo
cd sophus
mkdir build
cd build
cmake ..
make
sudo make install
echo "## Sophus installed ##\n"
```

#### Gazebo gym

```bash
git clone https://github.com/ytlei/808Fproject.git
cd 808Fproject
sudo pip3 install -e .
```

#### Dependencies and libraries
```
sudo pip3 install h5py
sudo apt-get install python3-skimage

# install Theano
cd ~/
git clone git://github.com/Theano/Theano.git
cd Theano/
sudo python3 setup.py develop

#install Keras
sudo pip3 install keras
```


#### Run (turtlebot simple env)

**Issues**:
- `spacenav_node` not compiling. `CATKIN_IGNORE`d.
- `wiimote` not compiling. `CATKIN_IGNORE`d.
- `kobuki_qtestsuite` not compiling. `CATKIN_IGNORE`d.


Agent dependencies:
```bash
cd 808Fproject/envs/installation
bash setup_kinetic.bash		
```

Run the environment with a sample agent:
```bash
cd 808Fproject/examples/scripts_turtlebot
python circuit2_turtlebot_lidar_qlearn.py
```

