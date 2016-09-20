# build armhf-ros:kinetic-ros-base
FROM fjctp/armhf-ros:kinetic-ros-core

# install ros packages
RUN apt-get update && apt-get install -y \
    ros-kinetic-ros-base=1.3.0-0* \
    && rm -rf /var/lib/apt/lists/*