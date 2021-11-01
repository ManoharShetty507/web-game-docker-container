# Web-game-docker-container
## Build own image and push it to Docker Hub

Check for the available images
###### --> docker images

Check for the running containers
###### --> docker ps

Check for all the running containers status
###### --> docker ps -a

Build the Docker Image (Make sure you have Dockerfile, and also make you don't miss out (.) which tells about the path.
###### --> docker build -t manoharshetty507/web-game:v1 .


Expose the created container and see if it accessible
###### --> docker run --rm -dit --name newimage -p 8500:80 manoharshetty507/web-game:v1

#### Push the created Image to Docker Hub

##### Make sure you login to Docker Hub in the Server

###### --> docker tag newimage manoharshetty507/web-game:v1
###### --> docker commit 2e55e8b542f8 manoharshetty507/newnginx:v1
###### --> docker push manoharshetty507/newnginx:v1

## Command:
###### --> docker tag <existing-image-name> <hub-user>/<repo-name>[:<tag>]
###### --> docker commit <existing-container-ID> <hub-user>/<repo-name>[:<tag>]
###### --> docker push <hub-user>/<repo-name>:<tag>

