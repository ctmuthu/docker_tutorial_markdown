# What happens on "docker run"

When you run the command `docker run hello-world`, several things happen:

1. **Image Check**: Docker checks if the "hello-world" image exists locally on your system. If it doesn't find the image, Docker automatically pulls it from Docker Hub, which is the default registry for Docker images.

2. **Container Creation**: Once Docker has the image (either by pulling it or finding it locally), it creates a new container based on that image. Containers are isolated, lightweight environments that contain all the necessary code and dependencies to run a specific application.

3. **Container Execution**: The container starts executing the command specified in the image's metadata. In the case of the "hello-world" image, the command is typically a simple program that prints a message like "Hello from Docker!" along with some other information.

4. **Output Display**: The output of the program within the container is captured and displayed in your terminal or command prompt. This is where you see the "Hello from Docker!" message and other details about your Docker installation.

5. **Container Exit**: After the program inside the container completes its execution (which is quite fast in the case of the "hello-world" image), the container exits. Docker containers are designed to be short-lived and can start and stop very quickly.

6. **Container Cleanup**: Docker automatically cleans up the stopped container, removing it from your system. This helps ensure that your system doesn't get cluttered with unused containers.

Running `docker run hello-world`:

docker run hello-world
```
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
70f5ac315c5a: Pull complete 
Digest: sha256:dcba6daec718f547568c562956fa47e1b03673dd010fe6ee58ca806767031d1c
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.(arm64v8)
 3. The Docker daemon created a new container from that image which runs the executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```
