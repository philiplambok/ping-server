# Ping Server

A simple HTTP server that responds with "pong" when you ping it.

## Getting Started Locally

### What You'll Need:
- Docker installed on your computer

### Steps:

1. **Build the Docker image:**
   ```
   docker build -t ping-server .
   ```

2. **Start the server:**
   ```
   docker run -d -p 3000:3000 --name ping-server ping-server
   ```

3. **Test it works:**
   ```
   curl http://localhost:3000
   ```
   You should see: `pong`

## Deploying to a Server

### From Your Computer:

1. **Create a version that works on Linux servers:**
   ```
   docker build --platform linux/amd64 -t yourname/ping-server .
   ```

2. **Share it online:**
   ```
   docker push yourname/ping-server
   ```

### On Your Server:

1. **Download the image:**
   ```
   docker pull yourname/ping-server
   ```

2. **Start the server:**
   ```
   docker run -d -p 3000:3000 --name ping-server yourname/ping-server
   ```

3. **Test it works:**
   ```
   curl http://your-server-address
   ```
   You should see: `pong`
