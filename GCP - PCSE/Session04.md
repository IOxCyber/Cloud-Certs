## Labs: Getting Started with Security Command Center:
- https://partner.cloudskillsboost.google/focuses/73442?parent=catalog

1. SCC:
- Security Command Center, which is a service offered by Google Cloud Platform (GCP). Security Command Center (SCC) provides centralized visibility and control for security-related issues across an organization's Google Cloud assets.
- SCC helps users:
```
Monitor and detect security threats and vulnerabilities: It continuously analyzes Google Cloud resources and logs to identify potential security issues such as misconfigurations, suspicious activity, or vulnerabilities.

Manage security findings: SCC provides a dashboard where users can view, filter, and investigate security findings. They can prioritize and take action on findings based on their severity and relevance to the organization's security posture.

Configure security settings: Users can customize SCC's behavior by configuring settings related to threat detection, vulnerability assessment, and compliance standards.
```

2. Security Health Analytics: Identify common misconfigurations in your environment such as open firewalls and public buckets, and CIS violations.
3. Web Security Scanner: Uncover common vulnerabilities such as cross-site scripting (XSS) and outdated libraries, that put your web applications at risk.
4. Container Threat Detection: Use kernel-level instrumentation to identify potential compromise of containers, including suspicious binaries.
5. Rapid Vulnerability Detection: Automatically scan your networks and web applications for critical vulnerabilities that have a high likelihood of being exploited.
6.Virtual Machine Threat Detection: Analyze Compute Engine instances to identify threats, including cryptomining abuse.
> Modules are pre-defined, or custom units of detection logic.

## Lab Gist:
```
Task 1: Explore SCC interface elements

Access Security Command Center (SCC) through the navigation menu.
Investigate panels displaying "New threats over time" and "Vulnerabilities per resource type."
Understand the difference between threats and vulnerabilities.
Explore findings categorized by resource type and severity.
Learn about different tabs in SCC for threats, vulnerabilities, compliance, findings, and sources.
Task 2: Configure SCC settings at project level

Access SCC settings and navigate to the Services tab.
Understand different built-in services such as Security Health Analytics and Container Threat Detection.
Enable specific modules for Security Health Analytics.
Configure settings for detecting misconfigurations and vulnerabilities.
Task 3: Analyze and fix SCC vulnerability findings

View all findings in SCC and filter them by category and severity.
Manage findings by changing their active state and muting irrelevant findings.
Create mute rules to automatically mute specific types of findings.
Fix vulnerabilities identified by SCC, such as open RDP and SSH ports, by adjusting firewall rules.
```
