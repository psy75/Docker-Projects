Projects Using Docker

This repository contains three Docker-based projects.
Below are the steps for installing Docker, building the images, running the containers, checking images, and pushing them to Docker Hub.

1. Install Docker

  Run the following commands to install Docker on Ubuntu:
  
  sudo apt update
  sudo apt install -y docker.io
  sudo systemctl start docker
  sudo systemctl enable docker


Check Docker installation:

  docker --version

2. Build the Docker Image (Go to the specific project directory)

Navigate into the project folder:

  cd project-folder-name

Build the Docker image:

  docker build -t my-image:latest .

3. Run the Docker Container
  docker run -it --name my-container-name my-image:latest

If your app uses a port:

  docker run -it -p 8000:8000 --name my-container-name my-image:latest

4. Check Docker Images
  docker images

Check running containers:

  docker ps

5. Push Your Image to Docker Hub
Login to Docker Hub
  docker login -u <your-username>

  For the password → use Docker Hub Access Token, not your actual password.

Tag your image before pushing
  docker -t my-image:latest <dockerhub-username>/<repo-name>:latest

Push the image
docker push <dockerhub-username>/<repo-name>:latest
