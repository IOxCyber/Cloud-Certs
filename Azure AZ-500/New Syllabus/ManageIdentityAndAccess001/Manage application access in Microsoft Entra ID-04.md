Access scenarios
Delegated access requires delegated permissions. Both the client and the user must be authorized separately to make the request.

App-only access (Access without a user): Application access is used in scenarios such as automation, and back up. This scenario includes apps that run as background services or daemons.

Types of permissions:
- ![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/65c70f77-d24b-465a-b6fd-0c58fbba8517)

- Application permissions, sometimes called app roles are used in the app-only access scenario, without a signed-in user present. 

Consent
-  Consent is a process where users or admins authorize an application to access a protected resource.
-  User consent happens when a user attempts to sign into an application. The user provides their sign-in credentials.
-  epending on the permissions they require, some applications might require an administrator to be the one who grants consent.
-  Preauthorization allows a resource application owner to grant permissions without requiring users to see a consent prompt for the same set of permissions that have been preauthorized.


 Application registration:
 - To delegate identity and access management functions to Microsoft Entra ID, an application must be registered with a Microsoft Entra tenant.
 - An application object is used as a template or blueprint to create one or more service principal objects. A service principal is created in every tenant where the application is used. Similar to a class in object-oriented programming, the application object has some static properties that are applied to all the created service principals (or application instances).
 - 

 Service principal object: 
 - The security principal defines the access policy and permissions for the user/application in the Microsoft Entra tenant. This enables core features such as authentication of the user/application during sign-in, and authorization during resource access.
Types:
 Application: This type of service principal is the local representation, or application instance, of a global application object in a single tenant or directory. 
 Managed Identity: Managed identities eliminate the need for developers to manage credentials.
 Legacy: 
 > When an application is permitted to access resources in a tenant (upon registration or consent), a service principal object is created. 

Managed Identity:
- provide a secure way to authenticate and access Azure resources without the need to manage credentials manually.

Type:
- System-assigned Managed Identity is automatically created and managed by Azure for an Azure service instance, such as a virtual machine or Azure Function.
- User-assigned Managed Identity is created and managed by the user and can be assigned to one or more Azure resources, allowing them to access Azure services securely.

> Microsoft Enterprise Application Proxy should be configured when there is a need to securely publish internal web applications to external users without exposing the application directly to the internet.


Que:
1.  To provide scoped access to the resources in your web API, you first need to register the API with the Microsoft identity platform.

2.  Microsoft Entra ID supports extensive access management for configured applications, enabling organizations to easily achieve the right access policies ranging from automatic, attribute based assignment (ABAC) or RBAC scenarios through delegation and including administrator management. With Microsoft Entra ID, usage and assignment reporting is fully integrated, enabling administrators to easily report on assignment state, assignment errors, and even usage.

3.  Implementing an authentication mechanism such as OAuth or OpenID Connect is the first step in ensuring that users are authenticated before accessing the web application, thereby protecting it from unauthorized access.

4.  By registering the web API and exposing it through scopes, assigning an owner and app role, the developer can provide permissions-based access to authorized users and client apps that access the API.

5.   Managed identities provide an automatically managed identity in Microsoft Entra ID for applications to use when connecting to resources that support Microsoft Entra authentication. Applications can use managed identities to obtain Microsoft Entra tokens without having to manage any credentials.







