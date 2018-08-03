# Docker 101 - Introduction to containers and Docker

## Description
> Docker provides a way to run applications securely isolated in a container, packaged with all its dependencies and libraries. -the official Docker [documentation](https://docs.docker.com/)

Simply put, Docker is a platform to build, run and even share so called [containers](https://en.wikipedia.org/wiki/Operating-system-level_virtualization). A container consists of an operating system (usualy a Linux distribution) and some software to perform a certain (set of) tasks.

This [Wikipedia article](https://en.wikipedia.org/wiki/Docker_(software) might be a readable summary of what Docker is and can do. Alternatively, [this website](https://docker-curriculum.com/) tries to offer a simplified tutorial like introductin to Docker for beginners (just read to introductionary chapter to get a basic grasp of what Docker is and can do, skimming the first chapter should give you a basic introduction to some phrasing and concepts).

> Note: [containers are __not__ virtual machines!](https://blog.docker.com/2016/03/containers-are-not-vms/)

## Installation
Follow the instructions for your operating system on https://www.docker.com/get-docker.

## Configuration
Operating system specific configuration steps are covered in the installation instructions.

## Usage

Docker comes with a rather large set of options and posibilities, all neatly described in the docker manpage and the (again, rather large) Docker [documentation](https://docs.docker.com/).

When trying to use a dockerised version of an application or trying to use a docker image downloaded from the internet, you should have received instructions on how to properly start this container.

Usually, you will be able to download a container using the 'get' command:
```
docker get [url]
```

When you are writing and distributing your own docker container, image or Dockefile, make sure you don't only read the docs, but also write the docs; at least supply a way to start a container in the way you intended and ensure that you at least supply your intended way of building from your dockerfile.

> Note: It is very likely that your container will end up in a [Kubernetes](https://kubernetes.io/) cluster.

## Test

Use the Ubuntu base image.
### Installation
If you did not already do so: find out how to install docker and get and run the `hello-world` container. This can be done through the docs.
### Interactive Ubuntu container
Try to run the ubuntu docker interactiveley (have Ba(sh) open in an Ubuntu container and try some basic Bash commands).
### Dockerfile to container
Write a Dockerfile, that uses the previously used Ubuntu imaage as it's base image for a container that simply runs:
```
echo hello!
```
Go through all the required steps to get your 'hello!' container running.
### Using programs and copying files in a Dockerfile
Write a simple python3 script called `hello.py`:
```
print('python!')
```

Write a dockerfile that installs python3, copy your `hello.py` into your Docker image and build and run.
### Alpine
If you are up for a tougher challenge, try to do the previous exeercise using the latest `alpine` (google it!) image as base image.

## Tips
If you managed to go through all the steps above and the went through the Docker documentation, you now have a basic understanding of how Docker containers work.

If you lack experience with Linux or computers in general, be sure to come back to this tutorial and the Docker documentation as you learn.

Aim to go through Docker's full feature set, Docker is heavily documented and usualy rather obvious. 

Remember: Docker might seem like a lot and complicated, but the tricky part of Docker is learning about Linux and programming, not Docker.

```
   Copyright 2018 Opensource Academy

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
