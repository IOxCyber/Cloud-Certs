1. You can enable `Facebook or Google accounts to be used to access Azure subscriptions,` but `only Google identities can be used for B2B`, No Twitter or AWS accounts to access Azure resources.
2. An `administrative unit can contain only users, groups, and devices`. You can also give role management rights to the resources in an administrative unit.
3. `Resource groups cannot contain users, groups, or devices.`
4. `Management groups can only contain other management groups or subscriptions`. Departments are used for billing.
5. By default, `guest users can invite other guests`. They are unable to read all directory information, register new applications, or read subscriptions.
6. `Sign-in risk is detected when users access their account from a different device or location`, and `self-remediation forces MFA to be required.`
7. Administer remediation requires admin intervention. User risk policies are triggered for users that have specific risk levels due to issues such as password leaks.
8. `FIDO2 security keys are typically USB devices but can also use Bluetooth or NFC.` and `Windows Hello for Business can be used as a primary authentication method and can be installed on a device that uses NFC.`
> FIDO2 security keys are an unphishable standards-based passwordless authentication method that can come in any form factor.
9. `FIDO2, Authenticator, Windows Hello support passwordless methods`.

***

10. `Privileged role administrators can manage PIM.` Assigning the Global Administrator role does not follow the principle of least privilege.
11. Security administrators have permissions to manage security-related features.
12. `Privileged authentication administrators` can set or reset any authentication method, passwords, `for any user, including global administrators.`
13. `Static user consent must specify all required permissions in the app's configuration in the Azure portal.`
14. With `incremental user consent and dynamic user consent, you can ask for a bare minimum set of permissions upfront and request more over time` as the customer uses additional app features.
15. Admin consent is required when your app needs access to certain high-privilege permissions, but it does not follow the principle of least privilege in this scenario.
16. A `user-assigned managed identity can be associated with more than one Azure resource.`
17. Creating a `system-assigned managed identity cannot be pre-authorized.`
18. Creating a service principal with password-based authentication or certificate-based authentication involves the use of credentials.
19. `Storage Blob Data Contributor can write to containers.`
20. Storage Blob Delegator allows the delegation of access keys.

***

21. Storage Account Contributor allows the management of storage accounts, but not access to the data.
22. Classic Storage Account Contributor allows the management of classic storage accounts, but not the access to the data.
23. `User Access Administrator is the least privileged role that grants access to Microsoft.Authorization/roleDefinition/write.`
24. Assigning the `Owner role does not follow the principle of least privilege`.
25. `Contributor does not have access to Microsoft.Authorization/roleDefinition/write.`
26. `Privileged Role Administrator is not an RBAC role.` and grants access to manage role assignments in Microsoft Entra, and all aspects of Microsoft Entra Privileged Identity Management (PIM).
27. `TCP, UDP, ICMP, ESP, AH, or Any. The ESP and AH protocols aren't currently available via the Azure portal` but can be used via ARM templates.
28. The priority setting for a security rule can be a number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers, which results in lower numbers having a higher priority. Once traffic matches a rule, processing stops. `100 is Smallest & has high priority > Other rules after it till 4096`
29. You can `associate an NSG to a virtual network subnet and network interface only.` You can associate zero or one NSGs to each virtual network subnet and network interface on a virtual machine. The same NSG can be associated to as many subnets and network interfaces as you choose.
30. Default security rules:
- Inbound: AllowVNetInBound, `AllowAzureLoadBalancerInBound,` DenyAllInbound.
- Outbound: AllowVnetOutBound, `AllowInternetOutBound,` DenyAllOutBound`
> You `can't remove the default rules, but you can override them by creating rules with higher priorities.`

###

