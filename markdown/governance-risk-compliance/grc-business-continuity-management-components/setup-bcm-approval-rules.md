---
title: Set up approval rules
description: Set up rules for approvals at each approval level by selecting an approver type and the requirement of approval from either one or all the stakeholders. Define filter conditions on the source table to which the approval rule is applied.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Approval configuration, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up approval rules

Set up rules for approvals at each approval level by selecting an approver type and the requirement of approval from either one or all the stakeholders. Define filter conditions on the source table to which the approval rule is applied.

## Before you begin

Role required: sn\_bcm.admin

## About this task

You can select specific approvers, approvers from the selected source table, dynamic approvers, or approvers that you choose to approve your business documents. The approvers can be a BIA owner, BCM lead, BCM manager, BCM admin, contributors, or one or all of them from the source table that you select.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

2.  Click an approval configuration record in the list.

3.  Click the approval levels record in the **Name** column of the Approval Levels section.

4.  Click **New** in the Approval Rules section.

5.  On the form, fill in the fields.

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
-   Scripted approvers: Script to determine approvers. See the script shown as an example below.![Sample script](../image/approval-rule-sample-script.png)
**Note:**

For security reasons, the BCM admin doesn’t have write access to the **Script** field on the Approval Rule form. Only the Approver Configurator developer has create and write access to the **Script** field on the Approval Rule form.

If you have the BCM admin role, you can set up an approval rule only with types of approvers from the Approver type list:

-   Specific approvers
-   Approver from source
For more information on the roles in the GRC: Approver Configurator application, see [Roles installed with GRC: Approver Configurator](../../grc-common/reference/roles-installed-with-approver-configurator.md).

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

Approver table.This field is available only if the Approver type is **Approver from source** or **Dynamic approvers**. Defaults to the source table if it is Approver from source.

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
</table>6.  Click **Submit**.


## Sample script to add assignees from CMDB dependencies as approvers

Field values on the form:

-   **Name**

    Assignee of CMDB dependency as approvers.

-   **Source**

    Dependency \[sn\_bia\_dependency\].

-   **Query using field**

    Dependency Group.Impact Analysis

-   **Approver type**

    Scripted approvers


![Sample script to add approvers.](../image/ScriptedApproverSampleScript.png "Sample script to add approvers")

**Parent Topic:**[Approval configuration](../concept/bcm-approval-configuration.md)

