# Remote Falcon Developer Documentation

- [Purpose of this Documentation](#purpose-of-this-documentation)
- [Methods of Running Remote Falcon](#methods-of-running-remote-falcon)
  - [Docker Compose](#docker-compose)
  - [Spring Boot](#spring-boot)

## Purpose of this Documentation
The intended purpose of this documentation (and entire repo) is to provide details on how to get Remote Falcon running on a local machine or in a cloud environment.

## Methods of Running Remote Falcon

### Docker Compose
At the moment, the only documented way of running Remote Falcon is via a [docker-compose.yaml](https://github.com/Remote-Falcon/developer-docs/blob/main/docker-compose.yaml) file. But, believe it or not, this is actually all you need to get Remote Falcon running locally. To use this method you'll need to have a valid Docker environment configured. Downloading [Docker Desktop](https://www.docker.com/products/docker-desktop/) is the easiest way to do that. Once you have Docker set up, you can open a terminal, navigate to the location of the docker-compose.yaml file, and run `docker compose up`. It really is that easy!

### Spring Boot
THis method requires pulling down each repo and running it via Spring Boot. This is a lot more work and is really only valuable if you're doing actual development. I'll document these steps at a later time.
