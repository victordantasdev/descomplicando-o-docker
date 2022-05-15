# Descomplicando o docker - linuxtips

> Esse repositório é um agregado de anotações do curso descomplicando o docker da linuxtips

## docker basic commands:

```bash
# Shows docker version
docker version 

# Shows containers in execution
docker container ls

# Shows containers images
docker image ls

# Kill an running container
docker container rm -f CONTAINER_ID

# Remove an container
docker container rm CONTAINER_ID

# Shows all containers
docker container ls -a

# Runs an container
docker container run

# Runs an container with an interactive terminal
# Tip: To exit a container without kill the process press Ctrl+p+q
docker container run -ti ubuntu

# Connect to an running container
docker container attach CONTAINER_ID

# Runs an container as daemon
docker container -d nginx

# Connect to an running container as daemon
docker container exec -ti CONTAINER_ID bash

# To stop an container
docker container stop CONTAINER_ID

# To start an container
docker container start CONTAINER_ID

# To restart an container
docker container restart CONTAINER_ID

# To pause an container
docker container pause CONTAINER_ID

# To unpause an container
docker container unpause CONTAINER_ID

# To get infos about an container
docker container inspect CONTAINER_ID

# To get container logs
docker container logs -f CONTAINER_ID

# To get container stats
docker container stats CONTAINER_ID
docker container top CONTAINER_ID
```

## Control container resources

```bash
# To limit memory
docker container run -d -m 128M nginx

# To limit cpu
docker container run -d --cpus 0.5 nginx

# To update container usage
docker container update --cpus 0.2 CONTAINER_ID
```

## Example:

```bash
docker container run hello-world
```

## Dockerimage

```bash
# To build docker image
docker image build -t IMAGE_NAME:IMAGE_VERSION DOCKER_IMAGE_PATH
```

## Volumes

```bash
# To mount an volume of type bind in container
docker container run -ti --mount type=bind,src=PATH_IN_YOUR_MACHINE,dst=PATH_ON_CONTAINER debian


# To mount an volume of type bind in container (read only)
docker container run -ti --mount type=bind,src=PATH_IN_YOUR_MACHINE,dst=PATH_ON_CONTAINER,ro debian

# To list all volumes
docker volume ls

# To create a volume
docker volume create VOLUME_NAME

# To inspect some volume
docker volume inspect VOLUME_NAME 

# To mount an volume of type volume in container
docker container run -ti --mount type=volume,src=VOLUME_NAME,dst=PATH_ON_CONTAINER debian
```




