
## Dockerfile and .dockerignore

This is a demo dockerfile.
```
FROM node:latest
WORKDIR /app
RUN npm i
COPY . .
EXPOSE 3500
CMD ['npm','run','dev']

```

This is a demo dockerignore

```
*.txt
node_modules
```


## Important Docker Commands

- *To show all running and stopped containers*

```
docker container ps -all
```

- *To show all images in DockerHub*

```
docker image ls -all
```

- *To remove all unused images, networks and containers*

```
docker system prune
```

- *To stop a running container*
```
docker stop <container_name>
```

- *Show logs of a container*
```
docker logs <container_name>
```

- *Run a docker container with special permission required*
```
docker run --name <container_name> -e POSTGRES_PASSWORD=mysecretepassword -d postgres
```

- *Remove a container forcefully(running container)*

```
docker container rm <container_name> -f
```

- *Remove a image*

```
docker image rm <image_name>
```

- *Inspect changes in container*

```
docker diff <container_name/id>
```
