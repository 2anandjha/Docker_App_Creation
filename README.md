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


Build an image from a Dockerfile
(base) anandmohanjhaoutlookcoms-MacBook-Pro:app anandmohan.jhaoutlook.com$ docker build -t getting-started .
[+] Building 30.4s (10/10) FINISHED                                                                                                                                                  
 => [internal] load build definition from Dockerfile                                                                                                                            0.0s
 => => transferring dockerfile: 183B                                                                                                                                            0.0s
 => [internal] load .dockerignore                                                                                                                                               0.0s
 => => transferring context: 2B                                                                                                                                                 0.0s
 => [internal] load metadata for docker.io/library/node:12-alpine                                                                                                               5.3s
 => [1/5] FROM docker.io/library/node:12-alpine@sha256:1ea5900145028957ec0e7b7e590ac677797fa8962ccec4e73188092f7bc14da5                                                         0.0s
 => [internal] load build context                                                                                                                                               0.3s
 => => transferring context: 4.63MB                                                                                                                                             0.3s
 => CACHED [2/5] RUN apk add --no-cache python g++ make                                                                                                                         0.0s
 => CACHED [3/5] WORKDIR /app                                                                                                                                                   0.0s
 => [4/5] COPY . .                                                                                                                                                              0.1s
 => [5/5] RUN yarn install --production                                                                                                                                        21.6s
 => exporting to image                                                                                                                                                          2.9s 
 => => exporting layers                                                                                                                                                         2.9s 
 => => writing image sha256:b84ecf6c8485c0491a62a5d09784e21047a79a603f0c5479a4205b4772b830d1                                                                                    0.0s 
 => => naming to docker.io/library/getting-started                                                                                                                              0.0s 
                                                                                                                                                                                     
Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them                                                                                 
(base) anandmohanjhaoutlookcoms-MacBook-Pro:app anandmohan.jhaoutlook.com$ docker run -dp 3000:3000 getting-started
09bb3b870c9372ee2cc8dae51ff5ec9e69cf4bf4492a2d7c4c8079eeedc898a7
(base) anandmohanjhaoutlookcoms-MacBook-Pro:app anandmohan.jhaoutlook.com$ 



