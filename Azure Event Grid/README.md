# AzureDevDocs
# Azure Event Grid
Event Grid is a service that you can utilise to connect your solutions together using architectures aimed towards utilising events. The event sources can be any range of Azure Services, including Event Hubs, IoT Hub, App Configuration, Blob Storage, Policies, Containers and many many more. The event grid then links these event sources with your applications, Azure Functions and much much more as a middleman.  
Alternatively, your own application can also be an event trigger for event grid too!  
It is similar to the Service Bus in that you can subscribe to events and do certain things when they happen. In fact, it's even possible to connect to Service Bus as an event trigger!  
Example uses:  
When an item gets added to Blob Storage, compress it using a certain algorithm (such as zipping the file) using a Serverless Function.  
When you get a successful order on your site, hash any important information using a function, and upload it to a database.  
Send some data to an Excel Spreadsheet which is located on your Azure Blob Storage account.  
# How-to: Azure Event Grid  
> **Info**  
> As part of the Azure Free Tier, your first 100,000 operations are free.  
Create an event grid  
In azure function, create a new function which is triggered by an event grid  
Create a new event and link it to the newly created function  
Update a blob that its linked to so it triggers the event  
Check if the event has triggered successfully