---
title: Monitor and plan improvements
description: Use the Continual Improvement Workbench to monitor and plan improvements in a single view. The workbench shows tile and list views of improvements in progress, as well as listings under review, and in the backlog to help you plan your sprint.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Continual Improvement Management, IT Service Management]
---

# Monitor and plan improvements

Use the Continual Improvement Workbench to monitor and plan improvements in a single view. The workbench shows tile and list views of improvements in progress, as well as listings under review, and in the backlog to help you plan your sprint.

## Before you begin

Role required: sn\_cim.improvement\_manager, sn\_cim.improvement\_coordinator

## About this task

The workbench is flexible graphical view that you can tailor to your needs, which is helpful for the Improvement Manager when running planning meetings and when doing a quick status update to other stakeholders.

The tile-based drag-and-drop user interface makes it easy to monitor, plan, and approve improvements.

<table id="table_amq_td5_bdb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview tab

</td><td>

Shows two groups of improvements.

-   Tiles in Implement and On Hold states.
-   Listings in Review state.

This list can be customized in the Workbench Review list layout.


 Use this section for daily monitoring and assessment of improvements being implemented, as well as those recently implemented that are in review.

</td></tr><tr><td>

Planning tab

</td><td>

Lists two groups of improvements.

-   Listings in Implement and On Hold states.
-   Listing for backlog \(New, Accepted, Assess, and Approved states\).

 Use this section for ranking and prioritization of improvements in the Implement state, or in the backlog \(improvement initiatives in Approved, Assess, Accepted, and New states, listed in that order\).

**Note:** Configuration changes made to the Planning workbench are reset when the Planning workbench is reloaded.

</td></tr></tbody>
</table>![CIM Improvement Workbench](../image/continual-improvement-workbench.png "Continual Improvement Management Improvement Workbench")

Features:

-   Tile layout \(12 improvement tiles shown by default\).
-   Search by keyword.
-   Sort by rank, priority, due date, or effort estimate.
-   Status on tile \(percentage complete, assignment, priority, and time left\)

    Percentage complete is based on the total planned duration of all CIM tasks in each phase of the improvement. For example, if a task in a phase that has a planned duration of 10 days is 100% complete in 10 days, and if another task in the same phase has a planned duration of 5 days and is 0% complete in 10 days, the phase to which these tasks belong will show as 50% complete.

    **Note:** Percent complete values are shown per phase, and per improvement.

-   Color-coded status badge on tile.

    |Status badge|Description|
    |------------|-----------|
    |![Complete icon](../image/cim-complete-icon.png)|All tasks have been completed \(percent complete is 100%\).|
    |![Overdue icon](../image/cim-overdue-icon.png)|Due date has passed.|
    |![Due soon icon](../image/cim-due-soon-icon.png)|Less than 15% of duration left until the due date.|
    |![On Hold icon](../image/cim-on-hold-icon.png)|Improvement has been placed on hold.|

-   Customize fields shown in workbench lists using the Workbench Review view.

    Access the Workbench Review view from the List Controls menu \(![List icon](../image/cim-list-controls.png)\) of the Improvement Register \(**List Controls** &gt; **View** &gt; **Workbench Review**\).

    **Note:** Only the fields visible in the Improvement Register \[Workbench Review\] view are shown in the workbench overview section.


On the planning page, you can prioritize your backlog using an easy-to-use drag-and-drop interface, similar to sprint planning, where you have an active sprint and a list of backlog items. Move backlog items to the Work in Progress list, which is your active sprint.

![CIM Workbench Plan](../image/cim-workbench-plan.png "Continual Improvement Management Workbench Plan")

Features:

-   Color coding on **Planned end date** field \(red, green\)
-   Search by keyword.
-   Move items up or down a list.
-   Group multiple items together.
-   Drag and drop within and between lists.

    **Note:** Moving an item, or group of items, from one list to another changes the state of the improvement.

    For example, moving an item from Backlog to Work in Progress changes the state from **Approved** to **Implement**. Conversely, moving an item from Work in Progress back to the Backlog changes the state to **Approved**.

    Only approved items can be moved from the Backlog list to the Implement list.

-   Customize fields shown in workbench lists using the Workbench Planning view.

    Access the Workbench Planning view from the List Controls menu \(![List icon](../image/cim-list-controls.png)\) of the Improvement Register \(**List Controls** &gt; **View** &gt; **Workbench Planning**\).

-   Filter by priority, benefits, effort estimate, and CIM Coordinator.

    **Note:** The filters are dynamic and show only the fields visible in the Workbench Planning view.

-   Toggle the Filter menu and fields shown using the Configuration menu \(![Configuration icon](../image/cim-config-menu.png)\).

    **Note:** Only the fields visible in the Improvement Register \[Workbench Planning\] view are shown in the workbench planning section.


## Procedure

1.  Navigate to **Continual Improvement** &gt; **Workbench**.

2.  On the Overview tab, analyze the Work in Progress tiles to get an overall picture of the improvements in progress.

    Color-coded alert banners call out improvements that need attention. You can click on a tile to view the improvement.

3.  Use the Planning tab to build the contents of your current sprint, according to capacity.

    1.  Drag and drop items from the Backlog list to the Work in Progress list.

    2.  Use the filters \(Priority, Benefits, Effort Estimate, and CIM Coordinator\) to narrow the data contained in the lists so you can focus on certain groups of improvements.

4.  Use the Configuration menu to customize the columns shown in the Planning tab lists that is specific to your needs.


