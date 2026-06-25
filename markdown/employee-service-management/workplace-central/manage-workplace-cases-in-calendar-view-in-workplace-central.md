---
title: Manage workplace cases in calendar view in Workplace Central
description: The Calendar view in Workplace Central enables case managers and case agents to view and manage assigned cases in a color-coded, week-based layout. Cases are organized chronologically by date field and can be filtered, grouped, and navigated by time zone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/manage-workplace-cases-in-calendar-view-in-workplace-central.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2026-05-18"
reading_time_minutes: 5
breadcrumb: [Working with Case management, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Manage workplace cases in calendar view in Workplace Central

The Calendar view in Workplace Central enables case managers and case agents to view and manage assigned cases in a color-coded, week-based layout. Cases are organized chronologically by date field and can be filtered, grouped, and navigated by time zone.

The Calendar view for case management in Workplace Central provides a visual, date-based representation of cases. The view defaults to the current week and displays all cases that span the selected week. Case managers can assess workload distribution and take action without navigating away from the calendar.

To access Calendar view:

-   Navigate to **All** &gt; **Workplace Central**.
-   Select **Case Management** &gt; **Calendar view** tab at the top of the workspace.

|Tab|Description|
|---|-----------|
|Overview|Displays all existing case management details on Workplace Central.|
|Calendar view|Cases displayed on an interactive weekly calendar, color-coded by priority.|
|List view|A traditional list view of cases. Case managers can bulk reassign cases to users within the assignment group.|

## Default week view and case types

When a case agent or manager navigates to the Calendar view tab, the view defaults to the current week. All cases that span or are scheduled within that week are displayed. Cases are placed on the calendar based on a date field that varies by case type.

-   Workplace Cases use the Delivery Time field.
-   Maintenance Cases use the Scheduled On date field.
-   Move Cases use the Due Date field.

## Color coding by priority

Each case card on the calendar is color-coded based on the priority of the case. Case managers can visually assess urgency without opening individual records. A legend is available on the calendar view to reference the color-to-priority mapping.

## Grouping and unassigned cases handling

Cases are grouped in the following hierarchy:

-   First level: Assignment Group
-   Second level: Assigned To \(individual user within the group\)

Cases with no assignment group and no assigned user are displayed under an Unassigned section at the bottom of the calendar.

Cases with no assignment group are grouped under No Assignment Group section at the bottom of the calendar. Cases with an assignment group but no individual assignee are grouped under an Unassigned section within that group.

You can also configure a custom group-by option. If a custom group-by field is specified, the calendar data is grouped by that field instead of the default hierarchy.

## Pagination and navigation

The Calendar view supports the following navigation options:

-   Scroll within the current week to view all assignment groups and their cases.
-   Navigate forward or backward one week at a time using navigation controls.
-   Select a specific date from a date picker to jump directly to the week containing that date.

## Filters

The following filter options are available on the Calendar view:

-   **Default Filters**

    Active Cases is applied as the default filter. This filter displays cases assigned to the current user or their team.

-   **Custom Filters**

    Create a custom filter using the built-in predicate builder. Select **Create new filter** and create a filter based on any case attribute, such as priority, status, or location.

-   **Campus filter**

    Select Campus to filter cases by campus. Entering a campus name displays all cases assigned to that campus or to any location within its hierarchy \(building, floor, area, space\).

    **Note:** When the Amsterdam campus is selected in the campus filter, the calendar displays all cases in the Amsterdam campus hierarchy. This includes buildings, floors, and individual spaces beneath it.


## Inline editing and reassignment

When you select a case card in the calendar, the side panel displays the case details allowing you to perform the following actions.

-   View all relevant case fields including priority, service agent, and location.
-   Edit case details by selecting a specific card on the Calendar view. For example, you can reassign a case to a different user or change the scheduled date.

**Note:** All edits made in the side panel are reflected immediately on the calendar without a page reload.

If a case manager identifies a user with an overloaded schedule and another with no cases, cases can be reassigned directly from the side panel. The calendar updates immediately.

## Time zone support

View case details in specific time zones apart from the default time zone. Select a time zone from the available options to update all event times in the Calendar view accordingly.

## Tool-tip context

Each card's tool-tip shows case number, priority, service, assigned agent, and location details.

## IFM Framework integration

When Integrated Facilities Management \(IFM\) providers are configured, cases on the calendar display a provider tag to indicate whether the case is handled internally or by an external FM provider.

|Tag|Meaning|
|---|-------|
|External|The case has an FM provider mapped to it|
|Internal|The case has no FM provider mapped.|

**Note:** If no FM providers are configured, provider tags are not displayed. Only the case short description appears on the calendar block. The tooltip includes the case number, priority, service agent, and location.

\[Omitted image "Calendarview-casemanagement.png"\] Alt text:

**Parent Topic:**[Working with Case management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/working-with-case-management.md)

**Related topics**  


[Manage workplace cases using Case management]()

[Work on a workplace case using Case management]()

[Create a workplace service case]()

[Create a child case and a child task]()

[Print a workplace case]()

[Managing print case]()

[Cancel or delete a case]()

[Manage workplace cases in List view in Workplace Central]()

[View Facility Assets in Workplace Central]()

