1. Compute Services: To execute the instruction on cloud.
VM (Hypervisor, Virtual Box etc), App Services, Container Instances, Azure Kubernates Services(AKS), Win Virtual Desk (same as desktop but on cloud)

2. Work of: Administrator > Created the VM | Developer > Develop the App | DevOps > Ensure that the App deployed perfectly in Environment created by Administrator.

3. Azure App Services: Fully managed platform to build, deploy & scale web apps, APIs.
RDP (Remote Desktop Protocol), 

4. Azure Container Services:
  1. Azure Container Instances: Lightweight virtual Env. (No Scaling)
  2. App Code + Dependency + Configuration Metadata = Docker Image > Container Created > Azure Container Registry: To deploy the Docker Image.

5. Azure Kubernetes Services: Temporary Containers to deploy microservices.

6. Azure Networking Services:
1. Azure Vnet: use to communicate for Azure resources over internet & on-premises network.
2. VPN: to communicate on public network b/w Azure resources & On-Premises.
3. Azure Express Route: Leased, dedicated pvt connection b/w  Azure resources & On-Premises. (Costly)

7. Azure Storage Services:
 1. Azure Blobs/Container Storage: (Binary Large Object) A massively scalable object storage for text and binary data. Also includes support for big data analytics through Data Lake Storage Gen2. can store unstructured data. (eg. Logs, Docs, Images)
 2. Azure Files: Highly available network file, accessed by the SMB(Server Msg Block) protocol.
 3. Azure Disks: Block-level storage for Azure VMs, Apps.
 4. Azure Queues: A messaging store for reliable messaging between application components.

> Geo-Location > Regions 60+ in 140 Countries (group of datacenters) > Zones (physical separated Datacenter within Regions) > Locally redundant Storage (Within Datacenter) 

8. Storage Tier:
Hot Tier(high read/write) > Cool Tier(Upto 30 days) > Achieve Tier(upto 180 days) (Frequency of Access Level)

9. Availability & Cost, Redundancy in Azure::
- Locally redundant storage (LRS), replicated 3 times within Datacenter
- Zone-redundant storage (ZRS) replicated in 3 zones within Regions
- Read-access geo-redundant storage (RA-GRS),  replicated data 3 times using LRS in Same Region & in secondary geo region (Readable)
- Geo-redundant storage (GRS), replicated data 3 times using LRS in Same Region & in secondary geo region < Only Supported in Gen Purpose V2
- Geo-zone-redundant storage (GZRS), copies data synchronously across three Azure availability zones in the primary region using ZRS & different zone of other geo region.
- Read-access geo-zone-redundant storage (RA-GZRS) Readable

> Note: With GRS or GZRS, the data in the secondary region isn't available for read or write access unless there's a failover

`Locally redundant storage (LRS) copies your data synchronously three times within a single physical location(Datacenter) in the primary region.at least 99.9999999999% (11 9's) over a given year.`

`Zone-redundant storage (ZRS) copies your data synchronously across three Azure availability zones with different physical location(Datacenter) in the primary region. high availability.at least 99.9999999999% (12 9's) over a given year.`

10. Storage service	Endpoint
- Blob Storage	https://<storage-account-name>.blob.core.windows.net
- Data Lake Storage Gen2	https://<storage-account-name>.dfs.core.windows.net
- Azure Files	https://<storage-account-name>.file.core.windows.net
- Queue Storage	https://<storage-account-name>.queue.core.windows.net
- Table Storage	https://<storage-account-name>.table.core.windows.net

> Storage account names must be between 3 and 24 characters in length and may contain numbers and lowercase letters only.

11. Tier in Blob:
a. Hot access tier: Optimized for storing data that is accessed frequently (for example, images for your website).
b. Cool access tier: Optimized for data that is infrequently accessed and stored for at least 30 days (for example, invoices for your customers).
c. Archive access tier: Appropriate for data that is rarely accessed and stored for at least 180 days, with flexible latency requirements (for example, long-term backups).

12. File in Blob:
- Shared access: Azure file shares support the industry standard SMB and NFS protocols, meaning you can seamlessly replace your on-premises file shares with Azure file shares without worrying about application compatibility.
- Fully managed: Azure file shares can be created without the need to manage hardware or an OS. This means you don't have to deal with patching the server OS with critical security upgrades or replacing faulty hard disks.
- Scripting and tooling: PowerShell cmdlets and Azure CLI can be used to create, mount, and manage Azure file shares as part of the administration of Azure applications. You can create and manage Azure file shares using Azure portal and Azure Storage Explorer.
- Resiliency: Azure Files has been built from the ground up to always be available. Replacing on-premises file shares with Azure Files means you don't have to wake up in the middle of the night to deal with local power outages or network issues.
- Familiar programmability: Applications running in Azure can access data in the share via file system I/O APIs. Developers can therefore leverage their existing code and skills to migrate existing applications. In addition to System IO APIs, you can use Azure Storage Client Libraries or the Azure Storage REST API.


13. Azure DB Services: 
- Azure Cosmos: NoSQL JSON data, Globally distributed, scalable.
- Azure SQL DB: DaaS (db as a service), Paas imp of MS sql server db.
- Azure DB for MySql: For App Developer.
- Azure DB for PostgreSQL: Based on Open Source

14. Data Types:
- Structure: Azure SQL DB data, eg. Emp data managed.
- Unstructured: Doc, Logs, Audio etc here.
- Partially Structural
