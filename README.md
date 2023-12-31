# Dockerized MERN Application with AKS Deployment

This project focuses on containerizing a MERN (MongoDB, Express.js, React, Node.js) application using Docker. Additionally, it includes a docker-compose setup for connecting the backend, frontend, and MongoDB containers.

## Quick Start

Clone the repository and run the following command to set up the containers: `make`

## Containerization Details

The project includes Dockerfiles for both the frontend and backend components, along with a docker-compose file to orchestrate the containers. MongoDB docker image retrieved from Docker Hub and linked with backend container using docker-compose.

## AKS Deployment

The application was deployed on Azure Kubernetes Service (AKS). Three pods were created for the backend, frontend, and MongoDB, each associated with their respective services. Nginx was employed to make the Express API accessible from outside the Kubernetes cluster. Check out the [demo](https://drive.google.com/file/d/1JLIibXXAJDI1RMO8rL-QgrRuA3qrX0S-/view?usp=sharing).

## CI/CD with Azure DevOps

Azure DevOps was utilized to establish a comprehensive CI/CD pipeline, automating the build and deployment processes. The containers are deployed to AKS as part of this pipeline. Explore the [demo](https://drive.google.com/file/d/1DlhI39iWF8_WjnV8wD7OUD8Xh7SLbps3/view?usp=sharing) for a visual walkthrough.

## Project Structure

- **backend/:** Backend application code and Dockerfile.
- **frontend/:** Frontend application code and Dockerfile.
- **docker-compose.yml:** Docker-compose configuration for connecting containers.
- **azure-pipeline.yml:** Azure DevOps pipeline configuration file.
- **Makefile:** Makefile with a startup command for easy setup.

## Clean Up

To stop and remove the containers, run: `make clean`

## Demo Videos

- [AKS Deployment](https://drive.google.com/file/d/1JLIibXXAJDI1RMO8rL-QgrRuA3qrX0S-/view?usp=sharing)
- [Azure DevOps CI/CD](https://drive.google.com/file/d/1DlhI39iWF8_WjnV8wD7OUD8Xh7SLbps3/view?usp=sharing)
