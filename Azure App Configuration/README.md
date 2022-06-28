# AzureDevDocs
# Azure App Configuration
Azure App Configuration is a service which centrally manages application settings and feature flags. Spreading configuration settings around many programs can cause errors that are harder to troubleshoot compared to more traditional software. The main recommendation for app configuration is to split code from configuration settings. Examples of software that benefit from App Configuration (credit: [Microsoft - What is Azure App Configuration?](https://docs.microsoft.com/en-us/azure/azure-app-configuration/overview)) are as follows:
-   Microservices based on Azure Kubernetes Service, Azure Service Fabric, or other containerized apps deployed in one or more geographies
-   Serverless apps, which include Azure Functions or other event-driven stateless compute apps
-   Continuous deployment pipeline
On top of this, App Configuration also complements Azure Key Vault, which stores Application secrets, to control access to features in real time. 
For example, if a secret is needed to use a certain application, then you can revoke this immediately by deleting the secret, which would cause the app to stop working (hopefully deliberately!).
You could also dynamically change an application's settings, without needing to completely restart the application, if it can handle it. 
