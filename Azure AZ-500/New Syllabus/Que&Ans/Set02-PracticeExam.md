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
39. 















