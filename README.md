# Turtlebot Demo
Turtlebot demo scripts, commands and resources

## Configure Environment Variables

### Step 1: Set Environment Variables
Set ```ROS_IP``` and ```ROS_MASTER_URI```
```
$ gedit ~/.bashrc
```
### Step 2: Source .bashrc
```
$ source ~/.bashrc
```

## Autonomous Navigation

### Step 1: In Workstation

```
$ roscore
```

### Step 2: In Turtlebot
```
$ roslaunch turtlebot_bringup minimal.launch
```

### Step 3: In Turtlebot
```
$ roslaunch turtlebot_navigation amcl_demo.launch map_file:=/home/ubuntu/Desktop/atrmap.yaml
```

### Step 4: In Workstation
```
$ roslaunch turtlebot_rviz_launchers view_navigation.launch --screen
```

### Step 5: In Workstation (Optional)
```
$ roslaunch turtlebot_teleop logitech.launch
```
