1. Network Security Groups (NSG):
- Network traffic can be filtered to and from Azure resources in an Azure virtual network.
- provide a distributed firewall for controlling inbound and outbound traffic in a virtual network.

> Azure Virtual Networks provide private and isolated network connectivity within the Azure cloud infrastructure.

## To enable external connectivity to Azure resources from the public internet:
- Assign a public IP address to specific Azure resources
- Deploy a Load Balancer[^1], gateway 
- Configure Network Security Group (NSG) Rules
- Implement Network Address Translation (NAT)

2. Deploy a Network Security Groups implementation:
- 100 NSGs per region(Max 500) per subscription, 200 rules in a single NSG(Max 400). 
- You can `apply only one NSG to a VM, subnet, or network adapter.`
- You can `apply an NSG to multiple resources.`
- <img width="380" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/76fc3bb7-0a25-435f-947a-bff9e89a5def">

  
3. Application Security Groups:
- a feature that `allows you to define and manage network security policies based on application-level` constructs rather than individual IP addresses.
- To `group Azure resources into logical groups based on the application` they belong to.
- Application-Centric Security, Network Security Group Integration, Cross-Subscription, and Cross-Region Support.
> ASGs in Azure are used with NSGs. ASGs alone do not provide network security capabilities, they are designed to complement NSGs and enhance their functionality.
- <img width="303" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/b22aa549-b4d0-4fbf-bcc1-5a8985d19bd8">


4. Service Endpoints:
- `Enables secure and direct connectivity between virtual networks and Azure platform services over the **Azure network**`.
- Enables resources to access Azure services without the need to traverse the public internet.
- <img width="500" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/3d20b64a-0a74-41af-8cc0-01fccdf82e57">

5. Private Links:
- Networking feature that `allows secure access to Azure services and customer-owned[^2] services over an Azure virtual network.`
- Allows Private Connectivity, Secure Data Transfer, isolation within your virtual network, and Service Publishing.
- Use Azure Private Link to securely access Azure PaaS (Platform-as-a-Service) services such as Azure Storage, Azure SQL Database, Azure Cosmos DB, Azure Data Lake Storage, Azure Key Vault, and more.
- to establish private connectivity between your virtual network and on-premises resources.
- To consume services from trusted partners or vendors without exposing them to the public internet and maintaining a private and secure connection.
- <img width="500" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/fae2850e-8b27-4ef3-9e52-202058a63c68">
- Private Link Service, Private Link Endpoint, Network Integration, Private IP Addressing, Security and Access Control, Service Publishing.

6. Azure Application Gateway: `web traffic load balancer and application delivery controller`
- Used for Web traffic load balancer and application delivery controller.
- Operates at the application layer of the network stack & transport layer (OSI layer 4 - TCP and UDP)
- <img width="500" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/df1655df-2813-4472-b158-4661810a4a3e">
- Features: `Secure Sockets Layer (SSL/TLS) termination, Autoscaling(Up&Down), Static VIP, Web Application Firewall, Ingress Controller for AKS, URL-based routing`


7. WAF (Web Application Firewall): `Fully Managed cloud-based firewall service`
- Protects web applications from various types of cyber threats and attacks.
- Traffic Monitoring, Threat Detection, Real-Time Blocking, Attack Mitigation, and Custom Security Policies.
- <img width="500" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/43ff3085-625a-48a3-b8ed-0638c2ac3ff1">



8. Azure Front Door: `global content delivery network (CDN)[^3] and application delivery service`
- `Acts as a gateway between users and your web applications`, improving their performance, availability, and security. 
- Features: `Load Balancing, Intelligent Routing, SSL/TLS termination, Traffic Analytics and Monitoring`


> Azure WAF is primarily focused on web application security.
> Azure Front Door focuses on global content delivery(CDN) and intelligent routing.
> Azure Application Gateway specializes in advanced application-level load balancing and traffic management.
>
> An application delivery services are Azure Front Door or Azure Application Gateway.

9. Express Route:
- a direct, private connection from your WAN (not over the public Internet) to Microsoft Services/Azure resources.
- ExpressRoute provides a dedicated, secure, and high-performance connectivity option for extending your on-premises network to Azure.
- <img width="500" alt="image" src="https://github.com/IOxCyber/Azure-Certs/assets/40174034/878f27bc-4e0c-4fa4-b1b6-cb5f510c9f67">


## Other connectivity options to access Azure Services:
```
Public Internet Access
Site-to-Site VPN, on-premises network to Azure virtual networks
Point-to-Site VPN, points = individual client devices
Azure Virtual WAN, remote locations to Azure
Azure VPN Gateway:
supports both Site-to-Site and Point-to-Site VPN
cross-premises connectivity between your on-premises network and Azure
```
> Cross-premises connectivity refers to establishing a network connection between different locations, typically between an organization's on-premises network and a cloud environment like Azure







[^1]: Azure Load Balancer and Application Gateway can act as frontend endpoints that accept incoming connections from the public internet and distribute the traffic to the appropriate resources within your virtual network.

[2]: Customer-owned services refer to services or resources that are owned and managed by the customer themselves. These services can be hosted in Azure or in an on-premises environment. 

[3]: Global content delivery network (CDN) refers to a distributed network of servers located around the world that stores copies of web content(images, videos, scripts, and other static or dynamic files) & delivers to end-users with high performance and low latency.

[4]: refers to a service or set of services that optimize the delivery of web applications to end-users. These services provide various capabilities to enhance the performance, availability, and security of web applications, ensuring a better user experience.
or
An application delivery service in Azure is like a specialized team that helps ensure your web applications reach users quickly, reliably, and securely.

