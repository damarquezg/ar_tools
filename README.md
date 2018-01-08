# Advanced Visual Geometry
ar_tools

### Step 1: Go to your catkin workspace
Creating a workspace for catkin : http://wiki.ros.org/catkin/Tutorials/create_a_workspace
```
$ cd catkin_workspace
$ cd src
$ git clone https://github.com/damarquezg/ar_tools.git
$ cd ..
$ source devel/setup.bash
$ catkin_make
```
### Step 2: Copy data
Download data: https://github.com/ar-tools/ar_data/blob/master/demo_single.bag
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
(Rviz fixed frame: world)
```
### Step 4: Run (open a new shell)
```
$ roscd ar_pose
$ rosbag play ar_data/demo_single.bag --clock -d 3
```
### Lab
```
1) play the bagfile: demo_single.bag (step 4)

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
    
5) Where is the camera position information?
    5.1) what can you conclude?
    
6) Write a simple subscriber and publisher to:
    6.1) take information about the camera position 
    6.2) publish the information as a "Pose" message
    6.2) write the camera position "trajectory" in a txt file
```
Help: 
ROS - Writing a Simple Publisher and Subscriber (C++):

http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28c%2B%2B%29

Writing a Simple Publisher and Subscriber (Python):

http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28python%29
```
    
7) Using the camera position file (6.2), plot the data (you can use matlab or python)
    7.1) what can you conclude?
```
