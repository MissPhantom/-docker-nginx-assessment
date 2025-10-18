
# Project Overview: Simple Nginx Web App in Docker

This project creates a simple web application that is encapsulated within a **Docker container**. It utilizes the **Nginx** web server to efficiently serve **static web content** (like HTML, CSS, and JavaScript). The main goal of using Docker is to package the application and all its necessary dependencies into an **image**, ensuring it runs consistently and reliably across various environments.



## Docker Build Command

The command below builds the Docker image from the current directory:

```bash
docker build -t my-nginx-app .
```

  * **`docker build`**: Initiates the process of creating a Docker image.
  * **`-t my-nginx-app`**: **Tags** the resulting image with the name `my-nginx-app`, making it easy to reference.
  * **`.`**: Specifies the build context, telling Docker to look for the **`Dockerfile`** in the **current directory**.



## Docker Run Command

This command starts a new container based on the built image and configures its networking:

```bash
docker run -d -p 8888:80 my-nginx-app
```

  * **`docker run`**: Executes a new container from a specified image.
  * **`-d`**: Runs the container in **detached mode** (in the background).
  * **`-p 8888:80`**: **Port mapping**. This crucial flag maps **port 8888** on your host machine to **port 80** inside the container (the port Nginx is listening on).
  * **`my-nginx-app`**: The name of the Docker image to be used for the container.
