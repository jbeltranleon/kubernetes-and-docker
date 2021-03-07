# Basic Docker CLI Commands

* Build the image: `docker build .`
* Run the image as a container: `docker run -p 3000:3000 <image-id>`
* Use the -d option start a detached container `docker run -p 3000:3000 -d <image-id>` this will "liberate" the terminal and keep running the container in the background
* Stop the container: `docker stop <containers-name or containers-id>`

> The exposed ports by the container with the `-p` label are sorted like: `<local-machine-port-to>:<container-port>`
 
* Run an interactive sesion from inside a container our hosting machine: `docker run -it <image>`eg: `docker run -it node` 
* Get all the posible options from a command in docker we can add the `--help`
* See the running containers: `docker ps`
* See all the containers: `docker ps -a`
* Start stopped container: `docker start <cointainer-id/cointainer-name>`
* See the logs of an specific container: `docker logs <cointainer-id>`. If we want see all the future logs we could use the `-f` flag.
* Delete a stoped container: `docker rm <docker-id>`, we could pass more that one container separated by space.
* List all the images: `docker images`
* Delete a image that is'n in use: `docker rmi <image-id>`, we could pass more that one image separated by space.
* Remove all unused images: `docker image prune` 
* Remove all the stoped containers: `docker container rm $(docker ps --filter "status=exited" -q)` 
* Remove automatically an unused container: `docker run --rm <container-id>`
* Get information from an image: `docker image inspect <image-id>`
* Copy all files from a local folder into an a container: `docker cp folder/. <container-id>:/folder_into_container`
* Copy all files from a container folder into an a local folder: `docker cp <container-id>:/folder_into_container folder`