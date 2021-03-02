# kubernetes-and-docker
Learn Docker, Docker Compose, Multi-Container Projects, Deployment and all about Kubernetes from the ground up! Udemy course Notes


# Docker
Docker is a **container** technology: A tool for creating and managing containers

* Container: A standardized unit of software (A package of code **and** dependencies to run that code)

> The same container always yields[produce or provide] the **exact same application and execution behavior** No matter where or by whom it might be executed.


## Images and Containers

**Images** are the templates/blueprints for containers

**Containers** are the running "unit of software" (concrete running instance)


> We can create images based on others images

---

> Images are Read Only. **The image is a "snapshot" of the latest version of the code when the image was created.**


### Layer based architecture

whenever you build an image, Docker caches every instruction result, and when you then rebuild an image, it will use these cached results if there is no need to run an instruction again.

> Every instruction into the Dockerfile is a layer. The **CMD** instruction is a layer that will only exist when the container is running.

> The container uses the code stored into the image, the container doesn't create a new copy of the code

If you try to remove an image while a container is using that image, you'll see an erro like this:

```
nodejs-app-starting-setup|main⚡ ⇒ docker rmi 2e6cc7c8b0ff
Error response from daemon: conflict: unable to delete 2e6cc7c8b0ff (cannot be forced) - image is being used by running container ded9c8642876
```





