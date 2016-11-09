# docker-consul-template
Dockerfile for consul-template Docker image based on Alpine

Small Docker image (20MB) for running a containerized [Consul Template](https://github.com/hashicorp/consul-template).

Built this container:

```
docker build --rm -t consul-template:latest ./
```

Run this container and mount a local directory for templates:

```
docker run -d -v /path/to/local/dir:/data consul-template:latest
```
