# Docker_App_Creation


Difference between VM and Docker
Virtual machines solve the same problem but in a different way. A virtual machine is a virtual instance of an entire operating system – maybe Linux or Windows. If you develop your app on a virtual instance of Linux, you can run that app anywhere that runs the same virtual instance of Linux.

Problem :  if you want to deploy a single web app, you need to run an entire virtual operating system. This is very expensive, especially if you have lots of apps to run.

Docker solves this problem by placing apps in virtual Containers that all run on the same operating system. Each container contains all the code, libraries, and dependencies like configuration files needed to run the app. This saves us a huge amount of storage, time, processing power and complexity.


The document will walk you through the initials for the docker  configuration for running an APP.
what is a Docker Image
A Docker image is a private file system just for your container. It provides all the files and code your container needs.
Steps for setting up the docker images
Start a container based on the image you built in the previous step. 
Running a container launches your application with private resources, securely isolated from the rest of your machine.
Save and share your image on Docker Hub to enable other users to easily download and run the image on any destination machine.

What is an image 
Most Dockerfiles start from a parent image. If you need to completely control the contents of your image, you might need to create a base image instead. Here’s the difference:

A parent image is the image that your image is based on. It refers to the contents of the FROM directive in the Dockerfile. Each subsequent declaration in the Dockerfile modifies this parent image. Most Dockerfiles start from a parent image, rather than a base image. However, the terms are sometimes used interchangeably.

A base image has FROM scratch in its Dockerfile.



