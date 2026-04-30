---
title: Optimize distribution of agents to MID Servers
description: Optimize the distribution of agents by allowing redistribution from one MID Server to another. Agents will always be connected to the MID Server with the fastest response time.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Optimize distribution of agents to MID Servers

Optimize the distribution of agents by allowing redistribution from one MID Server to another. Agents will always be connected to the MID Server with the fastest response time.

## Before you begin

Ensure that the following settings are configured:

-   The **sn\_agent.enable\_auto\_mid\_selection** system property is set to true. When using the `acc.yml` file, the property is **enable\_auto\_mid\_selection**.
-   On the MID Server page \(**Agent Client Collector** &gt; **MID Server**\):
    -   Status: Up
    -   Validated: Yes

Role required: agent\_client\_collector\_admin

## About this task

Only validated MID Servers can accept connections from agents.

## Procedure

1.  Navigate to **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.

2.  On the **MID Servers \[Agent Client Collector view\]** page, select the check box next to the MID Server from which you want to redistribute agents.

3.  In the **Actions on selected rows** list, select **Try redistributing connected agents**.

    Note the number of agents assigned to your MID Servers.

4.  Refresh the page to view the results of the redistribution attempt.

    The values in the **Number of agents** column for any affected MID Server will show a change if any agents were redistributed.


