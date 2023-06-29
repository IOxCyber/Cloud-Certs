# Unit 2:

## Deploy Azure AD connect:
- Hybrid Identity is the process of connecting your on-premises Active Directory with your Azure Active Directory.

## Authentication methods:
- Cloud Authentication (Azure AD password hash Sync, Azure AD Pass-through Auth)
- Federated Authentication (Auth by on-premises Active Directory Federation Services (AD FS))

- Azure AD Connect features:
  - Password hash synchronization (sync & use hash of a user on on-prem & AD) `same sign-in, not single sign-on`
    - Use this feature to sign in to Azure AD services like Microsoft 365, Microsoft Intune, CRM Online, and Azure Active Directory Domain Services (Azure AD DS).
    - This option just shares the password hash between two federated systems.
      
  - Pass-through authentication (Same pwd can be used on on-prem & AD)
    - alternative to Azure AD Password Hash Synchronization.
    - Supports user sign-in into all web browser-based app
    - PTA is a free feature uses 

  - Federation integration (used to configure a hybrid environment using an on-premises AD FS infrastructure)
   - Federation is a collection of domains that have established trust.
   - You can federate your on-premises environment with Azure AD and use this federation for authentication and authorization.
    
## Password writeback:
- a feature enabled with Azure AD Connect that allows password changes in the cloud to be written back to an existing on-premises directory in real time.

> Azure AD supports `SAML 2.0*, OpenID Connect*, OAuth 2.0*, and WS-Federation` protocols for authentication and authorization.

















