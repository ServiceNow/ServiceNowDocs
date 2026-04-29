---
title: Define policy exception and extension rules
description: Configure granular approval rules for policy exceptions and extensions using the GRC Approval Configurator.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [GRC Approval Configurator, Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define policy exception and extension rules

Configure granular approval rules for policy exceptions and extensions using the GRC Approval Configurator.

## Before you begin

Role required: sn\_compliance.manager to create the policy exception and extension rules.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

    The Approval Configurator is shipped with default templates for verification, final approval, and extension. The priority is set for each of them. By default, verification configuration is set with priority 1, approval configuration is set to priority 2, and extension approval configuration to priority 3.

2.  Select the configuration template.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for this configuration.|
    |Active|Select this option to activate the configuration.|
    |Applies to|Ensure that **Policy exception \(sn\_compliance\_policy\_exception\)** option is selected.|
    |Domain|Search for and select the functional group or role that should be associated with the approval flow.|
    |Filter Condition|Use filter conditions to define when the configuration should be activated. The available values are sourced from the Policy Exception table. You must set both the State and Sub-state conditions. Use logical operators such as AND or OR to build complex condition sets.|

4.  Select **New** in the **Approval Levels** table to add approval levels to the configuration.

    1.  Provide a name.

    2.  Assign a level.

    3.  Select **Submit**.

    You can add multiple levels for the configuration. Each level can have its own rule, assigned users or groups, and triggering conditions.

5.  Select the approval level you have created and select **New** to add the rule to the approval level.

    1.  Fill in the following fields.

<table id="table_ecj_kkz_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for this rule.

</td></tr><tr><td>

Description

</td><td>

Provide a description for the rule.

</td></tr><tr><td>

Source

</td><td>

Select the source table for rule evaluation.

</td></tr><tr><td>

Additional condition

</td><td>

Optionally refine the source table by applying additional filters.

</td></tr><tr><td>

Query using field

</td><td>

Select a field on the source record to query for matching approval conditions.

</td></tr><tr><td>

Approve type

</td><td>

Select the approver from the following options:-   **Specific approvers**: Select individual users, groups, or both as approvers directly. This option allows you to manually assign approvers without relying on dynamic or source-based logic.
-   **Approver from source**: Select approvers based on values from the source table. You can choose a user field, a group field, or both to dynamically determine approvers from the source record.
-   **Dynamic approvers**: Define approvers dynamically using the source. Apply static or advanced dynamic conditions to filter approvers. You can select a user field, group field, or both to determine who should approve.
-   **Scripted approvers**: Use a script to programmatically determine approvers. The script must populate the users and groups variables.


</td></tr><tr><td>

Approval required from

</td><td>

Select **All** to make it mandatory for all selected users to approve the exception. Select **Anyone** to allow a single user to approve on behalf of all approvers.

</td></tr></tbody>
</table>    2.  Select **Submit** after adding the details.


## Result

The rules are now set for approvals for policy exception and extension.

**Parent Topic:**[GRC Approval Configurator for approving policy exceptions and extensions](../concept/grc-approval-configurator-for-policy-extension-and-exception.md)

