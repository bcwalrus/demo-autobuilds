## Nginx Dockerfile

This repository contains the dockerfile of [Nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Usage

    docker run -d -p 80:80 <repo>

#### Attach persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/conf.d -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www/html <repo>

After few seconds, open `http://<host>` to see the welcome page.
