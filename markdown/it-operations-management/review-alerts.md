---
title: Review alerts
description: Access the Express List interface to review and manage alerts in your Event Management system.
locale: en-US
release: australia
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Event Management, alerts, Express List, ITOM, AIOps, alert management, operations]
breadcrumb: [ITOM Configuration console for Event Management, Now Assist for Setup \(AIOps\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Review alerts

Access the Express List interface to review and manage alerts in your Event Management system.

## Before you begin

Verify that you have installed the ITOM AIOps and Now Assist for IT Operations Management \(ITOM\) plugins.

Ensure you are in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

When reviewing alerts, validate the following to ensure your event pipeline is healthy and alerts are actionable:

-   Check CI binding. Alerts should populate the cmdb\_ci field. If there is no CI, your binding rules need tuning.
-   Verify severity spread. If everything lands as Critical or Info, your mapping needs work.
-   Confirm that clear events close alerts. Trigger a condition, then resolve it at the source. The alert should auto-close.
-   Spot-check key fields. Ensure node, source, resource, and message\_key are meaningfully populated \(not blank or generic\).
-   Review Error events. Check em\_event status = Error for parsing or mapping issues.
-   Check the alert count. Make sure it matches in both your source system and in ServiceNow.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Alert response**.

2.  Expand **Alert response**.

3.  Select **Review alerts**.

4.  Select **Review alerts in Express List**.

    Express List opens with a list of active alerts.

    **Note:** To get more information on alerts so you can more efficiently monitor systems and services,​ resolve alerts, evaluate the alert impact,​ track issues, and report incidents, see [Express List in the Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/express-list.md).

5.  To complete the setup, select **Mark as configured**.


