1. VPC:
-  Enables users to provision and manage their own logically isolated network.
-  Provides a way to organize and control cloud resources (VM, Storage, networking components etc)
-  offer network isolation, allowing users to create multiple VPCs for different projects, teams, or applications.

2. VPC Peering:
- you can ping/communicate via internal IPs by peering 2 different VPC.
- Once peered, instances within these VPCs can communicate with each other using internal IP addresses, as if they were on the same network.
- Communication over internal IPs is cheaper than Public IP.
![image](https://github.com/IOxCyber/Azure-Certs/assets/40174034/d3b7153c-f8f2-456f-b46e-11615d96db85)

- https://partner.cloudskillsboost.google/catalog_lab/1032

3. Network and Security Admin roles:
Network Admin: `Permissions to create, modify, and delete networking resources`, except for firewall rules and SSL certificates.
- Network Admin role has permissions to list but not modify/delete firewall rules.
- 
Security Admin: `Permissions to create, modify, and delete firewall rules and SSL certificates.`


5. 



## Lab:
- Networks use network tags to identify which VM instances are subject to certain firewall rules and network routes
- The default-allow-internal firewall rule allows traffic on all protocols/ports within the default network.
- you are only able to HTTP access the external IP address of the blue server as the allow-http-web-server only applies to VM instances with the web-server tag.
- the `Compute Engine default service account`, which is enabled on all instances created by Cloud Shell command-line and the Cloud Console.
- the `Compute Engine default service account` does not have the right permissions to allow you to list or delete firewall rules.
- 
- 
