# ping-server

## How to run with Docker

1. Build the image

  ```sh
  docker build -t philiplambok/ping-server .
  ```

2. Run the container

  ```sh
  docker run -d -p 3000:3000 philiplambok/ping-server
  ```

3. Test the container

  ```sh
  curl http://localhost:3000/
  ```

4. Stop the container

  ```sh
  docker stop ping-server
  ```

5. Upload the image to Docker Hub with version tag

  ```sh
  docker push philiplambok/ping-server
  ```

6. In production server, SSH into the server and run the following commands:

  ```sh
  docker pull philiplambok/ping-server
  docker run -d --name ping-server -p 3000:3000 philiplambok/ping-server
  ```
