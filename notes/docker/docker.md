![](docker_logo.png)

## [Docker](https://docs.docker.com/get-started/)

Docker is a platform for developers and sysadmins to build, run, and share applications with containers

## Container

A container is nothing but a running process, with some added encapsulation features applied to it in order to keep it isolated from the host and from other containers

Each container interacts with its own private filesystem; this filesystem is provided by a Docker image


## Image

An image includes everything needed to run an application - the code or binary, runtimes, dependencies, and any other filesystem objects required.



**--publish or -p** asks Docker to forward traffic incoming on the host’s port 8000 to the container’s port 8080. Containers have their own private set of ports, so if you want to reach one from the network, you have to forward traffic to it in this way. Otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture.



`docker build --tag container-name:version <path-to-docker-file>`

`docker run -p 80:80 -it -d container-name:version`

`docker exec 'container_name' <command-to-run>`

**Dockerfile**
## [Docker File Builder](https://docs.docker.com/engine/reference/builder/)
    List of commands to use inside docker build file


`docker tag flaskserver:3.0 salakhaliffjr/flaskserver:3.0`


`docker login`

`docker push salakhaliffjr/flaskserver:3.0`


Entrypoint
![](2020-10-04-19-33-29.png)


To skip port map

`docker run <image> --network=host`

View detailed info 

`docker inspect <container-name>`


## File Storage 

Docker Files location

`/var/lib/docker`

## **Persistence**

`docker volume <volume-name>`

not mandatory, docker automatically createsw volume if none exist

creates a folder in `/var/lib/docker/volumes/<volume-name>` 

`docker run -v <volume-name>:</path/in/container>  container-name:tag`

newer method 

`docker run --mount type=bind,source=/path/in/local/system, target=/path/in/container container-name:tag`
