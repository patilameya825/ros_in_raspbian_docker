FROM armv7/armhf-ubuntu:xenial
MAINTAINER Ameya Patil (patil.ameya825@gmail.com)
RUN apt-get update
RUN apt-get install -y lsb-release
RUN sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
RUN apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
RUN apt-get update
RUN apt-get install -y ros-kinetic-desktop-full
RUN rosdep init
RUN rosdep update
RUN echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
RUN /bin/bash -c 'source ~/.bashrc'
CMD roscore
