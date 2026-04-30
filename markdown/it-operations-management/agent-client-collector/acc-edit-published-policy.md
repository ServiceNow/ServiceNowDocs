---
title: Edit a published policy
description: A policy with a status of published has been passed through the MID Server and sent to the agent. To edit a published policy, you must enable editing.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a new Agent Client Collector policy, Working with checks and policies, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Edit a published policy

A policy with a status of **published** has been passed through the MID Server and sent to the agent. To edit a published policy, you must enable editing.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

You select a Published policy and then select the **Edit in Sandbox** option to enable editing of the policy. You edit the policy in the sandbox and then save, republish, or delete the policy, as needed. The following diagram illustrates the flow of editing a published policy:

![Editing policy workflow](../image/ACC-Policy-Workflow.png)

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Click a policy for which the **Publish status** is **Published**.

3.  Activate or deactivate the policy, as needed, by clicking the **Activate** or **Deactivate** button.

4.  Select the **Edit in Sandbox** button.

    The policy is now in **Draft view**, and its fields are editable.

    **Note:**

    -   When you select this option, the policy's check instances are also editable.
    -   Although the policy is in **Draft view**, its **Publish status** remains **Published**.

        ![Policy draft view](../image/ACC-Policy-Draft-View.png)

    While editing the policy's fields, you can select the following options, as needed:

<table id="table_ywt_pbm_blb"><thead><tr><th>

Button

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Revert All Changes

</td><td>

Reverts the changes you entered into the Sandbox policy fields to the most recently published values. The policy's **Publish status** returns to **Published**, and remains in **Draft view** for editing.This button appears only after entering updates into the Sandbox policy fields.

</td></tr><tr><td>

View Published

</td><td>

Returns to the most recently published policy. The policy returns to **Published** view.

</td></tr><tr><td>

Save

</td><td>

Saves the changes you entered into the Sandbox policy fields. The policy remains in **Draft view**, and the **Publish status** is **Published\***. The asterisk indicates that the current published version is not the most up to date, since there are changes that have not yet been published.

</td></tr><tr><td>

Republish

</td><td>

Publishes the updates you entered into the Sandbox policy fields. The policy is saved with your updates and opens as the published policy.-   The published policy's **Publish status** is set to **Queued** if the policy changes result in either:

    -   A change in which agents are running the policy \(that is, a change to the monitored CI filter\).
    -   A change in the policy’s check instances.
The policy's publishing job recalculates Queued policies and sends them to the relevant MID Servers.

-   The published policy's **Publish status** is set to **Ready to publish** if the changes to the policy do not require any agent recalculation \(that is, a change to the policy interval\).

The policy's publishing job sends Ready to publish policies to the relevant MID Servers, without recalculating those policies. After the policy publishing job processes a policy, the policy **Publish status** moves to **Published**.

This button appears only after entering updates into the policy fields, for a policy whose **Publish status** is **Published\***.

</td></tr><tr><td>

Delete

</td><td>

Deletes the policy.This button appears only when viewing the published policy, and deletes both the Published and Sandbox policies.

</td></tr></tbody>
</table>5.  Select checks in the **Available** cell of the Checks tab, and move them to the **Selected** cell for them to be included in the policy.

    Checks can be selected multiple times, when you are monitoring more than one process. You can also select a group of checks in the **Filter checks by groups** field, which presents checks of the selected group in the **Available** cell.

6.  In the **Check Instances** table, view the check instances that are configured for the policy, or select a check instance to edit it.

7.  On the **Agents** tab, view the agents that are executing the policy.

    The list of agents is calculated based on the monitored CIs.

    This tab appears only when viewing a published policy.


