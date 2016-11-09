# docker-consul-template
Dockerfile for consul-template Docker image based on Alpine

Small Docker image (20MB) for running a containerized [Consul Template](https://github.com/hashicorp/consul-template).

Built this container:

```
docker build --rm -t consul-template:latest ./
```

This docker image can be used like the `consul-template` binary itself. Any cli arguments can be added. Just make sure that you mount your local folder containing your templates as `/data` into this container like so:

```
docker run -d -v /path/to/local/dir:/data consul-template:latest -consul 127.0.0.1:8500 -template "/tmp/template.ctmpl:/var/www/nginx.conf"
```

If you need to interact with other services (e.g. restart after config change) you have to find a way to do this from inside the container. 