31. Microsoft.Network/virtualNetworks/virtualNetworkPeerings/write and Microsoft.Network/virtualNetworks/peer/action are the required permissions for resource manager operations.
32. Microsoft.ClassicNetwork/virtualNetworks/peer/action is only for classic interface operations. Microsoft.Network/virtualNetworks/join/action is not for peering features.
33. Microsoft.Network/privateDnsZones/* is for DNS.
34. A private link service will allow access from outside the virtual network to an endpoint by using NAT.
35. `For different regions, cannot use regional integration; you can use only gateway-required virtual network integration.` To be able to implement this type of integration, you must first deploy a virtual network gateway in VNet1.
36. `Service Endpoint provides secure and direct access to Azure services` over a private connection `within a subnet of your virtual network`
37. Private Link allows you to access Azure Platform-as-a-Service (PaaS) services privately from your virtual network. It enables you to connect to services over a private endpoint within your VNet.
### > Service Endpoints are typically used for accessing Azure services like Azure Storage, Azure SQL Database, and Azure Cosmos DB from within a VNet, `while Private Link is more suitable for accessing PaaS services like Azure Blob Storage, Azure SQL Database, Azure App Service, etc., privately from your VNet.`
38. `Azure backbone network is the underlying infrastructure that connects all Azure data centers globally.` It's a high-speed, resilient network that ensures reliable and low-latency connectivity between Azure services, regions, and data centers.
39. `Azure SQL managed instance requires an empty subnet`, meaning it cannot have any existing resources deployed within the subnet. This ensures that the managed instance has exclusive use of the subnet's IP address space and does not conflict with other resources.
40. `Application Gateway is a web traffic load balancer that enables you to manage traffic to web apps.` Application Gateway works at Layer 7, which enables routing based on path or host headers as well as SSL off-loading.

###

41. Front Door is implemented globally. Azure Front Door is a global, scalable, and secure entry point for web applications, APIs, and content delivery, provides Global Load Balancing, Web Application Firewall (WAF), SSL Offloading, Traffic Routing, Session Affinity, Analytics and Monitoring.
42. `Traffic Manager is an Azure service that enables you to control the distribution of user traffic to your specified endpoints`, which can be Azure resources or external resources. It works by directing incoming traffic to the closest or best-performing endpoint based on the chosen routing method (e.g., priority, weighted, geographic).`Traffic Manager is implemented globally and does not allow path-based routing.`
43. Azure Load Balancer does not provide path-based routing (involves directing traffic to specific endpoints based on the URL path specified in the request. )
44. `Azure Kubernetes Service RBAC Writer has access to secrets.` Azure Kubernetes Service RBAC Reader does not have access to secrets. Azure Kubernetes Service RBAC Cluster Admin and Azure Kubernetes Service RBAC Admin do not follow the principle of least privilege.
45. `Azure Arc-enabled Kubernetes is the only configuration that includes Kubernetes and can be deployed to AWS.`
46. A `SAS is the most secure way to access Azure Files by using REST calls`. A shared key allows any user with the key to access data. Microsoft Entra and Active Directory Domain Service (AD DS) are unsupported for REST calls.
47. A service shared access signature (SAS) delegates access to a resource in just one of the storage services: Azure Blob Storage, Azure Queue Storage, Azure Table Storage, or Azure Files.
48. Always Encrypted saves the encrypted data and only the client driver can decrypt it. TDE still allows users managing the database to see data.
49. Dynamic data masking does not encrypt anything, it just masks data & user can use UNMASK permissions to see the data.
50. `Append is used to add fields to existing properties.` Modify is used to add, update, or remove properties, it does not ensure that a field has value. `DeployIfNotExists is used to deploy resources.` Audit is used to check for compliance.

###

51. `Policies Can be assigned at the management group, subscription, resource group, or resource level.`
52. `Initiatives (gr. of Policies, applied at higher level) assigned at the management group or subscription level, also at the resource group.`
53. Defender EASM applies the crawling technology of Microsoft to discover assets that are related to your known online infrastructure and actively scans these assets to discover new connections over time.
54. `Vulnerability assessment is supported for Azure SQL Database, Azure SQL Managed Instance, and Azure Synapse Analytics.`
55. Stopping the Syslog daemon on the virtual machine will stop the virtual machine from sending both Syslog and CEF messages.
56. Configuring diagnostic settings and sending the logs to Azure Storage meets both the retention time and encryption requirements.
57. `Event Grid can capture key rotation events from Key Vault and trigger an Azure function to generate a new key` in SQL and store it in Key Vault.
58. `Purge protection prevents keys from being permanently deleted for a certain number of days`, and software-protected key vaults are less expensive than HSM-protected key vaults.
59. `Soft delete allows for the recovery of deleted resources or data within a specified retention period.`
60. Defender for Key Vault is used to alert for unusual and unplanned activities. Key Vault key expiration cannot be monitored by using action group alerts.

###

61. Key Vault Managed HSM supports importing keys generated in an on-premise HSM. Also, managed HSM does not store or process customer data outside the Azure region in which the customer deploys the HSM instance.
62. `Key Vault Secrets User allows read access to secret content.`
63. `Key Vault Crypto Officer (perform actions on encryption keys)` allows the user to perform actions on encryption keys, not secrets.
64. `Key Vault Reader (read Metadata)` allows the user to read the metadata of key vaults and its certificates, keys, and secrets, but not to read sensitive values, such as secret contents or key material.
65. `Key Vault Secrets Officer does not follow the principle of least privilege.`

E.O.F
