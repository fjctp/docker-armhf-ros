# build armhf-ros:kinetic-ros-opencv3
FROM fjctp/armhf-ros:kinetic-ros-base

# install ros packages
RUN apt-get update && apt-get install -y \
    ros-kinetic-opencv3 \
    ros-kinetic-vision-opencv \
    && rm -rf /var/lib/apt/lists/*