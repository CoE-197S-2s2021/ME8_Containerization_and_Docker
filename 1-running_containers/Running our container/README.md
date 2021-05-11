# Exercise 1: Running Our Container

1. Running `docker run`

<img src="1 - hello world.png" alt="1">

2. Cheking the containers after running `docker run`

* Running `docker ps` and `docker ps -a`

<img src="2 - check running containers.png" alt="2">

3. Running the `/bin/bash` command

* Running `docker run ubuntu:16.04 /bin/bash` then `docker run -it ubuntu:16.04 /bin/bash`

<img src="3 - docker :bin:bash.png" alt="3">

4. Running indetached mode

* Running `docker run -d ubuntu:16.04 /bin/sleep 3600` and checking if it's running the sleep command in a new container.

<img src="4 - docker :bin:sleep 3600.png" alt="4">

5. Reattaching to the container.

* Running `docker exec -it be7 /bin/bash` then `ps aux`

<img src="5.png" alt="5">

6. Stopping the Docker container.

* Running `docker stop afc`

<img src="6 - kill -9.png" alt="6">

7. Removing the containers

* Running `docker rm afc2` and `docker rm $(docker ps -a -q)` to remove the remaining containers

<img src="7 - remove all docker images.png" alt="7">

