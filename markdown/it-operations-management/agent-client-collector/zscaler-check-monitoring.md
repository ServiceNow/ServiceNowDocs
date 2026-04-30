---
title: Check Zscaler monitoring
description: Check the monitoring status of your Zscaler app, to verify that it is running properly.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform Zscaler remediation, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Check Zscaler monitoring

Check the monitoring status of your Zscaler app, to verify that it is running properly.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

If the monitoring app is down, the Zscaler tunnel status is either **51\(SERVICE-DOWN-ERROR\)** or **56\(SYSTEM\_SOCKETS\_EXHAUSTED\_ERROR\)**. When that happens, a remediation check runs, which shuts down and then starts the Zscaler app.

By default, the Zscaler monitoring check \(**zscaler-monitoring-check**\) runs automatically every 30 minutes. If you are experiencing problems with your Zscaler app, you may want to run the check more often or immediately. For details, see [Customize the Zscaler monitoring check](zscaler-customize-monitoring.md).

## Procedure

1.  Navigate to **All** &gt; **Remediate Zscaler VPN** &gt; **Monitoring Status**.

    The **Application Monitoring Status** page appears.

    ![Application monitoring status page](../image/zscaler-app-monitoring-status.png "Application Monitoring Status page")

    -   If the Zscaler app is running properly, the **Application Status** column displays the **Up** value.
    -   If the Zscaler app is not running properly, the **Application Status** column displays the **Down** value.
2.  If the **Application Status** column displays the **Down** value, the remediation check \(**zscaler-remediation-check**\) runs.

    -   For details on customizing the amount of time after which the system verifes the Zscaler status, see [Customize the Zscaler remediation wait time](customize-remediation-wait-time.md).
    -   For details on monitoring Zscaler remediation checks, see [Check Zscaler remediation](zscaler-check-remediation.md).

