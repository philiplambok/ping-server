# ping-server

## How to run with Docker

1. Build the image

  ```sh
  docker build -t ping-server .
  ```

2. Run the container

  ```sh
  docker run -p 3000:3000 ping-server
  ```

3. Test the container

  ```sh
  curl http://localhost:3000/ping
  ```
