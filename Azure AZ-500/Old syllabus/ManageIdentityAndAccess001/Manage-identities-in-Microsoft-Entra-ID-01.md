# Secure Azure solutions with Azure Active Directory:

## MS ENTRA ID aka Active Directory:
- `Cloud-based identity and access management service to secure Azure services & resources.`
- `A database where user cred stored & used to auth users across assets to access services/resources`
- Used by IT Admins, Devs, and CRM for SSO, Credentials, Secure Key, self-service password reset, and MFA, Microsoft 365, Office 365, Azure, or Dynamics CRM Online subscribers, domain controller[^1].
- `Paid licenses (Premium P1 and P2)` enhance Azure AD with self-service options(Pwd reset), advanced administration, and security features.
> "Pay as you go" feature licenses. You can also get licenses for features such as, Microsoft Entra Business-to-Customer (B2C).

## Add new user:
- must be a User Administrator or Global Administrator.
- Azure Portal > ENTRA ID > Users > Create new user or Invite external user
- can also invite the new guest user to collaborate with your organization.
- Delete a user: Azure Active Directory > Users > Azure AD tenant > Delete user.
- ENTRA groups, you can grant access and permissions to a group of users instead of each user.

## Group types:
1. `Security`: Used to manage user and computer access to shared resources.
2. `Microsoft 365`: Provides collaboration opportunities by giving group members access to a shared mailbox, calendar, files, SharePoint sites, and more.

## Group Membership types: `Assigned, Dynamic User & Device`
1. `Assigned: Lets you add specific users as members of a group and have unique permissions.`
2. `Dynamic user: Lets you use dynamic membership rules to automatically add and remove members.` If a member's attributes change, the system looks at your dynamic group rules for the directory to see if the member meets the rule requirements (is added), or no longer meets the rules requirements (is removed).
3. `Dynamic device: Lets you use dynamic group rules to automatically add and remove devices.` If a device's attributes change, the system looks at your dynamic group rules for the directory to see if the device meets the rule requirements (is added), or no longer meets the rules requirements (is removed).


## Secure external identities: 
1. `B2B collaboration` is a feature within `Microsoft Entra External ID that lets you invite guest users` to collaborate with your organization even if they don't have Microsoft Entra ID or an IT department.
![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/3fc154c5-1243-4a06-8fe1-f1fbda0bcd8f)

2. `B2B direct connect - Establish a mutual, two-way trust with another Microsoft Entra organization` for seamless collaboration. `Supported Team channels only.`

3. `Microsoft Entra B2C - Publish modern SaaS apps or custom-developed apps (excluding Microsoft apps) to consumers and customers`, while using Microsoft Entra B2C for identity and access management `with Customer Identity and Access Management (CIAM) solution.`

> Microsoft Entra B2C is built on the same technology as Microsoft Entra External ID, it's a separate service with some feature differences.

4. Microsoft Entra multitenant organization - Collaborate with multiple tenants in a single Microsoft Entra organization via cross-tenant synchronization.


## Implement Microsoft Entra Identity protection:
- Microsoft Entra ID Protection helps organizations detect, investigate, and remediate identity-based risks.
- Can be fed back to a security information and event management (SIEM) tool for further investigation and correlation.
- ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/60459f2e-4ed1-4941-bdb4-0cf85d721ea4)


## Ques:
1. B2B collaboration allows external users to sign in to the organization using their own credentials and access the apps and resources shared with them.

2. Based on the detected risk level, risk-based Conditional Access policies can be enabled to require access controls such as providing a strong authentication method, perform multifactor authentication, or perform a secure password reset.

3. Microsoft Entra entitlement management is an identity governance feature that lets you manage identity and access for external users at scale by automating access request workflows, access assignments, reviews, and expiration.

4. As part of the sign-up flow, a company can provide options for different social or enterprise identity providers.

5. The User Administrator must sign in to the Azure portal in the User Administrator role, navigate to Microsoft Entra ID Users, and select either Create new user or Invite external user from the menu to add a new user to their Microsoft Entra ID organization


























