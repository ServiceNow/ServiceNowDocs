---
title: Run an Agent Client Collector Security Incident Response command
description: Run a specified command, on a machine referenced by an incident, to retrieve information on the incident's CI. For example, if you run a ps command on an incident, the command retrieves the status of active processes in the system. Commands are listed according to the CI operating system associated with the security incident.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Security Incident Response, Agent Client Collector, IT Operations Management]
---

# Run an Agent Client Collector Security Incident Response command

Run a specified command, on a machine referenced by an incident, to retrieve information on the incident's CI. For example, if you run a `ps` command on an incident, the command retrieves the status of active processes in the system. Commands are listed according to the CI operating system associated with the security incident.

## Before you begin

Role required: sn\_si.admin or sn\_si.basic

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select an incident.

3.  In the Related Links section, select **Agent Client Collector Capabilities**.

    The **Agent Client Collector Capabilities** dialog box opens.

4.  Select **Run Command on Agent**.

5.  In the **ACC Integration Capabilities** field, select **Run Command on agent**.

    The **ACC Integration Command** field appears.

6.  Select the command you want to run.

    The available commands are those configured on the ACC Integration Commands page, as described in [Create an Agent Client Collector Security Incident Response command](acc-create-command.md).

7.  Select **Submit**.

    The command runs on the security incident's CI, according to the OS specified in the command.


**Parent Topic:**[Agent Client Collector Security Incident Response](../concept/acc-security-incident-response.md)

