# Docker Run Command - Running Containers in the Background

The `docker run` command is a fundamental part of working with Docker containers. One of its key options is the `-d` flag, which allows you to run a container in the background. This is particularly useful when you want a container to continue running independently of your terminal session. In this documentation, we'll explore how the `-d` option works and provide examples with two different containers: Alpine and Nginx.

## Table of Contents

- [What is the `-d` Option?](#what-is-the--d-option)
- [Running an Alpine Container](#running-an-alpine-container)
- [Running an Nginx Container](#running-an-nginx-container)
- [Conclusion](#conclusion)

## What is the `-d` Option?

The `-d` option stands for "detached mode," and when used with the `docker run` command, it instructs Docker to run the container in the background. In detached mode, the container continues to run even if you close your terminal session, making it suitable for long-running services and applications.

## Running an Alpine Container

Alpine Linux is a lightweight Linux distribution often used as a base image for Docker containers. However, Alpine containers don't typically run any background processes, so they exit immediately by default. Let's see how the `-d` option behaves with an Alpine container:

```bash
docker run -d alpine
```

In this case, you'll notice that the container starts in detached mode, but it doesn't run any persistent processes. As a result, it will exit almost immediately after starting, even though it's in the background. To see the container's status, you can use `docker ps -a` to list all containers:

```bash
docker ps -a
```

## Running an Nginx Container

Nginx is a popular web server and reverse proxy server used to serve web content. When you run an Nginx container with the `-d` option, it starts a web server in the background that can handle web requests:

```bash
docker run -d nginx
```

Unlike the Alpine container, Nginx has a built-in background process (the web server) that keeps running. You can access the Nginx server by connecting to the appropriate port on your host machine.

To find the port mapping, you can use the following command:

```bash
docker ps
```

You'll see an entry for your Nginx container, showing the port mapping, which allows you to access the Nginx web server in a web browser.

## Conclusion

In summary, the `-d` option with the `docker run` command is used to run containers in detached mode, meaning they run in the background. The behavior of the `-d` option depends on the container image being used. Some containers, like Alpine, may exit immediately since they don't have persistent background processes. Others, like Nginx, will keep running and can serve as long-running services.

When using the `-d` option, it's essential to be aware of the specific behavior of the container image you're working with to ensure it meets your intended use case.