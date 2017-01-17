# Dockerfiles for ROS on Raspberry Pi
## Start ROS server
```bash
docker run -it --rm --net foo --name master fjctp/armhf-ros-kinetic-base roscore
```
## Start publisher/listener (using command tools)
```bash
docker run -it --rm --net foo --name tester \
           --env ROS_HOSTNAME=tester \
           --env ROS_MASTER_URI=http://master:11311 \
           fjctp/armhf-ros-kinetic-base bash
```

```bash
rostopic pub /chatter std_msgs/String -r 2 "Do you hear me?"
rostopic echo /chatter 
```

## Note
- For raspberry pi 2/3 only
- Make sure container's name and hostname match, otherwise ROS nodes cannot exchange message
