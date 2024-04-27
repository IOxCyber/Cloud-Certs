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
3. `VPN Gateway: Establishes a secure connection between an on-premises network and an Azure virtual network, enabling hybrid connectivity` and extending on-premises networks to Azure.
4. `ExpressRoute: Provides a private, dedicated connection between an on-premises network and Azure data centers`, offering higher reliability, faster speeds, and lower latencies compared to VPN connections.

> A network security group contains as many rules as desired, within Azure subscription limits.
> Augmented security rules simplify security definition for virtual networks, allowing you to define larger and complex network security policies, with fewer rules.
> A service tag represents a group of IP address prefixes from a given Azure service.

## Plan and implement security for storage:
- Azure Key Vault makes it easy to rotate your keys without interruption to your applications and provides secure management of your access keys.
- Azure Key Vault provides a secure way to manage and rotate storage account access keys, which should be done regularly to maintain security.
- Microsoft recommends that clients use either Microsoft Entra ID or a shared access signature SAS to authorize access to data in Azure Storage.
- Authorization ensures that resources are secure and only accessible to authorized users or applications.
- BYOK is used to securely transfer an existing key from an on-premises HSM to Azure Key Vault for secure storage and management.




























