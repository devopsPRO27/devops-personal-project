# DevOps Assignment with Jenkins Pipeline

This assignment outlines the steps to create a Jenkins pipeline that automates the following tasks:

1. Clone the code from a Git repository.
2. Build a Dockerfile
3. and now build a jenkinsfile to perfum those steps:
- clone the code [checkout]
- build the docker image [build]
- run a bashscript to check if the image built successfully [test] 
- push the image to docker hub [push]

## Prerequisites

- Jenkins installed and configured
- Docker installed on the Jenkins server
- Terraform installed on the Jenkins server
- A DockerHub account (or another container registry)
- A Git repository containing the application code
