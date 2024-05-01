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
![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/2f188023-18fa-436b-bbf1-3f5cce6d9256)



## Grant limited access to Azure Storage resources using shared access signatures (SAS):
- `shared access signature (SAS) provides secure delegated access to resources in your storage account.`
### Types:
1. A `user delegation SAS` is secured with Microsoft Entra credentials, applies to `Blob storage only.`
2. A `service SAS` is secured with the storage account key, applies to only one of the Azure Storage services: `Blob storage, Queue storage, Table storage, or Azure Files.`
3. `Account SAS`, Service-level operations (For example, the Get/Set Service Properties and Get Service Stats operations) & To Read, write, and delete operations that aren't permitted with a service SAS.
> Delegated means to access stoage resources on your behalf by the apps.

## Note: When your application design requires shared access signatures for access to Blob storage, use Microsoft Entra credentials to create a user delegation SAS when possible for superior security.


## shared access signature forms:
1. `Ad hoc SAS.` When you create an ad hoc SAS, the start time, expiry time, and permissions are specified in the SAS URI. Any type of SAS can be an ad hoc SAS.
2. Service SAS with stored access policy. A stored access policy is defined on a resource container, which can be a blob container, table, queue, or file share.

> A user delegation SAS or an account SAS must be an ad hoc SAS. Stored access policies are not supported for the user delegation SAS or the account SAS.







