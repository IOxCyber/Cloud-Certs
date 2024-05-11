1. You must disable CEF messages on the virtual machine and prevent the setting to send CEF messages from being read. Stopping the Syslog daemon on the virtual machine will stop the virtual machine from sending both Syslog and CEF messages. Enabling the Syslog daemon to listen and disabling the Syslog daemon from listening to network messages does not handle the duplication of events.

2. Sign-in logs include information about sign-ins and how resources are used by your users. Audit logs include information about changes applied to your tenant, such as user and group management or updates applied to your tenant’s resources. Activity logs include subscription-level events, not tenant-level activity. Provisioning logs include activities performed by the provisioning service, such as the creation of a group in ServiceNow or a user imported from Workday.

3. Configuring diagnostic settings and sending the logs to Azure Storage meets both the retention time and encryption requirements. Activity log data type is kept for 90 days by default, but the logs are stored by using Microsoft-managed keys. Configuring a workspace retention policy is not the most cost-efficient solution for this. Event Hubs is a real-time event stream engine and is not designed to be used instead of a database or as a permanent store for indefinitely held event streams.

4. Configuring diagnostic settings and sending the logs to Event Hubs will enable log export to the SOC partner. Configuring a workspace retention policy and diagnostic settings and sending the logs to Azure Storage does not export the logs outside of Azure. Installing the SIEM connector enables Microsoft Sentinel to import the logs from the on-premises SIEM.

5. Event Grid can capture key rotation events from Key Vault and trigger an Azure function to generate a new key in SQL and store it in Key Vault. A web app can get events from Event Grid to create and rotate a key, but it costs more than using a Azure Functions. Log Analytics cannot trigger a function.

6. Soft delete is a feature in Azure services that allows for the recovery of deleted resources or data within a specified retention period.

7. Using Event Grid triggers the Microsoft.KeyVault.CertificateNearExpiry event. Key Vault cannot be monitored by using Application Insights. Defender for Key Vault is used to alert for unusual and unplanned activities. Key Vault key expiration cannot be monitored by using action group alerts.

8. Key Vault Managed HSM supports importing keys generated in an on-premise HSM. Also, managed HSM does not store or process customer data outside the Azure region in which the customer deploys the HSM instance. On-premises-generated keys are still managed, after implementing Key Vault Firewall. Enforcing HSM-backed keys does not enforce them to be imported. Disabling the Allow trusted services option does not have a direct impact on key importing.

9. Key Vault Secrets User allows read access to secret content. Key Vault Crypto Officer allows the user to perform actions on encryption keys, not secrets. Key Vault Reader allows the user to read the metadata of key vaults and its certificates, keys, and secrets, but not to read sensitive values, such as secret contents or key material. Key Vault Secrets Officer does not follow the principle of least privilege.

10. To secure access to the otherwise publicly accessible AKS control plane/API server, you can enable and use authorized IP ranges. These authorized IP ranges only allow defined IP address ranges to communicate with the API server. Customizing CoreDNS for AKS, implementing the Open Service Mesh AKS add-on, and configuring Front Door applies to the cluster, not the Kubernetes control plane.

11. Azure Kubernetes Service RBAC Writer has access to secrets. Azure Kubernetes Service RBAC Reader does not have access to secrets. Azure Kubernetes Service RBAC Cluster Admin and Azure Kubernetes Service RBAC Admin do not follow the principle of least privilege.

12. Azure Arc-enabled Kubernetes is the only configuration that includes Kubernetes and can be deployed to AWS.

13. When deploying an AKS cluster, local accounts are enabled by default. Even when enabling RBAC or Microsoft Entra integration, --admin access still exists essentially as a non-auditable backdoor option. To disable local accounts on an AKS cluster, you should use the --disable-local-accounts flag with the az aks create command. The remaining options do not remove local accounts.

14. A SAS is the most secure way to access Azure Files by using REST calls. A shared key allows any user with the key to access data. Microsoft Entra and Active Directory Domain Service (AD DS) are unsupported for REST calls.

