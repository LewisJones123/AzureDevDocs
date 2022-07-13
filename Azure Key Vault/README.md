# AzureDevDocs
# Azure Key Vault
In a lot of your applications, especially those which are connected to the internet, you will require data such as Connection Strings, API Keys and more to be stored. As these can make your app extremely vulnerable if stored incorrectly, it is important that they are stored in an encrypted manner.  
Azure Key Vault helps you with this, using enterprise grade encryption for both your generated keys as well as your secrets. You can then use links to these secrets and keys in confidence, knowing that they are fully encrypted at rest and during transit, only being decrypted at the destination where it is required.  
# Azure Key Vault - Supported types:
> **Note**  
> As part of the Azure Tier, you recieve the following benefits free of charge (for 12 months):  
> - 10,000 transactions using RSA-2048 Keys, or secrets, at the Standard tier.  
Within Azure Key Vault, you can store the following things:  
- Keys, with support for activation, expiration, RSA/EC keys, as well as tags. Key rotation also available.  
- Secrets, with a name, value and activation/expiration date. Secrets can be checked within Azure, but must have admin privileges.  
- Certificates, with support for self-signed, integrated and non integrated Certificate Authorities, with a validity period of choice. There are many settings for certificates. Note that certificates are relatively expensive.
- Access Policies: Policies can be setup for users who have access to the same key vault. This means that Administrators can prevent people from accessing keys, reading keys, creating keys etc. Limiting allows for refined control of all components.  
# Azure Key Vault - Setting up a vault
Setting up an Azure Key Vault is relatively straightforward. As usual, you can either do it through the Portal, or the command line.  
## Creating a vault in the Azure Portal
1. Firstly, in the search bar at the top, search for key vault.  
![Image of key vault search](images/step1.png)  
2. On the next screen, ensure that your resource group and subscription are set to the one you've been using throughout, and then set a name. The region can be whichever, choose one close to you. Leave the pricing tier as standard, as premium is far more expensive!  
![Image of key vault creation screen](images/step2.png)  
> **Warning**  
> The next section is extremely important. This is where you can enforce purge protection of secrets, ensuring they aren't deleted immediately.  
> It is highly recommended that in a production environment, you enable purge protection, as this prevents immediate loss of secrets.  
1. In terms of recovery options, set the days to retain deleted vaults to whatever you like between 7 and 90 days (the higher the better), and disable purge protection (we want to delete the vault at some point without having to wait ages!)  
![Image of key vault creation screen](images/step3.png)  
After this, press review and create and create your Key Vault!  
