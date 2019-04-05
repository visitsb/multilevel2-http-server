# multilevel2-http-server
Dockerized container for [multilevel2-http](https://github.com/visitsb/multilevel2-http)

# How to use
Here is an example docker service definition for compose
```
version: '3.7'

services:
  ...
  multilevel2-http-server:
    image: visitsb/multilevel2-http-server
    volumes:
      - /root/data/multilevel2-http-server:/db
    environment:
      - NODE_ENV=production
      - USER=test
      - PASSWORD=test
```

Available environment variables (with defaults) are ones below-
```
ENV NODE_ENV production
ENV DEBUG multilevel2-http/server
ENV HOST 0.0.0.0
ENV PORT 80
ENV USER admin
ENV PASSWORD test
ENV DB /db
```

# Docker Hub
The image is available on docker hub as [visitsb/multilevel2-http-server](https://hub.docker.com/r/visitsb/multilevel2-http-server).