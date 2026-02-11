# Docker Basics: Test Questions.
This document contains structured test questions based on Docker fundamentals.
Each section matches the command reference for consistency and easy revision.

## Section 1: Docker Installation and Verification.
1.1. What command is used to install Docker Engine on a Debian-based system?
1.2. Which command checks whether the Docker service is running?
1.3. How do you verify that Docker was installed successfully?

--------------------------------------------------------------

## Section 2: Docker Image Management.
2.1. Which command lists all Docker images available locally?
2.2. What command is used to download an image from Docker Hub?
2.3. How would you remove a Docker image from your system?
2.4. What is the purpose of a Docker image?

-------------------------------------------

## Section 3: Docker Container Management.
3.1. Which command creates and runs a container from an image?
3.2. How do you list only the containers that are currently running?
3.3. What command lists all containers, including stopped ones?
3.4. How do you stop a running Docker container?
3.5. Which command removes a stopped container?
3.6. What is the difference between a Docker image and a Docker container?

--------------------------------------------------------------------------

## Section 4: Practical Scenarios.
4.1. You install Docker on a Linux system but when you run the command 'docker --version', the command is not found.
What steps do you take to troubleshoot and fix the issue?

4.2. You pull an image successfully but when you try to run it, the container exits immediately.
What could cause this behaviour and how would you investigate it?

4.3. A container is running but the application inside it is not responding.
Which commands would you use to inspect the container and diagnose the problem?

4.4. You want to test a Docker image without permanently keeping the container on your system.
How would you run the container and ensure that it is autoomatically removed after stopping?

4.5. Your system is running low on disk space and you suspect Docker is the cause.
How would you identify unused images and containers and how would you clean the up safely?

4.6. You run a container and it works correctly but when you stop it, all changes inside the container are lost.
Why does this happen and how can it be prevented in a real-world setup?

----------------------------------------------------------------------------------------------------------------

## Section 5: Docker System & Logs.
5.1. Which command shows system-wide Docker information?
5.2. How do you view the logs of a running container.
5.3. Why is it useful to check container logs?

-----------------------------------------------

## Section 6: Dockerfile & Image Build Concepts:
6.1. What is a Dockerfile?
6.2. How does a Dockerfile make building images repeatable?
6.3. What is the difference between a Dockerfile and a Docker image?

--------------------------------------------------------------------

## Section 7: Conceptual & Troubleshooting.
7.1. What problems does Docker solve in traditional application deployment?
7.2. Explain the difference between containers and virtual machines.
7.3. Why are containers considered lightweight?
