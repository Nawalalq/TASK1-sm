# TASK1-sm
‏‏Write the steps to install Ros1 and Write the Ros installation algorithm on the Jetson nano
# Task 1-1: Steps to install Ros1 and Ros1 version:
  1- Download VirtualBox
  
 VirtualBox download link:
 
 https://www.virtualbox.org/wiki/Downloads
 
 2- Download ubuntu20.04
 
 ubuntu20.04 download link:
 
 https://releases.ubuntu.com/20.04/
 
 3- Then go to the VirtualBox program and click on new, type a name for the device, and then click on next
 
 4- Choose the space, then next, after that a new device will be created
 
 5- Click on start, then choose the file in which the ubuntu copy is stored
 
 6- Then choose install ubuntu, then press next, then choose the language, then the region, then enter the name and code, and ubuntu will be installed
 
 7- How to install Ros1:
 
 Run Terminal and type the following commands:
 
 Command Prompt Link:
 http://wiki.ros.org/Installation/Ubuntu
 
  Ros version:
 Rosverstion:1.14.3

# Commands install ROS1:
Command Prompt Link:

 http://wiki.ros.org/Installation/Ubuntu
 
Command:

 sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'


 sudo apt install curl # if you haven't already installed curl
 curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc |  sudo apt-key add -


 sudo apt update

 sudo apt install ros-noetic-desktop-full

 sudo apt install ros-noetic-PACKAGE

 sudo apt install ros-noetic-slam-gmapping

 apt search ros-noetic

 source /opt/ros/noetic/setup.bash

 echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
 source ~/.bashrc


 echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc
 source ~/.zshrc

 sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

 sudo apt install python3-rosdep

 sudo rosdep init

 rosdep update
 
 # Task1-2: Write the Ros installation algorithm on the Jetson nano:
 
  1- Download xubuntu 20.04 through the following link:
  
 xubuntu 20.04 link:
 
 https://forums.developer.nvidia.com/t/xubuntu-20-04-focal-fossa-l4t-r32-3-1-custom-image-for-the-jetson-nano/121768
 
 2- Unzip the xubuntu 20.04 folder after the download process is finished using 7zip
 
 3- Download the baleana Etcher program through the following link:
 
 Baleana Etcher link:
 
 https://www.balena.io/etcher/
 4- When launching the baleana Etcher program, select
 flash from file then choose xubuntu20.04
 
 5- After that choose flash
 
 6- A window will appear, close it
 
 7- Complete the xubuntu 20.04 installation process, choose the language and region, enter the name and code and complete the other settings
 Install Ros2 Foxy:
 
 1- Open the terminal
 
 2- Then copy the following commands
 
  Command link:
  
 https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html

# Commands install ROS2:

Command link:

 https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html
 
 Command:
 
 local

 sudo apt update && sudo apt install locales
 sudo locale-gen en_US en_US.UTF-8
 sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
 export LANG=en_US.UTF-8

 local

 apt-cache policy |  grep universe

 500 http://us.archive.ubuntu.com/ubuntu focal/universe amd64 Packages
     release v=20.04,o=Ubuntu,a=focal,n=focal,l=Ubuntu,c=universe,b=amd64


 sudo apt install software-properties-common
 sudo add-apt-repository universe


 sudo apt update && sudo apt install curl gnupg2 lsb-release
 sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg


 echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source)  /etc/os-release && echo $UBUNTU_CODENAME) main" |  sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null


 sudo apt update

 sudo apt upgrade

 sudo apt install ros-foxy-desktop

 sudo apt install ros-foxy-ros-base

 source /opt/ros/foxy/setup.bash
 ros2 run demo_nodes_cpp talker


