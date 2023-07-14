# Unit 3: Deploy AD protection

## Identity Protection:
- a tool that allows organizations to automate the detection and remediation of identity-based risks
- 3 key tasks: Automate the detection > Investigate Risk > Export Risk Detection data.
- can configure risk-based policies in Azure Active Directory (Azure AD) that automatically respond to risky behaviors
- 3 Policies in AD: User risk, Sign-in risk, MFA registration Policy.
- Also choose the threshold for `risk level - low and above, medium and above, or high.`

## User risk policy:
- Applied to user sign-ins.
- Automatically respond based on a specific user’s risk level
- Provide the condition (risk level) and action (block or allow)

## Sign-in Policy:
- Sign-in Risk Policy supports `Location based access/block`,
- `Conditional Access policies` by default apply to browser-based applications.

## Deploy MFA:
- <img width="500" alt="image" src="https://github.com/cybersome/Azure-Certifications-Guides/assets/40174034/121301af-ffba-4ae9-a3fe-5d29cf6d5ced">
- Method: Call, Text to phone, Notification through mobile app, Verification code from mobile app.
- Features: Block and unblock users, Fraud alerts, OATH tokens, Trusted IPs for Federated Users[^1].
> Remember, you can only enable MFA for organizational accounts stored in Azure Active Directory. These are also called work or school accounts.


## Azure AD conditional access:
- a feature in Microsoft Azure that lets you set rules to control how people access your organization's data.
- define conditions like where they're accessing from(Location), what type of device they're using(Device compliance), and if there are any security risks(User sign-in risk), User group membership.
- with an `Azure AD Premium license`.
- Conditional access comes with six conditions: user/group, cloud application, device state, location (IP range), client application, and sign-in risk.
> The Users and Groups condition is mandatory in a conditional access policy. In your policy, you can either select All users or select specific users and groups.

## Implement access reviews:
- enable organizations to efficiently manage group memberships, access to enterprise applications, and role assignments.
- Azure AD Premium P2 licenses are not required for users with the Global Administrator or User Administrator roles that set up access reviews, configure settings, or apply the decisions from the reviews.


## Labs:
- Access reviews. Access reviews enable organizations to efficiently manage group memberships, access to enterprise applications, and role assignments. User's access can be reviewed on a regular basis to make sure only the right people have continued access.
- Global Administrator. To use Identity Protection a user must be in one of these roles. Each role has different privileges but only the Global Administrator can reset a user’s password.
- Identity Protection can recognize logins from unexpected locations and times.
- Confirming that a user was compromised is a valid option when reviewing identity projection reports.
- It is possible to force a user, group or users, or all users to use MFA with a conditional access policy. 
- Identity Protection helps you configure risk-based conditional access for your applications to protect them from identity-based risks. `Azure Active Directory Premium P2`







[^1]: Federated identity allows authorized users to access multiple applications and domains using a single set of credentials.
