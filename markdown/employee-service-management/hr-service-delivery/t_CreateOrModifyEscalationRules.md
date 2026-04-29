---
title: Configure escalation rules for HR cases
description: Create escalation rules to automatically route HR cases from one tier to another based on agent skills and workload.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage HR roles, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure escalation rules for HR cases

Create escalation rules to automatically route HR cases from one tier to another based on agent skills and workload.

## Before you begin

Verify the following before configuring escalation rules:

-   HR tier groups are created with appropriate agents
-   Email addresses are configured for each tier group
-   Agents have the correct roles, skills, and location assignments

Role required: sn\_hr\_core.admin

## About this task

Escalation rules define the path that HR cases follow when they need to be reassigned. Cases typically escalate from lower-skilled tiers to higher-skilled tiers based on complexity, workload, or agent availability.

The system uses roles, groups, skills, and location to determine the appropriate escalation target for each case.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Manage Roles** &gt; **Escalation Rules**.

2.  Create a new escalation rule by selecting **New**, or modify an existing rule by opening it from the list.

3.  In the **Escalate from** field, select the source tier.

    This tier contains agents with fewer skills who will escalate cases to the next tier. You can select an existing tier using the lookup icon or create a new tier by selecting **New**.

4.  In the **Escalate to** field, select the destination tier.

    This tier contains agents with more advanced skills who will receive escalated cases. You can select an existing tier using the lookup icon or create a new tier by selecting **New**.

5.  Select **Submit** to save the escalation rule.

    The escalation rule is now active and will route cases between the specified tiers.


## Result

You can view group information by selecting any tier in the **Escalate from** or **Escalate to** fields. The escalation rule takes effect immediately for new case assignments.

**Parent Topic:**[Manage HR roles](../concept/c_ManageRoles.md)

**Related topics**  


[Manage HR Groups](t_ManageHRGroups.md)

