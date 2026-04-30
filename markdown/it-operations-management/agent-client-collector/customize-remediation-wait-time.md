---
title: Customize the Zscaler remediation wait time
description: Configure the amount of time \(in seconds\) by which the Zscaler remediation check verifies the Zscaler status. This amount of time indicates how often the system checks the Zscaler status after the remediation check runs.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Check Zscaler monitoring, Perform Zscaler remediation, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Customize the Zscaler remediation wait time

Configure the amount of time \(in seconds\) by which the Zscaler remediation check verifies the Zscaler status. This amount of time indicates how often the system checks the Zscaler status after the remediation check runs.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **Agent Client Collector** &gt; **Agents** &gt; **Configuration** &gt; **Check Definition**.

2.  Select **zscaler-remediation-check**.

3.  In the **Command** field, modify the value to: `zscaler_app_remediator.rb --wait_time=<time_in_sec>`, where `<time_in_sec>` is the number of seconds the system waits before checking the Zscaler status.

    By default, the system waits 30 seconds.

4.  Select **Save**.

    -   If the Zscaler app is running within the configured `wait_time`, the remediation result is **Success**.
    -   If the Zscaler app is not running within the configured `wait_time`, the remediation result is **Failed**.

