---
title: Manage workplace cases in List view in Workplace Central
description: The List view tab provides a traditional list view of cases in Workplace Central.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/manage-cases-in-list-view-in-workplace-central.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 3
breadcrumb: [Working with Case management, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Manage workplace cases in List view in Workplace Central

The List view tab provides a traditional list view of cases in Workplace Central.

The List view tab complements the Calendar view by offering a structured, row-based representation of the same case data, making it suitable for users who prefer list-based navigation or to perform bulk operations.

To access List view:

-   Navigate to **All** &gt; **Workplace Central**.
-   Select **Case Management** &gt; **List view** tab at the top of the workspace.

## Shared filter state

When a user navigates from the Calendar view to the List view tab, all active filters including case type \(Workplace, Maintenance, Move\) and campus are preserved.

For example, if a user filters by Maintenance Cases in the Calendar view, the List view tab also displays only Maintenance Cases.

## Condition builder

In addition to the filters inherited from the Calendar view, the List view tab includes an integrated condition builder. You can define additional filter conditions using the condition builder to further refine the list of cases displayed.

## Fixed condition filter

When a case manager or case agent navigates to the List Tab in Workplace Central, the condition builder displays a set of populated filters that are automatically carried over from the Calendar View. These are referred to as fixed filters.

The filters applied using the predicate builder, the case type filter, and the Campus filter are automatically passed as fixed filters into the condition builder.

These fixed filters are locked in the condition builder and cannot be removed or replaced. To refine the list further, you can add conditions directly in the condition builder. Any additional conditions are appended to the fixed filters using an AND operator.

## Assign declarative action

The List view tab includes a declarative Assign action that allows enables case managers to assign multiple cases to a specific user.

-   Select one or more cases from the list.
-   Select Assign.
-   If the selected cases share an assignment group, the user select shows only the users who are members of all applicable assignment groups \(intersection\).
-   If no assignment group is tagged to the selected cases, the user picker shows all users from the sys\_user table.
-   Selecting a user and confirming the assignment updates all selected cases immediately. The updated assignees are reflected in the list.

## Export and standard list actions

The List view tab exposes standard presentational list component actions, including export options. You can export the current filtered list for offline use or reporting purposes.

\[Omitted image "casemgmt-listview-tab.png"\] Alt text:

**Parent Topic:**[Working with Case management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/working-with-case-management.md)

**Related topics**  


[Manage workplace cases using Case management]()

[Work on a workplace case using Case management]()

[Create a workplace service case]()

[Create a child case and a child task]()

[Print a workplace case]()

[Managing print case]()

[Cancel or delete a case]()

[Manage workplace cases in calendar view in Workplace Central]()

[View Facility Assets in Workplace Central]()

