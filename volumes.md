# Volumes

Volumes are folders on your host machine hard drive which are mounted (available or mapped) into docker containers.

We connect a folder inside of the container to a folder outside of the container, on your hosrt machine and **changes in either folder will be reflected in the other one**.

## Volumes (Managed by docker)

* **Anonymous volumes**: They are only accesible using the `docker volume` command and only exist as long as our container exist. Into a docker file we could add: `VOLUME [ "/data" ]`
* **Named volumes**: Are great for data which should be persistent but which you don't need to to edit or view directly because you don't really have access to that folder on your host machine. The named volumes aren't created inside of the Dockerfile but using `docker run` command with the flag `-v`. `<host-machine>:<container-folder>`

## Bind Mounts (Managed by you)
