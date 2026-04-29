---
title: Close an incident communication plan
description: Close an incident communication plan after its execution or if it is no longer needed.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Incident Communications, Incident Communications Management, IT Service Management]
---

# Close an incident communication plan

Close an incident communication plan after its execution or if it is no longer needed.

## Before you begin

Role required: itil, ia\_admin, or admin

## About this task

-   The business rule **IA\_State\_Management** allows any user with the ia\_admin role or an itil user who is assigned to the incident communication plan, to close or cancel an incident communication plan.
-   If a user with the itil role closes or cancels a parent incident, all related incident communication plans are closed or canceled.

    **Note:** Use the incident management property **Close open Incident Communication Plans when Incident is closed or canceled** \(**com.snc.incident.incident\_alert.closure**\) to control this behavior.


## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident communications plan record that you want to close.

3.  In the **State** field, select **Closed**.

4.  Right-click on the form header and click **Save**.


**Parent Topic:**[Managing Incident Communications](../concept/working-with-inci-comm-mgmt.md)

