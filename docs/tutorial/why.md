---
title: Why use Docker Compose for development?
---

One way to create a container is by using a container image. An image is a template that defines a container.

However, images typically define containers used in production. They are not supposed to contain development-related commands, so for our environment this is not ideal.

Instead, we will create and run our container using Docker Compose, which is the Docker's native tool for managing multi-container applications without creating an image.