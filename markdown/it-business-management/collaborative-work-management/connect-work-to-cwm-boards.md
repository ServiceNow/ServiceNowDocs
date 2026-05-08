---
title: Connect work from other ServiceNow apps to CWM Boards
description: Enable a consolidated view of all relevant work by connecting work items from different ServiceNow applications to a Board in Collaborative Work Management.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Connect work, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Connect work from other ServiceNow apps to CWM Boards

Enable a consolidated view of all relevant work by connecting work items from different ServiceNow applications to a Board in Collaborative Work Management.

## Before you begin

Role required: sn\_cwm.cwm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, select a Board that you want to connect work for.

3.  From the Board header, select the Board more options icon \(![](../images/cwm-icon-column-actions.png)\) and select **Connect work**.

    If you already have connected any work items, then this label is displayed as **Connected work**.

    ![Connect work option in the CWM Board header.](../images/cwm-connected-work.png)

4.  In the Manage connected work modal, select **+ Add new**.

    ![Connect new work items.](../images/cwm-connected-work-add.png)

5.  Choose a table and define the conditions to filter the records from the selected table.

    1.  From the **Table** field, select a table.

        For example, to bring in all the incidents, select the Incident \[incident\] table.

        **Note:** Only those tables that you have access to and from the applications that are already installed and active in your ServiceNow instance are available for you.

    2.  Change the value in the **Name** field according to your requirement.

    3.  Use the condition builder to add conditions and filter the records from the table you selected.

        For example, you'd like to bring in incidents that are active and belong to certain categories. Then, your condition set would be similar to the following:

        **Active is true** and **Category is Inquiry / Help** or **Category is Software**.

    4.  Select the Update count icon \(![Update count icon.](../images/cwm-icon-update-count.png)\) to check the number of records that exist which match the filter criteria that you defined.

        **Note:** Ensure that the number of records available for your filter criteria are not more than 100. You can change this number by default to 500 by working with your admin to update the system property **sn\_cwm.connect\_work\_import\_limit**.

        ![Define conditions to connect records from other ServiceNow applications.](../images/cwm-connected-work-define.png)

6.  Select **Save**.

7.  Repeat steps 4 through 6 to connect work items of other types.

    You can connect up to 10 work item types to a Board and you can add only one connected work configuration per table.

8.  Select **Save**.


## Result

-   The Board is refreshed to load and display all the connected work items.
-   Any existing information such as Assigned to, State, and Start and End dates is also shown on the Board.
-   With the Sprint planning view enabled, you can see all these connected work items in the Backlog list. For more information about performing sprint planning, see [Sprint planning in CWM](../concept/agile-sprint-planning-in-cwm.md).

![CWM Board with connected work items displayed in the List view.](../images/cwm-connected-work-board.png)

## What to do next

To enable additional fields from any connected work table, change the form layout configuration for the Default view of the table. You can then surface these fields as columns in CWM. For more information, see Show or hide fields on a form.

**Parent Topic:**[Connected work in CWM](../concept/unified-boards-for-connected-work-in-cwm.md)

**Related topics**  


[Manage connected work item types in CWM](manage-connected-work-item-types-in-cwm.md)

[Update filter conditions for connected work in CWM](update-conditions-for-connected-work-in-cwm.md)

