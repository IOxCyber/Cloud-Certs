## Network Security Groups (NSGs) in Azure:
- `NSGs act as virtual firewalls`, controlling inbound and outbound traffic to Azure resources based on defined security rules.
- They are `associated with subnets, network interfaces, or VMs,` providing an additional layer of defense against unauthorized access.

> Security rules are evaluated and applied based on the five-tuple (1. source, 2. source port, 3. destination, 4. destination port, and 5. protocol)

## Inbound and outbound communication in Azure:
1. `Inbound communication refers to traffic coming into Azure resources` from external sources, such as requests to access a virtual machine or web application hosted in Azure.
2. `Outbound communication involves traffic leaving Azure resources` to reach external destinations, such as responses from a web server or database queries sent to an external service.

> Unless you have a specific reason to, we recommend that you associate a network security group to a subnet, or a network interface, but not both.

## Application Security Groups (ASGs) in Azure:
- Allowing you to group virtual machines and define network security policies based on those groups
- They `allow you to define network security rules based on these groups`, simplifying the application of security policies across multiple VMs with similar roles or functions.

## Virtual network connection types in Azure:
1. `Virtual Network Peering: Connects two virtual networks in the same Azure region,` enabling seamless communication between resources in those networks.

2. (Virtual Network-to-Virtual Network) `VNet-to-VNet connection: Links two virtual networks across Azure regions`, allowing resources in different regions to communicate securely.

3. `VPN Gateway: Establishes a secure connection between an on-premises network and an Azure virtual network, enabling hybrid connectivity` and extending on-premises networks to Azure over the public Internet.
- Azure VPN Gateway supports both site-to-site VPN and point-to-site VPN connections.
- S2S: Establishes a secure and encrypted connection between your on-premises VPN device (such as a router or VPN appliance) and the Azure VPN Gateway.
- P2S: Individual client devices (such as laptops or desktop computers) can securely connect to your Azure virtual network over the internet. Uses OpenVPN® Protocol, an SSL/TLS based VPN protocol,  Secure Socket Tunneling Protocol (SSTP), a proprietary TLS-based VPN protocol, IKEv2 VPN, a standards-based IPsec VPN solution.

4. `ExpressRoute: Provides a private, dedicated connection between an on-premises network and Azure data centers`, offering higher reliability, faster speeds, and lower latencies compared to VPN connections. By default traffic over an ExpressRoute connection isn't encrypted.

> A network security group contains as many rules as desired, within Azure subscription limits.
> Augmented security rules simplify security definition for virtual networks, allowing you to define larger and complex network security policies, with fewer rules.
> A service tag represents a group of IP address prefixes from a given Azure service.

## Plan and implement security for storage:
- Azure Key Vault makes it easy to rotate your keys without interruption to your applications and provides secure management of your access keys.
- Azure Key Vault provides a secure way to manage and rotate storage account access keys, which should be done regularly to maintain security.
- Microsoft recommends that clients use either Microsoft Entra ID or a shared access signature SAS to authorize access to data in Azure Storage.
- Authorization ensures that resources are secure and only accessible to authorized users or applications.
- BYOK is used to securely transfer an existing key from an on-premises HSM to Azure Key Vault for secure storage and management.


## Secure Virtual Hub:
- A virtual hub is a Microsoft-managed virtual network that enables connectivity from other resources.
- A secured virtual hub is an Azure Virtual WAN Hub with associated security and routing policies configured by Azure Firewall Manager.

## Azure Storage firewalls and virtual networks:
- Storage accounts have a public endpoint that's accessible through the internet. You can also create private endpoints for your storage account.
- The Azure Storage firewall provides access control for the public endpoint of your storage account.

- **Note**: Storage firewall rules apply to the public endpoint of a storage account. You don't need any firewall access rules to allow traffic for private endpoints of a storage account.

## Azure control plane and data plane:
- Azure operations can be divided into two categories - control plane and data plane. 
- The `control plane manages the configuration and operation of Azure resources`.
- The `data plane handles the actual data processing and traffic flow within Azure.`

### Examples:
- You create a virtual machine through the control plane. After the virtual machine is created, you interact with it through data plane operations, such as Remote Desktop Protocol (RDP).
- You create a storage account through the control plane. You use the data plane to read and write data in the storage account.

> Azure Storage firewall rules only apply to data plane operations. Control plane operations are not subject to the restrictions specified in firewall rules.


## Network security group (NSG) flow logging:
- a feature of Azure Network Watcher that allows you to log information about IP traffic flowing through a network security group.
- Flow data is sent to Azure Storage from where you can access it and export it to any visualization tool, security information and event management (SIEM) solution, or intrusion detection system (IDS).
- Flow logs operate at Layer 4 of the Open Systems Interconnection (OSI) model and record all IP flows going in and out of a network security group.
- Logs are collected at 1-minute intervals through the Azure platform in JSON, retent in 1 year.























