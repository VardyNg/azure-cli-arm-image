This repo contains the Dockerfile and instruction that produced vardyng/azure-cli:latest image.

### Build image
```sh
docker buildx create --name mybuilder mybuilder
```
```sh
docker buildx use mybuilder
```
```sh
docker buildx build \
  --load \
  --platform linux/arm64/v8 \
  -t vardyng/azure-cli:latest .
```

### Push image to Docker Hub
```sh
docker push vardyng/azure-cli:latest
```