# Advanced Visual Geometry
ar_tools

### Step 1: Go to your catkin workspace
```
$ cd catkin_workspace
$ cd src
$ git clone https://github.com/damarquezg/ar_tools.git
$ cd ..
$ source devel/setup.bash
$ catkin_make
```
### Step 2: Copy data
```
$ roscd ar_pose
$ mkdir ar_data
$ cd ar_data
(copy bag files here)
```
### Step 3: Run (in your catkin workspace)
```
$ source devel/setup.bash
$ roslaunch ar_pose avg_lab.launch
(Rviz fixed frame: ar_marker)
```
### Step 4: Run (open a new shell)
```
$ roscd ar_pose
$ rosbag play demo_single.bag --clock -d 3

### Lab
```
1) play bagfile demo_single.bag (step 4)
2) Examine the data: 
    2.1) what kind of data are in the bag file?
    2.2) display the data
    2.3) what can you conclude?
3) launch avg_lab.launch (step 3)
4) Examine the topics:
    4.1) list the topics
    4.2) display messages published to topics
    4.3) display the type information of topics
    4.4) what can you conclude?
5) Where is the position of the camera ?
6) Write a simple subscriber and publisher to:
    6.1) take information about the position of the camera 
    6.2) write the position of the camera in a txt file
7) Using the postion of the camera file (6.2) plot the data (you can use matlab or python)
