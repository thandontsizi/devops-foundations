# Docker Commands Reference:
This document lists essential Docker commandswith short, clear explanations.
It is intended as an offline reference for learning and practice.

## 1. Docker Installation and Verification:
1.1 Docker Engine Installation:
Command: sudo apt install docker.io -y
Explanation: Installs Docker and required dependencies on a Debian-based system.

1.2 Check Docker Service Status:
Command: sudo systemctl status docker
Explanation: Shows whether the Docker service is running and enabled.

1.3 Verify Docker Installation:
Command: docker --version
Explanation: Shows the installed Docker version, confirming successful installation.

------------------------------------------------------------------------------------

## 2. Docker Image Management:
2.1 List Local Docker Images:
Command: docker images
Explanation: Lists all Docker images currently available on the system.

2.2 Pull an Image from Docker Hub:
Command: docker pull hello-world
Explanation: Downloads rhe "hello-world" image from the Docker Hub to the local machine.

2.3 Remove a Docker Image:
Command: docker rmi IMAGE_ID
Explaination: Deletes a Docker image from the local system by using the image's ID.

-----------------------------------------------------------------------------------

## 3. Docker Container Management: 
3.1 Run a Container: 
Command: docker run IMAGE 
Explaination: Creates and starts a container from the specified image. 

3.2 List Running Containers: 
Command: docker ps 
Explanation: Shows containers that are currently running. 

3.3 List All Containers: 
Command: docker ps -a 
Explanation: Shows all containers, including stopped ones. 

3.4 Stop a Running Container: 
Commmand: docker stop CONTAINER_ID 
Explaination: Gracefully stops a running container. 

3.5 Remove a Container: 
Command: docker rm CONTAINER_ID 
Explaination: Deletes a stopped container from the system.
