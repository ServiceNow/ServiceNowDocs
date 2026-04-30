---
title: Agent Client Collector architecture
description: The Agent Client Collector is a ServiceNow agent installed on your Windows, Linux, and macOS devices to monitor your company’s infrastructure and installed applications.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector architecture

The Agent Client Collector is a ServiceNow agent installed on your Windows, Linux, and macOS devices to monitor your company’s infrastructure and installed applications.

## Agent Client Collector architecture - overview

The Agent Client Collector is built on a Sensu framework and comes installed with monitoring capabilities for servers, databases, application servers, and middleware. It also supports extending monitoring through additional checks from the Sensu community or Nagios-compatible plugins, allowing you to customize monitoring to your needs.

## Monitoring with checks and policies

The agent runs checks on the host to gather relevant data, transforming it into events or metrics. These checks are defined within ServiceNow and are associated with monitoring policies. A policy is a combination of the Configuration Items \(CIs\) being monitored and the checks that run on those CIs. The checks are associated with policies to monitor different aspects of the system.

You can customize check instances - such as adjusting the frequency or specifying parameters like login credentials for databases - without affecting the original check definition. Customization of a check instance takes effect only on the check instance associated with the policy and does not change the global check definition. This customization ensures flexibility in monitoring various CIs under different scenarios.

## Data collection and transmission

After installation, the agent collects information on its host and processes. The agent pushes the collected data to the ServiceNow instance through the MID Server. The MID Server serves as a bridge between the agent and the ServiceNow instance, ensuring the data is transformed and securely sent for processing.

On the instance, CIs are created for the host and applications classified from the running processes \(such as Microsoft SQL Server\). Once these CIs are created, the active monitoring policies associated with the CIs are downloaded to the agent’s MID Server, which then pushes the policies to the agent for execution.

## Data storage and use

The results from the checks are stored in the ServiceNow instance:

-   CI data: CMDB for Configuration Items.
-   Event data: Events table \(for example, alerts triggered by threshold breaches\).

This data can be leveraged for monitoring, alerting, and reporting. Integration ensures real-time visibility into the health of your infrastructure and applications, while also enabling proactive issue detection and remediation.

![Agent client collector configuration flow](../image/ACC-Configuration-Flow-New.png)

1.  Define a monitoring policy in the ServiceNow instance.
2.  The MID Server fetches the check instances from the instance and passes them to the agent.
3.  The agent runs the checks, collects data, and sends the results back to the MID Server.
4.  The MID Server sends the collected data to the ServiceNow instance, where it is stored in the CMDB or events tables.

The commands and their configurations that run on the Agent are called **checks**. The Agent comes by default with **check definitions**, which determine a specific command and the default frequency with which it runs. Checks are defined on the instance and are passed to the Agent via the MID Server.

A **policy** is a combination of the CIs being monitored by the Agent Client Collector and the checks that run on those CIs. You associate check definitions with policies. Those check definitions are then referred to as **check instances**. You can customize check instances to meet your needs. For example, customize the running interval or the parameters specific to the policy, such as the login credentials to access a MySQL database. Customization of a check instance takes effect only on the check instance associated with the policy, which does not affect the original check definition or already created check instances in other policies.

**Parent Topic:**[Exploring Agent Client Collector Framework](exploring-agent-client-collector-framework.md)

