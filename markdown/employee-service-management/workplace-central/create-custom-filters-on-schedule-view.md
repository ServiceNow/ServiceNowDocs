---
title: Create custom filters on the schedule view
description: Create custom filters in the schedule view to control which records appear in your list. You can set filter conditions to view only the records that meet your criteria.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-09-24"
reading_time_minutes: 3
breadcrumb: [Working with schedule view, Working with Event planner, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Create custom filters on the schedule view

Create custom filters in the schedule view to control which records appear in your list. You can set filter conditions to view only the records that meet your criteria.

## Before you begin

Role required: sn\_wsd\_rsv.reservation\_viewer

## About this task

The following are filter categories:

-   Default filters: Provided by default for all users. The system includes All active rooms and My planned reservations as default filters. By default, the All active rooms filter is selected.
-   Custom filters: Create, modify, or delete your own filters. Set filters for individual users, everyone, or specific groups.

    |Option|Description|
    |------|-----------|
    |Me|Creates a personal filter that only you can access. This option is unavailable if you do not have write access to the **User** field.|
    |Everyone|Creates a global filter accessible to all users. This option is available to users with the filter\_global role.|
    |Group|Creates a group filter accessible only to members of the selected user group. This option is available to users with the filter\_group role. If you do not have write access to the **Group** field, this option is unavailable.|

-   Temporary filters: Apply filters directly without saving. Temporary filters are visible only to the logged-in user and are removed on refresh, logout, or session timeout.

**Note:** The filters are stored in the sys\_filter table.

## Procedure

1.  Navigate to **All** &gt; **Workplace central** &gt; **Workplace Central**.

    You can also open Workplace Central from Employee Center directly by navigating to **All** &gt; **Self-service** &gt; **Employee Center** &gt; **Workspaces** &gt; **Workplace Central**.

2.  Select the event planner icon ![event planner icon](../images/event-planner-icon.png).

3.  Select **Open Scheduled view**.

    The schedule view page opens, displaying locations based on any previously applied location filters.

4.  Select the filter drop-down menu and select **Create new filter**.

    The Advanced filter pop-up appears with the **Conditions** tab selected by default. For more information about condition builder, see [https://developer.servicenow.com/dev.do\#!/reference/next-experience/yokohama/now-components/now-predicate-builder/uib-setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-predicate-builder/uib-setup) now-predicate-builder UIB Setup.

5.  Define filter conditions in the following tabs as needed:

    -   Conditions: Use the condition builder to construct a statement with contextually generated fields. Select the **Field**, **Operator**, and **Value**. To view the Meeting Room or Workspace Reservable Purpose, along with the Room or Workspace or Desk Space type, you can filter by Space type using the following filter condition:![Use predicate builder to logically group elements using AND or OR logic.](../images/wsd-condition-builder.png)
    -   Group by: Organize event sections dynamically using the Group by filter condition. Applying a group by filter updates the schedule view to show sections based on the selected attribute. For example, grouping by campus displays separate sections for each campus, while grouping by space type organizes sections according to room types.
    -   Related list conditions: Include relationships with other tables in the filter by selecting related table records from the drop-down list. For more information, see [Add related list conditions](https://www.servicenow.com/docs/access?context=create-related-list-query&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). For Reservable Purpose, use Related list conditions to apply filtering on related tables as shown in the following image:![You can apply filtering on related tables using the Related list conditions tab.](../images/wsd-related-list-conditions.png)
    In this context, &gt;=1 means, that the system return the parent record \(the space\) only when there is at least one record in the related list \(M2M table\) that meets the specified filter condition.

    **Note:** You must define at least one filter condition to create a custom filter.

6.  Select **Saved filters** and select **Save active filters**.

7.  In the Save Filter pop-up, do the following:

    -   **Filter name**: Enter a name for the filter.
    -   **Permissions**: Set the filter visibility. You can set the filter visibility to yourself, everyone, or to a specific group.
8.  Select **Save**.

9.  Select **Apply filters** to implement the custom filter.

    **Note:** The selected or applied filter stays active until the user navigates back to the page and changes it.


**Parent Topic:**[Working with schedule view](working-with-schedule-view.md)

