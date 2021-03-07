# Basic Docker CLI Commands

* To build the image: `docker build .`
* To run the image as a container: `docker run -p 3000:3000 <image-id>`
* Use the -d option to start a detached container `docker run -p 3000:3000 -d <image-id>` this will "liberate" the terminal and keep running the container in the background
* To stop the container: `docker stop <containers-name or containers-id>`

> The exposed ports by the container with the `-p` label are sorted like: `<local-machine-port-to>:<container-port>`
 
* To run an interactive sesion from inside a container to our hosting machine: `docker run -it <image>`eg: `docker run -it node` 
* To get all the posible options from a command in docker we can add the `--help`
* To see the running containers: `docker ps`
* To see all the containers: `docker ps -a`
* To start stopped container: `docker start <cointainer-id/cointainer-name>`
* To see the logs of an specific container: `docker logs <cointainer-id>`. If we want to see all the future logs we could use the `-f` flag.
* To delete a stoped container: `docker rm <docker-id>`, we could pass more that one container separated by space.
* To list all the images: `docker images`
* To delete a image that is'n in use: `docker rmi <image-id>`, we could pass more that one image separated by space.
* To remove all unused images: `docker image prune` 
* To remove all the stoped containers: `docker container rm $(docker ps --filter "status=exited" -q)` 
* Remove automatically an unused container: `docker run --rm <container-id>`