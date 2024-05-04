## 1. Azure Blueprints:
- allow organizations to create standardized, repeatable sets of Azure resources that comply with organizational standards, facilitating rapid and compliant deployment of cloud environments for development teams.
- Blueprints are a declarative way to orchestrate the artifacts such as: Role Assignments, Policy Assignments, Azure Resource Manager templates (ARM templates), Resource Groups.
- It is `a set of resource groups, policies, role assignments, and ARM template deployments` that can be version controlled, audited, and tracked.
- Azure Blueprints automate the deployment of resources, including security policies, RBAC settings, and ARM templates, ensuring a consistent and compliant environment.
- Available Roles: ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/a528204f-9457-43fc-b692-0aa95ab28229)


## 2. Azure Policy: `JSON Format`
- `Set of Rules in "if" statements "then" in JSON format ` to enforce on Azure resources
- Used to enforce standards and assess compliance at scale, ensuring resources conform to corporate policies and regulatory requirements through its compliance dashboard.
## - Common use cases for Azure Policy include implementing governance for resource consistency, regulatory compliance, security, cost, and management (built-ins in Azure)
- `All Policy data and objects (definitions, initiatives, and assignments) will be readable to all roles over its scope and are encrypted at rest.`
- Azure Policy evaluates resources and actions by comparing the properties of those resources to business rules.
- These `business rules, described in JSON format, are known as policy definitions.`
- `Several business rules can be grouped together to form a policy initiative` (sometimes called a policySet).
- Policies can be assign to `management groups, subscriptions, resource groups, or individual resources.`
- You can `assign any of these policies through the Azure portal, PowerShell, or Azure CLI.`
- An initiative definition is a collection of policy definitions that are tailored toward achieving a singular overarching goal.
- An assignment is a policy definition or initiative that has been assigned to a specific scope. This scope could range from a management group to an individual resource.

- When Updated: `Every 24 hrs`
```
A resource is created or updated in a scope with a policy assignment.
A policy or initiative is newly assigned to a scope.
A policy or initiative already assigned to a scope is updated.
During the standard compliance evaluation cycle, which occurs once every 24 hours.
```
## 3. Azure Arc: `simplifies governance and management of multicloud and on-premises resources`
- you can extend your policy-based governance across different cloud providers and even to your local data centers.
- Azure Arc allows you to manage the following resource types hosted outside of Azure:
```
Servers: Manage Windows and Linux physical servers and virtual machines hosted outside of Azure.
Kubernetes clusters: Attach and configure Kubernetes clusters running anywhere, with multiple supported distributions.
Azure data services: Run Azure data services on-premises, at the edge, and in public clouds using Kubernetes and the infrastructure of your choice. SQL Managed Instance and PostgreSQL (preview) services are currently available.
SQL Server: Extend Azure services to SQL Server instances hosted outside of Azure.
Virtual machines: Provision, resize, delete and manage virtual machines based on VMware vSphere or Azure Stack HCI and enable VM self-service through role-based access.
```
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/7f6a0832-7171-4eaf-bcfe-d26337efb22b)

> Azure Virtual Network Manager (preview) enables you to apply consistent management and security policies to multiple Azure virtual networks (VNets) throughout your cloud infrastructure.

## 4. Azure RBAC permissions in Azure Policy:
- Azure Policy has several permissions, known as operations `2 resource Provider: Microsoft.Authorization & Microsoft.PolicyInsights`
- The Resource Policy Contributor role includes most Azure Policy operations.
- The owner has full rights.
- Both Contributor and Reader have access to all read Azure Policy operations.
> All Policy objects, including definitions, initiatives, and assignments, will be readable to all roles over its scope. 

## 5. Azure Dedicated S/W Security Module(HSM): `Azure service that provides cryptographic key storage in Azure`
- Dedicated HSMs provide a high level of security for cryptographic operations and key management by physically isolating and protecting keys from unauthorized access.
- `Offers FIPS 140-2 Level 3-validated cryptographic key storage globally, ensuring exclusive control and high availability across Azure regions with Thales Luna 7 HSM appliances, accessible via VPN for on-premises integration and managed through Thales customer support.`
- Azure Dedicated HSM isn't ideal for scenarios where Microsoft cloud services utilize customer-managed encryption keys but lack integration with Azure Dedicated HSM.
- The purpose of a `dedicated Hardware Security Module (HSM) is to securely manage and store cryptographic keys, perform cryptographic operations, and enforce security policies` to protect sensitive data and applications from unauthorized access and tampering.

> Many will find the Azure Key Vault or Azure Managed HSM service to be more appropriate and cost effective..
>
> Customers must have a assigned Microsoft Account Manager and meet the monetary requirement of five million ($5M) USD or greater in overall committed Azure revenue annually to qualify for onboarding and use of Azure Dedicated HSM.

## 6. Azure Key Vault: `designed for securely storing and managing secrets, keys, and certificates`
- Azure Key Vault has two service tiers: Standard, which encrypts with a software key, and a Premium tier, which includes hardware security module(HSM)-protected keys.
- All requests to Azure Key Vault MUST be authenticated. Azure Key Vault supports Microsoft Entra access tokens that may be obtained using OAuth2 
> Zero Trust is a security strategy comprising three principles: "Verify explicitly", "Use least privilege access", and "Assume breach".

### Key Vault key rotation feature:
- requires key management permissions and enables end-to-end zero-touch rotation for encryption at rest for Azure services with customer-managed key (CMK) stored in Azure Key Vault.
- `Assign a "Key Vault Crypto Officer" role to manage rotation policy and on-demand rotation.`
- Key rotation generates a new key version of an existing key with new key material (encryption, decryption, signing, or verification operations).
> Key Permissions to manage rotation policy on keys: `Rotate, Set Rotation Policy, and Get Rotation Policy`
- ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/7ffec5ba-52d1-4780-90a5-1cac48679da5)

> Azure Key Vault enables Microsoft Azure applications and users to store and use several types of secret/key data: keys, secrets, and certificates. Keys, secrets, and certificates are collectively referred to as "objects".
>
> Azure offers several options for storing and managing your keys in the cloud, including Azure Key Vault, Azure Managed HSM, Azure Dedicated HSM, and Azure Payment HSM.


## 7: Provide access to Key Vault keys, certificates, and secrets:
- Azure role-based access control (Azure RBAC) is an authorization system built on Azure Resource Manager that provides centralized access management of Azure resources.
- Azure RBAC model allows users to set permissions on different scope levels: management group, subscription, resource group, or individual resources.
- `To add role assignments`, you must have `Microsoft.Authorization/roleAssignments/write and Microsoft.Authorization/roleAssignments/delete permissions`, such as K`ey Vault Data Access Administrator, User Access Administrator,or Owner.`
> Key Vault resource provider supports two resource types: vaults and managed HSMs.
> Azure `App Service certificate configuration through Azure Portal does not support the Key Vault RBAC permission model`.
> Classic subscription administrator roles like 'Service Administrator' and 'Co-Administrator' are not supported.


## 8. Azure landing zone: ``
- an environment that follows key design principles across eight design areas.
- These design principles accommodate all application portfolios and enable application migration, modernization, and innovation at scale.
- An Azure landing zone uses subscriptions to isolate and scale application resources and platform resources.
- Subscriptions for application resources are called application landing zones, and subscriptions for platform resources are called platform landing zones.

### Important facts about management groups:
```
10,000 management groups can be supported in a single directory.
A management group tree can support up to six levels of depth.
This limit doesn't include the Root level or the subscription level.
Each management group and subscription can only support one parent.
Each management group can have many children.
All subscriptions and management groups are within a single hierarchy in each directory.
```



