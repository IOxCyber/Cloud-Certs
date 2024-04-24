## Microsoft Entra authentication:
```
Self-service password reset
Microsoft Entra multifactor authentication
Hybrid integration to write password changes back to on-premises environment
Hybrid integration to enforce password protection policies for an on-premises environment
Passwordless authentication
```

## Self-service password reset works in the following scenarios:
```
Password change - when a user knows their password but wants to change it to something new.
Password reset - when a user can't sign in, such as when they forgot password, and want to reset their password.
Account unlock - when a user can't sign in because their account is locked out and want to unlock their account.
```

## Microsoft Entra multifactor authentication:
```
Something you know, typically a password.
Something you have, such as a trusted device that is not easily duplicated, like a phone or hardware key.
Something you are - biometrics like a fingerprint or face scan.
```

## Microsoft Entra multifactor authentication settings are available in the Azure portal:
![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/7806eec0-8377-490c-8933-cbecbba7f652)

> Microsoft Entra ID supports the use of OATH TOTP (Time-based One Time Password) SHA-1 tokens that refresh codes every 30 or 60 seconds. You can purchase these tokens from the vendor of your choice.


## Implement passwordless authentication:
- Microsoft global Azure and Azure Government offer the following three passwordless authentication options that integrate with Microsoft Entra ID:
```
Windows Hello for Business.
Microsoft Authenticator.
Fast Identity Online2 (FIDO2) security keys.
```


## Implement single sign-on (SSO):
- ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/fe543ab7-afac-4bd2-b8e2-73efe823a123)

## The following SSO protocols are available to use:
1. OpenID Connect and OAuth - Choose OpenID Connect and OAuth 2.0 if the application you're connecting to supports it.
2. SAML - Choose SAML whenever possible for existing applications that don't use OpenID Connect or OAuth.
3. Password-based - Choose password-based when the application has an HTML sign-in page. Password-based SSO is also known as password vaulting.
4. Linked - Choose linked when the application is configured for SSO in another identity provider service.
5. Disabled - Choose disabled SSO when the application isn't ready to be configured for SSO.
6. Integrated Windows Authentication (IWA) - Choose IWA single sign-on for applications that use IWA, or for claims-aware applications.
7. Header-based - Choose header-based single sign-on when the application uses headers for authentication.

## Microsoft Entra Verified ID:
- Decentralized architectures can be used to enhance existing solutions and provide new capabilities.

## Configure Microsoft Entra Verified ID:
- ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/e9d55a6c-05d3-40ba-8db0-8726bf80b7a9)


## Ques:
- The DC Agent service processes password validation requests from the password filter DLL of the DC Agent using the current locally available password policy and returns the result of pass or fail.
- Microsoft Entra multifactor authentication adds additional security over only using a password when a user signs in by prompting the user for additional forms of authentication, such as responding to a push notification or entering a code from a software or hardware token.
- The Linked option lets you configure the target location when a user selects the application in your organization's end user portals.
- It's important to have processes in place to renew certificates prior to their expiration, and to identify the right roles and email distribution lists involved with managing the lifecycle of the signing certificate. The certificate duration can be changed in the Microsoft Entra admin center.
- The purpose of using Microsoft Entra Verified ID service for verification is to unlock privileges to subjects that possess verified credential expert cards.
- The purpose of using Microsoft Entra Verified ID service for verification is to unlock privileges to subjects that possess verified credential expert cards.





























