---
title: Exploring Agent Client Collector Framework
description: Learn how the Agent Client Collector Framework \(ACC-F\) helps measure the performance of your infrastructure machines. Agent Client Collector Framework analyzes data on installed agents to discover and monitor your Configuration items \(CIs\).
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Exploring Agent Client Collector Framework

Learn how the Agent Client Collector Framework \(ACC-F\) helps measure the performance of your infrastructure machines. Agent Client Collector Framework analyzes data on installed agents to discover and monitor your Configuration items \(CIs\).

## Agent Client Collector Framework overview

The Agent Client Collector is an agent that is installed on infrastructure components. The Agent Client Collector executes commands on the machines it is installed on and sends output data to the ServiceNow® instance via a dedicated MID Server. Managing Agent Client Collector on the ServiceNow® instance and MID Server is part of the Agent Client Collector Framework \(ACC-F\) application. Agent Client Collector Framework stores events and metrics in the relevant database, and provides CI performance data to other Agent Client Collector applications.

## Agent Client Collector Framework workflow

The following illustration describes the layout and data flow within the Agent Client Collector Framework application.

![ACC-F Infographic](../image/acc-framework-infographic.png "Collecting and distributing data with ACC-F")

1.  ACC-F is deployed on the customer's ServiceNow instance.
2.  Agents are installed on the host machines \(Linux, Windows, or macOS\) and collect data on the hosts and configuration items \(CIs\).
3.  Data passes to the customer instance through the MID Server.
4.  Data displays in the different Agent Client Collector applications.
    1.  Agent Client Collector Monitoring \(ACC-M\)
    2.  Agent Client Collector for Visibility \(ACC-V\)
    3.  Agent Client Collector Log Analytics \(ACC-L\)
    4.  Agent Client Collector Security Incident Response \(SIR\)
    5.  Agent Client Collector Live CI View
    6.  Software Asset Management \(SAM\)
    7.  Agent Client Collector Spoke

## Agent Client Collector Framework benefits

Agent Client Collector Framework provides data to other Agent Client Collector components.

|Benefit|Feature|Users|
|-------|-------|-----|
|Monitor your system’s health, performance, and availability through automated collection of events and metrics, leveraging automated configurations.|[Agent Client Collector Monitoring](acc-monitoring-landing-page.md)|NOC User, Event Management administrator|
|Track server inventory, software installations and usage continuously with non-admin access and minimal network communication.|[Agent Client Collector for Visibility](acc-visibility-landing-page.md)|CMDB/Discovery administrator|
|Gather detailed inventory data of devices not connected to your network or running in isolated environments \(air-gapped\).|[Agent Client Collector Framework Air Gapped Configuration Item Management Solution](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585753)|CMDB/Discovery administrator|
|Minimize triage time of incidents by direct access of live device details and interactions to remediate.|[View live CI data with Agent Client Collector](../task/acc-live-ci-view.md)|ITSM user|
|Trigger remote actions against managed devices, without additional credential or network communication.|[Agent Client Collector Security Incident Response](acc-security-incident-response.md)|Automation expert|
|Stream log data into your instance to predict problems and solve them before they happen, to minimize user impact.|[Agent Client Collector Log Analytics](acc-log-analytics.md)|Agent Client Collector administrator|

