---
layout: post
title:  "[mac] Docker & NodeJS"
date:   2021-11-02 09:00:00 +0900
category: mac
---

## rosetta 다운로드
```bash
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```


## 도커 다운로드
[Docker Desktop – Mac with Apple chip](https://docs.docker.com/desktop/mac/apple-silicon)


## 도커 셋업
```bash
docker pull node:14.17.6
docker images
```

```bash
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE  
node         14.17.6   8beedd044dbc   2 weeks ago   891MB
```

```bash
docker run -d -it --name node_14_17_6 -v /Users/joyplug/Documents/Project/docker/node_14_17_6:/app node:14.17.6
docker ps -a
```

```bash
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS          PORTS     NAMES
b5c97eb3507b   node:14.17.6   "docker-entrypoint.s…"   About a minute ago   Up 58 seconds             node_14_17_6
```

```bash
docker exec -it node_14_17_6 /bin/bash
docker commit node_14_17_6 node_14_17_6:0.0.1
docker images
```

```bash
REPOSITORY     TAG       IMAGE ID       CREATED          SIZE
node_14_17_6   0.0.1     3a9f19bebb20   20 seconds ago   891MB
node           14.17.6   8beedd044dbc   2 weeks ago      891MB
```

```bash
docker stop node_14_17_6
docker ps -a
```

```bash
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                       PORTS     NAMES
b5c97eb3507b   node:14.17.6   "docker-entrypoint.s…"   11 minutes ago   Exited (137) 4 seconds ago             node_14_17_6
```

## 컨테이너 삭제 및 커밋버전 실행
```bash
docker rm node_14_17_6
docker ps -a
docker images

docker run -d -it --name node_18_12_1_001 -v /Users/joyplug/Desktop/Project/docker/node_18_12_1:/app node_18_12_1:001
docker exec -it node_18_12_1_001 /bin/bash
```
