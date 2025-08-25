# DevOps-Projects
Repo for all DevOps projects. 

## Project-1: Building To-Do List in Python, Dockerize and Deploy in GKE
- Develop and test the application in Python.
- Build the application to Image using Docker.
- Make sure the application runs as a container in Docker. 
- Push the Image in Docker Hub.
- Deploy the Image in a GKE cluster and expose it externally.

## Project-2: Build, Push and Deploy the same To-Do List using GitHub Acitons
With GitHib Actions workflow, automated the deployment of the To-do List app:
- **First Job:** Build a Docker image of the code, and push it to Docker Hub
- **Second Job:** Test the image using docker before deploying it to a K8 cluster.
- **Third Job:** Deploy to GKE.