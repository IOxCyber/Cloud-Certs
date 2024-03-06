1. To start using PIM in your directory, you must first enable PIM.
2. To `revoke a stored access policy, you can either delete it, or rename it` by changing the signed identifier.
3. `Changing the signed identifier breaks the associations between any existing signatures and the stored access policy`. Deleting or renaming the stored access policy immediately affects all of the shared access
 signatures associated with it.
4. By allowing users to authenticate to Azure HDInsight, `connectivity should be established through Azure Virtual Networks and a VPN gateway for secure communication.` from On-Prem systems.
5. Ensures that password policies and user logon restrictions apply to user accounts: password hash synchronization with seamless single sign-on (SSO).
6. `Password hash synchronization requires the least effort regarding deployment, maintenance, and infrastructure.` This level of effort typically applies to
 organizations that only need their users to sign in to Office 365, SaaS apps, and other Azure AD-based resources.
7. A `federated authentication system relies on an external trusted system to authenticate users.`
8. For `pass-through authentication, you need one or more (we recommend three) lightweight agents installed on existing servers.`
9. Step: 2 Verify your identity by using multi-factor authentication (MFA)
10. Click Verify my identity to verify your identity with Azure MFA. You'll be asked to pick an account.
 Step 3: Sign up PIM for Azure AD roles
 Once you have enabled PIM for your directory, you'll need to sign up PIM to manage Azure AD roles.
