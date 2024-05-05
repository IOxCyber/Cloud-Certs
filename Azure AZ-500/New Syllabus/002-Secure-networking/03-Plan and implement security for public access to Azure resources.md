## Azure Firewall Manager:
- A security management service that provides central security policy and route management for cloud-based security perimeters.
- Firewall Manager can provide security management for two network architecture types:
- - A. Secured virtual hub (Microsoft-managed resource) & B. Hub virtual network (create and manage yourself.)
- `Azure Firewall Policies can be used across regions. For example, you can create a policy in West US, and use it in East US.`


## Azure Web Application Firewall:
- Web Application Firewall (WAF) provides centralized protection of your web applications from common exploits and vulnerabilities.
- WAF can be deployed with Azure Application Gateway, Azure Front Door, and Azure Content Delivery Network (CDN) service

## DDos Attack:
- DDoS attack attempts to exhaust an application's resources, making the application unavailable to legitimate users.
- Azure DDoS Protection protects at layer 3 and layer 4 network layers. For web applications protection at layer 7, you need to add protection at the application layer using a WAF offering.

### Tiers:
1. `Azure DDoS Network Protection`, combined with application design best practices, provides enhanced DDoS mitigation features to defend against DDoS attacks.
2. `DDoS IP Protection` is a pay-per-protected IP model. DDoS IP Protection contains the same core engineering features as DDoS Network Protection, but will differ in the following value-added services: DDoS rapid response support, cost protection, and discounts on WAF



## Points:
- Elliptic Curve Cryptography (ECC) certificates work with App Service
- After you add a private certificate to an app, the certificate is stored in a deployment unit that's bound to the App Service plan's resource group, region, and operating system combination, internally called a webspace.
- The Azure Application Gateway infrastructure includes the virtual network, subnets, network security groups (NSGs), and user-defined routes (UDRs).
