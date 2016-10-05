# Dockerfiles for ROS on Raspberry Pi
## Example (for x64)
### Start master
docker run -it --rm --net foo --name master ros:ros-kinetic-tutorials roscore

### Start talker
docker run -it --rm --net foo --name talker --env ROS_HOSTNAME=talker --env ROS_MASTER_URI=http://master:11311 ros:ros-kinetic-tutorials rosrun roscpp_tutorials talker

### Start listener
docker run -it --rm --net foo --name listener --env ROS_HOSTNAME=listener --env ROS_MASTER_URI=http://master:11311 ros:ros-kinetic-tutorials rosrun roscpp_tutorials listener

### Start tester (using command tools)
docker run -it --rm --net foo --name tester --env ROS_HOSTNAME=tester --env ROS_MASTER_URI=http://master:11311 ros:ros-kinetic-tutorials bash

rostopic pub /chatter std_msgs/String -r 2 "Do you hear me?"
rostopic echo /chatter 

### Note
Make sure container's name and hostname match, otherwise ROS nodes cannot exchange message
