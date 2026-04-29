---
title: Exploring Agent Client Collector
description: The Agent Client Collector Framework \(ACC-F\) is a powerful solution for monitoring the performance and health of infrastructure components by using agents installed on servers and devices. It collects and sends critical system data to ServiceNow for analysis, enabling proactive management and troubleshooting of Configuration Items \(CIs\).
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Exploring Agent Client Collector

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
|Monitor your system’s health, performance, and availability through automated collection of events and metrics, leveraging automated configurations.|[Agent Client Collector Monitoring](acc-monitoring-landing-page.md)|NOC User, Event Management administrator|
|Track server inventory, software installations and usage continuously with non-admin access and minimal network communication.|[How Agent Client Collector for Visibility - Content works](how-acc-v-works.md)|CMDB/Discovery administrator|
|Gather detailed inventory data of devices not connected to your network or running in isolated environments \(air-gapped\).|[Agent Client Collector Framework Air Gapped Configuration Item Management Solution](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585753)|CMDB/Discovery administrator|
|Minimize triage time of incidents by direct access of live device details and interactions to remediate.|[View live CI data with Agent Client Collector](../task/acc-live-ci-view.md)|ITSM user|
|Stream log data into your instance to predict problems and solve them before they happen, to minimize user impact.|[Agent Client Collector Log Analytics](acc-log-analytics.md)|Agent Client Collector administrator|

