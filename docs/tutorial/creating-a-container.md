---
title: Step 2. Creating a container definition with Docker Compose
---

In Docker Compose, a container configuration is defined in a file called `docker-compose.yml`.

1. In the `node-dev` directory, create a file named `docker-compose.yml` with the following content:
```yaml
version: '3'
services:  
  dev:
    image: node:20
    volumes:
      - ./apps:/home/app
    working_dir: /home/app
    ports:
      - 3000:80
    command: >
      bash -c "npm i &&
      npm i -g nodemon &&
      nodemon -L server.js localhost 80"
```
Let's examine the structure of `docker-compose.yml`:
- `version`: Version of Docker Compose.
- `services`: List of containers.
   - `dev`: Name of our container.
      - `image`: Image used to start the container.
      - `volumes`: Mounting point of a local directory (`./apps`) into a container directory (`/home/app`). 
      - `working_dir`: Working directory inside the container.
      - `ports`: Mapping of a local port (3000) to a container port (80).
      - `command`: Commands that are executed when the container is launched. In our case, these commands install all dependencies and start the server.