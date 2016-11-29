# Automatic Redirects for HTTP requests

[![Docker Stars](https://img.shields.io/docker/stars/foxylion/nginx-https-redirect.svg?style=flat-square)](https://hub.docker.com/r/foxylion/nginx-https-redirect/) [![Docker Pulls](https://img.shields.io/docker/pulls/foxylion/nginx-https-redirect.svg?style=flat-square)](https://hub.docker.com/r/foxylion/nginx-https-redirect/)

A minimal nginx which redirects all requests to the https version.

Can be used for example to redirect all plain requests of an Amazon ELB to the HTTPS port.

## Usage

Without a Docker Swarm:
```
docker run -d --name proxy-redirect -p 80:80 foxylion/nginx-https-redirect
```

In a Docker Swarm:
```
docker service create  --name proxy-redirect -p 80:80 --replicas 2 foxylion/nginx-https-redirect
```
