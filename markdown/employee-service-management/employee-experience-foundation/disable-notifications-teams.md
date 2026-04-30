---
title: Review the active notifications for Microsoft Teams
description: The notifications added by ServiceNow for Microsoft Teams, might duplicate existing notifications in your instance. Review and disable any duplicate notifications to avoid notifying users multiple times for the same event.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Review the active notifications for Microsoft Teams

The notifications added by ServiceNow for Microsoft Teams, might duplicate existing notifications in your instance. Review and disable any duplicate notifications to avoid notifying users multiple times for the same event.

## Before you begin

Role required: admin

## About this task

You will find the following duplicate notifications after installing the IT Service Management integration with Microsoft Teams application.

-   Incident Update
-   MS teams Non-actionable Approval
-   Requested Item Update

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Notifications** &gt; **Provider Notifications**.

    You can also navigate to **All** &gt; **System Notifications** &gt; **Provider** &gt; **Notifications**. ![Notifications](../images/notifications.png)

2.  On the Notifications list, select the **Name** column to sort the list in alphabetical order.

    This collates all the duplicate notifications.

3.  Search for the **Incident Update** notification.

    ![Duplicate notifications](../images/duplicate-notifications02.png)

4.  Select one of the **Incident Update** notifications.

5.  Clear the **Active** field.

    ![Un-check active option](../images/un-check_active.png)

6.  Select **Update**.

7.  Repeat the process for the following notifications:

    -   MS teams Non-actionable Approval
    -   Requested Item Update

## Result

Leave a comment on an incident record, only one notification appears about the comment in Microsoft Teams.

**Parent Topic:**[Configure IT Service Management integration with Microsoft Teams](../concept/sn-ms-teams-config-it.md)

