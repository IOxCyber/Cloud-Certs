# Azure Storage Services: 
Blob Storage: A scalable object storage service for unstructured data such as text or binary data.
File Storage: Fully managed file shares that can be accessed via the Server Message Block (SMB) protocol.
Queue Storage: A messaging store for reliable messaging between application components.
Table Storage: A NoSQL key-value store for semi-structured data.
Disk Storage: Persistent, high-performance block storage for Azure Virtual Machines.
Data Lake Storage: Secure, massively scalable, and performant storage for big data analytics solutions.


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


## Data protection overview:
- `data protection` refers to strategies for protecting the storage account and data within it from being deleted or modified, or for restoring data after it has been deleted or modified. 

## Immutable storage for Azure Blob Storage: `WORM: Wtrite Once, Read Many`
- `Time-based retention` & `Legal hold policies.`
- If any one of the policies are active/set then `objects can be created and read, but not modified or deleted.`

## More info:
- A time-based retention policy can be configured at the account, container, or version level.
> Individual blobs can't be configured with their own immutability policies.

- A legal hold is a temporary immutability policy that can be applied for legal investigation purposes or general protection policies.
-  A legal hold can be configured on an individual blob version level

## Grant limited access to Azure Storage resources using shared access signatures (SAS):
- `shared access signature (SAS) provides secure delegated access to resources in your storage account.`
### Types:
1. A `user delegation SAS` is secured with Microsoft Entra credentials, applies to `Blob storage only.`
2. A `service SAS` is secured with the storage account key, applies to only one of the Azure Storage services: `Blob storage, Queue storage, Table storage, or Azure Files.`
3. `Account SAS`, Service-level operations (For example, the Get/Set Service Properties and Get Service Stats operations) & To Read, write, and delete operations that aren't permitted with a service SAS.
> Delegated means to access stoage resources on your behalf by the apps.

## Note: 
- When your application design requires shared access signatures for access to Blob storage, use Microsoft Entra credentials to create a user delegation SAS when possible for superior security.
- Azure Storage supports using Microsoft Entra ID to authorize requests to blob data. 

## shared access signature forms:
1. `Ad hoc SAS.` When you create an ad hoc SAS, the start time, expiry time, and permissions are specified in the SAS URI. Any type of SAS can be an ad hoc SAS.
2. Service SAS with stored access policy. A stored access policy is defined on a resource container, which can be a blob container, table, queue, or file share.

> A user delegation SAS or an account SAS must be an ad hoc SAS. Stored access policies are not supported for the user delegation SAS or the account SAS.

## Azure Files:
- Azure Files is Microsoft's easy-to-use cloud file system. Azure file shares can be seamlessly used in Windows and Windows Server.
- The SMB protocol requires TCP port 445 to be open
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/2bc175ec-d4a7-4a1c-8197-b99a9c7d225d)

## Azure Blob Storage lifecycle management:
- offers a rule-based policy that you can use to transition blob data to the appropriate access tiers or to expire data at the end of the data lifecycle.
- hot storage is best during the early stages.
- Cool storage is most appropriate for occasional access.
- Archive storage is the best tier option after the data ages over a month.

> The lifecycle management feature is available in all Azure regions.

# > Lifecycle management policies are free of charge. Customers are billed for standard operation costs for the Set Blob Tier API calls. Delete operations are free.








