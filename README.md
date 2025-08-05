# learningros
Notes I took while learning ros2 HUMBLE HAWKSBILL!!!

# ROS2(Robot Operating System 2)
### Essentially it works kind of like unreal engine blue prints semantically but the individual nodes can be a lot
### more abstracted and also include hardware sensors, motors and other programs

# Nodes
### kind of like python modules that do their own thing

```
```

# Topics
### this is essentially like the middle layer that will send data over from one node to another in
### a continous manner

```
```

# Services
### kind of like topics but they follow a caller and response model rather than a publisher and subscriber model like topics
### generally for one and done type of communication rather than continous

```
```

# Parameters 
### Are configuration values of a node
### 

```
ros2 param list
ros2 param get /turtlesim background_r
ros2 param set /turtlesim background_r 255

ros2 param dump /turtlesim > turtlesim.yaml
```

# Actions
### Are like continously running services with feedback and are also cancelable
```

```
# Using bag to record topic into a data base
```
ros2 bag record <topic_name>
ros2 bag play <ros_bag_name>
```

# Building packages with colcon
### append --symlink-install to avoid rebuilding after editing python scripts
```
colcon build
ros2 pkg create --build-type ament_cmake --license Apache-2.0 <package_name>

# For targeting specific packages you want to bulid
colcon build --packages-select my_package
```


