---
title: Configure the frequency of updating the agent MID Server list
description: By default, the list of MID servers connected to agents is updated once daily. If you have a dynamic environment that adds MID servers frequently, you may want to schedule updates more often, or execute the job on demand.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring ACC with a MID Server, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure the frequency of updating the agent MID Server list

By default, the list of MID servers connected to agents is updated once daily. If you have a dynamic environment that adds MID servers frequently, you may want to schedule updates more often, or execute the job on demand.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Locate the **Update Mid List for All Agents** job.

3.  To run the job immediately, click **Execute Now**.

4.  To edit the frequency by which the job runs:

    1.  In the **Run** field, select **Periodically**.

        The **Repeat Interval** field appears.

        ![Repeat interval field](../image/ACC-Repeat-Interval.png "Repeat interval field")

    2.  Configure the frequency by which you want the job to run.

        The cells next to the **Hours** cell represent minutes and seconds, respectively.

    3.  Click **Update** to update the job frequency.


**Parent Topic:**[Configuring Agent Client Collector with a MID Server](../concept/acc-configuring-with-mid.md)

