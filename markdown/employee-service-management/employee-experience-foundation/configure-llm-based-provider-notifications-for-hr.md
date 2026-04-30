---
title: Configure LLM based provider notifications for HR
description: Enable LLM-based actionable provider notifications for HR.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure LLM based provider notifications for HR

Enable LLM-based actionable provider notifications for HR.

## Before you begin

Ensure the following:

-   You have the latest version of the HR Service Delivery for Microsoft 365.
-   The following LLM Assets have their **Status** as **Published** and are **Active**:

    -   \_view\_approval\_details\_LLM\_
    -   \_view\_add\_comments\_\_LLM\_
    To check, navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.


Role required: admin

## Procedure

1.  Navigate to **ServiceNow for Microsoft 365** &gt; **Notifications** &gt; **Provider Notifications**.

2.  In the Notifications list, select **Approvals - Actionable**.

    1.  Scroll down to the Related links, select **Actions** tab.

        Verify that two **View Details** notification actions are listed.

        **Important:** If only one action is listed, you must update to the latest version of the application.

    2.  In the Related links, select **Link Actions to Content**.

    3.  Select **Approvals link action**.

    4.  Select the lock icon next to the **Actions** field.

    5.  From the list of actions, select the other **View Details** action as well.

        Verify that the **Actions** field displays two **View Details** actions.

    6.  Select **Update**.

    7.  Save the form.

3.  In the Notifications list, select **Incident commented actionable**.

    1.  Scroll down to the Related links, select **Actions** tab.

        Verify that two **View last comment** notification actions are listed.

        **Important:** If only one action is listed, you must update to the latest version of the application.

    2.  In the Related links, select **Link Actions to Content**.

    3.  Select **Incident commented content actions**.

    4.  Select the lock icon next to the **Actions** field.

    5.  From the list of actions, select the other **View last comment** action as well.

        Verify that the **Actions** field display two **View last comment** actions.

    6.  Select **Update**.

    7.  Save the form.


## What to do next

You can customize the fields displayed in approval notifications. For more information, see [Customizing approval notification fields](../concept/customizing-approval-notifications.md).

**Parent Topic:**[Configure HR Service Delivery integration with Microsoft Teams](../concept/sn-ms-teams-config-hr.md)

