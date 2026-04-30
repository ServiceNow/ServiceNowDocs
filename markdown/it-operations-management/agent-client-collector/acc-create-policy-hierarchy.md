---
title: Create a policy hierarchy
description: Policies are attached to groups of related CIs. If you have a subgroup of related CIs, you can attach a new policy to the subgroup using a policy hierarchy, without creating the new policy from scratch.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a new Agent Client Collector policy, Collecting data from your system devices, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Create a policy hierarchy

Policies are attached to groups of related CIs. If you have a subgroup of related CIs, you can attach a new policy to the subgroup using a policy hierarchy, without creating the new policy from scratch.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Policy hierarchy enables you to use a policy as a template to create a new policy, which is then attached to a subgroup of the original policy's CIs. The original policy is the **parent** policy, and the new policy is the **child** policy.

**Note:** You cannot create a child policy when a proxy agent is in place for the parent policy.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  On the **Policies** page, select a published policy with a Hierarchy value of either **None** or **Parent**.

3.  Select the **Create Child** button at the top of the page or underneath the **Monitored CIs** tab.

    A new \(child\) policy opens with the same parameters as the original policy. The name of the policy is **&lt;Policy name&gt;&lt;date and time created&gt;**.

    **Note:** The child policy inherits the parent policy's parameters only when it is first created; there is no continuous inheritance from the parent to the child.

    The following fields appear hard-coded with the indicated values:

    |Field|Value|
    |-----|-----|
    |Publish status|Draft|
    |Hierarchy|Child|
    |Parent|&lt;Name of the parent policy&gt;|

    The **Order** field value indicates the priority by which the agent attaches itself to the policy. A lower number indicates higher priority, and each created child policy takes on a higher value than the policy preceding it. You can modify this value, as needed.

4.  Modify the policy's parameters, as needed.

    The following buttons appear on the child policy page:

    |Button|Description|
    |------|-----------|
    |Compare to Parent|Select to display the differences between the child policy and its parent policy.|
    |Return to Parent|Select to leave the child policy page \(without saving\) and return to the parent policy.|

    The following buttons appear on the parent policy page:

<table id="table_vj5_gpp_54b"><thead><tr><th>

Button

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deactivate

</td><td>

Appears for an active policy. Enables you to select from the following: -   Deactivate the parent policy and all of its child policies
-   Deactivate only the parent policy


</td></tr><tr><td>

Activate

</td><td>

Appears for an inactive policy. Enables you to select from the following: -   Activate the parent policy and all of its child policies
-   Activate only the parent policy


</td></tr><tr><td>

Delete

</td><td>

Enables you to select from the following:-   Delete the parent policy and all of its child policies
-   Delete only the parent policy


</td></tr></tbody>
</table>5.  Select **Save**.

    Child policies appear on the **Child Policies** tab of the parent policy.


