1. Azure Blueprints:
- allow organizations to create standardized, repeatable sets of Azure resources that comply with organizational standards, facilitating rapid and compliant deployment of cloud environments for development teams.
- Blueprints are a declarative way to orchestrate the artifacts such as: Role Assignments, Policy Assignments, Azure Resource Manager templates (ARM templates), Resource Groups.
- It is `a set of resource groups, policies, role assignments, and ARM template deployments` that can be version controlled, audited, and tracked.
- 

2. Azure Policy: `JSON Format`
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
> Azure Arc, you can extend your policy-based governance across different cloud providers and even to your local datacenters.
>
> Azure Virtual Network Manager (preview) enables you to apply consistent management and security policies to multiple Azure virtual networks (VNets) throughout your cloud infrastructure.


### Azure RBAC permissions in Azure Policy:
- Azure Policy has several permissions, known as operations `2 resource Provider: Microsoft.Authorization & Microsoft.PolicyInsights`
- The Resource Policy Contributor role includes most Azure Policy operations.
- The owner has full rights.
- Both Contributor and Reader have access to all read Azure Policy operations.
> All Policy objects, including definitions, initiatives, and assignments, will be readable to all roles over its scope. 


3. Azure Dedicated HSM:
- offers FIPS 140-2 Level 3-validated cryptographic key storage globally, ensuring exclusive control and high availability across Azure regions with Thales Luna 7 HSM appliances, accessible via VPN for on-premises integration and managed through Thales customer support.
- Azure Dedicated HSM isn't ideal for scenarios where Microsoft cloud services utilize customer-managed encryption keys but lack integration with Azure Dedicated HSM.
- The purpose of a dedicated `Hardware Security Module (HSM) is to securely manage and store cryptographic keys, perform cryptographic operations, and enforce security policies` to protect sensitive data and applications from unauthorized access and tampering.

4. ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/7ffec5ba-52d1-4780-90a5-1cac48679da5)

## Quiz:
- Key Vault is specifically designed for securely storing and accessing secrets, keys, and certificates, providing a centralized management solution for these sensitive data.
- Azure Blueprints automate the deployment of resources, including security policies, RBAC settings, and ARM templates, ensuring a consistent and compliant environment.
- Azure Key Vault supports configuring automatic key rotation policies, enhancing security by regularly updating cryptographic keys without manual intervention.
- Dedicated HSMs provide a high level of security for cryptographic operations and key management by physically isolating and protecting keys from unauthorized access.
  





