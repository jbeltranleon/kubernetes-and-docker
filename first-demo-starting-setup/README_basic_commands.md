# Basic Docker CLI Commands

* To build the image: `docker build .`
* To run the image as a container: `docker run -p 3000:3000 <image-id>`
* Use the -d option to start a detached container `docker run -p 3000:3000 -d <image-id>` this will "liberate" the terminal and keep running the container in the background
* To stop the container: `docker stop <containers-name or containers-id>`

> The exposed ports by the container with the `-p` label are sorted like: `<local-machine-port-to>:<container-port>`


