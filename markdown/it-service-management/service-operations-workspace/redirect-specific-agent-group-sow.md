---
title: Redirect agents of a specific group to Service Operations Workspace
description: Enable only agents of specific user groups to be automatically redirected to Service Operations Workspace after logging in to the ServiceNow instance.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Landing page redirection in SOW for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Redirect agents of a specific group to Service Operations Workspace

Enable only agents of specific user groups to be automatically redirected to Service Operations Workspace after logging in to the ServiceNow instance.

## Before you begin

Role required: admin

## About this task

Only the agents who are part of specified user groups are redirected to Service Operations Workspace. All other agents are redirected either to the agent-configured landing page or ServiceNow AI Platform landing page.

## Procedure

1.  From the **All** menu, navigate to **user\_criteria.list**.

2.  Select the **ITIL non-admin** user criteria record.

3.  For the **Groups** field, select the required user groups whose agents must access Service Operations Workspace.

4.  Select **Update**.

5.  Ensure that the itil role is assigned to each agent.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and then open the user record for the agent.

    2.  In the **Roles** list, ensure that the **itil** role is added and active.

    3.  If the itil role isn't already added to the user record, add the itil role by following these steps.

        1.  In the **Roles** list, select **Edit**.
        2.  On the **Edit Members** form, add the itil role from the **Collection** list to the **Roles List** list.
        3.  Select **Save**.

