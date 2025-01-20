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
4) ```mkdir husarion_ws/src -p```
5) ```cd husarion_ws/src``` 
6) ```git clone https://github.com/micro-ROS/micro-ROS-Agent.git```
7) ```sudo apt update && rosdep update```
8) ```sudo apt upgrade ros-humble-fastcdr```
9) ```git clone https://github.com/husarion/rosbot_ros.git```
