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


## Generate a Map

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
$ roslaunch turtlebot_navigation gmapping_demo.launch
```

### Step 4: In Workstation
```
$ roslaunch turtlebot_rviz_launchers view_navigation.launch
```

### Step 5: In Workstation
```
$ roslaunch turtlebot_teleop logitech.launch
```

### Step 6: Drive around a few times to generate a map
```
DRIVE SLOWLY TO AVOID MAPPING ERRORS
```

### Step 7: Drive Turtlebot BACK to where you can connect it to a monitor.
```
Connect Turtlebot to a monitor.
```
### Step 8: In Turtlebot
```
$ rosrun map_server map_saver -f /home/ubuntu/Desktop/newatrmap.yaml
```

### Step 9: Check map is there
```
$ ls /home/ubuntu/Desktop/newatrmap.yaml
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
$ roslaunch turtlebot_navigation amcl_demo.launch map_file:=/home/ubuntu/Desktop/newatrmap.yaml
```

### Step 4: In Workstation
```
$ roslaunch turtlebot_rviz_launchers view_navigation.launch --screen
```

### Step 5: In Workstation (Optional)
```
$ roslaunch turtlebot_teleop logitech.launch
```
