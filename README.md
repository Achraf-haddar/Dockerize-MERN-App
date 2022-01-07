# Dockerize MERN Application

I followed this [tutorial](https://medium.com/swlh/how-to-create-your-first-mern-mongodb-express-js-react-js-and-node-js-stack-7e8b20463e66) to get basic app working.

I then containerized the api server and react client and created docker-compose to connect them. You can clone the repository and run the following command:
```
make
```
I tried to deploy the application on AKS (Azure Kubernetes cluster). For this, I created three pods (backend, frontend and mongodb) attached with three services. I used nginx to make the Express api accessible from outside of kubernetes. You can see the demo [here](https://drive.google.com/file/d/1JLIibXXAJDI1RMO8rL-QgrRuA3qrX0S-/view?usp=sharing).

# Build Full CI CD using Devops Azure and Deploy to AKS:
I used Devops Azure to build a full CI CD pipeline and deploy the containers on AKS.
You can see the demo [here](https://drive.google.com/file/d/1DlhI39iWF8_WjnV8wD7OUD8Xh7SLbps3/view?usp=sharing).
