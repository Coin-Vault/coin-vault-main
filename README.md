# Coin Vault

This is the official repository of Coin Vault!  
Coin Vault is a crypto exchange project created by Rob Rutjes for semester 6 Fontys ICT.

Below is a guiding line if you are new to the project and want/need te partisipate in it:  

## 1. Enterprise Architecture (microservices)

For the project there is an Enterprise Architecture Diagram that showcases all the microservices in the system. 


![Enterprise Architecture Diagram](https://i.ibb.co/0DTpvmP/Schermafbeelding-2023-06-12-103209.png)


The current state of the project is that three of the microservices are up and running
- Trade microservice
- Portfolio microservice
- React.js front end

## 2. Trade Microservice

As the name of this microservice suggests this API services handles the trades.  
The programming language used is C# .NET Core 7.0

### How to start? And important commands
- To run the API localy run `dotnet run` in the CLI
- To run the linter run `dotnet format` in the CLI

## 3. Portfolio Microservice

As the name of this microservice suggests this API services handles the portfolio's.  
The programming language used is C# .NET Core 7.0

### How to start? And important commands
- To run the API localy run `dotnet run` in the CLI
- To run the linter run `dotnet format` in the CLI

## 4. React.js Front-end

### How to start? And important commands
- After cloning the repository run `npm install` in the CLI
- To run react.js localy run `npm start` in the CLI
- To run the linter run `npm run lint` in the CLI

## 5. Support FaaS

For the support functionallity there is a FaaS (function as a service) deployed in the Azure cloud.  
This service is responsible for support tickets that users can create if they have a problem or question.

## 6. GitHub CI/CD Pipeline

In each GitHub repository there is CI/CD pipeline that runs serveral checks. 

For the C# .NET core API's: 
- Sonarcloud (Securtity checks, code coverage tests & code smells)
- SuperLinter (Runs the `dotnet format` checks linter)
- Build (Full build of the application)
- Tests (Unit/Intergration tests)

When all checks succeeds a Docker image is created an pushed to Docker Hub. 

If a tests fails check if you run al the important commands above for the C# API.

Otherwise contact a senior developer of the project.

To merge the code to the main branche at least one review is needed.

## 7. Kubernetes Deployment

As this project uses microserivces it's also utilizing the service of kubernetes.  
There is a repository `coin-vault-kubernetes` where all the kubernetes files are stored.  

If you want to run the full system in production the only thing you need to do is start-up docker with kubernetes and apply all the kubernetes deployment files with `kubectl apply -f {filename.yaml}`

## 78 Cloud Services

Which services are in the cloud:
- RabbitMQ running at [CloudAMQP](https://www.cloudamqp.com/)
- MSSQL database running at [Azure](https://azure.microsoft.com/)
- Support FaaS running at [Azure](https://azure.microsoft.com/)
