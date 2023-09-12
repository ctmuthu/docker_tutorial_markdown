# Docker Command Options:

#### Management Commands:

1. `docker start`: Start one or more stopped containers.
2. `docker stop`: Stop one or more running containers.
3. `docker restart`: Restart one or more containers.
4. `docker pause`: Pause all processes within one or more containers.
5. `docker unpause`: Unpause all processes within one or more containers.
6. `docker rm`: Remove one or more containers.
7. `docker ps`: List containers.
8. `docker inspect`: Display detailed information about a container or image.

#### Image Commands:

1. `docker pull`: Pull an image or a repository from a registry.
2. `docker build`: Build an image from a Dockerfile.
3. `docker push`: Push an image or a repository to a registry.
4. `docker images`: List images.
5. `docker rmi`: Remove one or more images.
6. `docker tag`: Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.

#### Network Commands:

1. `docker network create`: Create a network.
2. `docker network connect`: Connect a container to a network.
3. `docker network disconnect`: Disconnect a container from a network.
4. `docker network ls`: List networks.

#### Volume Commands:

1. `docker volume create`: Create a volume.
2. `docker volume ls`: List volumes.
3. `docker volume rm`: Remove one or more volumes.

#### System Commands:

1. `docker info`: Display system-wide information.
2. `docker version`: Show the Docker version information.
3. `docker login`: Log in to a Docker registry.
4. `docker logout`: Log out from a Docker registry.
5. `docker system prune`: Remove unused data (containers, images, networks, volumes).

#### Miscellaneous Commands:

1. `docker exec`: Run a command in a running container.
2. `docker attach`: Attach to a running container.
3. `docker run`: Run a command in a new container.
4. `docker logs`: Fetch the logs of a container.
5. `docker cp`: Copy files/folders between a container and the local filesystem.
6. `docker commit`: Create a new image from a container's changes.
