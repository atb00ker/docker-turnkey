# FreeRDP

[![Version](https://img.shields.io/badge/Version-2.0.0--dev-success)](#)
[![GitHub](https://img.shields.io/badge/Github-turnkey-success)](https://github.com/atb00ker/docker-turnkey/tree/master/freerdp)
[![Dockerhub](https://img.shields.io/badge/docker--hub-turnkey-blue)](https://hub.docker.com/repository/docker/atb00ker/docker-turnkey)
[![Pull](https://img.shields.io/badge/Pull-atb00ker/docker--turnkey:freerdp-blue)](#)

FreeRDP: http://www.freerdp.com/

### Usage

1. Allow connection to the X server: `xhost local:root`

2. Run the container:

```bash
docker run --rm --name freerdp \
           --volume /tmp/.X11-unix:/tmp/.X11-unix \
           --env DISPLAY=unix$DISPLAY \
           atb00ker/docker-turnkey:freerdp \
           /cert-ignore /u:'username' /p:'password' /v:'<address>:<port>'
```

### Build

```bash
docker build --file $PWD/freerdp/Dockerfile $PWD/freerdp \
             --tag atb00ker/docker-turnkey:freerdp
```
