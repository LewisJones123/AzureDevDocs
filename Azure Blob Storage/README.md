# AzureDevDocs
# Azure Blob Storage - recap
Blob containers are object-oriented storage. This means its very similar to your actual hard drive, containing data such as music, documents and pictures. There are different types of blob storage, dependent on the optimisation required.

 - Block: General use, for text and binary data. Use this one for your regular files as a backup strategy, or for use with other applications in the cloud. Made of blocks and managed individually. Maximum size is 4.75TiB.
 - Append - Optimised for append operations - updating files. Maximum size is also 4.75TiB.
 - Page  - Used for random access files. Also used for Virtual Hard Drives. Maximum size is 8TiB.
There are also storage accounts - two different versions.
You want to use V2 for the vast majority of the time, with V1 also being available for legacy applications - but it is not recommended for general use.
# Blob Storage - Alternative types of storage
Within blob storage there are also other options:
 - Block blob storage - Mostly for Block and Append blobs. Has a high transaction rate, and works great with large amounts of small objects, as well as loads with a low-latency requirement.
 - File storage - Enterprise only. Premium file sharing. Only supports file store.
 - Blob storage - Legacy version of Block Blob Storage. 
# Blob Storage - Tiers of access
 
 - Premium - Optimised for low-latency operations, priced for high transactional usage.
 - Hot - Normal, default level of access. Instant access to files. Most expensive.
 - Cold - Data is archived in this tier. Data can take time to access, but is much cheaper to store.
 - Archive - Data is archived even deeper in this storage. Data can take many hours to access, but it is extremely cheap compared to Hot storage, and even cold storage.
# Documentation
[Microsoft Azure Blob Storage](https://azure.microsoft.com/en-gb/services/storage/blobs/)  
[Blob Storage Pricing](https://azure.microsoft.com/en-gb/pricing/details/storage/blobs/) - Worth a look to see the vast price differences between Hot, Cold and Archive!  
[Introduction to Blob Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction)
