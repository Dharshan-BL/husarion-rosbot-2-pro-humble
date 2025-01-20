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
8) ```sudo apt update && rosdep update```
9) ```sudo apt upgrade ros-humble-fastcdr```
10) ```git clone https://github.com/husarion/rosbot_ros.git```
