## Azure offers different technologies for providing remote access to VMs:
1. `Azure Bastion, a platform as a service (PaaS)` solution, for accessing VMs through a browser or currently in preview through the native SSH/RDP client on Windows workstations
2. `Just in time (JIT) access provided through Microsoft Defender for Cloud.`
3. `Hybrid connectivity options, such as Azure ExpressRoute and VPNs`
4. `Public IP attached directly to the VM or through a NAT rule` via an Azure public load balancer

## Azure Bastion: 
- Fully Managed PaaS enabling secure RDP/SSH to Azure VMs, accessed directly via Azure portal or native clients, without requiring public IPs or VPNs.
- Bastion is `deployed to a virtual network and supports virtual network peering.`
- Azure Bastion `manages RDP/SSH connectivity to VMs created in the local or peered virtual` networks.

## Azure Bastion can be used in Azure Virtual WAN topology however there are some limitations:
- `Cannot be deployed inside of a Virtual WAN virtual hub.`
- `must use the Standard SKU and also the IP based connection feature must be enabled`
- Deployed in any spoke virtual network connected in a Virtual WAN, for accessing Virtual Machines, in its own or, other virtual networks that are connected to the same Virtual WAN, via its associated hubs, through Virtual WAN virtual network connections; providing routing is configured correctly.

## Azure Container Registry roles and permissions:
- Azure role-based access control (Azure RBAC) to assign specific permissions to users, service principals, or other identities that need to interact with a registry.
- `Owner == Contributor` & `AcrPush = Pull/Push both` & `AcrPull == Only Pull`
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/28fc6055-3430-4cb3-878c-78ffd12992a4)

## Access and identity options for Azure Kubernetes Service (AKS):
- Using Kubernetes `role-based access control (Kubernetes RBAC)`, you can grant users, groups, and service accounts access to only the resources they need.
- With Azure Kubernetes Service (AKS), you can further enhance the security and permissions structure using `Microsoft Entra ID and Azure RBAC`.
- Role: `Before assigning permissions to users with Kubernetes RBAC, you'll define user permissions as a Role. Grant permissions within a namespace using roles.`
- ClusterRoles: A `ClusterRole grants and applies permissions to resources across the entire cluster, not a specific namespace.`
> Kubernetes roles grant permissions; they don't deny permissions.

- RoleBindings, you can `logically segregate a single AKS cluster, only enabling users to access the application resources in their assigned namespace.`
- ClusterRoleBinding, you `bind roles to users and apply to resources across the entire cluster, not a specific namespace.` 

- Metrics play an important role in cluster monitoring, identifying issues, and optimizing performance in the AKS clusters.
- Control plane logs for AKS clusters are implemented as resource logs in Azure Monitor.
- Resource logs aren't collected and stored until you create a diagnostic setting to route them to one or more locations i.e Azure Log Analytics workspace.
- Container Insights collect various types of telemetry data from containers and Kubernetes clusters to help you monitor, troubleshoot, and gain insights into your containerized applications running in your AKS clusters.
- `The Logs and events grouping captures the logs from the ContainerLog or ContainerLogV2, KubeEvents, KubePodInventory tables, but not the metrics.`

## Azure Monitor:
- Azure Monitor is a comprehensive monitoring solution for collecting, analyzing, and responding to monitoring data from your cloud and on-premises environments.
- Azure Monitor collects and aggregates the data from every layer and component of your system across multiple Azure and non-Azure subscriptions and tenants.
- You can also integrate other Microsoft and non-Microsoft tools.
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/7e7055cb-1cf6-4817-9ab6-dbf9da0a432c)
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/7bf88b2a-bef4-4a41-9988-6017cec79d0b)


## Azure Managed Grafana: 
- The most common way to analyze and present Prometheus data is with a Grafana Dashboard.
- Azure Managed Grafana includes prebuilt dashboards for monitoring Kubernetes clusters including several that present similar information as Container insights views.

## Workbook
- Azure Monitor Workbooks is a feature in Azure Monitor that provides a flexible canvas for data analysis and the creation of rich visual reports.

## Alerts:
- Azure Monitor alerts help you detect and address issues before users notice them by proactively notifying you when Azure Monitor collected data.
- You can set alerts on metrics, logs, and the activity log. Different types of alerts have benefits and drawbacks.
### Two types of metric rules used by Container insights:
- `Prometheus metrics based alerts` AND `Platform metric based alerts`

> Log alerts allow you to alert on your data plane and control plane logs. 

# Overview of managed disk encryption options:
## 1. Azure Disk Storage Server-Side Encryption (AKA `encryption-at-rest or Azure Storage encryption)`
- Always enabled and automatically encrypts data stored on Azure managed disks (OS and data disks), supports customer-managed keys as well.

## 2. Encryption at host: `can be combined with Azure Storage Encryption to ensure Encryption at rest and flow`
- a Virtual Machine option.
- Enhances Azure Disk Storage Server-Side Encryption to `ensure that all temp disks and disk caches are encrypted at rest and flow encrypted` to the Storage clusters.

## 3. Azure Disk Encryption: `encrypts the OS and data disks of Azure virtual machines (VMs) inside your VMs `
- Encrypts the OS and data disks of Azure virtual machines (VMs) inside your VMs.
- Uses the `DM-Crypt feature of Linux` or the `BitLocker feature of Windows`.
- ADE is integrated with Azure Key Vault to help you control and manage the disk encryption keys and secrets.
- `Azure Disk Encryption is zone resilient, the same way as Virtual Machines.`
- helps protect and safeguard your data to meet your organizational security and compliance commitments.

## 4. Confidential disk encryption: `protected disk content accessible only to the binded VM`
- Binds disk encryption keys to the virtual machine's TPM` and makes the protected disk content accessible only to the VM.

> Customer control of keys ✅ When configured with DES (All of the Encryption Options)
> HSM Support: with Azure Key Vault Premium and Managed HSM.

- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/60e068c6-5848-4b71-83cd-c860bcdd0d7b)

### Note: Microsoft Defender for Cloud has the following disk encryption recommendations:
- Virtual machines should encrypt temp disks, caches, and data flows between Compute and Storage resources (Only detects Azure Disk Encryption)
- Windows virtual machines should enable Azure Disk Encryption or EncryptionAtHost (Detects both Azure Disk Encryption and EncryptionAtHost)
- Linux virtual machines should enable Azure Disk Encryption or EncryptionAtHost (Detects both Azure Disk Encryption and EncryptionAtHost)

> Azure Disk Encryption is not available on Basic, A-series VMs, or on virtual machines with a less than 2 GB of memory.

# Azure security baseline for API Management:
- The Microsoft cloud security benchmark provides recommendations on how you can secure your cloud solutions on Azure.
- The content is grouped by the security controls defined by the Microsoft cloud security benchmark.
- Can monitor this security baseline and its recommendations using Microsoft Defender for Cloud.


## Points:
- Hardening: Process of securing a system by reducing its attack surface and minimizing vulnerabilities.
- Auditing enables tracking of database access and activities, helping to identify unauthorized actions and ensure compliance with security policies.
- Always Encrypted provides a comprehensive encryption solution, protecting sensitive data throughout its lifecycle.
- TDE encrypts stored data, ensuring it remains inaccessible to unauthorized users without the appropriate encryption keys.
- The Microsoft Purview governance portal provides tools for discovering, classifying, and managing sensitive data across an organization's data estate.
- Microsoft Entra database authentication enhances security by allowing for Microsoft Entra ID-based authentication, providing a more secure and manageable access control mechanism.
