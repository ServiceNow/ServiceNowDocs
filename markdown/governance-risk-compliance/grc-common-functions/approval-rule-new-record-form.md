---
title: Approval Rule New Record form
description: Use the Approval Rule New Record form to create an approval rule for the approval level for a policy record.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Set up an approval rule, Use Approver Configurator for setting up approvals for setting up approvals, Common GRC features, Governance, Risk, and Compliance]
---

# Approval Rule New Record form

Use the Approval Rule New Record form to create an approval rule for the approval level for a policy record.

<table id="table_ln3_y5g_3rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the approval rule. For example, Approval rule 1.

</td></tr><tr><td>

Description

</td><td>

Brief description about the approval rule.

</td></tr><tr><td>

Active

</td><td>

Option to mark the approval rule record as active.

</td></tr><tr><td>

Source

</td><td>

Source table that the approval rule is applied to. Optionally, you can apply an additional condition on the source table. Select a field to filter the source records based on the **Applies to** table that is to be filled in the approval configuration.

</td></tr><tr><td>

Additional condition

</td><td>

Additional filter condition that can be applied on the source table.

</td></tr><tr><td>

Query using field

</td><td>

Field that connects the approving table and the source table.

</td></tr><tr><td>

Approver type

</td><td>

Type of approvers for the policy. See the following options for approver types.-   Specific approvers: Select users as approvers by selecting **Users**, **Group**, or both.
-   Approver from source: Select approver from the source table. You can select a user column, group column, or both from which to read the approver.
-   Dynamic approvers: Select approvers dynamically from the approver table by applying static and/or advanced dynamic conditions. You can select a user column, group column, or both from which to read the approver.
-   Scripted approvers: Write a script to determine approvers. Variables **users** and **groups** are used in the script.

**Note:** For security reasons, the Approver Configurator developers have read and write access to the **Script** field on the Approval Rule form. For more information on setting up the approval rules, see [Set up an approval rule for the approval level](../task/set-up-approval-rules.md).


</td></tr><tr><td>

Approval required from

</td><td>

One or more stakeholders from whom the approval is required.

</td></tr><tr><td class="sub-head" colspan="2">

Approver type \(Approvers selected for the record\)

</td></tr><tr><td>

Option 1: **Specific approvers**

</td><td>

When the Approver type is **Specific approvers**, the approvers are as follows:-   Users: User reference or list of approvers from the approver table.
-   Group: User group reference as approver from the approver table.

</td></tr><tr><td>

Option 2: **Approver from source**

</td><td>

When the Approver type is **Approver from source**, the approvers are as follows:-   In the **Approval required from** field, the available options are:
    -   **All**
    -   **Anyone**
-   In the **Approvers** section, the available options are:
    -   **Approvers from**
    -   **User field**
    -   **Group field**

</td></tr><tr><td>

Option 3: **Dynamic approvers**

</td><td>

When the Approver type is **Dynamic approvers**, the approvers are as follows:-   In the **Approval required from** field, the available options are:
    -   **All**
    -   **Anyone**
-   In the **Approvers** section, the available options are:
    -   **Approvers from**
    -   **Filter by**
    -   **Advanced**
    -   **User field**
    -   **Group field**

</td></tr><tr><td>

Option 4: **Scripted approvers**

</td><td>

When the Approver type is **Scripted approvers**, the approvers are as follows:-   In the **Approval required from** field, the available options are:
    -   **All**
    -   **Anyone**
-   In the **Scripted approvers** section, the custom script for the approval configuration is displayed.

**Note:** Only users with a developer role can modify the custom script.

</td></tr></tbody>
</table>**Parent Topic:**[Set up an approval rule for the approval level](../task/set-up-approval-rules.md)

