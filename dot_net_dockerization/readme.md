In this tutorial, we have a .NET application and we want to dockerize it. This module will walk through that process.

We'll learn how to:
1. Create a Dockerfile
1. Build docker image
1. Run a docker image
1. Stop a container
1. Remove a container
1. Remove an image
1. Working with Docker Compose

## Introduction to containers
Depending on the programming language and platform for your application, we will find the corresponding Docker image. That image will have all the required dependencies and libraries already installed. 

For example, for .NET Core apps, there are multiple images available that contains the SDK and/or runtime for multiple versions.

These images are typically available on a Container Registry like hub.docker.com, for [.NET Core](https://hub.docker.com/_/microsoft-dotnet), for [Java](https://hub.docker.com/_/openjdk), for [NodeJs](https://hub.docker.com/_/node).

There are also images available for database engines like [MySQL](https://hub.docker.com/_/mysql), [SQL Server](https://hub.docker.com/_/microsoft-mssql-server), [Oracle](https://hub.docker.com/_/oracle-database-enterprise-edition), Cassandra, etc.



## 1) Create a Dockerfile

We have a sample .NET Core 5.0 web MVC application. We can run this application through the .NET cli tool:

```dotnetcli
$ dotnet build
$ dotnet run
```

Now we want to run this same application in a Docker container. The process is similar to running the application inside a virtual machine:
1. Choose a base VM running Linux or Windows.
1. Install the application dependencies and libraries (typically app SDK and Runtime). 
1. Build the application. 
1. Deploy the application into the VM.

With containers, the process will be:

1. Choose a base docker image with application dependencies and libraries (steps 1 and 2 for VMs).
1. Build the application.
1. Deploy the application into the image.