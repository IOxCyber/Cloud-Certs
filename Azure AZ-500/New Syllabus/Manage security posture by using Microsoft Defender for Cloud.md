1. Microsoft Entra Connect is an on-premises Microsoft application that's designed to meet and accomplish your hybrid identity goals.
2. Sign-in features not natively supported by Microsoft Entra ID.
3. `Microsoft Entra pass-through authentication allows your users to sign in to both on-premises and cloud-based applications using the same passwords.`
4. Multifactor authentication is a process in which a user is prompted for additional forms of identification during a sign-in event.
5. A `security initiative is a collection of Azure Policy definitions or rules that are grouped together towards a specific goal or purpose`. Security initiatives simplify the management of your policies by grouping a set of policies together, logically, as a single item.
6. Custom initiatives allow organizations to extend the capabilities of Microsoft Defender for Cloud by creating and applying security policies that match their unique operational and security requirements.
7. `Security Administrator`: Has the same view rights as security reader. `Can also update the security policy and dismiss alerts.`
8. `Security reader: Has rights to view Defender` for Cloud items such as recommendations, alerts, policy, and health. `Can't make changes.`
9. Microsoft Defender for Cloud provides tools to assess and ensure compliance with various industry and regulatory standards, helping organizations understand their compliance posture and make necessary adjustments.
10. Integrating hybrid and multicloud environments with Microsoft Defender for Cloud allows organizations to centralize their security management, gaining visibility and control over their distributed resources.
11. You can connect your non-Azure computers in any of the following ways:
```
Onboarding with Azure Arc:
By using Azure Arc-enabled servers (recommended)
By using the Azure portal
Onboarding directly with Microsoft Defender for Endpoint
```
9. Defender for Cloud Usages: 
- Defender for Containers > `At least one Amazon EKS cluster with permission to access to the EKS Kubernetes API server > The resource capacity to create a new Amazon SQS queue > Kinesis Data Firehose delivery stream > Amazon S3 bucket in the cluster's region.`
- Defender for SQL > Microsoft Defender for `SQL enabled on your subscription > An active AWS account, with EC2 instances running SQL Server or RDS Custom for SQL Server > Azure Arc for servers installed on your EC2 instances or RDS Custom for SQL Server.`
- Defender for Servers > Microsoft Defender for `Servers enabled on your subscription > An active AWS account, with EC2 instances > Azure Arc for servers installed on your EC2 instances.`
- Defender Cloud Security Posture Management (CSPM) > `Microsoft Azure subscription > Enable Microsoft Defender for Cloud on your Azure subscription > Connect your non-Azure machines, AWS accounts.`
10. To enable the Azure Arc auto provisioning, you need Owner permission on the relevant Azure subscription.
11. Defender External Attack Surface Management: `includes the discovery of the following kinds of assets`
- helps organizations identify and assess internet-facing assets for vulnerabilities, ensuring they can proactively manage and reduce their attack surface.
```
Domains
Hostnames
Web Pages
IP Blocks
IP Addresses
ASNs
SSL Certificates
WHOIS Contacts
```
- It recursively search for `infrastructure with observed connections to known legitimate assets, known as discovery "seeds"`
- Users that have been assigned either Owner or Contributor roles can create, delete, and edit Defender EASM resources and the inventory assets within it.










