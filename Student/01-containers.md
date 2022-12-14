# Challenge 1: Containers

**[Home](../README.md)** - [Next Challenge >](./02-aks_private.md)

## Introduction

This challenge will cover the basics of containers and container runtimes, and get you familiar with the components of the application we will use throughout this hack.

## Description

Create an Azure Container Registry in a new Resource Group. Build the API and Web images in this repository and store them in your new ACR.

The application we will use in this hack has three components, as the following picture describes: a [web](./Resources/web) tier offers an HTML portal that shows the information produced by the [api](./Resources/api), that in its turn access a **database** with a simple query that shows the database version. You will find the source code for each application in the files supplied for this hack:

![app architecture](./images/app_arch.png)

Using Azure Container Instances:
  - Deploy the **database** as an Azure SQL Database
  - Deploy the **API** image as Azure Container Instance in Azure
  - Make sure that the API can connect to the database
  - Deploy the **web** frontend that will connect to the API
 

For both you should get in the web frontend something like the following. If the frontend is able to get the database version through the API it means that the whole chain is working (web -> api -> database):

## Success Criteria

- You can access the web component
- The web container can access the API container
- The api can access the database, and the database version is correctly displayed in the frontend

Here a sample screenshot of what it should look like:

![sample output](./images/aci_web.png)

Note the two links at the bottom of the page in the picture above will not work at this stage yet.

## Learning Resources

These docs might help you achieving these objectives:

- [API image documentation and source code](./Resources/api/README.md)
- [Web image documentation and source code](./Resources/web/README.md)
- [Run SQL Server container images with Docker](https://docs.microsoft.com/sql/linux/quickstart-install-connect-docker)
- [Azure Container Registry](https://docs.microsoft.com/azure/container-registry/container-registry-intro)
- [Azure Container Instances](https://docs.microsoft.com/azure/container-instances/)
