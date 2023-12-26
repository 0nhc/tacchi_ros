# tacchi_ros
This repository contains my reimplementation code for [Tacchi: A Pluggable and Fast Gel Deformation Simulator for Optical Tactile Sensors](https://arxiv.org/abs/2301.08343)

## 1. Prerequisite
* ROS 1 (I used Noetic.)
* Anaconda3 (Optional but recommended.)

## 2. Installation
Clone and compile this repository in your workspace.
```sh
cd <your_ws>/src
git clone https://github.com/0nhc/tacchi_ros
cd ..
rosdep install --from-paths src --ignore-src -r
catkin_make
```
Create virtual Python environment in Anaconda3.
```sh
conda create -n tacchi_ros python=3.9
conda activate tacchi_ros
cd <your_ws>/src/tacchi_ros
pip install -r requirements.txt
```

## 3. Tacchi Demo in Gazebo
Launch the demo.
```sh
# Terminal 1
cd <your_ws>
source devel/setup.bash
conda activate tacchi_ros
roslaunch gelsight_simulation simulation.launch

# Terminal 2
cd <your_ws>
source devel/setup.bash
conda activate tacchi_ros
rosrun gelsight_simulation data_collection_ti.py 
```