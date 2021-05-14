# Exercise 3: Building images

1. Deleting the old Docker image from the previous activity

* Running `docker rmi f7b`

<img src="1 - remove old images.png" alt="1">

2. Building the Dockerfile

```dockerfile
    FROM ubuntu:16.04
    LABEL author="Joie Llantero"

    ENV PING_TARGET "google.com"

    RUN apt-get update \
        && apt-get install -y iputils-ping \
        && apt-get clean \
        && cd /var/lib/apt/lists && rm -fr *Release* *Sources* *Packages* \
        && truncate -s 0 /var/log/*log

    CMD ["sh", "-c", "ping $PING_TARGET"]
```

3. Running the Dockerfile to build the image

* Running `docker build -t 'root/ping'

<img src="2 - docker build.png" alt="2">

* Checking the docker images

<img src="3 - check images.png" alt="3">

4. Optimizing the Dockerfile

* Adding `apt-get clean` to the Dockerfile

<img src="4 - apt get clean.png" alt="4">

* Running the new optimized Dockerfile

<img src="5 - optimized dockerfile.png" alt="5">

5. Running ping using the dockerfile

* Running `docker run -it root/ping`

<img src="6 - docker run.png" alt="6">