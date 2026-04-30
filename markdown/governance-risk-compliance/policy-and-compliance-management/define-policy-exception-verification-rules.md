---
title: Define the policy verification rules
description: Configure granular approval rules for policy exceptions and extensions by using the GRC Approval Configurator. This allows you to manage approvals with precise rule definitions and support multi-level approval workflows.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Policy exceptions and extensions with GRC Approval Configurator, Policy and Compliance Management enhancement steps, Implementing Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define the policy verification rules

Configure granular approval rules for policy exceptions and extensions by using the GRC Approval Configurator. This allows you to manage approvals with precise rule definitions and support multi-level approval workflows.

## About this task

Verification rules validate policy exception or extension requests before they proceed to review or approval. These rules are configured using the Verification Configuration template, allowing you to define conditions based on status, sub-status, and other filters. When a policy exception is created, it enters the New state, triggering verification approvals. Upon successful verification, the request advances to the Analyze state for further evaluation.

## Before you begin

Role required: sn\_compliance.manager to create the policy verification rules.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

    The GRC Approval Configurator is shipped with default template for verification called **Policy Exception - Verification Config**.

2.  Select **Policy Exception - Verification Config**.

3.  On the form, fill in the fields.

<table id="table_klc_gq4_plb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Priority

</td><td>

By default, the verification configuration is set with priority 1.**Note:** The verification configuration is set to priority 1 by default and should be retained to ensure initial verification approval before

</td></tr><tr><td>

Filter Condition

</td><td>

Filter conditions to define when the configuration should be activated. The available values are sourced from the Policy Exception table.

 By default, State is set to New. This is a mandatory condition.

 You can set other filter conditions as well. Use logical operators such as AND or OR to build complex condition sets.

</td></tr><tr><td>

Domain

</td><td>

Functional group or role that should be associated with the approval flow.

</td></tr><tr><td>

Applies to

</td><td>

Verify that the **Policy exception \(sn\_compliance\_policy\_exception\)** option is selected.

</td></tr><tr><td>

Active

</td><td>

Option to enable the configuration.

</td></tr><tr><td>

Name

</td><td>

Name of the verification configuration.

 By default, the template name is **Policy Exception - Verification Config**. You can change the template name.

</td></tr></tbody>
</table>4.  Add approval levels to the configuration in the Approval Levels table.

    A default approval level called **Verification Config - Level 1** is already set up. You can add multiple levels for the configuration. Each level can have its own rules, assigned users or groups, and triggering conditions.

5.  Select **Verification Config - Level 1**.

6.  On the form, change the following fields:

<table id="table_zgr_qyx_rgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

By default, the name provided is Verification Config - Level 1. You can retain the same name or change the name.

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

