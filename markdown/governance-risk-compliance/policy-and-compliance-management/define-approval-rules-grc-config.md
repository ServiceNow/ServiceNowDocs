---
title: Define the policy exception approval rules
description: Approval rules define how policy exception requests are reviewed and approved, enabling organizations to create customized, multi-level workflows.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Policy exceptions and extensions with GRC Approval Configurator, Policy and Compliance Management enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define the policy exception approval rules

Approval rules define how policy exception requests are reviewed and approved, enabling organizations to create customized, multi-level workflows.

## Before you begin

Role required: sn\_compliance.manager to create the policy exception approval rules.

## About this task

Approval rules enable organizations to create customized, multi-level workflows for reviewing and approving policy exception requests based on specific filter conditions. These rules support dynamic assignment of approvers and allow configuration of approval requirements at each level. Once configured, requests are automatically routed to the designated approvers, streamlining the approval process.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

    The GRC Approval Configurator is shipped with default template for approval called **Policy Exception - Approval Config**.

2.  Select **Policy Exception - Approval Config**.

3.  On the form, fill in the fields.

<table id="table_klc_gq4_plb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to enable the configuration.

</td></tr><tr><td>

Filter Condition

</td><td>

Filter conditions to define when the configuration should be activated. The available values are sourced from the Policy Exception table.

 By default, State is set to Awaiting Approval. This is a mandatory condition.

 You can set other filter conditions as well. Use logical operators such as AND or OR to build complex condition sets.

</td></tr><tr><td>

Name

</td><td>

Name of the approval configuration.

 By default, the template name is **Policy Exception - Approval Config**. You can change the template name.

</td></tr><tr><td>

Domain

</td><td>

Functional group or role that should be associated with the approval flow.

</td></tr><tr><td>

Priority

</td><td>

By default, the approval configuration is set with priority 2.**Note:** The approval configuration is set to priority 2 by default and should be retained to ensure that this approval triggers immediately after verification of policy exception requests.

</td></tr><tr><td>

Applies to

</td><td>

Verify that the **Policy exception \(sn\_compliance\_policy\_exception\)** option is selected.

</td></tr></tbody>
</table>4.  Add approval levels to the configuration in the Approval Levels table.

    A default approval level called **Approval Config - Level 1** is already set up. You can add multiple levels for the configuration. Each level can have its own rules, assigned users or groups, and triggering conditions.

5.  Select **Verification Config - Level 1**.

6.  On the form, change the following fields:

<table id="table_zgr_qyx_rgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

By default, the name provided is Approval Config - Level 1. You can retain the same name or change the name.

</td></tr><tr><td>

Level

</td><td>

Keep the level as 1, as this is the first level that we are configuring.

</td></tr></tbody>
</table>7.  Select **Submit**.

8.  Add additional approval levels to the configuration by selecting **New** in the Approval Levels table.

    |Field|Description|
    |-----|-----------|
    |Name|Provide a name to the new level.|
    |Level|Assign the level.|

9.  Select **Submit**.

    After adding the required approval levels, add verification rules to each level.

10. To add verification rules, select the configured verification level, and do the following:

    1.  In Approval Rules, select **New**.

    2.  On the form, fill in the fields.

<table id="table_ecj_kkz_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for this rule.

</td></tr><tr><td>

Description

</td><td>

Description for the rule.

</td></tr><tr><td>

Source

</td><td>

Source table for rule evaluation.

</td></tr><tr><td>

Additional condition

</td><td>

Option to refine the source table by applying additional filters.

</td></tr><tr><td>

Query using field

</td><td>

Field on the source record to query for matching approval conditions.

</td></tr><tr><td>

Approve type

</td><td>

Approval type options:-   **Specific approvers**: Select individual users, groups, or both as approvers directly. This option enables you to assign approvers manually without relying on dynamic or source-based logic.
-   **Approver from source**: Select approvers that are based on values from the source table. You can select a user field, a group field, or both to determine approvers dynamically from the source record.
-   **Dynamic approvers**: Define approvers dynamically using the source. Apply static or advanced dynamic conditions to filter approvers. You can select a user field, group field, or both to determine who should approve.
-   **Scripted approvers**: Use a script to determine the approvers programmatically. The script must populate the users and groups variables.


</td></tr><tr><td>

Approval required from

</td><td>

Approval options: Select **All** to make it required for all the selected users to approve the exception. Select **Anyone** to enable a single user to approve on behalf of all approvers.

</td></tr></tbody>
</table>    3.  Select **Submit**.


**Parent Topic:**[Define policy exceptions and extensions with the GRC Approval Configurator](../concept/define-policy-exceptions-and-extensions-with-the-grc-approval-configurator.md)

