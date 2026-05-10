---
title: Create an ad hoc obligation task in Software Asset Workspace
description: Create an obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ad hoc obligation task, obligation in software asset workspace]
breadcrumb: [Manage obligation tasks in the Software Asset Workspace, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create an ad hoc obligation task in Software Asset Workspace

Create an obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.

## Before you begin

Role required: sn\_cm\_obligation.obligation\_fulfiller

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Open an active obligation record either from the **Obligations** tab within the contract record or from the **Obligations** view.

<table id="choicetable_bdx_54g_jhc"><thead><tr><th align="left" id="d258505e81">

Method

</th><th align="left" id="d258505e84">

Steps

</th></tr></thead><tbody><tr><td id="d258505e90">

**From the contract record**

</td><td>

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Software contracts**.
2.  Select an active contract record.
3.  Select the **Obligations** tab.
4.  Select an active obligation record.


</td></tr><tr><td id="d258505e133">

**From the Obligations view**

</td><td>

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Obligations**.
2.  Select an active obligations record.


</td></tr></tbody>
</table>3.  Select the **Obligation tasks** tab.

4.  Select **New**.

5.  On the New obligation task form, completed the following steps:

    1.  In the **Assigned to** field, update the assigned user.

    2.  In the **Due date** field, select the due date for the obligation task completion.

    3.  Select **Save**.


## Result

-   An ad hoc obligation task record is created for the obligation and listed in the **Obligations tasks** tab.
-   The assigned user who fulfills the obligation is notified through email.
-   The obligation task record is saved in the Obligation Tasks \[sn\_cm\_obligation\_obligation\_task\] table.

## What to do next

View the obligation record by navigating to one of the following paths:

-   Navigate to the **Obligations tasks** tab within the obligation record.
-   Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Obligation tasks**.

**Parent Topic:**[Manage obligation tasks in the Software Asset Workspace](../concept/manage-obligation-tasks-software-asset-workspace.md)

**Related topics**  


[Create an obligation record in the Software Asset Workspace](create-obligation-record-sam.md)

