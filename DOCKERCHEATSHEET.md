Sign in to Docker

```sh
docker login
```

Build Docker

```sh
docker build -t jgking2/node-web-app .

#Maps docker port 8080 -> machine port 49160
docker run -p 49160:8080 -d jgking2/node-web-app
```

### Managing repo

```sh
docker push $DOCKER_USER_ID/node-web-app

docker pull $DOCKER_USER_ID/node-web-app

```

```sh
#Gets the running processes, used to get container id
docker ps

#View logs with
docker logs $CONTAINER_ID
```
