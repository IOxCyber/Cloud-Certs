## Microsoft Entra Permissions Management:
- Cloud infrastructure entitlement management (CIEM) solution that provides comprehensive visibility into permissions assigned to all identities.
- Permissions Management detects, automatically right-sizes and continuously monitors unused and excessive permissions.
- Allows customers to address three key use cases:
  - Discover: Customers can assess permission risks by evaluating the gap between permissions granted and permissions used.
  - Remediate: Customers can right-size permissions based on usage, grant new permissions on-demand, and automate just-in-time access for cloud resources.
  - Monitor: Customers can detect anomalous activities with machine learning-powered (ML-powered) alerts and generate detailed forensic reports.
  
## Access Review:
- User access can be reviewed regularly to make sure only the right people have continued access.
- Using this feature requires Microsoft Entra ID Governance subscriptions for your organization's users.
- Access reviews in Microsoft Entra ID, part of Microsoft Entra, enable organizations to efficiently manage group memberships, access to enterprise applications, and role assignments.

## Configure Azure role permissions:
- `To assign Azure roles, you must have: Microsoft.Authorization/roleAssignments/write permissions,` such as User Access Administrator or Owner.
- Create a new custom role to grant access to manage app registrations. `Microsoft Entra admin center`

## Configure Microsoft Entra Privileged Identity Management:
- Privileged Identity Management provides time-based and approval-based role activation.
![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/d813ae53-f516-4daf-b3e6-2fb6fb16024a)

## Notes:
1. `Microsoft Entra ID Governance is an identity governance solution` that enables organizations to improve productivity, strengthen security and more easily meet compliance and regulatory requirements.
2. Conditional Access policies are enforced after first-factor authentication is completed. Conditional Access isn't intended as an organization's first line of defense for scenarios like denial-of-service (DoS) attacks, but it can use signals from these events to determine access.

## Common signals:
- ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/a43b0e03-5253-469a-b65b-d98938badee0)

## Commonly applied policies:
```
Requiring multifactor authentication for users with administrative roles
Requiring multifactor authentication for Azure management tasks
Blocking sign-ins for users attempting to use legacy authentication protocols
Requiring trusted locations for Microsoft Entra ID multifactor authentication registration
Blocking or granting access from specific locations
Blocking risky sign-in behaviors
Requiring organization-managed devices for specific applications
```

### Management Groups:
- Management groups provide a governance scope above subscriptions. You organize subscriptions into management groups; the governance conditions you apply cascade by inheritance to all associated subscriptions.
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/6df0f033-526d-403e-aa7a-3b4217437223)
- Management groups aren't currently supported in Cost Management features for Microsoft Customer Agreement (MCA) subscriptions.
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/4cffcedb-51d2-4b10-a544-55ec35908fa2)


## Que:
1. To add a role assignment for a new user: Select the Constrained recommended option under Delegation type on the Conditions tab.
2. The first step to enable Permissions Management is to ensure they have a Microsoft Entra ID tenant and are eligible for or have an active assignment to the Permissions Management Administrator role.
3. `to grant access to a specific resource group` in Azure: The first step is to identify the needed scope by `searching for the resource group` in the Azure portal.
4. Microsoft Entra Privileged Identity Management `PIM can be used to create access reviews for privileged access to Azure resources and Microsoft Entra ID roles.`
5. The `two main steps in the role assignment process` are `selecting the role to assign and adjusting the role settings and duration.`


 








