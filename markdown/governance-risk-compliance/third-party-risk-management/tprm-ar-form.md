---
title: Approval rule form
description: The approval rule form captures all the information needed to create an approval rule. An admin or third-party risk admin can create an approval rule.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Approval process management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Approval rule form

The approval rule form captures all the information needed to create an approval rule. An admin or third-party risk admin can create an approval rule.

<table id="table_ln3_y5g_3rc"><thead><tr><th>

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

Table to which the approval rule is applied.Third-party due diligence request \[sn\_tprm\_dd\_request\] table is the source table for due diligence requests.

</td></tr><tr><td>

Query using field

</td><td>

Field that connects the approving table and the source table.

**Note:** This field is only required if you’re not using the Third-party due diligence request \[sn\_tprm\_dd\_request\] table as a source.

</td></tr><tr><td>

Additional condition

</td><td>

Filter conditions that you can apply on the source table.

 These filter conditions determine when the rule is applied.

</td></tr><tr><td>

Approver type

</td><td>

Type of approver:

-   Specific approvers: Your choice of approvers.
-   Approver from source: Users or groups from the source table.
-   Dynamic approvers: Approvers that are selected dynamically from any table.
-   Scripted approvers: Script to determine your approvers. In the following example, a new approval rule record is shown with Scripted approvers as the selected **Approver type**. A script is started where you can update the parent, users, and groups parameters.

**Note:**

For security reasons, a user with the admin role doesn’t have write access to the **Script** field on the Approval Rule form. Only the Approver Configurator developer has create and write access to the **Script** field on the Approval Rule form.

If you have the admin role, you can set up an approval rule only with the following types of approvers from the Approver type list:

-   Specific approvers
-   Approver from source

For more information on the roles in the GRC: Approver Configurator application, see [Roles installed with GRC: Approver Configurator](../../grc-common/reference/roles-installed-with-approver-configurator.md).

</td></tr><tr><td>

Approval required from

</td><td>

Any user or all stakeholders from whom the approval is required.

</td></tr><tr><td>

Description

</td><td>

Brief note that describes the approval rule.

</td></tr><tr><td class="sub-head" colspan="2">

Approvers

</td></tr><tr><td>

Approvers from

</td><td>

Approver table.This field is available only if the Approver type is **Approver from source** or **Dynamic approvers**. This field defaults to the source table if the approver is from the source table.

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

Script field to apply an advanced filter on the approver table.

</td></tr><tr><td>

Users

</td><td>

One or more users that are designated as approvers.

</td></tr><tr><td>

Group

</td><td>

Group of approvers.

</td></tr><tr><td class="sub-head" colspan="2">

Scripted approvers

</td></tr><tr><td>

Script

</td><td>

Script to determine approvers. **users** and **groups** in the script are selected as approvers.

</td></tr></tbody>
</table>**Parent Topic:**[Approval process management](tprm-ws-dd-mgt-pg-approvals.md)

