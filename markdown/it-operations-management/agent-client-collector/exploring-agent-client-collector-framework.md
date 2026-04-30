---
title: Exploring Agent Client Collector Framework
description: The Agent Client Collector Framework \(ACC-F\) is a powerful solution for monitoring the performance and health of infrastructure components by using agents installed on servers and devices. It collects and sends critical system data to ServiceNow for analysis, enabling proactive management and troubleshooting of Configuration Items \(CIs\).
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Exploring Agent Client Collector Framework

The Agent Client Collector Framework \(ACC-F\) is a powerful solution for monitoring the performance and health of infrastructure components by using agents installed on servers and devices. It collects and sends critical system data to ServiceNow for analysis, enabling proactive management and troubleshooting of Configuration Items \(CIs\).

## Agent Client Collector Framework overview

The Agent Client Collector Framework enables organizations to monitor and manage the health of their infrastructure through agents installed on key systems. These agents execute predefined commands on the machines they are installed on, sending the resulting data back to the ServiceNow® instance via a dedicated MID Server. The framework enables seamless management of both the Agent Client Collector and MID Server, storing event data and performance metrics in the appropriate database. By providing insights into CI performance, ACC-F helps organizations identify and resolve issues quickly, improving operational efficiency and system reliability.

## Agent Client Collector Framework workflow

The following illustration describes the layout and data flow within the Agent Client Collector Framework application.

![ACC-F Infographic](../image/acc-framework-infographic.png "Collecting and distributing data with ACC-F")

1.  Agent installation: The agent is installed on infrastructure components, such as servers, devices, and network equipment. These agents are responsible for executing system commands and gathering performance data from the host machine. ACC-F is deployed on the customer's ServiceNow® instance.
2.  Data collection: The agent runs predefined scripts or queries \(checks\) on the infrastructure components to collect various system metrics and events. This includes performance data such as CPU usage, memory utilization, disk space, and network activity. The agent also collects error logs and system alerts.
3.  MID Server communication: The agent sends the collected data to the ServiceNow instance through a dedicated MID Server. The MID Server acts as a secure communication bridge between the infrastructure and the ServiceNow platform, ensuring data is transmitted reliably and securely.
4.  Data Storage: Upon receiving the data, the ServiceNow instance stores the events and performance metrics in the relevant database. This data is then associated with the respective Configuration Items \(CIs\) within the ServiceNow CMDB Configuration Management Database \(CMDB\), enabling efficient tracking and reporting.
5.  Data Analysis and Reporting: The collected data is analyzed within the ServiceNow instance, where it is used for monitoring, troubleshooting, and reporting purposes. This analysis helps identify potential issues or areas of improvement, triggering alerts or actions to resolve problems proactively.
6.  Feedback Loop: Based on the analysis, the system can trigger remediation actions, such as running corrective scripts, reconfiguring settings, or notifying responsible teams for further investigation. The feedback is looped back into the system, allowing for continuous monitoring and optimization.

## Agent Client Collector Framework benefits

Agent Client Collector Framework provides data to other Agent Client Collector components.

|Benefit|Feature|Users|
|-------|-------|-----|
|Monitor your system’s health, performance, and availability through automated collection of events and metrics, leveraging automated configurations.|[Agent Client Collector Monitoring](acc-monitoring-landing-page.md)|NOC User, Event Management administrator|
|Track server inventory, software installations and usage continuously with non-admin access and minimal network communication.|[Agent Client Collector for Visibility - Content](acc-visibility-landing-page.md)|CMDB/Discovery administrator|
|Gather detailed inventory data of devices not connected to your network or running in isolated environments \(air-gapped\).|[Agent Client Collector Framework Air Gapped Configuration Item Management Solution](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585753)|CMDB/Discovery administrator|
|Minimize triage time of incidents by direct access of live device details and interactions to remediate.|[View live CI data with Agent Client Collector](../task/acc-live-ci-view.md)|ITSM user|
|Trigger remote actions against managed devices, without additional credential or network communication.|[Agent Client Collector Security Incident Response](acc-security-incident-response.md)|Automation expert|
|Stream log data into your instance to predict problems and solve them before they happen, to minimize user impact.|[Agent Client Collector Log Analytics](acc-log-analytics.md)|Agent Client Collector administrator|

-   **[Agent Client Collector Framework use case](acc-framework-use-case.md)**  
The Agent Client Collector Framework use case demonstrates how a financial organization can use Agent Client Collector Framework to assist in IT asset discovery.
-   **[Agent Client Collector architecture](acc-concept.md)**  
The Agent Client Collector is a ServiceNow agent installed on your Windows, Linux, and macOS devices to monitor your company’s infrastructure and installed applications.
-   **[Agent Client Collector plugins](acc-assets.md)**  
An Agent Client Collector plugin is a script or group of scripts that extend the Agent Client Collector's capabilities. Plugins enhance monitoring by collecting metrics, performing specialized checks, and triggering events based on conditions, like monitoring an application's queue size when it reaches 60% or 80%. Plugins ensure scalable, customizable monitoring to adapt to evolving infrastructure or application needs.
-   **[Verify data collection in Agent Client Collector](acc-data-collection-concept.md)**  
Collect data by gathering essential information from an agent's host system before executing any checks or policies. This process ensures that the Agent Client Collector has accurate and up-to-date data on the infrastructure, processes, and applications running on the host.
-   **[Checks and policies](checks-policies.md)**  
A check is a combination of a command and its configuration. The check is executed on the Agent Client Collector's devices to gather data from those devices.
-   **[Secure parameters in the Agent Client Collector](acc-using-secure-parameters.md)**  
Secure parameters in the Agent Client Collector \(ACC\) refers to securely passing sensitive data, such as user names, passwords, and API keys, during check execution, without exposing the sensitive data in the command line. Parameters are passed to the script through standard input \(STDIN\), hiding them from logs or any process that might capture command-line arguments.
-   **[Agent Client Collector configuration data files](acc-config-data-files.md)**  
Configuration data files store dynamic instance data, such as virtual machine details, that check definitions use during execution. This ensures that checks are executed with up-to-date and accurate information about the instance being monitored.
-   **[Agent Client Collector logs](acc-logs-concept.md)**  
Agent Client Collector \(ACC\) logs play a critical role in monitoring the activity and performance of the agent. Logs offer valuable feedback that helps identify potential issues, especially when the agent's performance is suboptimal. By providing insights into areas of concern, these logs are essential for troubleshooting and resolving issues, ultimately improving the overall effectiveness of the agent.
-   **[Agent Client Collector API](acc-api.md)**  
Use the Agent Client Collector \(ACC\) API to create a flow that executes an `osquery` command on agents and processes the results. By leveraging the ACC API, you can automate the querying of agent data and streamline the processing of results, making it easier to monitor and manage system performance.
-   **[Agent Client Collector health instance scan suite](acc-instance-scan-suite.md)**  
The Agent Client Collector \(ACC\) health instance scan suite consists of checks that detect anomalies and other issues that might occur on your instance. These checks are designed to ensure the overall health and performance of the ACC, proactively identifying potential problems before they impact system operations.
-   **[Domain separation and Agent Client Collector](domain-separation-agent-client-collector.md)**  
Domain separation is supported for Agent Client Collector \(ACC\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Agent Client Collector Framework](acc-framework-landing-page.md)

