# Ping Server

## Build Docker image

```sh
$ docker build -t ping-server .
```

## Run Docker container

```sh
$ docker run -p 300:3000 ping-server
```

## Test Docker container

```sh
$ curl http://localhost:3000/ping
```
