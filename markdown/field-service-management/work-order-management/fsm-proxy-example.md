---
title: Example: Configure proxy actions for an assignment group
description: Create a proxy policy that lets users in an assignment group perform proxy actions on behalf of other technicians in that same group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/fsm-proxy-example.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring proxy actions, Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Example: Configure proxy actions for an assignment group

Create a proxy policy that lets users in an assignment group perform proxy actions on behalf of other technicians in that same group.

## Before you begin

Role required: sn\_fsm\_proxy\_actn.proxy\_admin

## About this task

After you create the policy, assign the sn\_fsm\_proxy\_actn.proxy\_agent role to each agent who needs to perform proxy actions. For more information on adding a role, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md).

## Procedure

1.  Select **All** &gt; **Field Service** &gt; **Proxy Configuration** &gt; **Policy**.

2.  Select **New**.

3.  In the **Name** field, enter a name for the policy.

4.  Confirm the **Table** field is set to **Work Order Task \[wm\_task\]**.

5.  Under **Conditions**, select **Add Filter Condition** and define who the policy applies to.

    For example, set the condition to **Assignment group is** to scope the policy to a specific team.

6.  Select the **Actions Configuration** tab.

7.  Select the actions to allow, or select **Enable all actions**.

8.  Select the **Delegation Policy Roles** table.

9.  Select **New**, and then select the roles you want to add.

10. Select **Submit**.

11. Select **Update**.


