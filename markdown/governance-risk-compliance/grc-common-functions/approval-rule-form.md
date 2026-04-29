---
title: Approval Rule form
description: Use the Approval Rule form to create an approval rule.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Set up an approval rule, Use Approver Configurator for setting up approvals for setting up approvals, Common GRC features, Governance, Risk, and Compliance]
---

# Approval Rule form

Use the Approval Rule form to create an approval rule.

<table id="table_ln3_y5g_3rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the approval rule.

</td></tr><tr><td>

Source

</td><td>

Table to which the approval rule is applied.

</td></tr><tr><td>

Query using field

</td><td>

Field that connects the approving table and the source table.

</td></tr><tr><td>

Additional condition

</td><td>

Filter conditions applied on the source table.

</td></tr><tr><td>

Approver type

</td><td>

Type of approver.-   Specific approvers: Your choice of approvers.
-   Approver from source: Users or groups from the source table.
-   Dynamic approvers: Approvers selected dynamically from any table.
-   Scripted approvers: Script to determine approvers. See the script shown as an example below.![Sample script.](../../grc-business-continuity-management/image/approval-rule-sample-script.png)

**Note:**

For security reasons, the BCM admin doesn’t have write access to the **Script** field on the Approval Rule form. Only the Approver Configurator developer has create and write access to the **Script** field on the Approval Rule form.

If you have the BCM admin role, you can set up an approval rule only with the following types of approvers from the Approver type list:

-   Specific approvers
-   Approver from source

For more information on the roles in the GRC: Approver Configurator application, see [Roles installed with GRC: Approver Configurator](roles-installed-with-approver-configurator.md).

</td></tr><tr><td>

Approval required from

</td><td>

One or more stakeholders from whom the approval is required.

</td></tr><tr><td>

Description

</td><td>

Brief note about the approval rule.

</td></tr><tr><td class="sub-head" colspan="2">

Approvers

</td></tr><tr><td>

Approvers from

</td><td>

Approver table. This field is available only if the Approver type is **Approver from source** or **Dynamic approvers**. Defaults to the source table if it is Approver from source.

</td></tr><tr><td>

Filter by

</td><td>

Conditions to filter records from the approver table.This field is available only if the Approver type is **Dynamic approvers**.

</td></tr><tr><td>

Advanced

</td><td>

Option to set a scripted dynamic condition.

</td></tr><tr><td>

User field

</td><td>

User reference or list of approvers from the approver table.

</td></tr><tr><td>

Group field

</td><td>

User group reference as approver from the approver table.

</td></tr><tr><td>

Dynamic condition

</td><td>

Script field to apply advanced filter on approver table.

</td></tr><tr><td>

Users

</td><td>

One or more users designated as approvers.

</td></tr><tr><td>

Group

</td><td>

Group of approvers.

</td></tr><tr><td class="sub-head" colspan="2">

Scripted approvers

</td></tr><tr><td>

Script

</td><td>

Script to determine approvers; **users** and **groups** in the script are selected as approvers.

</td></tr></tbody>
</table>**Parent Topic:**[Set up an approval rule for the approval level](../task/set-up-approval-rules.md)

