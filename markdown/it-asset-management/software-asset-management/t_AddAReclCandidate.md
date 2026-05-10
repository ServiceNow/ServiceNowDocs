---
title: Add a software removal candidate in Software Asset Management classic
description: Removal candidates reclaim software resources in your environment. They are created from reclamation rules, or can be created manually.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Software license usage, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Add a software removal candidate in Software Asset Management classic

Removal candidates reclaim software resources in your environment. They are created from reclamation rules, or can be created manually.

## Before you begin

Role required: sam\_user

## About this task

Software reclamation is integrated with Workflow and Client Software Distribution to automate the process of uninstalling software from devices and reclaiming software rights. However, you can also create a removal candidate manually.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Removal Candidates**

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_t5j_dq2_kxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique removal candidate number that is automatically generated.

</td></tr><tr><td>

Assignment group

</td><td>

Automatically set to the software managers group authorized to respond to removal candidates.

</td></tr><tr><td>

Assigned to

</td><td>

Person primarily responsible for working this task.

</td></tr><tr><td>

Name

</td><td>

Removal candidate name that is automatically generated. Contains the software installation display name.

</td></tr><tr><td>

Description

</td><td>

Description of why the task exists, and what the user must do, if they receive an approval.

</td></tr><tr><td>

State

</td><td>

[Current state](../concept/c_SAMOptimization.md) of the removal candidate.-   Attention Required
-   Ready
-   Awaiting User
-   Awaiting Approval
-   Awaiting Revocation
-   Closed Complete
-   Closed Skipped
-   Closed Canceled


</td></tr><tr><td>

Opened

</td><td>

Date the task was opened.

</td></tr><tr><td>

Closed

</td><td>

Date the task was closed.

</td></tr><tr><td>

Justification

</td><td>

Justification for becoming a removal candidate.-   Low Usage \(default\)
-   Unallocated
-   Unlicensed
-   Restricted Software


</td></tr><tr><td class="sub-head" colspan="2">

Removal Candidate

</td></tr><tr><td>

Applies to

</td><td>

Item type to which the reclamation rule applies.-   Installed Software
-   Subscription Software
-   Engineering App License


</td></tr><tr><td>

Software installation

</td><td>

The software installation being reclaimed.

</td></tr><tr><td>

Engineering App License**Note:** Only appears if **Engineering App License** is selected in the **Applies to** list.

</td><td>

The Engineering application license that you want to reclaim.

</td></tr><tr><td>

User

</td><td>

Name of the user assigned to the software installation. This value can be changed so that another user receives the notification of software being uninstalled.

If the **Bulk Reclamation** check box is selected, this becomes a mandatory field.

</td></tr><tr><td>

Bulk Reclamation

</td><td>

Select this check box to reclaim multiple software installations.

 Once you select this check box, the **Software installation** field is no longer visible. To add software installations, refer to sub steps mentioned in step 4.

</td></tr><tr><td>

Reclamation rule

</td><td>

The reclamation rule that created the removal candidate.

</td></tr><tr><td>

Rights to reclaim**Note:** Only shown if **Engineering App License** is selected in the **Applies to** list.

</td><td>

The number of rights that you want to reclaim. For example, you have 100 rights installed on a license server but you want to reclaim only 40 rights.

</td></tr><tr><td>

Potential savings

</td><td>

Estimated cost of savings if all removal candidates are in Closed Complete state, meaning the software was uninstalled and the rights were harvested \(unused rights \* average price per right from entitlements\).

</td></tr><tr><td>

Notify user

</td><td>

Check box for notifying the user assigned to the hardware on which the software is installed requesting permission via email to remove the software.

</td></tr><tr><td>

Configuration item

</td><td>

The device on which the software is installed.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes

</td><td>

Used to track the actions that have been performed on this task.

</td></tr></tbody>
</table>4.  Select **Save**.

    The removal candidate record is created. If you selected the **Bulk Reclamation** check box, perform the following sub steps to add software installations, before proceeding to the next step. If you didn't select the **Bulk Reclamation** check box, proceed to the next step.

    1.  Select **Edit** in the Software Installation related list.

    2.  In the Edit Members page, move the software installations from the Collection box to the Software Installation List box.

        Only the software installations that are assigned to the specified user appear in the Collection box.

    3.  Select **Save**.

        The software installation you added appears in the Software Installations related list. The state of the removal candidate moves from **Attention Required** to **Ready** and a name is generated in the **Name** field. Continue to select **Edit** to add more software installations. If you decide to remove all software installations, then the state reverts back to **Attention Required** and the name no longer appears in the **Name** field. For the name to be generated and for the removal candidate to be in **Ready** state, at least one software installation must be selected in the removal candidate form.

5.  Select **Reclaim**.

    Once your software installation is reclaimed and removed from your system, the Software Installation column becomes empty. You can refer to the following fields on the Software installation related list to give you insights into the history of the reclaimed software installation.

    -   Display name
    -   Product
    -   Publisher
    -   Software model
    You may select any action button on the form to further configure the removal candidate. Action buttons are dependent on the removal candidate's justification and state.

    |Action|Description|
    |------|-----------|
    |Update|Update the removal candidate.|
    |Close Complete|Reclaim rights and close the removal candidate.|
    |Close Skipped|Close the removal candidate without reclaiming rights.|
    |Delete|Delete removal candidate.|


**Parent Topic:**[Software license usage](../concept/sam-license-workbench.md)

