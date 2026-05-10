---
title: Send Notification action
description: Send an email notification to predefined recipients with predefined content. Select or create a Notification \[sysevent\_email\_action\] record to configure the email notification.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Send Notification action

Send an email notification to predefined recipients with predefined content. Select or create a Notification \[sysevent\_email\_action\] record to configure the email notification.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

-   **Record**

    Data type: **Record**

    Reference to record to send notification \[sysevent\_email\_action\] about.

-   **Table**

    Data type: **Table Name**

    Table of the record to send a notification about. This input is automatically populated when you select a record.

-   **Notification**

    Data type: **Record**

    Reference to the Notification \[sysevent\_email\_action\] to send. If there is no associated Notification for the type of record you select, you will need to create one from **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.


## Outputs

This action has no outputs, although it does send the notification specified by the input values.

## General guidelines

Use these general guidelines when using the Send Notification action.

-   **Select the Send Notification action to send an email notification**

    Select this action when you want to send an email notification to predefined recipients containing predefined content. For information about creating an email notification, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).

-   **Use a Integration Hub spoke action for other types of notifications**

    Use an Integration Hub spoke action to send a notification through an external service such as Microsoft Teams. For a list of available integration spokes and their actions, see [Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/spokes-list.md).


**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

