# Azure App Services Dashboard

## Features & Roadmap
- [x] List apps
- [x] List app slots
- [x] Link to Azure pages for apps
- [x] Start/Stop apps
- [x] Link Kudu
- [x] Show App Settings and Connection Strings
- [x] Switch between Resource Groups
- [ ] Latest deployment info
- [x] Link hostnames
- [x] Restart apps
- [ ] Auto-refresh in the background
- [x] Function App support
- [ ] Show configuration
- [ ] Show CORS settings
- [ ] Show WebJobs

## How to run

Prerequisites: .NET Core 3.1 SDK

1) Clone the repo
2) [Create a Service Principal for your app with the Contributor role](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal)
3) Fill in the Azure section of `appsettings.Development.json`
4) Run the project
