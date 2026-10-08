---
title: End a resource assignment
description: End a resource assignment at a specific date to release a resource from a task before the planned end date. Future effort is removed and the heatmap updates to reflect the resource's availability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/end-resource-assignment-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# End a resource assignment

End a resource assignment at a specific date to release a resource from a task before the planned end date. Future effort is removed and the heatmap updates to reflect the resource's availability.

## Before you begin

-   You can end assignments on individual resource assignment rows. You can't end a child assignment.
-   Role required: it\_demand\_manager

## About this task

Use End Assignment when a resource completes their work before the task's planned end date. This releases the resource from the assigned task without changing the task plan. The assignment start date and any recorded actuals remain unchanged.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand's timeline, grouped by **Primary Group**.

5.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for any resource assignment row and select **End assignment**.

    The End Assignment modal opens with a date picker and a status list.

6.  Select an end date using the date picker.

    The default end date is latest of the following, irrespective of the assignment state.

    -   Today's date
    -   The assignment start date
    -   Last recorded date of actuals
    For group assignments, the default end date is the latest of the following.

    -   Today's date
    -   Start date of the assignment
    -   Latest date of recorded actuals among all the child assignments
    The following end dates aren't valid:

    -   Before the assignment start date
    -   After the task's planned end date
    -   Before the end date of the last recorded actuals
7.  Change the assignment status using the status list.

8.  Select **Change End Date**.

    If the selected end date equals the assignment start date, a follow-up prompt appears. Select one of the following options:

    -   **Keep Effort** — retains the effort allocated for that day.
    -   **Remove Effort** — clears the effort for that day.
    Future effort from the new end date onward is removed and the heatmap updates to reflect the resource's released capacity. Recorded actuals aren't affected.


