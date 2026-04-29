---
title: View VIP status for a caller in incident
description: View the callers with VIP status on the incident records list view as well as incident form. Organizations commonly designate VIP status in the user record for some of their VIP users.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# View VIP status for a caller in incident

View the callers with VIP status on the incident records list view as well as incident form. Organizations commonly designate VIP status in the user record for some of their VIP users.

## Before you begin

Role required: personalize\_list or admin

## About this task

When a caller is assigned to an incident, the user record is automatically checked for VIP status. If the caller is a VIP caller, an icon appears beside the caller name in the list view or the caller field in the form view.

To set the status of the VIP caller manually, navigate to **All** &gt; **System Security** &gt; **Users** or select on the required caller name from the list of incident record. On the User form, select the **VIP** check box to set the VIP status of the caller.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  View the record for the VIP caller in the list of incident records.

    ![Incident list with flagged VIP caller](../image/VIPCallers.png)

3.  Click the record to view the VIP status in the **Caller** field.

    ![VIP caller](../image/VIPCallerIndication.png)


