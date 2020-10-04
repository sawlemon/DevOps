![](docker_logo.png)

## [Docker](https://docs.docker.com/get-started/)

Docker is a platform for developers and sysadmins to build, run, and share applications with containers

## Container

A container is nothing but a running process, with some added encapsulation features applied to it in order to keep it isolated from the host and from other containers

Each container interacts with its own private filesystem; this filesystem is provided by a Docker image


## Image

An image includes everything needed to run an application - the code or binary, runtimes, dependencies, and any other filesystem objects required.



**--publish or -p** asks Docker to forward traffic incoming on the host’s port 8000 to the container’s port 8080. Containers have their own private set of ports, so if you want to reach one from the network, you have to forward traffic to it in this way. Otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture.



`sudo docker build --tag container-name:version <path-to-docker-file>`

`docker run -p 80:80 -it container-name:version`

`docker exec 'container_name' <command-to-run>`

## [Dockr File Builder](https://docs.docker.com/engine/reference/builder/)


