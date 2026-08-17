---
title: Assign Event Management admin role to group
description: Assign the evt\_mgmt\_admin role to users who will be in charge of configuration and operational control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/assign-aiops-user-role.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 1
keywords: [EM group roles]
breadcrumb: [Configure Event Management using ServiceNow Otto for Setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Assign Event Management admin role to group

Assign the evt\_mgmt\_admin role to users who will be in charge of configuration and operational control.

## Before you begin

Verify you have installed the ITOM AIOps and ServiceNow Otto for IT Operations Management \(ITOM\) plugins.

Ensure you're in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin

## About this task

The evt\_mgmt\_admin role provides groups with the necessary permissions to configure and manage Event Management settings, including alert processing, incident creation, and operational controls.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Platform foundations**.

2.  Expand **Platform foundations**.

3.  Select **Assign Event Management admins**.

4.  Select **Add group**.

    By default, the **Assign role to existing group** is selected.

5.  If you want to create your group, select **Create new group** and perform the following steps:

    1.  In the **Group name** field, enter the name of the group.
    2.  In the **Description** field, enter a description.
    3.  In the **Users** field, select the users to add to the group.
    4.  Select **Save**.
6.  In the **Group** field, select the group to assign the evt\_mgmt\_admin role to.

7.  Select **Save**.

    The role is assigned to the selected group.

8.  To complete the setup, select **Mark as configured**.


