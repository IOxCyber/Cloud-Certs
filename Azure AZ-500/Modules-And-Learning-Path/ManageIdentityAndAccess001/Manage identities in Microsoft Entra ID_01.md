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








