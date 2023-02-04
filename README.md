# Food Order API

[![Black Code Style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

- [Link to API Documentation](https://documenter.getpostman.com/view/15138887/2s935oKijy)

![Screenshot](doc.png?raw=true "API DOC")

## Overview

Food Order API is a single endpoint for placing bulk orders to [nourish.me](https://nourish.me) API, a mock api.

## Prerequisites

To run this project, you will need to have the following installed:

- [Python 3.10](https://python.org): Base programming language for development
- [Flask](https://flask.palletsprojects.com/en/2.0.x/): Development framework used for the application
- [Celery](https://github.com/celery/celery): A simple, flexible, and reliable distributed system to process vast amounts of tasks
- [Redis](https://github.com/redis/redis-py): A NoSQL Database that serves as Cache, Celery Broker and Result Backend
- [Docker Engine and Docker Compose](https://www.docker.com/) : Containerization of the application and services orchestration

## Installation

- create a .env file with the variables in the .env.example file
  - `cp env.example .env`

- Run `make build`

  - Running the above command for the first time will download all docker-images and third party packages needed for the app.
  - **NB: This will take several minutes for the first build**

- Run `make up`

  - Running the above command will Start up the application and all the services needed for the app to run.

- Run `make down` to stop the servers

- Run `make test` to run tests

- Other commands can be found in the Makefile

## Exploring The App

Make sure that all the above servers are running before you start exploring the project.

- The API is accessible at `http://localhost:8000/v1/orders`
