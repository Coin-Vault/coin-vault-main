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

## 4. React.js front end

## 5. GitHub CI/CD Pipeline

## 6. Kubernetes deployment

As this project uses microserivces it's also utilizing the service of kubernetes.  
There is a repository `coin-vault-kubernetes` where all the kubernetes files are stored.  
If you want to run the full system in production the only thing you need to do is start-up docker with kubernetes and apply all the kubernetes deployment files with `kubectl apply -f {filename.yaml}`
