## Microsoft Defender for Cloud: `Development security operations (DevSecOps), cloud security posture management (CSPM), cloud workload protection platform (CWPP) solution`
- Cloud-native application protection platform (CNAPP) comprises security measures and practices designed to protect cloud-based applications from various cyber threats and vulnerabilities.
- Provides tools to assess and ensure compliance with various industry and regulatory standards, helping organizations understand their compliance posture and make necessary adjustments.
> When you enable Defender for Cloud, you automatically gain access to Microsoft Defender XDR.
- Microsoft `Defender for Storage, Databases, Containers, App Service, Key Vault, Resource Manager, and DNS.`
- Microsoft Defender for Cloud is a multicloud security solution. It `provides native CSPM capabilities for Azure, AWS, and Google Cloud environments and supports threat protection across these platforms.` You can also connect non-Azure workloads in hybrid scenarios by using Azure Arc.

## Defender for Cloud combines the capabilities of:
```
A development security operations (DevSecOps) solution that unifies security management at the code level across multicloud and multiple-pipeline environments
A cloud security posture management (CSPM) solution that surfaces actions that you can take to prevent breaches
A cloud workload protection platform (CWPP) with specific protections for servers, containers, storage, databases, and other workloads.
```

## Azure Arc:
- You can connect your non-Azure computers in any of the following ways:
```
Onboarding with Azure Arc:
By using Azure Arc-enabled servers (recommended)
By using the Azure portal
Onboarding directly with Microsoft Defender for Endpoint
```
> To enable the Azure Arc auto-provisioning, you need Owner permission on the relevant Azure subscription.

## Defender External Attack Surface Management: `includes the discovery of the following kinds of assets`
- Helps organizations identify and assess internet-facing assets for vulnerabilities, ensuring they can proactively manage and reduce their attack surface.
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

## Protect cloud workloads:
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/ed432c13-f28a-44e1-bad1-f7b1401f2046)


## Defender for Cloud Usages: 
- Defender for Containers > `At least one Amazon EKS cluster with permission to access to the EKS Kubernetes API server > The resource capacity to create a new Amazon SQS queue > Kinesis Data Firehose delivery stream > Amazon S3 bucket in the cluster's region.`
- Defender for SQL > Microsoft Defender for `SQL enabled on your subscription > An active AWS account, with EC2 instances running SQL Server or RDS Custom for SQL Server > Azure Arc for servers installed on your EC2 instances or RDS Custom for SQL Server.`
- Defender for Servers > Microsoft Defender for `Servers enabled on your subscription > An active AWS account, with EC2 instances > Azure Arc for servers installed on your EC2 instances.`
- Defender Cloud Security Posture Management (CSPM) > `Microsoft Azure subscription > Enable Microsoft Defender for Cloud on your Azure subscription > Connect your non-Azure machines, AWS accounts.`

> Sign-in features not natively supported by Microsoft Entra ID.
> Microsoft Entra `pass-through authentication allows your users to sign in to both on-premises and cloud-based applications using the same passwords.`

## 5. A `security initiative is a collection of Azure Policy definitions or rules that are grouped together towards a specific goal or purpose`. Security initiatives simplify the management of your policies by grouping a set of policies together, logically, as a single item.
- Custom initiatives allow organizations to extend the capabilities of Microsoft Defender for Cloud by creating and applying security policies that match their unique operational and security requirements.
- `Security Administrator`: Has the same view rights as security reader. `Can also update the security policy and dismiss alerts.`
- `Security reader: Has rights to view Defender` for Cloud items such as recommendations, alerts, policy, and health. `Can't make changes.`


## Secure score in Defender for Cloud: `The higher the score, the lower the identified risk level is.`
- The secure score aggregates security findings into a single score(<100) so that you can assess, at a glance, your current security situation. 


