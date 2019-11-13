# Purpose
Run a web server in a container which displays its hostname and a NICKNAME
environment variable

# Requirement
* Docker

# Usage
I wrote a Makefile to handle the life cycle of images and containers, the
syntax is as follows:

## Getting Help
    $ make help

## Building the image
    $ make build

## Running the container
    $ make run

## Getting a shell access into the running container
    $ make shell

## Pushing the image to DockerHub
    $ make push

## Stopping the container
    $ make stop

## Removing the image
    $ make clean
