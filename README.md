# Descomplicando o docker - linuxtips

> Esse repositório é um agregado de anotações do curso descomplicando o docker da linuxtips

## docker basic commands:

```bash
# Shows docker version
docker version 

# Shows containers in execution
docker container ls

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

# Stop an container
docker container stop CONTAINER_ID

# Start an container
docker container start CONTAINER_ID

# Restart an container
docker container restart CONTAINER_ID
```

## Example:

```bash
docker container run hello-world
```
