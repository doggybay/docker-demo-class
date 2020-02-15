# Docker Demo

## Docker
---
Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. 
A container is a box that contains all the dependencies an application would need to run quickly and reliably. This would allow the application to move from one computing environment to another.

## `Dockerfile`
---
  
A `Dockerfile` is a set of instructions passed to build and image.
To create a `Dockerfile` we simply create a file in the root of our directory and name it `Dockerfile`.
`Dockerfile.example` can serve as a template.

We also want to create a .dockerignore file to avoid docker coping unnecessary files. Same concept at a `.gitignore`.

## `docker-compose.yml`
---
A `docker-compose.yml` file allows a developer to launch multiple containers that are related to one another.


## Commands
---
### Build Image
---
- docker build -t [tag name] .
  > `docker build -t docker-demo-server .`
- docker images
- docker run -p [host port]:[container port] -d [image tag]
  > `docker run -p 8000:8000 -d docker-demo-server`
### View logs
---
- docker ps
- docker logs [container id]
### Enter a container
- docker exec -it [container id] [entry point to app]
  > `docker exec -it docker-demo-server /bin/bash`
### Pull Image
---
- docker pull [image name]
  > `docker pull postgres`
- docker run [image name]
  > `docker run --rm   --name pg-docker -e POSTGRES_PASSWORD=example -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data  postgres`
- docker stop [image name]
  > `docker stop postgres`
### Image Management
---
- docker images
- docker image rm [image name]
  > `docker image rm postgres`
### Container Management
---
- docker container list [--all opt flag]
- docker rm [container name]
  > `docker rm docker-demo-server`
- docker ps

