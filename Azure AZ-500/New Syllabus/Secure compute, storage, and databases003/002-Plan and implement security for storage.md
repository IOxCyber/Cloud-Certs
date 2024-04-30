# Enable infrastructure encryption for double encryption of data:
- Azure Storage automatically encrypts all data in a storage account at the service level using 256-bit AES with GCM mode encryption.
- `Infrastructure encryption can be enabled for the entire storage account, or for an encryption scope within an account`, **data is encrypted twice**.
- `Infrastructure-level encryption relies on Microsoft-managed keys and always uses a separate key.`
- To doubly encrypt your data, you must first create a storage account or an encryption scope.
- `The storage account must be of type general-purpose v2 or premium block blob.`
> Service-level encryption supports the use of either Microsoft-managed keys or customer-managed keys with Azure Key Vault or Key Vault Managed Hardware Security Model (HSM). 

# Authorize access to data in Azure Storage:
- Each time you access data in your storage account, your client application makes a request over HTTP/HTTPS to Azure Storage.
- Every request to a secure resource must be authorized. Authorization ensures that the client application has the appropriate permissions to access a particular resource in your storage account.
- 
![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/2f188023-18fa-436b-bbf1-3f5cce6d9256)
