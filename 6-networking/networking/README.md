# Exercise 6: Networking

1. Default `bridge` network

    <img src="1 - bridge.png" alt="1">

* Running `docker run --rm -d --name dummy root/ping:latest` and `docker network inspect bridge`

    <img src="2 - run ping.png" alt="2">

* Running `docker run --rm -d -e PING_TARGET=172.17.0.2 --name pinger root/ping:latest` and `docker ps`

    <img src="3 -  add another ping container.png" alt="3">

* Running `docker run --rm -d -e PING_TARGET=dummy --name pinger root/ping:latest`

    <img src="4 - dummy.png" alt="4">

2. Managing custom networks

* Running `docker network create skynet`

    <img src="5 - skynet.png" alt="5">

3. Adding containers to a network

    <img src="6 - adding containers.png" alt="6">

4. Connecting between containers in a network 

* Running `docker run --rm -d --name widgetdb --network skynet -p 5432 postgres`

    <img src="7 - widgetdb.png" alt="7">

* Running `docker run --rm -d --name gadgetdb --network skynet -p 5432 postgres`

    <img src="8 - gadgetdb.png" alt="8">

5. Building ports to the host

    <img src="9 - gadgetdb widgetdb.png" alt="9">

    <img src="10 - access.png" alt="10">