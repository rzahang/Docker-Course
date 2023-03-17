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

