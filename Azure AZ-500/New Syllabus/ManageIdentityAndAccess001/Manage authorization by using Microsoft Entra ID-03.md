## Configure Azure role permissions:
- To assign Azure roles, you must have: Microsoft.Authorization/roleAssignments/write permissions, such as User Access Administrator or Owner.
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

## Que:
1. To add a role assignment for a new user: Select the Constrained recommended option under Delegation type on the Conditions tab.
2. The first step to enable Permissions Management is to ensure they have a Microsoft Entra ID tenant and are eligible for or have an active assignment to the Permissions Management Administrator role.
3. `to grant access to a specific resource group` in Azure: The first step is to identify the needed scope by `searching for the resource group` in the Azure portal.
4. Microsoft Entra Privileged Identity Management `PIM can be used to create access reviews for privileged access to Azure resources and Microsoft Entra ID roles.`
5. The `two main steps in the role assignment process` are `selecting the role to assign and adjusting the role settings and duration.`










