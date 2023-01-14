This repo contains the Dockerfile and instruction that produced vardyng/azure-cli:latest image.

### Build image
```sh
docker buildx create --name mybuilder mybuilder
```
```sh
docker buildx use mybuilder
```
```sh
TAG=latest
IMAGE=vardyng/azure-cli
```
```sh
docker buildx build \
--push \
--platform linux/arm/v7,linux/arm64/v8,linux/amd64 \
--tag $IMAGE:$TAG .
```