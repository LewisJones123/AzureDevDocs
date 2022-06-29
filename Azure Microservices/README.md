# AzureDevDocs

# Azure Microservices - Summary
Note: Most of this information is sourced from Microsoft's official page on Microservices Architecture, which can be found [here.](https://docs.microsoft.com/en-gb/azure/architecture/microservices/)  

Azure Microservices are not a single service offering within Azure, it is instead a collection, which is formed together to create an application where each function is "loosely coupled" - they are as independent of each other as possible. Theoretically, the most loosely coupled application could have any one component fail and the full app doesn't entirely break at the same time.
# Building an Azure microservice solution
When it comes to making an Azure Microservice solution, you want to create components that do not have any coupling with any other. You could have a 1:1 team to microservice, meaning that each team would be assigned a separate microservice.  
Utilising Azure Functions is a great part of the Microservice solution. A team, or individual, could write and maintain a single function, which connects to another function, and so on, until a full pipeline is processed.  
Utilising CI/CD pipelines works with Microservices, as you can continually push regular updates, and utilising the power of CI/CD pipelines, test that the entire solution still works, while minimising the amount of work needed to revert where required.  
To start with building a Microservice, you will need an API gateway.  
An API gateway is an entry point for your connections - you can have load balancers and autoscalers here to keep your application running smoothly under increased loads.  
This API gateway should redirect the clients to the relevant APIs calls, depending on what information was passed into the URL.  
These functions should then do the API call separately to the API gateway.  
If done correctly, these functions should then be loosely coupled - if the Function fails, the API gateway can still respond with a HTML response code.  
Further, more detailed explanations of Microservices can be found [here.](https://docs.microsoft.com/en-gb/azure/architecture/microservices/)  
