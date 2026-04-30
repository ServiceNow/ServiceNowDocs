---
title: Customize the Zscaler monitoring check
description: Customize the frequency by which the Zscaler monitoring check runs. By default, the Zscaler monitoring check runs every 30 minutes. If your Zscaler app is not working efficiently, you can set the check to run more frequently.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Check Zscaler monitoring, Perform Zscaler remediation, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Customize the Zscaler monitoring check

Customize the frequency by which the Zscaler monitoring check runs. By default, the Zscaler monitoring check runs every 30 minutes. If your Zscaler app is not working efficiently, you can set the check to run more frequently.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

For details on customizing the Zscaler monitoring check, see [Perform Zscaler remediation](../concept/zscaler-remediation-concept.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Policies**.

2.  Select the **Zscaler Monitoring Policy** entry.

3.  Select the **Scheduling** tab.

4.  In the **Interval \(sec\)** field, modify the value to the number of seconds for the monitoring check to wait in between executions.

    The default value is 1800.

    To run the monitoring check immediately, enter a value of **1**.


## Result

Zscaler monitoring checks run according to the frequency specified in the Interval \(sec\) field.