15. The Storage Blob Data Reader role uses Microsoft Entra to authenticate. User delegation SAS is a method that uses Microsoft Entra to generate a SAS. Both methods work whether the shared keys are allowed or prevented. Service SAS and account SAS use shared keys to generate.

16. Adding a Microsoft Entra administrator and assigning your account the SQL Security Manager built-in role are prerequisites for enabling Microsoft Entra-only authentication. Selecting Support only Microsoft Entra authentication for this server enforces the Azure SQL logical server to use Microsoft Entra authentication. A connection to the data plane of the logical server is not needed.

17. az sql server ad-only-auth enable enables authentication only through Microsoft Entra. az sql server ad-admin create and az sql mi ad-admin create do not stop other authentication methods. az sql mi ad-only-auth enable enables Microsoft Entra-only authentication for Azure SQL Managed Instance, not Microsoft SQL Server.

18. Enabling Always Encrypted saves the encrypted data and only the client driver can decrypt it. TDE still allows users managing the database to see data. Dynamic data masking does not encrypt anything, it just masks data and still allows users to unmask it at the database level if they have UNMASK permissions. Symmetric key encryption uses keys stored in a SQL database, not the client application.

19. Granting the UNMASK permission to User1 removes the mask from User1 only. Creating a Conditional Access policy for Azure SQL Database, and then granting access is not enough for User1 to see the data, only to sign in. Using the ALTER TABLE statement to edit the masking function affects all users. Using the ALTER TABLE statement to drop the masking function removes the mask altogether.

20. he correct CLI command adds a rule to allow access from the 10.0.2.0/24 subnet to the storage account. The resource group should be for RG2, not RG1. The CLI commands that create network security group (NSG) rules simply allow the entire virtual network to send requests to all storage endpoints.

21. You can configure the network conditions to Conditional Access, ensuring that the location is determined by the public IP address a client provides to Microsoft Entra or the GPS coordinates provided by the Microsoft Authenticator app. You need to configure App Service authentication, specifically the Action to take when request is not authenticated option. Application security groups are unsupported by web apps and configuring a Front Door IP restriction rule does not affect sa1.

22. Adding the web app’s outbound IP addresses to the Azure Cosmos DB account’s allowed IP address range allows access from the web app. Enabling the Allow access from Azure Portal option allows portal access for anyone, including User1. Portal access will still not be allowed after adding the IP address of User1 to the Azure Cosmos DB account’s allowed IP address range or signing in as User1 and selecting Add my current IP to the allowed IP address range.

23. The priority setting for a security rule can be a number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers, which results in lower numbers having a higher priority. Once traffic matches a rule, processing stops. To ensure that other rules cannot override Rule1, you must configure Rule1 to have the highest priority, which means that it must be configured with a priority of 100.

24. You can associate an NSG to a virtual network subnet and network interface only. You can associate zero or one NSGs to each virtual network subnet and network interface on a virtual machine. The same NSG can be associated to as many subnets and network interfaces as you choose.

25. Microsoft.Network/virtualNetworks/virtualNetworkPeerings/write and Microsoft.Network/virtualNetworks/peer/action are the required permissions for resource manager operations.

