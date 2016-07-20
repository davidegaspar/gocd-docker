# gocd-docker

run gocd with docker containers

## server

base server from public repo

## agents

- java
- nodejs
- java-nodejs

#### build

```
cd nodejs
docker build -t local/gocd-agent-nodejs .
```

## volumes

- lib - gocd binaries
- config - gocd config files
- logs - gocd logs
- home - gocd home

#### create volumes

```
docker volume create --name=home
```

#### access volumes

you can add files to these volumes by spinning up a container with -v

```
docker exec -it server /bin/bash
```
