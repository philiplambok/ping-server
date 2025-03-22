# ping-server

It's an simple HTTP server to return a "pong" message.

## Running the server in local via Docker

1. Create the Docker image from Dockerfile

```sh
$ docker build -t ping-server .
```

2. Run the Docker container based on the image

```sh
$ docker run -p 8080:8080 ping-server
```

3. Test the application

```
$ curl http://localhost:8080
pong
```
