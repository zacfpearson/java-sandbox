# SpringRedis

## Overview
The purpsose of spring-redis is to learn how to use redis and java with docker. 

## Install Dependencies
Install docker

## Network 
Run `docker network create -d bridge java-redis-bridge`

## Build
From this directory run: `docker build -t java-redis-client:dev -f docker/Dockerfile app`

## Start Redis Message Broker

This app depends on a redis server running on the same bridge network with the resovable hostname redis-broker. The easiest way to get redis up and running is with their Docker image. 
`docker run --network=java-redis-bridge --name=redis-broker --rm redis:alpine`

## Run

Run: `docker run --network=java-redis-bridge -t java-redis-client:dev `