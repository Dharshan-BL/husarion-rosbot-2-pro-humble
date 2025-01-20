# husarion-rosbot-2pro-humble


1) Run the docker using:
   ```
   docker run -it --rm --name my_rosbot_container \
    --net=host \
    --privileged \
    -e ROS_DOMAIN_ID=10 \
    my_rosbot_image
   ```
