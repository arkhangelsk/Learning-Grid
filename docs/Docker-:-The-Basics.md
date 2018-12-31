## What is Docker?
Docker is a system to create, deploy, and run applications by using containers.

## What is a Docker Image?
A Docker Image is the template (application plus required binaries and libraries) needed to build a running Docker Container (the running instance of that image).

As templates, images are what can be used to share a containerized applications. Collections of images are stored/shared in registries like Docker Hub. When you download an image, it can then be used (as a template) to spin up multiple running Containers in your own environment.

## What is a Docker Container?
* A container is a runnable instance of an image.
* A container is defined by its image as well as any configuration options you provide to it when you create or start it. 

**Reference:** 

https://docs.docker.com/engine/docker-overview/#docker-objects 

https://www.quora.com/What-are-Docker-Images

## What is the Dockerfile?

* A Dockerfile list all the commands that user would normally execute manually in order to build a Docker image.
* Docker reads the Dockerfile and executes those commands one-by-one and builds the target image.
* To build an image using a Dockerfile, use below command:
```
docker build -f /path/to/Dockerfile
```

## How to determine the size of a Docker image?
Use command `docker images` to determine the size of the docker image (last column)

![docker-image-size](https://github.com/arkhangelsk/Learning-Grid/blob/master/images/docker-image-size.png)

## Creating your first docker container:

https://www.jamescoyle.net/how-to/1503-create-your-first-docker-container

https://www.vultr.com/docs/how-to-use-docker-creating-your-first-docker-container

## Setting up puppeteer environment with Docker:
https://github.com/ebidel/try-puppeteer/tree/master/backend

https://zwischenzugs.com/2017/10/16/puppeteer-headless-chrome-in-a-container/

https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md#running-puppeteer-in-docker

https://dev.to/ikeryo1182/constracting-puppeteer-environment-with-vagrant-and-docker-5ano

***

## Resources:

Book: [Docker in Practice](https://www.manning.com/books/docker-in-practice-second-edition?a_aid=zwischenzugs&a_bid=550032fc)

Article: [How to Dockerize your End-to-End acceptance tests](https://medium.freecodecamp.org/how-to-dockerize-your-end-to-end-acceptance-tests-dbb593acb8e0)

Quora: [What is docker?](https://www.quora.com/qemail/track_click?al_imp=eyJ0eXBlIjogMzMsICJoYXNoIjogIjB8MTB8MXw2NDc2NDgyMCJ9&al_pri=ReadMoreLinkClickthrough&aoid=1EjNS7gFO2a&aoty=1&aty=4&click_pos=10&ct=1544738197431220&et=130&id=3db5a8fb14274d369619d549556aad9f&source=7&src=1&st=1544738197547871&stories=1_m5m85t9ONMK%7C1_ROMquNe97oK%7C1_qJ3zFPQjWCi%7C1_duVMKaAMwH1%7C1_LAjfv22RpYB%7C1_alUBLFEQmA8%7C1_V7JcvVDQTJi%7C1_IdWComB7OKu%7C1_VTSGzAkbwc2%7C1_1EjNS7gFO2a&ty=1&ty_data=1EjNS7gFO2a&uid=YsTkMQnEFdZ&v=0)

Docker Learning Series:

[Docker Series — What is Docker?](https://medium.com/pintail-labs/docker-series-what-is-docker-9eddca88f434)

[Docker Series — Starting your first container](https://medium.com/pintail-labs/docker-series-starting-your-first-container-92dfd1dc859)

[Docker Series — Creating your first Dockerfile](https://medium.com/pintail-labs/docker-series-creating-your-first-dockerfile-573bfea4991)

[Docker Series — Building your first Docker image](https://medium.com/pintail-labs/docker-series-building-your-first-image-8a6f051ae637)

[Docker Series — Moving past one container with Docker Compose](https://medium.com/pintail-labs/docker-series-moving-past-one-container-bf32b45831d3)

[Docker Series — Cheat Sheet](https://medium.com/pintail-labs/docker-series-cheat-sheet-e1841961c61)

