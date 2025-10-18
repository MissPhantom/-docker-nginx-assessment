1. Brief Description of the Project
This project is a simple web application that runs inside a Docker container. It uses an Nginx web server to serve static web content (such as HTML, CSS, and JavaScript files). Docker is used to package the application and its dependencies into an image so it can run consistently across different environments.

2. Docker Build Command
docker build -t my-nginx-app .
docker build → builds a Docker image.
-t my-nginx-app → tags the image with the name my-nginx-app.
. → tells Docker to use the current directory (which contains the Dockerfile).

3. Docker Run Comman
docker run -d -p 8888:80 my-nginx-app
docker run → runs a new container.
-d → runs it in detached mode (in the background).
-p 8888:80 → maps port 8888 on your host to port 80 inside the container.
my-nginx-app → specifies the image to use.


