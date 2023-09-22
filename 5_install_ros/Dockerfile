FROM docker.io/ubuntu:20.04

RUN ln -sf /usr/share/zoneinfo/Asia/Jakarta /etc/localtime \
&& apt-get update \
&& apt-get upgrade -y \
&& apt-get install -y curl \
	wget \
	gnupg \
	git \
	guvcview \
	g++ \
	cmake \
	v4l-utils \
	libgtk2.0-dev \
	make \
	unzip \
	unrar \
	lsb-core \
&& apt-get clean \
&& sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' \
&& curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | apt-key add - \
&& apt-get update \
&& apt-get install -y ros-noetic-ros-base \
	python3-rosdep \
	python3-rosinstall \
	python3-rosinstall-generator \
	python3-wstool build-essential \
	python3-catkin-tools \
	python3-catkin-pkg \
	ros-noetic-dynamixel-sdk \
&& echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc \
&& rosdep init \
&& rosdep update \
&& rm -rf /var/lib/apt/lists 

WORKDIR /workspace
