# DevOps Assignment with Jenkins Pipeline

This assignment outlines the steps to create a Jenkins pipeline that automates the following tasks:

1. Clone the code from a Git repository.
2. Build a Dockerfile
3. Build a Docker image.
3. Push the Docker image to DockerHub (or another container registry).
4. Run a Terraform file to start a new EC2 instance and deploy the Docker container.
5. Test that the container is running and functioning correctly using two `curl -X` commands in a Bash script.

## Prerequisites

- Jenkins installed and configured
- Docker installed on the Jenkins server
- Terraform installed on the Jenkins server
- AWS CLI configured with appropriate permissions
- A DockerHub account (or another container registry)
- A Git repository containing the application code

## Pipeline Steps

```groovy
pipeline {
    agent any

    environment {
        DOCKERHUB_CREDENTIALS = credentials('dockerhub-credentials-id')
    ...............
    ...............
    .jenkins code .
    ...............
    ...............
    post {
        always {
            cleanWs()
        }
    }
}