- Microsoft.ClassicNetwork/virtualNetworks/peer/action is only for classic interface operations. Microsoft.Network/virtualNetworks/join/action is not for peering features. Microsoft.Network/privateDnsZones/* is for DNS.
26. A private link service will allow access from outside the virtual network to an endpoint by using NAT. Since you do not control the IP addressing for other virtual networks, this ensures connectivity even if IP addresses overlap. Once a private link service is used in the load balancer, other users can create a private endpoint on virtual networks to access the load balancer.

27. WebApp1 and VNet1 are in different regions and cannot use regional integration; you can use only gateway-required virtual network integration. To be able to implement this type of integration, you must first deploy a virtual network gateway in VNet1.

28. You can deploy an SQL managed instance to a dedicated virtual network subnet that does not have any resource connected. The subnet can have a service endpoint or can be delegated for a different service. For this scenario, you can deploy managed1 to Subnet2, Subnet3, and Subnet4 only. You cannot deploy managed1 to Subnet1 because Subnet1 has a connected virtual machine.

29. Application Gateway is a web traffic load balancer that enables you to manage traffic to web apps. Application Gateway works at Layer 7, which enables routing based on path or host headers as well as SSL off-loading. Front Door is implemented globally. Traffic Manager is implemented globally and does not allow path-based routing. Azure Load Balancer does not provide path-based routing.  

30. You can enable Facebook or Google accounts to be used to access Azure subscriptions, but only Google identities can be used for B2B, which is required for resource management. You cannot use Twitter or AWS accounts to access Azure resources.  

31. An administrative unit can contain only users, groups, and devices. You can also give role management rights to the resources in an administrative unit. Resource groups cannot contain users, groups, or devices. Management groups can only contain other management groups or subscriptions. Departments are used for billing.

32. By default, guest users can invite other guests. They are unable to read all directory information, register new applications, or read subscriptions.

33. By using a sign-in risk policy with self-remediation, a sign-in risk is detected when users access their account from a different device or location, and self-remediation forces MFA to be required, whereas administer remediation requires admin intervention. User risk policies are triggered for users that have specific risk levels due to issues such as password leaks.

34. When you configure Microsoft Entra MFA, you can configure authentication to use Windows Hello for Business. With this method, users will sign in by using a biometric factor such as a fingerprint or require a PIN to be entered on the device. With Windows Hello for Business, validation is performed locally. Internet access or a mobile network are not needed nor required. The remaining options require a mobile network or a network connection to provide authentication.

35. FIDO2 incorporates the web authentication (WebAuthn) specification. Users can register, and then select a FIDO2 security key at sign-in as their main means of authentication. FIDO2 security keys are typically USB devices but can also use Bluetooth or NFC. OATH software tokens and voice call voice call verification is unsupported as a primary authentication method. Windows Hello for Business can be used as a primary authentication method and can be installed on a device that uses NFC.

36. Windows Hello for Business, security keys, and the Microsoft Authenticator app all support passwordless authentication. The remaining options do not support passwordless authentication.

37. Privileged role administrators can manage PIM. Assigning the Global Administrator role does not follow the principle of least privilege. Security administrators have permissions to manage security-related features. Privileged authentication administrators can set or reset any authentication method, including passwords, for any user, including global administrators.

38. In a static user consent scenario, you must specify all required permissions in the app's configuration in the Azure portal. With incremental user consent and dynamic user consent, you can ask for a bare minimum set of permissions upfront and request more over time as the customer uses additional app features. Admin consent is required when your app needs access to certain high-privilege permissions, but it does not follow the principle of least privilege in this scenario.

39. Using certificate credentials ensures that the credentials are not transmitted during authentication, that they are stored securely, and that the credential usage follows the principle of least privilege.

40. A user-assigned managed identity can be associated with more than one Azure resource. Creating a system-assigned managed identity cannot be pre-authorized. Creating a service principal with password-based authentication or certificate-based authentication involves the use of credentials.

41. After you edit the Collaboration restrictions settings, if you try to invite a user from a blocked domain, you cannot. Security defaults and PIM do not affect guest invitation privileges. By default, the Allow invitations to be sent to any domain (most inclusive) setting is enabled. In this case, you can invite B2B users from any organization.

42. Storage Blob Data Contributor can write to containers. Storage Blob Delegator allows the delegation of access keys. Storage Account Contributor allows the management of storage accounts, but not access to the data. Classic Storage Account Contributor allows the management of classic storage accounts, but not the access to the data.

43. User Access Administrator is the least privileged role that grants access to Microsoft.Authorization/roleDefinition/write. Assigning the Owner role does not follow the principle of least privilege. Contributor does not have access to Microsoft.Authorization/roleDefinition/write. Privileged Role Administrator grants access to manage role assignments in Microsoft Entra, and all aspects of Microsoft Entra Privileged Identity Management (PIM). This is not an RBAC role.

44. The correct CLI command allows the application to provide SSO for Microsoft Entra users in any tenant. The CLI commands requiring a web app do not create a gallery entry for the application and configuring the sign-in audience to Microsoft Entra and personal Microsoft accounts does not restrict users to only Azure accounts.
  

  
