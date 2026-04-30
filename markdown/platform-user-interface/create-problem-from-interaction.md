---
title: Create a problem from an interaction
description: You can create a problem record directly from an Interaction when the customer makes contact regarding an issue and you need to investigate.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Interaction records in Workspace, Getting work from chats, Finding issues to work on in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a problem from an interaction

You can create a problem record directly from an Interaction when the customer makes contact regarding an issue and you need to investigate.

## Before you begin

-   Role required: workspace\_user or admin
-   Activate the Problem Management Best Practice — com.snc.best\_practice.problem plugin
-   Select the **Allow Problem creation from Interaction** \(**glide.problem.interaction.allow\_create**\) problem property

**Note:** The Interaction feature is a more efficient way to create a problem from an interaction than the New Call feature from Service Desk Call \(com.snc.service\_desk\_call\) plugin that you might have used previously.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Workspace Home**.

2.  Click the list icon \(![List icon](../image/icon-list-view.png)\) and click the Interaction list.

3.  Click the interaction record from which you want to create a problem.

4.  On the interaction page, click the more actions icon \(![More actions icon](../image/more-actions-icon.png)\) and select **Create Problem**.

5.  On the form, fill in the fields.

<table id="table_un2_dyl_n3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated. Number that identifies the problem record.

</td></tr><tr><td>

First reported by

</td><td>

Task that first identified this problem.

</td></tr><tr><td>

Category and Subcategory

</td><td>

Group to which the problem belongs to such as software or hardware. After selecting the category, select the subcategory, if applicable.

</td></tr><tr><td>

Service

</td><td>

Business service that the problem applies to.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the problem applies to. The CI class of the selected configuration item identifies the type of problem, for example, hardware, network, or database.

</td></tr><tr><td>

State

</td><td>

State management process. The field value changes as the problem proceeds from one state to another state. The states available are: **New**, **Assess**, **Root Cause Analysis**, **Fix in Progress**, **Resolved**, and **Closed**.**Note:** To access the new state management process, activate the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) plugin.

</td></tr><tr><td>

Impact

</td><td>

Effect that the problem has on business operations, for example, `Major revenue loss.`

</td></tr><tr><td>

Urgency

</td><td>

Extent to which the problem resolution can bear delay.

</td></tr><tr><td>

Priority

</td><td>

How quickly the service desk should address the problem. The **Priority** field is automatically set to the **Impact** and **Urgency** values.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the problem is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

Problem coordinator to whom the problem is assigned. If an assignment rule applies, the problem is automatically assigned to the appropriate user or group.

</td></tr><tr><td>

Problem statement

</td><td>

Brief description of the problem. **Note:** Activate the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) plugin.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the problem.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notification when work notes are added to the problem.

</td></tr><tr><td>

Work notes

</td><td>

Informative notes about the work performed on the problem.

</td></tr><tr><td class="sub-head" colspan="2">

Analysis Information

</td></tr><tr><td>

Workaround

</td><td>

Method used to overcome the issue.if no resolution is available yet.

</td></tr><tr><td>

Cause notes

</td><td>

The cause of the problem.

</td></tr><tr><td class="sub-head" colspan="2">

Resolution information

</td></tr><tr><td>

Resolved

</td><td>

Auto-generated. Date and time when the user resolved the problem.

</td></tr><tr><td>

Resolved by

</td><td>

Auto-generated. The user who resolved the problem.

</td></tr><tr><td>

Fix notes

</td><td>

How the problem was fixed.

</td></tr><tr><td class="sub-head" colspan="2">

Auto-generated information

</td></tr><tr><td>

Opened

</td><td>

Auto-generated. Date and time when the user opened the problem.

</td></tr><tr><td>

Opened by

</td><td>

Auto-generated. User who opened the problem.

</td></tr><tr><td>

Confirmed

</td><td>

Auto-generated. Date and time when the issue was confirmed as a problem.

</td></tr><tr><td>

Confirmed by

</td><td>

Auto-generated. User who accessed the issue and confirmed that it was a problem.

</td></tr></tbody>
</table>6.  Click **Save**.

    A problem record is created and the record appears in the Related tasks related list on the Interaction form.


