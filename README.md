# Dockerized Apache Web Server Deployment

## Project Description

This project demonstrates how to deploy an Apache web server inside a Docker container.

## Technologies

- Docker
- Ubuntu
- Apache2
- HTML
- AWS EC2

## Build

docker build -t webserver .

## Run

docker run -d -p 8080:80 webserver

## Test

curl http://localhost:8080

## Port Mapping

EC2 Host Port 8080 → Container Port 80