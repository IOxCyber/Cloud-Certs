## Azure Monitor:
- Azure Monitor is a comprehensive `monitoring solution for collecting, analyzing, and responding to monitoring data from your cloud and on-premises environments.`
- Azure Monitor collects and aggregates the data from every layer and component of your system across multiple Azure and non-Azure subscriptions and tenants.

## High-level Architecture:
- Azure Monitor can monitor these types of resources in Azure, other clouds, or on-premises:
```
Applications
Virtual machines
Guest operating systems
Containers including Prometheus metrics, Kubernates
Databases
Security events in combination with Azure Sentinel
Networking events and health in combination with Network Watcher
Custom sources that use the APIs to get data into Azure Monitor
```
## You can also export monitoring data from Azure Monitor into other systems so you can:
- Integrate with other third-party and open-source monitoring and visualization tools
- Integrate with ticketing and other ITSM systems
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/8e46510c-3ecc-4ff1-9ee2-50c272085d89)

## Azure Monitor Logs:
- a feature of Azure Monitor that collects and organizes log and performance data from monitored resources.
- Log queries are written in Kusto Query Language (KQL)
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/82143482-3e21-4c3a-8e0a-5a98ff3703d0)


## Data platform:
- Azure Monitor stores data in data stores for each of the three pillars of observability, plus an additional one:
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/8d0fa3e1-a2e7-487d-b769-7312eca321c1)
```
metrics
logs
distributed traces: technique used to trace requests as they travel through a distributed system.
changes
```

## Log Analytics in Azure Monitor:
- Tool in the Azure portal that's used to edit and run log queries against data in the Azure Monitor Logs store.
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/6dcee253-42c8-4ea3-8307-9f16da7a0210)


## Azure Monitor Metrics:
- collects numeric data from monitored resources into a time-series database. Metrics are numerical values.

### Types of metrics:
- Native metrics use tools in Azure Monitor for analysis and alerting.
- Platform metrics are collected from Azure resources.
- Prometheus metrics are collected from Kubernetes clusters
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/9cca021c-3eee-4a22-9496-ddabefe34b8c)

> Azure Monitor provides REST APIs that allow you to get data in and out of Azure Monitor Metrics.
> All communication between connected systems and the Azure Monitor service is encrypted using the TLS 1.2 (HTTPS) protocol

> Azure Monitor Metrics can only store numeric data in a particular structure, whereas Azure Monitor Logs can store a variety of data types that have their own structures.
> You can also perform complex analysis on Azure Monitor Logs data by using log queries, which can't be used for analysis of Azure Monitor Metrics data.


## Microsoft Sentinel: `SIEM & SOAR Tool`
- Microsoft Sentinel is a scalable, cloud-native solution that provides:
- Security information and event management (SIEM) & Security orchestration, automation, and response (SOAR)
- With Microsoft Sentinel, you get a single solution for attack detection, threat visibility, proactive hunting, and threat response.
- Microsoft Sentinel inherits the Azure Monitor tamper-proofing and immutability practices. While Azure Monitor is an append-only data platform, it includes provisions to delete data for compliance purposes.
- Sentinel leverages Azure Monitor's capabilities to ingest and store security-related data, including logs, events, and alerts, which are then processed, analyzed, and correlated to detect and respond to security threats.
- ![image](https://github.com/IOxCyber/Cloud-Certs/assets/40174034/08531a2b-d946-45aa-a715-9ecc7baf2c3d)
> For example: if you use the ServiceNow ticketing system, `use Azure Logic Apps connector` to automate your workflows and open a ticket in ServiceNow each time a particular alert or incident is generated.

## Microsoft Sentinel data connectors:
- Data connectors are used to ingest your data in Sentinel.
- For example, the Microsoft Defender XDR connector is a service-to-service connector that integrates data from Office 365, Microsoft Entra ID, Microsoft Defender for Identity, and Microsoft Defender for Cloud Apps.


# Notes: 
# P1 and P2 subscriptions are licensing tiers that provide access to a range of security features and products across the Microsoft ecosystem, including Azure services like Azure Sentinel and Microsoft Defender for Cloud. 
## 2"Azure Sentinel" and "Defender for Cloud" subscriptions are specific offerings within Azure that focus on security management and threat protection.















