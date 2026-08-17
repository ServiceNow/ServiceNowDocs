---
title: Assign Event Management operator role to group
description: Assign the evt\_mgmt\_operator role to groups to enable operations teams to work with alerts and manage Event Management workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/assign-aiops-role-grp.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Event Management, operators, role assignment]
breadcrumb: [Configure Event Management using ServiceNow Otto for Setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Assign Event Management operator role to group

Assign the evt\_mgmt\_operator role to groups to enable operations teams to work with alerts and manage Event Management workflows.

## Before you begin

Verify you have installed the ITOM AIOps and ServiceNow Otto for IT Operations Management \(ITOM\) plugins.

Ensure you are in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

The evt\_mgmt\_operator role provides the necessary permissions for operations teams to view alerts, manage incidents, and use Event Management tools. Assign this role to groups that contain your L1 and L2 operations staff who will be working with alerts on a daily basis.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Platform foundations**.

2.  Expand **Platform foundations**.

3.  Select **Assign Event Management operators**.

4.  Select **Add group**.

    By default, the **Assign role to existing group** is selected.

5.  If you want to create your group, select **Create new group** and perform the following steps:

    1.  In the **Group name** field, enter the name of the group.
    2.  In the **Description** field, enter a description.
    3.  In the **Users** field, select the users to add to the group.
    4.  Select **Save**.
6.  In the **Group** field, select the group to assign the evt\_mgmt\_operator role to.

7.  Select **Save**.

    The role is assigned to the selected group.

8.  To complete the setup, select **Mark as configured**.


