# Azure App Services Dashboard

![.NET Core](https://github.com/faso/AzureAppServicesDashboard/workflows/.NET%20Core/badge.svg)

## How to run

First, gather your connection info so the dashboard can see your Azure resources

[Create a Service Principal for your app with the Contributor role](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal)

You will need your tenant ID, subscription ID, AD domain name, app registration client ID and secret
Now, you can either run it using Docker with a prebuilt image, build your own Docker image or build the app from source

## Running using Docker

```
docker run -d -p 8080:80 --name AzureAppDashboard \ 
  -e Azure:TenantId='REPLACE' \ 
  -e Azure:ClientId='REPLACE' \ 
  -e Azure:SubscriptionId='REPLACE' \ 
  -e Azure:ClientSecret='REPLACE' \
  -e Azure:DomainName='REPLACE' 
  fas0/azureappdashboard
```

Go to `http://localhost:8080/`

## Building a Docker image

Build the image
```
git clone https://github.com/faso/AzureAppServicesDashboard.git
cd AzureAppServicesDashboard
docker build --tag AzureAppDashboard .
```
Run it with
`docker run -d -p 8080:80 --name AzureAppDashboard AzureAppDashboard`

Go to `http://localhost:8080/`

## Building from source

Prerequisites: .NET Core 3.1 SDK

1) Clone the repo
2) Fill in the Azure section of `appsettings.Development.json`
3) Run the project

## Features & Roadmap
- [x] List apps
- [x] List app slots
- [x] Link to Azure pages for apps
- [x] Start/Stop apps
- [x] Link Kudu
- [x] Show App Settings and Connection Strings
- [x] Switch between Resource Groups
- [x] Latest deployment info
- [x] Link hostnames
- [x] Restart apps
- [x] Auto-refresh in the background
- [x] Function App support
- [ ] Dark mode
