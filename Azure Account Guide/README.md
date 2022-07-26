# AzureDevDocs
# Azure Account Guide
This guide will provide information on the tiers available within Azure. This includes support plans, as well as how the different payment models work.  
This is mostly covered in the Cloud Fundamentals exam, but it's always worth revisiting!
# Azure Free Tier  
When you setup your account for the first time, you recieve $200 free credit, which expires in 30 days after creation, as well as access to all free tier services, both the 12 month access and permanent access.  
While a list can be found online, a few highlights of the Azure Free Tier include: 

12 MONTHS FREE ACCESS (YOU MUST ENABLE PAY-AS-YOU-GO AFTER THE FIRST 30 DAYS)
- Azure Virtual Machines: 750 hours per month for a Windows and a Linux B1s VM. Includes 2x 64GB SSDs.  
- Azure CosmosDB: 400 RU/s, 25GB Storage.
- Azure Archive Stroage - 10GB LRS Storage, 10GB LRS or GRS Write/Retrieval, 100 reads.  
- Azure Face: 30,000 transactions per month, detecting and identifying emotions in images.
- Azure Key Vault: 10,000 transactions for RSA-2048 bit keys, Standard tier.  

ALWAYS FREE SERVICES (NO NEED TO ENABLE PAY-AS-YOU-GO). RESETS MONTHLY  
- Azure CosmoDB: 1,000 RU/s, 25GB storage.
- Azure Functions: 1,000,000 requests.
- Azure DevOps: 5 users, unlimited private Git repos
- Azure Security Center: Free Policy assessment and recommendations.
- Azure Advisor: Personalised recommendations & best practices.
- Azure Notifications Hub: 1 million push notifications + free namespace.
- Azure Virtual Network: 50 virtual networks.
- Azure Data Catalog: Unlimited users.
... AND MORE!  
Note: Not all of these services are covered in the AZ-204 exam, but they are just some highlights of the services available. If you have a free account, feel free to experiment with them all for free!  

# Azure - Support plans
As part of Azure, there are support plans available to help your business run successfully. Support plans range from Basic to Enterprise, with vastly increasing prices between each tier. Here we will discuss the support plans available, and the features within them:  
  
Basic - Free for all Azure customers. Includes:
- Billing Support
- 24/7 self-help resources
- Submit as many relevant support tickets as needed.
- Azure Advisor access.
- Azure Health Status and Notifications.  
  
Developer - $29 per month. Includes:
- All of the basic tier benefits.
- Good for trial & non-production environments.
- Third-party software support including interoperability & configuration guidance/troubleshooting
- Access during business hours via Email for technical support (9am-5pm Mon-Fri in UK, 6am-6pm Pacific time US)  
- Response time below 8 hours for Minimal business impact severity issues.
- General guidance on Architecture.  
  
Standard - $100 per month. Includes:
- All of the basic and developer benefits.
- Access to support 24/7 via email and phone after support ticket is raised.
- As Developer for minimal business impact (8hrs) response.
- For medium business impact, 4hrs response time.
- For severe business impact, 1hr response time.  
  
Professional Direct - $1,000 per month. Includes:
- Everything from the Basic, Developer & Standard tiers.
- Response time for minimal business impact is four hours, and moderate business impact is two hours, halved from standard tier.
- Architecture support from a pool of ProDirect delivery managers.
- Access to the Support API, allowing programatically created tickets.
- Operations support: Service reviews and adivsory consultation.
- Webinar training led by Azure Experts.
- Proactive Guidance from a pool of delivery managers.
There may be additional Enterprise tiers available, for example for Government clients in the US, however limited information is available for these, and they are far out of scope for this documentation.  
# Azure Web Service Plans
As part of Azure Web Service, there are six tiers available, ranging from a free plan to an isolated high performance plan.  
Each plan has perks, as listed below. Note that these are all subject to change, and are accurate as of July 2022.  
  
Free plan - Try for free:
- 10 Web, Mobile or API apps
- 1GB of Disk Space
- Shared Compute Type  
  
Shared plan - Environment for dev/test ($0.013/hour)  
  
- 100 Web, mobile or API apps
- No increase in disk space over free tier.
- Ability to use Customised Domains.
- Shared compute type.  
   
Basic - Dedicated Environment for dev/test
- Unlimited number of Web, Mobile or API apps.
- 10GB of Disk Space (up from 1GB in Free/Shared).
- Up to 3 maximum instances (up from 1).
- Support for Customised Domain, Hybrid connectivity, Virtual Network connectivity & Private Endpoints
- Dedicated Compute Type
  
Standard - Run Production Workloads
- Unlimited number of Web, Mobile or API apps.
- 50GB of Disk Space (up from 10GB in Basic).
- Up to 10 maximum instances.
- Support for Customised Domain, Hybrid Connectivity, Auto Scaling, Virtual Network Connectivity & Private Endpoints.
- Dedicated Compute Type  
  
Premium - Enhanced Performance and Scale
- As Dedicated tier and:
- 250GB of Disk Space (up from 50GB).
- Up to 30 maximum instances (NOTE: NOT ALL REGIONS SUPPORT THIS!) (up from 10)  

Isolated - High-Performance, Security and Isolation
- As Premium tier and:
- 1TB of Disk Space (up from 250GB).
- Up to 100 maximum instances (Supported by all regions).
- Isolated Compute Type.  

Wow - that's a lot of features! But there's more.  
Within each tier, there are sub tiers, which have differing amounts of CPU cores, RAM and storage, for different prices. I won't list them all here as there are a few instances, but here are some examples:  
- Basic Service Plan Instance B1: 1 CPU core, 1.75GB RAM, 10GB Storage: $0.075/hour.
- Basic Service Plan Instance B2: 2 CPU cores, 3.50GB RAM, 10GB Storage: $0.15/hour.
- Isolated v2 Service Plan Instance I3v2: 8 CPU cores, 32GB RAM, 1TB Storage: Prices start at $1.216/hour for 3 year reserved, $2.248/hour for Pay as you go

(Please note: If you, or your business has Windows Server licenses that are transferrable to Azure, you may be eligible for heavy discounts utilising parts of your Azure license). Read more about Azure Hybrid benefit pricing at: https://azure.microsoft.com/en-gb/pricing/hybrid-benefit/#faqs).
