# Exercise 1: Pulling an image

1. Running `docker images`

<img src="1 - docker images.png" alt="1">

2. Pulling from Dockerhub

* Running `docker search ubuntu`

<img src="2.1 - docker search.png" alt="2.1">

* Running `docker pull ubuntu:16.04`

<img src="2.2 - docker pull.png" alt="2.2">

3. Pulling different versions on the same image

* Running `docker pull ubuntu:16.10`

<img src="3 - docker images.png" alt="3">

4. Removing unwanted images

* Running `docker rmi <IMAGE ID>`

<img src="4.1 - delete image.png" alt="4.1">

* Running `docker images` should reflect the deleted image.

<img src="4.2 - recheck images.png" alt="4.2">