Deploy and configure network security groups to protect your Azure solutions
Configure and lockdown service endpoints and private links
Secure your applications with Application Gateway, Web App Firewall, and Front Door
Configure ExpressRoute to help protect your network traffic

1. Network Security Groups (NSG):
- Network traffic can be filtered to and from Azure resources in an Azure virtual network.
- provide a distributed firewall for controlling inbound and outbound traffic in a virtual network.

## To enable external connectivity to Azure resources from the public internet:
- Assign a public IP address to specific Azure resources
- Deploy a Load Balancer[^1], gateway 
- Configure Network Security Group (NSG) Rules
- Implement Network Address Translation (NAT)

2. Deploy a Network Security Groups implementation:
- 100 NSGs per region(Max 500) per subscription, 200 rules in a single NSG(Max 400). 
- You can `apply only one NSG to a VM, subnet, or network adapter.`
- You can `apply an NSG to multiple resources.`
- 





























[^1]: Azure Load Balancer and Application Gateway can act as frontend endpoints that accept incoming connections from the public internet and distribute the traffic to the appropriate resources within your virtual network.
