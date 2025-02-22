# C# RabbitMQ Example

This is a simple example of how to use RabbitMQ with C#.

## Setup

Running RabbitMQ in a docker container is the easiest way to get started. To do this, run the following command in the terminal:


- ```docker run -d --name your_container_name -p 5672:5672 -p 15672:15672 rabbitmq:3.12-management```


To run a slightly better container with the UI you can run the management version:

- ```docker pull rabbitmq:management```
- ```docker run -d --name rabbitmq1 -p 5672:5672 -p 15672:15672 rabbitmq:management```
- login by visiting http://localhost:15672 (note this is http and not https!) in a browser:
	- username: guest 
	- password: guest


## Creating the projects
``` 
- dotnet new sln --name workshop
- dotnet new console --name workshop.receive
- dotnet new console --name workshop.send
- dotnet sln add **/*.csproj

```

In both projects, we need to install the RabbitMQ.Client package. To do this, run the following command in the terminal:

```
- dotnet add package RabbitMQ.Client  
```
Remember to add this package to both projects.

In the package manager console run this for both projects:
```
- install-package RabbitMQ.Client
```
## Running the project

Run the workshop.receive project first (right click on project, then debug and start new instance), then the workshop.send project. 
