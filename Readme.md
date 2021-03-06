[![Build Status](https://travis-ci.org/maxnus/eureka-server-docker.svg?branch=master)](https://travis-ci.org/maxnus/eureka-server-docker)

## Introduction
This is a Java based container image running Eureka service discovery server

### Versioning
| Docker Tag | GitHub Release | Eureka Version | Java Version |
|-----|-------|--------|--------|
| latest | master | 1.4.2.RELEASE | openjdk-8-jdk-alpine |

## Building from source
To build from source you need to clone the git repo and run maven build:
```
$ git clone https://github.com/maxnus/eureka-server-docker.git
```

followed by
```
$ sh mvnw clean package docker:build ( or mvnw.cmd clean package docker:build for Windows )
```

## Pulling from Docker Hub
```
$ docker pull dmakeroam/discovery-server-eureka:latest
```

## Running
To run the container:
```
$ docker run -p 8761:8761 -d dmakeroam/discovery-server-eureka:latest
```

## Docker-Compose Example

```
version: '3'

services:
    discovery-server:
        restart: always
        image: dmakeroam/discovery-server-eureka:latest
        ports:
        - "8761:8761"
```
