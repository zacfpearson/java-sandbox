# SpringRabbitmq

## Overview
The purpsose of spring-rabbitmq is to learn how to use rabbitmq and java with docker. 

## Install Dependencies
Install docker

## Network 
Run `docker network create -d bridge java-rabbitmq-bridge`

## Build
From this directory run: `docker build -t java-rabbitmq-client:dev -f docker/Dockerfile app`

## Start Rabbitmq Server

This app depends on a rabbitmq server running on the same bridge network with the resovable hostname rabbitmq-server. The easiest way to get rabbitmq up and running is with their Docker image. 
`docker run --network=java-rabbitmq-bridge --name=rabbitmq-server --rm rabbitmq:alpine`

## Run

Run: `docker run --network=java-rabbitmq-bridge -t java-rabbitmq-client:dev`