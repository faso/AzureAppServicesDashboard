# Azure App Services Dashboard

![.NET Core](https://github.com/faso/AzureAppServicesDashboard/workflows/.NET%20Core/badge.svg)

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

## How to run

Prerequisites: .NET Core 3.1 SDK

1) Clone the repo
2) [Create a Service Principal for your app with the Contributor role](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal)
3) Fill in the Azure section of `appsettings.Development.json`
4) Run the project
