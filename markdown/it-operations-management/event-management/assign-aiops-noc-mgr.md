---
title: Assign AIOps NOC managers to group
description: Assign the evt\_aiops\_manager role to the group that is responsible for managing NOC operators and AIOps AI specialists.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/assign-aiops-noc-mgr.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
breadcrumb: [Configure Event Management using ServiceNow Otto for Setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Assign AIOps NOC managers to group

Assign the evt\_aiops\_manager role to the group that is responsible for managing NOC operators and AIOps AI specialists.

## Before you begin

Verify you have installed the ITOM AIOps and ServiceNow Otto for IT Operations Management \(ITOM\) plugins.

Ensure you are in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin

## About this task

The evt\_aiops\_manager role provides the permissions that operations leaders need to oversee alert handling, manage team assignments, and configure Event Management tools. Assign this role to groups that contain your operations managers and team leads who supervise L1 and L2 staff and own alert-handling outcomes.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Promote to Production**.

2.  Expand **Promote to Production**.

3.  Select **Assign AIOps NOC managers**.

4.  Select **Add group**.

    By default, the **Assign role to existing group** is selected.

5.  If you want to create your group, select **Create new group** and perform the following steps:

    1.  In the **Group name** field, enter the name of the group.
    2.  In the **Description** field, enter a description.
    3.  In the **Users** field, select the users to add to the group.
    4.  Select **Save**.
6.  In the **Group** field, select the group to assign the evt\_aiops\_manager role to.

7.  Select **Save**.

    The role is assigned to the selected group.

8.  To complete the setup, select **Mark as configured**.


