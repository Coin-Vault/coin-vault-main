# Coin Vault

Welcome to the official repository of Coin Vault!

Coin Vault is a crypto exchange project created by Rob Rutjes for semester 6 Fontys ICT.

Below is a guide if you are new to the project and want to participate:

## 1. Enterprise Architecture (microservices)

The project follows an Enterprise Architecture Diagram that showcases all the microservices in the system.

![Enterprise Architecture Diagram](https://i.ibb.co/0DTpvmP/Schermafbeelding-2023-06-12-103209.png)

Currently, three of the microservices are up and running:

- Trade microservice
- Portfolio microservice
- React.js front end

## 2. Trade Microservice

The Trade Microservice is responsible for handling trades. It is built using C# .NET Core 7.0.

### Getting Started and Important Commands

- To run the API locally, execute `dotnet run` in the CLI.
- To run the linter, use the command `dotnet format` in the CLI.

## 3. Portfolio Microservice

The Portfolio Microservice handles portfolios within the system. It is built using C# .NET Core 7.0.

### Getting Started and Important Commands

- To run the API locally, execute `dotnet run` in the CLI.
- To run the linter, use the command `dotnet format` in the CLI.

## 4. React.js Front-end

### Getting Started and Important Commands

- After cloning the repository, run `npm install` in the CLI.
- To run the React.js application locally, execute `npm start` in the CLI.
- To run the linter, use the command `npm run lint` in the CLI.
- To run the cypress e2e test, us the command `npx cypress run` in the CLI.

## 5. Support FaaS

The support functionality is implemented using a Function as a Service (FaaS) deployed in the Azure cloud.    
This service handles support tickets created by users for problem resolution and inquiries.

## 6. GitHub CI/CD Pipeline

Each GitHub repository includes a CI/CD pipeline that runs several checks:

For C# .NET Core APIs:
- Sonarcloud (Security checks, code coverage tests & code smells)
- SuperLinter (Runs the `dotnet format` linter)
- Build (Full build of the application)
- Tests (Unit/Integration tests)

If all checks pass, a Docker image is created and pushed to Docker Hub.

If any tests fail, make sure you have executed all the important commands mentioned above for the C# APIs. Otherwise, reach out to a senior developer for assistance.

For React.js front-end:
- ESLint (Runs the `npm run lint` linter)
- End-2-End test (Runs the `npx cypress run` Cypress)

At least one review is required to merge the code into the main branch.

## 7. Kubernetes Deployment

Since this project utilizes microservices, it also utilizes Kubernetes for deployment. The "coin-vault-kubernetes" repository contains all the Kubernetes files required.

To run the full system in production, start Docker with Kubernetes and apply all the Kubernetes deployment files using the command `kubectl apply -f {filename.yaml}`.

## 8. Security

Security is crucial for this project. All APIs use JWT tokens for authorization, and Auth0 is employed for authentication.

When working on the project, please prioritize security measures.

## 9. Cloud Services

The project utilizes the following cloud services:
- RabbitMQ running on [CloudAMQP](https://www.cloudamqp.com/)
- MSSQL database hosted on [Azure](https://azure.microsoft.com/)
- Support FaaS deployed on [Azure](https://azure.microsoft.com/)

## 10. Contact

We hope this guide helps new developers quickly get started with the project. If you have any further questions, feel free to reach out to a senior developer on the project.
