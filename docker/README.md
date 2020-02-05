# LLVM in docker container

## Build and Run
build and run a container on a host in this directory
```
$ docker-compose build
$ docker-compose up -d
```

connect to the container via VSCode or
attach to the container via terminal application as follows
```
$ docker ps
CONTAINER ID    NAMES
012345          docker_llvm_template_1
$ docker attach CONTAINER_ID_or_NAME
```

## Attach

If you exit the container after attaching, it must stop.
So, dettach container using the CTRL-p CTRL-q key sequence
if you want to keep the container running.

host's directory will be mounted in /hostos directory of the cointainer.
see the volumes entry in docker-compose.yml
```
# cd /hostos
# ls
LICENSE    README.md  docker/    src/
# cd src
# clang++ main.cpp
# ./a.out
hello world!
```

## Stop and Remove

stop and remove the container on the host
```
$ docker-compose stop
$ docker-compose rm
```
