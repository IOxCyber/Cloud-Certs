## Zero Trust model:
- Based on the principle of `never trust, always verify`.
- Requires that all components—user identity, device, network, and applications—be validated.
- Security policy enforcement is at the center of a Zero Trust architecture.
- `Principles: Verify explicitly, Use least privilege access, Assume breach`
> tional Institute of Standards and Technology has a Zero Trust Architecture, NIST 800-207
- Azure AD Privileged Identity Management as the service to help protect your privileged accounts.

 ## PIM features: & `Activation settings`
 - just-in-time privileged access
 - `Duration` / time-bound access to resources by using start and end dates
 - `approval to activate` privileged roles
 - `Enforcing Azure Multi-Factor Authentication (MFA)`
 - `justification to understand why users activate`.
 - Getting notifications when a user is assigned a privilege
 - Conducting access reviews
 - audit history for an internal or external audit

> Roles not managed in PIM: Roles within Exchange Online or SharePoint Online
###
- To use PIM: Azure AD `Premium P2, Enterprise Mobility + Security (EMS) E5, or Microsoft 365 M5`
- `Elevated access includes job roles that need greater access`, including support, resource administrators, resource owners, service administrators, and global administrators. 
- <img width="500" alt="image" src="https://github.com/cybersome/Azure-Certifications-Guides/assets/40174034/3447a663-6bab-4ddb-ae03-51dcc27758b5">
- Permanent administrators have persistent elevated role connections.
- Eligible administrators have privileged access only when they need it
  

## Quiz:
- Global Admin. Of the options listed, only the Global Admin role has the permission to enable PIM.
- Assign the user the Contributor role at the resource group level. This gives the new hire the least privileges necessary for the role.
- Resource locks prevent other users in your organization from accidentally deleting or modifying critical resources.
- Assign the user to the Contributor role on VM3. This means the user won't have access to VM1 or VM2
- Management groups can be used to organize and manage subscriptions.
- Resources can easily be moved between resource groups, so this is correct.

## Policy permissions and custom policies:
- Azure Policy has several permissions, known as operations, in two resource providers: 1. Microsoft.Authorization & 2.Microsoft.PolicyInsights
- RBAC is an authorization system built on Azure Resource Manager that provides fine-grained access management of Azure resources.
> a subscription is associated with only one Azure AD tenant. Also note that a resource group can have multiple resources but is associated with only one subscription. Lastly, a resource can be bound to only one resource group.
- All Policy objects, including definitions, initiatives, and assignments, will be readable to all roles over its scope.
- <img width="500" alt="image" src="https://github.com/cybersome/Azure-Certifications-Guides/assets/40174034/2ca33b88-5943-4e0f-a5cd-bef8f44c45db">
> To create or delete management locks, you must have access to **Microsoft.Authorization/***or Microsoft.Authorization/locks/* actions.  
- As an administrator, you may need to lock a subscription, resource group, or resource.






