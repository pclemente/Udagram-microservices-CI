# Udagram Image Filtering Microservice

Repo link: https://github.com/pclemente/Udagram-microservices-CI/

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:
1. [The Simple Frontend](/udacity-c3-frontend)
A basic Ionic client web application which consumes the RestAPI Backend.
2. [The RestAPI Feed Backend](/udacity-c3-restapi-feed), a Node-Express feed microservice.
3. [The RestAPI User Backend](/udacity-c3-restapi-user), a Node-Express user microservice.

## Docker Install

You can Install with Docker by adding the different parts, or directly using the Docker compose script in (/docker) using

```bash
docker-compose -p CP -f docker-compose.yml up -d
```

Docker images can be obtained from https://hub.docker.com/u/pclementeperez

## kubernetes

The Kubernetes cluster can be run by applying the following commands in the docker/k8s folder

```bash
kubectl apply -f backend-feed-deployment.yaml
kubectl apply -f backend-user-deployment.yaml
kubectl apply -f frontend-deployment.yaml
kubectl apply -f reverseproxy-deployment.yaml
```

## Secrets

Please make sure to provide the secrets the App requires,
POSTGRESS_USERNAME=ADDYOUROWN
POSTGRESS_PASSWORD=ADDYOUROWN
POSTGRESS_DB=ADDYOUROWN
POSTGRESS_HOST=ADDYOUROWN
AWS_REGION=ADDYOUROWN
AWS_PROFILE=ADDYOUROWN
AWS_BUCKET=ADDYOUROWN
JWT_SECRET=ADDYOUROWN
