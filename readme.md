# Docker Static Website - CI Practice

This project is a simple static website served using **Nginx** inside a Docker container.

The purpose of this repository is to practice:

- Writing a Dockerfile
- Using Docker Compose
- Creating a CI pipeline with GitHub Actions
- Running a basic smoke test
- Pushing Docker images to a registry

---

## 🐳 Dockerfile

The application uses the official `nginx` image as a base and copies `index.html` into the default nginx web directory.

Build locally:

```bash
docker build -t my-website .
docker run -p 8080:80 my-website






** Docker Compose **

The project also includes a compose.yaml file with:

Web service (nginx static site)

PostgreSQL database (for learning purposes)

Named volume for database persistence

Run:

docker compose up --build


** CI Pipeline (GitHub Actions) **

The CI pipeline automatically runs on:

Push to main

Pull requests

Pipeline steps:

Checkout repository

Build Docker image

Run container

Perform smoke test using curl

Stop container

The smoke test verifies that the container starts correctly and responds on port 80.


** Learning Goals **

This project focuses on understanding:

Containerization

Image building

Port mapping

Named volumes

Basic CI automation

Smoke testing

This is a learning project created for DevOps elective Week 05.