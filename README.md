## ROS in Docker for Raspberry Pi 4

```
git clone https://github.com/patilameya825/ros_in_raspbian_docker.git
```

**Build Dockerfile**
```
cd ros_in_raspbian_docker/Docker
docker build -t ros-kinetic-armv7-armhf-ubuntu:latest .
```

**Run terminal in ROS container, built from the above image**
```
docker run -it ros-kinetic-armv7-armhf-ubuntu bash
```

### NOTES ON DOCKER USAGE
* To list images in docker
```
docker image ls
```
* To list containers and their infos
```
docker ps -a
```
* To delete a container
```
docker rm <container-id>
```
* To delete an image
```
docker rmi <image-id>
```
* To create a container
```
docker container create --name <container-name> <image-id>
```
For other options, such as, exposing ports, binding volumes, setting workdir, etc., refer
```
docker container create --help
```
Example: Attach 8000 port of host to container's 8080 port, bind host's /home/pi/Documents directory to container's /home/ubuntu/Documents directory, and set /home/ubuntu as workdir
```
docker container create -p 8000:8080 -v /home/pi/Documents:/home/ubuntu/Documents --workdir /home/ubuntu --name container_1 image_1
```
* To start a container in Interactive mode
```
docker start -i <container-id> bash
```
* To stop a container
```
docker stop <container-id>
```
* To run a stopped container in terminal
```
docker run -it <container-id> bash
```

### Follow Me On 
***https://github.com/patilameya825/ros_in_raspbian_docker***

### Post Issues At
***https://github.com/patilameya825/ros_in_raspbian_docker/issues***
