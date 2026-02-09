# Docker Basics:
## Folder Purpose:
This folder covers the fundamentals of Dockeras part of the DevOps and/or the Cloud Engineering learning path.

The goal is to understand containerisation concepts and basic Docker usage before moving on to more advanced topics such as orchestration and cloud deployments.

This folder contains:
- Conceptual explanations of Docker.
- A reference of essential Docker commands.
- Tests to validate understanding.
- A hands-on project that demonstrates Docker in practice.

----------------------------------------------------------

## Learning Objectives:
By completing this folder you should be able to:
- Explain what Docker is and why it is used.
- Understand the difference between images and containers.
- Build a simple Docker image using a Dockerfile.
- Run and manage containers.
- Explain basic container lifecycle commands.

----------------------------------------------------------

## Overview of Docker:
Docker is a containerisation platform that allows applications to be packaged together with everything they need to run. 
This includes application code, runtime, system libraries, and dependencies. 
The result is a portable and consistent unit that behaves the same way across different environments.

Docker solves the common problem of applications working on one machine but failing on another due to environment differences.

------------------------------------------------------------------------------------------------------------------------------

## Why Docker Exists:
Before Docker, applications were often installed directly on servers. 
This led to:
- Dependency conflicts.
- Environment inconsistencies.
- Difficult rollbacks and upgrades.
- Slow and error-prone deployments.

Docker introduces a standardised way to package and run applications making deployments faster, safer, and more predictable.

----------------------------------------------------------------------------------------------------------------------------

## What Is a Docker Image:
A Docker image is a read-only template used to create containers.

An image includes:
- Application code.
- Dependencies and libraries.
- Environment configuration.
- Instructions for running the application.

Images are immutable and can be reused across systems.

------------------------------------------------------

## What Is a Docker Container:
A Docker container is a running instance of a Docker image.

Containers:
- Are lightweight and fast to start.
- Run in isolation to the host system.
- Can be stopped, restarted, and removed.
- Share the host operating system kernel.

Multiple containers can be created from the same image.

-------------------------------------------------------

## What Is a Dockerfile:
A Dockerfile is a text file that contains a set of instructions used to build a Docker image.

A Dockerfile defines:
- The base image.
- Files to include.
- Commands to execute during image creation.
- The default command to run when the container starts.

Dockerfiles enable repeatable and automated image builds.

---------------------------------------------------------

## Images vs Containers:
- An image is a blueprint or template.
- A container is a running instance of that template.

Images do not change when built (immutable). Containers can start, stop, and be removed.

----------------------------------------------------------------------------------------

## How Docker Fits Into DevOps:
Docker is a foundational DevOps tool because it:
- Ensures consistency across environments.
- Simplifies application deployment.
- Supports microservices architecture.
- Integrates well with CI/CD pipelines and cloud platforms.

Docker is typically used before introducing orchestration tools such as Kubernetes.
