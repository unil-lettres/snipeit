# Introduction

Docker configuration for the [Snipe-IT](https://snipeitapp.com/) application.

# Development with Docker

## Docker installation

A working [Docker](https://docs.docker.com/engine/install/) installation is mandatory.

## Docker environment file

Please make sure to copy & rename the **example.env** file to **.env**.

``cp example.env .env``

You can replace the values if needed, but the default ones should work for local development.

## Build & run

Build & run all the containers for this project.

``docker-compose up`` (add -d if you want to run in the background and silence the logs)

## Frontends

To access the main application please use the following link.

[http://127.0.0.1:8000](http://127.0.0.1:8000)

# Deployment with Docker

Copy and rename the environment file.

``cp example.env .env``

You should replace the values since the default ones are not ready for production.

Please also make sure to copy & rename the **docker-compose.override.yml.prod** file to **docker-compose.override.yml**.

`cp docker-compose.override.yml.prod docker-compose.override.yml`

You can replace the values if needed, but the default ones should work for production.

Build & run all the containers for this project:

`docker-compose up -d`

Use a reverse proxy configuration to map the url to port `8000`.

# Helm

The Helm charts for this project are available at [https://github.com/unil-lettres/k8s](https://github.com/unil-lettres/k8s), in the ``elett`` directory.
