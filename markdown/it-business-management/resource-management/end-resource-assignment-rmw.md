---
title: End a resource assignment
description: End a resource assignment at a specific date to release a resource from a task before the planned end date. Future effort is removed and the heatmap updates to reflect the resource's availability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/end-resource-assignment-rmw.html
release: brazil
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [end assignment, end resource assignment, resource assignment, resource management workspace]
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# End a resource assignment

End a resource assignment at a specific date to release a resource from a task before the planned end date. Future effort is removed and the heatmap updates to reflect the resource's availability.

## Before you begin

-   End Assignment is available on individual resource assignment rows. You can't end a child assignment.
-   This action is not available in list view.
-   Recorded actuals aren't affected by ending an assignment.
-   Role required: resource\_user

## About this task

Use End Assignment when a resource completes their work before the task's planned end date. This releases the resource from the assigned task without changing the task plan. The assignment start date and any recorded actuals remain unchanged.

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(\[Omitted image "rmw-resource-cards-L1-icon.png"\] Alt text: Resource cards icon.\) from the menu and open a resource card.

3.  Select the chevron icon \(\[Omitted image "rmw-chevron-image.png"\] Alt text: Chevron icon.\) to expand the resource view and locate the assignment row.

4.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for the resource assignment row and select **End Assignment**.

    The End Assignment modal opens with a date picker and a status list.

5.  Select an end date using the date picker.

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
6.  Change the assignment status using the status list.

7.  Select **Change End Date**.

    If the selected end date equals the assignment start date, a follow-up prompt appears. Select one of the following options:

    -   **Keep Effort** — retains the effort allocated for that day.
    -   **Remove Effort** — clears the effort for that day.
    Future effort from the new end date onward is removed and the heatmap updates to reflect the resource's released capacity. Recorded actuals aren't affected.


**Parent Topic:**[Using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/using-rmw.md)

