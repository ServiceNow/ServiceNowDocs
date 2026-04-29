---
title: Update approvals action group
description: Approvals action group provides quick access to approve or reject the requests directly from the approvals page.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Action framework, Setup task management, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Update approvals action group

Approvals action group provides quick access to approve or reject the requests directly from the approvals page.

## Before you begin

Role required: sp\_admin or sn\_hr\_sp.esc\_admin

## About this task

You can use the default set of actions or customize the actions to suit your business needs.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Action framework** &gt; **Action Groups**.

2.  Click **New** or edit an existing **Approvals action group** record.

3.  Edit the **Action group name**

4.  Click **Save** or **Update**.

    Use the Action group m2m table to add multiple actions into a group.

5.  On the **Action group M2Ms** related list, click New or update an existing record.

    1.  Select the **Action** item from the available options such as **Approve** or **Reject** or [Configure actions](config-approval-hub-actions.md).

    2.  Edit the **Order** of the action item.

    3.  Select **Primary** to set the option as primary.

    4.  Select one of the following **Action Visibility** options.

        -   Visibility to Self
        -   Visibility to Manager
        -   Visibility to all
        -   Visible to all except Self
        -   User criteria: Select the user criterion from the available options.
        -   Advanced: Define a custom visibility with the Advanced option through a script. For example, `answer = context.state.toString() === 'requested';`.
        **Note:** The `context` is the GlideRecord parameter for the rendered action. You can modify the parameter as needed.

6.  Click **Save** or **Update**.


## Result

Approvals action group is configured to perform quick actions such as **Approve** and **Reject** from the approval page.

