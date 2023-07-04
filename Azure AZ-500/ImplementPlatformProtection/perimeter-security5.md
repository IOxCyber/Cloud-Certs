## Define defense in depth:
- protecting a valuable object with multiple security controls at each level.
- includes various security controls such as firewalls, access controls, encryption, monitoring, and threat detection.
- <img width="500" alt="image" src="https://github.com/cybersome/Azure-Certifications-Guides/assets/40174034/7ba53b3b-40ff-480c-9608-13d83e355fa1">
- Azure Perimeter Network is a service that provides a `dedicated network connection between on-premises networks and Azure virtual networks`
- Azure `Perimeter Network uses Azure Private Link technology` to establish a direct, secure, and isolated connection.
 
## Network Micro-Segmentation:
- means `creating virtual "locks" or boundaries around different parts of network` to restrict access and prevent unauthorized communication between various components.
- a way to `create secure zones in data centers` and Azure deployments that allow you to isolate workloads and protect them individually.

## Virtual networks:
- Azure Virtual Network enables Azure Virtual Machines (VM), to securely communicate with each other, the internet, and on-premises networks.
- A virtual network uses two types of IP addresses: Private & Public

## Enable (DDoS) Protection:
- A denial of service attack (DoS) is an attack that has the goal of preventing access to services or systems.
- originates from multiple networks and systems
- 5 pillars of `software quality: Scalebility, Availablity, Resiliency[^1], Management, Security.
- Configure: Basic or Standard (full layer 3 to layer 7, Load Blancers[^2] mitigation capability)
- Types: Volumetric(flood the network layer), Protocol (SYN flood attacks, reflection attacks), Resource (application) (HTTP protocol violations, SQL injection, cross-site scripting, and other layer 7 attacks) 

## Azure Firewll:
1. Azure Firewall has three rule types: NAT rules, network rules, and application rules.
2. Network rules are applied before application rules in the order of precedence.
3. If a match is found in network rules, application rules are not processed.
4. If there's no network rule match and the packet protocol is HTTP/HTTPS, application rules are evaluated.
5. If no match is found in any rule type, the packet is denied by default.
6. Azure Firewall is a cloud-based network security service that safeguards Azure Virtual Network resources, offering stateful firewall capabilities, high availability, and unlimited scalability.


## VPN forced tunneling:
- VPN forced tunneling in Azure is a feature that allows you to direct all the network traffic from your virtual network through a virtual private network (VPN) gateway.
- <img width="500" alt="image" src="https://github.com/cybersome/Azure-Certifications-Guides/assets/40174034/5eb7f977-86f8-49f4-8134-ed903999ba91">

## UDRs and NSGs:
- UDRs and NSGs help provide layer 3 and layer 4 (of the OSI model) security. NVAs help provide layer 7, application layer, security.
- <img width="427" alt="image" src="https://github.com/cybersome/Azure-Certifications-Guides/assets/40174034/7385fc25-7d8b-42db-8113-03498d45ad9a">
- User Defined Routes: UDRs allow you to define custom routing rules within an Azure virtual network.
- NSGs act as a distributed firewall, allowing you to filter network traffic at the subnet or network interface level.
- Network Virtual Appliances (NVAs): NVAs are virtual machines or appliances that provide network functions, such as firewalls, load balancers, or intrusion detection systems
- Hub Virtual Network: Vnets in Azure which serves as the hub. This VNet typically hosts shared services, such as firewalls, gateways, or network appliances.

  
> Use forced tunneling to redirect internet bound traffic back to the company's on-premises infrastructure. Forced tunneling is commonly used in scenarios where organizations want to implement packet inspection or corporate audits. Forced tunneling in Azure is configured via virtual network user-defined routes (UDR).
>
> Application rules define fully qualified domain names (FQDNs) that can be accessed from a subnet. Usage of FQDNs would be appropriate to allow Windows Update network traffic.
> 
> Azure Firewall can limit the outbound IP addresses and ports that can be accessed. Define network rules that assign source address, protocol, destination port, and destination address.



## Notes:
- Outbound traffic: Data leaving your Azure resources to external destinations.
- Inbound traffic: Data arriving at your Azure resources from external sources.
- A Fully Qualified Domain Name (FQDN) in Azure refers to the complete and unique address that identifies a specific resource within the Azure cloud environment.
- 
- VPN uses `Encryption, Tunneling, VPN Server, IP Address Masking, Secure Connection`

[^1]: ability of a network infrastructure to withstand and recover from disruptions or failures without significant impact on its functionality and performance.
[^2]: Load balancers in Azure are network devices that distribute incoming network traffic across multiple servers or virtual machines to ensure efficient resource utilization and high availability.
