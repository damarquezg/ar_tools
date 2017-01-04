# Advanced Visual Geometry
ar_tools

### Go to your catkin workspace
```
$ cd catkin_workspace
$ cd src
$ git clone https://github.com/damarquezg/ar_tools.git
$ cd ..
$ source devel/setup.bash
$ catkin_make
```
### Copy data
```
$ roscd ar_pose
$ mkdir ar_data
$ cd ar_data
(copy bag files here)
```
### Run (in your catkin workspace)
```
$ source devel/setup.bash
$ roslaunch ar_pose avg_lab.launch
(Rviz fixed frame: ar_marker)
```
### Run (open a new shell)
```
$ roscd ar_pose
$ rosbag play demo_single.bag --clock -d 3
