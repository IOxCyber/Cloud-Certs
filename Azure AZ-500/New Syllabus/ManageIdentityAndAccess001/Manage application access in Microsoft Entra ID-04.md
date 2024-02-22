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

 














