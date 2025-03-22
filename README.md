# ping-server

It's an simple HTTP server to return a "pong" message.

## Running the server in local via Docker

1. Create the Docker image from Dockerfile

```sh
$ docker build -t ping-server .
```

2. Run the Docker container based on the image with the name ping-server

```sh
$ docker run -d -p 3000:3000 --name ping-server ping-server
```

3. Test the application

```
$ curl http://localhost:3000
pong
```

## Deploy the application in linux server

### From local

1. Create the Docker image for linux

```sh
$ docker build --platform linux/amd64 -t philiplambok/ping-server .
```

2. Push the Docker image to Docker Hub

```sh
$ docker push philiplambok/ping-server
```

### From server

1. Pull the Docker image from Docker Hub

```sh
$ docker pull philiplambok/ping-server
```

2. Run the Docker container based on the image with the name ping-server

```sh
$ docker run -d -p 3000:3000 --name ping-server philiplambok/ping-server
```
