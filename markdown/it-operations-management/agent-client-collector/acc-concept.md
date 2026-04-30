---
title: Agent Client Collector architecture
description: The Agent Client Collector is a ServiceNow agent installed on your Windows, Linux, and macOS devices to monitor your company’s infrastructure and installed applications.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector architecture

The Agent Client Collector is a ServiceNow agent installed on your Windows, Linux, and macOS devices to monitor your company’s infrastructure and installed applications.

The Agent Client Collector is built on a Sensu framework and comes installed with monitoring capabilities for servers, databases, application servers, and middleware. It also enables you to adopt and extend monitoring with additional checks from the Sensu community, as well as with any Nagios-compatible plugins. Checks and policies run in the agent to retrieve the relevant data, which is transformed into events or metrics, as appropriate. Events and metrics are sent from the agent to ITOM Health in your ServiceNow instance through a pre-installed MID Server and stored in either the CMDB table \(for Discovery data\), or the events table \(for events\).

The commands and their configurations that run on the Agent are called **checks**. The Agent comes by default with **check definitions**, which determine a specific command and the default frequency with which it runs. Checks are defined on the instance and are passed to the Agent via the MID Server.

A **policy** is a combination of the CIs being monitored by the Agent Client Collector and the checks that run on those CIs. You associate check definitions with policies. Those check definitions are then referred to as **check instances**. You can customize check instances to meet your needs. For example, customize the running interval or the parameters specific to the policy, such as the login credentials to access a MySQL database. Customization of a check instance takes effect only on the check instance associated with the policy, which does not affect the original check definition or already created check instances in other policies.

After the initial launch of the Agent Client Collector, the agent collects information on its host and the host's processes. To do so, the agent pushes the collected information to the instance through the MID Server. The instance creates a CI for the host and also creates CIs for applications classified from the running processes' information, such as Microsoft SQL Server. Once those CIs are created, the active policies defined for the CIs are downloaded to the agent’s MID Server and are then pushed to the agent. This is illustrated in the following diagram.

![Agent client collector configuration flow](../image/ACC-Configuration-Flow-New.png)

The flow indicates the following:

1.  On the ServiceNow instance, the user defines a monitoring policy. This policy includes its monitoring target class or classes of CIs, checks, check parameters, and frequency.
2.  The MID Server periodically fetches from the instance for policy check instances, and passes the checks onto the agent.
3.  The Agent runs its scheduled checks and pushes the results to the MID Server. The MID Server passes the collected data back to the instance, where it is stored in the relevant database.

