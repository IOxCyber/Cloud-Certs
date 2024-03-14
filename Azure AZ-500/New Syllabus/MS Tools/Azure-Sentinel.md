1. The `Azure Monitor activity log is a platform log in Azure` that provides insight into subscription-level events, Activity log events are retained in Azure for 90 days and then deleted.
2. A `Log Analytics workspace is a centralized repository and analytics engine in Azure Monitor` that collects and analyzes telemetry data from various sources, including applications, servers, virtual machines, containers, and other resources across hybrid and multi-cloud environments.
3. `Activity log data in a Log Analytics workspace is stored in a table` called `AzureActivity` that you can retrieve with a log query in Log Analytics, Activity log events are retained in the Azure platform for 90 days.
4. Azure Sentinel:
- Azure Sentinel, Microsoft's cloud-native SIEM solution, utilizes AI and ML to analyze diverse data sources like logs and alerts, enabling real-time detection and response to security threats.
- `Log Analytics is Azure service that stores the log data` that is ingested into Microsoft Sentinel that stores the log data for Microsoft Sentinel.
- After you onboard Microsoft Sentinel into your workspace, use `data connectors to start ingesting your data into Microsoft Sentinel.`
- Built-in connectors enable connection to the broader security ecosystem for non-Microsoft products.
- To add more data connectors, install the solution associated with the data connector from the Content Hub.
- `Enable a data connector with REST API integration` on the provider side, using Azure Functions, for data connectors.
- Agent-based integration for data connectors:
- - can use the Syslog protocol to connect an agent to any data source that can perform real-time log streaming.
  - 'Syslog' stream events from Linux-based, Syslog-supporting devices into Microsoft Sentinel using the Azure Monitor Agent (AMA), receives events from the Syslog daemon over UDP.
  - Common Event Format (CEF): data appears in the CommonSecurityLog table.
  - Custom logs, Service-to-service integration for data connectors for AWS & Azure.
  - Deploy data connectors as part of a solution.
  - `syslog, Common Event Format (CEF), Trusted Automated eXchange of Indicator Information (TAXII) (for threat intelligence), Azure, AWS services`

 5. After connecting your data sources to Microsoft Sentinel, `create custom analytics rules to help discover threats and anomalous behaviors in your environment.`

 6. `The size limit for an entire alert is 64 KB.`
 7. `Up to 150 alerts can be grouped into a single incident.`
 
 8. Configure automation in Microsoft Sentinel:
- Playbooks `sequences of automated steps or actions designed to execute specific security workflows or response processes in response to security incidents.`
- Playbooks are collections of procedures that can be run from Microsoft Sentinel in response to an entire incident, to an individual alert, or to a specific entity.
- `In order to trigger the playbook, you'll then create an automation rule.`
- Playbooks in Microsoft Sentinel are based on workflows built in Azure Logic Apps.
- 
- Automation rules: `predefined or custom-defined conditions or triggers that automatically initiate actions or responses` when specific security events or conditions are detected.
- Automation in Microsoft Sentinel `allows for the setup of playbooks that automatically execute responses to threats, improving the speed and consistency of security operations.`
- To use a playbook to respond automatically to an entire incident or to an individual alert, create an automation rule that will run when the incident is created or updated, or when the alert is generated.
- This automation rule will include a step that calls the playbook you want to use.

- Playbook Example:
```
When the playbook is called by an automation rule passing it an incident, the playbook opens a ticket in ServiceNow or any other IT ticketing system.
It sends a message to your security operations channel in Microsoft Teams or Slack to make sure your security analysts are aware of the incident.
It also sends all the information in the incident in an email message to your senior network admin and security admin. The email message will include Block and Ignore user option buttons.
The playbook waits until a response is received from the admins, then continues with its next steps.
If the admins choose Block, it sends a command to Microsoft Entra ID to disable the user, and one to the firewall to block the IP address.
If the admins choose Ignore, the playbook closes the incident in Microsoft Sentinel, and the ticket in ServiceNow.
In order to trigger the playbook, you'll then create an automation rule that runs when these incidents are generated. That rule will take these steps:
The rule changes the incident status to Active.
It assigns the incident to the analyst tasked with managing this type of incident.
It adds the "compromised user" tag.
Finally, it calls the playbook you just created. (Special permissions are required for this step.)
```

> Note:
- Microsoft `Sentinel must be granted explicit permissions in order to run playbooks`, whether manually or from automation rules. 
- If a playbook appears "grayed out" in the drop-down list, it means Sentinel does not have permission to that playbook's resource group.
- Click the Manage playbook permissions link to assign permissions.

9. By defining and customizing analytics rules, users can tailor Microsoft Sentinel's threat detection capabilities to their specific needs, enhancing security monitoring and alerting.
10. The connectors allow Microsoft Sentinel to collect data across a wide range of security solutions, providing a unified view for threat detection and response.
11. Azure Monitor allows organizations to collect, analyze, and act on telemetry data from Azure and on-premises environments, enhancing security event visibility and response.
12. 


