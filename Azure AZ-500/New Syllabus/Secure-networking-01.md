Network Security Groups (NSGs) in Azure:

`NSGs act as virtual firewalls`, controlling inbound and outbound traffic to Azure resources based on defined security rules.
They are associated with subnets, network interfaces, or VMs, providing an additional layer of defense against unauthorized access.

> Security rules are evaluated and applied based on the five-tuple (1. source, 2. source port, 3. destination, 4. destination port, and 5. protocol)

Inbound and outbound communication in Azure:

Inbound communication refers to traffic coming into Azure resources from external sources, such as requests to access a virtual machine or web application hosted in Azure.
Outbound communication involves traffic leaving Azure resources to reach external destinations, such as responses from a web server or database queries sent to an external service.

> Unless you have a specific reason to, we recommend that you associate a network security group to a subnet, or a network interface, but not both.

Application Security Groups (ASGs) in Azure:

ASGs are used to simplify network security management by grouping virtual machines (VMs) based on application requirements.
They allow you to define network security rules based on these groups, simplifying the application of security policies across multiple VMs with similar roles or functions.

Virtual network connection types in Azure:

Virtual Network Peering: Connects two virtual networks in the same Azure region, enabling seamless communication between resources in those networks.
VNet-to-VNet (Virtual Network-to-Virtual Network) connection: Links two virtual networks across Azure regions, allowing resources in different regions to communicate securely.
VPN Gateway: Establishes a secure connection between an on-premises network and an Azure virtual network, enabling hybrid connectivity and extending on-premises networks to Azure.
ExpressRoute: Provides a private, dedicated connection between an on-premises network and Azure data centers, offering higher reliability, faster speeds, and lower latencies compared to VPN connections.































