---
title: Exploring Agent Client Collector Framework
description: The Agent Client Collector Framework \(ACC-F\) is a powerful solution for monitoring the performance and health of infrastructure components by using agents installed on servers and devices. It collects and sends critical system data to ServiceNow for analysis, enabling proactive management and troubleshooting of Configuration Items \(CIs\).
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Exploring Agent Client Collector Framework

The Agent Client Collector Framework \(ACC-F\) is a powerful solution for monitoring the performance and health of infrastructure components by using agents installed on servers and devices. It collects and sends critical system data to ServiceNow for analysis, enabling proactive management and troubleshooting of Configuration Items \(CIs\).

## Agent Client Collector Framework overview

The Agent Client Collector Framework enables organizations to monitor and manage the health of their infrastructure through agents installed on key systems. These agents execute predefined commands on the machines they are installed on, sending the resulting data back to the ServiceNow® instance via a dedicated MID Server. The framework enables seamless management of both the Agent Client Collector and MID Server, storing event data and performance metrics in the appropriate database. By providing insights into CI performance, ACC-F helps organizations identify and resolve issues quickly, improving operational efficiency and system reliability.

## Agent Client Collector Framework workflow

The following illustration describes the layout and data flow within the Agent Client Collector Framework application.

![ACC-F Infographic](../image/acc-framework-infographic.png "Collecting and distributing data with ACC-F")

1.  Agent Installation: The agent is installed on infrastructure components, such as servers, devices, and network equipment. These agents are responsible for executing system commands and gathering performance data from the host machine. ACC-F is deployed on the customer's ServiceNow® instance.
2.  Data collection: The agent runs predefined scripts or queries \(checks\) on the infrastructure components to collect various system metrics and events. This includes performance data such as CPU usage, memory utilization, disk space, and network activity. The agent also collects error logs and system alerts.
3.  MID Server communication: The agent sends the collected data to the ServiceNow instance through a dedicated MID Server. The MID Server acts as a secure communication bridge between the infrastructure and the ServiceNow platform, ensuring data is transmitted reliably and securely.
4.  Data Storage: Upon receiving the data, the ServiceNow instance stores the events and performance metrics in the relevant database. This data is then associated with the respective Configuration Items \(CIs\) within the ServiceNow CMDB Configuration Management Database \(CMDB\), enabling efficient tracking and reporting.
5.  Data Analysis and Reporting: The collected data is analyzed within the ServiceNow instance, where it is used for monitoring, troubleshooting, and reporting purposes. This analysis helps identify potential issues or areas of improvement, triggering alerts or actions to resolve problems proactively.
6.  Feedback Loop: Based on the analysis, the system can trigger remediation actions, such as running corrective scripts, reconfiguring settings, or notifying responsible teams for further investigation. The feedback is looped back into the system, allowing for continuous monitoring and optimization.

## Agent Client Collector Framework benefits

Agent Client Collector Framework provides data to other Agent Client Collector components.

|Benefit|Feature|Users|
|-------|-------|-----|
|Monitor your system’s health, performance, and availability through automated collection of events and metrics, leveraging automated configurations.|[Enable metrics collection and evaluation](../task/acc-distributed-mid-cluster.md)|NOC User, Event Management administrator|
|Track server inventory, software installations and usage continuously with non-admin access and minimal network communication.|[How Agent Client Collector for Visibility - Content works](how-acc-v-works.md)|CMDB/Discovery administrator|
|Gather detailed inventory data of devices not connected to your network or running in isolated environments \(air-gapped\).|[Agent Client Collector Framework Air Gapped Configuration Item Management Solution](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585753)|CMDB/Discovery administrator|
|Minimize triage time of incidents by direct access of live device details and interactions to remediate.|[View live CI data with Agent Client Collector](../task/acc-live-ci-view.md)|ITSM user|
|Stream log data into your instance to predict problems and solve them before they happen, to minimize user impact.|[Agent Client Collector Log Analytics](acc-log-analytics.md)|Agent Client Collector administrator|

-   **[Agent Client Collector Framework use case](acc-framework-use-case.md)**  
The Agent Client Collector Framework use case demonstrates how a financial organization can use Agent Client Collector Framework to assist in IT asset discovery.
-   **[Agent Client Collector architecture](acc-concept.md)**  
The Agent Client Collector is a ServiceNow agent installed on your Windows, Linux, and macOS devices to monitor your company’s infrastructure and installed applications.
-   **[Domain separation and Agent Client Collector](domain-separation-agent-client-collector.md)**  
Domain separation is supported for Agent Client Collector \(ACC\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Agent Client Collector plugins](acc-assets.md)**  
An Agent Client Collector \(ACC\) plugin is a script or group of scripts that extend the Agent Client Collector's capabilities. Plugins enhance monitoring by collecting metrics, performing specialized checks, and triggering events based on conditions, like monitoring an application's queue size when it reaches 60% or 80%. Plugins ensure scalable, customizable monitoring to adapt to evolving infrastructure or application needs.
-   **[Secure parameters in Agent Client Collector](acc-using-secure-parameters.md)**  
Secure parameters in Agent Client Collector \(ACC\) refers to securely passing sensitive data, such as user names, passwords, and API keys, during check execution, without exposing the sensitive data in the command line. Parameters are passed to the script through standard input \(STDIN\), hiding them from logs or any process that might capture command-line arguments.
-   **[Agent Client Collector logs](acc-logs-concept.md)**  
Agent Client Collector \(ACC\) logs play a critical role in monitoring the activity and performance of the agent. Logs offer valuable feedback that helps identify potential issues, especially when the agent's performance is suboptimal. By providing insights into areas of concern, these logs are essential for troubleshooting and resolving issues, ultimately improving the overall effectiveness of the agent.
-   **[Operating system and application monitoring using Agent Client Collector](itom-monitoring-for-acc.md)**  
IT Operations Management \(ITOM\) monitoring for the Agent Client Collector is installed on the ServiceNow® instance. It monitors the specific operating system and applications that are installed on the host machine.
-   **[Agent-based data flow](acc-events-alerts-metrics.md)**  
The Agent Client Collector gathers information on the health of the CI that the Agent is installed on, and the applications that run on the hosts. The Agent runs several checks and pushes the checks' results to the MID Server, where they are converted into events or metrics.
-   **[Agent Client Collector Monitoring use case](acc-monitoring-use-case.md)**  
The Agent Client Collector Monitoring use case demonstrates how organizations can achieve unified monitoring across hybrid IT environments.
-   **[Windows event log monitoring](windows-event-log-monitoring.md)**  
Windows event log monitoring tracks, analyzes, and manages event logs generated by various Windows OS components.
-   **[How Agent Client Collector for Visibility - Content works](how-acc-v-works.md)**  
Agent Client Collector for Visibility - Content \(ACC-VC\) requires installation of ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.

**Parent Topic:**[Agent Client Collector](acc-landing-page.md)

