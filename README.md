# husarion-rosbot-2pro-humble

Creating your docker image:

1) cd to folder containing docker
2) docker build -t shirke_image .
3) Run the docker using:
   ```
   docker run -it --rm --name my_rosbot_container \
    --net=host \
    --privileged \
    -e ROS_DOMAIN_ID=10 \
    my_rosbot_image
   ```
4) ```docker commit <container_name> <new_image_name>```
5) ```mkdir husarion_ws/src -p```
6) ```cd husarion_ws/src``` 
7) ```git clone https://github.com/micro-ROS/micro-ROS-Agent.git```
8) ```sudo apt upgrade libfastcdr-dev```
9) ``` cd husarion_ws/src```
10) ```git clone https://github.com/eProsima/Fast-CDR.git```
11) ```cd ~/husarion_ws```
12) ```colcon build --symlink-install```
13) ```echo "source /root/husarion_ws/install/local_setup.bash" >> ~/.bashrc```
14) ```sudo apt upgrade ros-humble-fastcdr```
15) ```git clone https://github.com/husarion/rosbot_ros.git```



---- New attempt ---- 
```docker run -it --rm -v /dev:/dev -v /dev/shm:/dev/shm --privileged --net=host microros/micro-ros-agent:humble serial -D /dev/ttyS4  serial -b 576000```


---------------------- RPLIDAR A3 -----------------------------------
1) ```git clone https://github.com/Slamtec/sllidar_ros2.git```
2) ```source scripts/create_udev_rules.sh```
3) ```ros2 launch sllidar_ros2 view_sllidar_a3_launch.py serial_port:=/dev/ttyUSB0```

----------------- ASTRA 3D camera -----------------------------------

1) ```git clone https://github.com/orbbec/ros2_astra_camera.git```
2) ```cd ~/ros2_ws/src/ros2_astra_camera/astra_camera/scripts```
      ```sudo bash install.sh```
3) ```sudo service udev restart``` (if udevadm is not running: ```ps aux | grep udev```)
4) ```sudo udevadm control --reload-rules && sudo udevadm trigger```







