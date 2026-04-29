---
title: Configure action group
description: Configure a set of related action items as an action group.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Action framework, Setup task management, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure action group

Configure a set of related action items as an action group.

## Before you begin

Role required: sp\_admin or sn\_hr\_sp.esc\_admin

## About this task

Action group provides quick access to action items such as approve or reject the requests directly from the approvals page. You can modify the actions to suit your business needs.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Action framework** &gt; **Action Groups**.

2.  Click **New** or edit an existing record such as **Approvals action group**.

3.  Edit the **Action group name** or click save or update.

    Proceed to add multiple actions into a group using the Action m2m group table.

4.  On the **Action group M2Ms** related list, click new or update an existing record.

    1.  Select the **Action** from the available options such as **Approve** or **Reject** or [Configure actions](config-approval-hub-actions.md).

    2.  Edit the **Order** of the action item.

    3.  Select **Primary** to set the option as primary.

    4.  Select one of the following **Action Visibility** options.

        -   Visibility to Self: Visible to owner or self only
        -   Visibility to Manager: Visible to the manager of the user
        -   Visibility to all
        -   Visible to all except Self: Visible to all except self
        -   User criteria: Select the criterion of the users for whom the action is visible
        -   Advanced: Define a custom visibility with the Advanced option through a script. For example, `answer = context.state.toString() === 'requested';`
5.  Click Save or Update.


## Result

Action group is configured to provide quick access to the actions. For example, approvals action group has a default set of actions **Approve** and **Reject** that you can use from the approval page.

