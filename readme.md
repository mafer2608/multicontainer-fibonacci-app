## 1. BUILD AND DEPLOY IN DEV ENVIRONMENT

* run containers with docker-compose
docker-compose up

* run the container but builds the images
docker-compose up --build

## 2. BUILD AND DEPLOY IN DEV ENVIRONMENT

- Push code to github.
- Travis automatically pulls repo.
- Travis builds a test image, test code.
- Travis builds prod images.
- Travis pushes built prod images to Docker Hub.
- Travis pushes project to AWS EB.
- EB pulls images from Docker Hub, deploys.
  