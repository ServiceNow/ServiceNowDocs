---
title: Set the agent log level
description: Configure the agent log level directly from your ServiceNow instance, without needing to access the acc.yml configuration file.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Agent Client Collector logs, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Set the agent log level

Configure the agent log level directly from your ServiceNow® instance, without needing to access the `acc.yml` configuration file.

## About this task

Configuring the agent log level from the instance changes the log level temporarily, and doesn’t update the log level in the `acc.yml` configuration file. When restarting the agent, the log level reverts to its status as set in the `acc.yml` configuration file.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an agent.

3.  In the related links, select **Set Log Level**.

4.  In the Set Log Level dialog box, select the log level to invoke for the agent, and select **OK**.

5.  Reset the log level to its originally configured level by doing one of the following actions:

    -   In the related links, select **Reset Log Level**.
    -   Restart the agent.

**Parent Topic:**[Using Agent Client Collector logs](../concept/logs-acc.md)

